<script lang="ts">
	let canvas: HTMLCanvasElement | undefined = $state();

	$effect(() => {
		if (!canvas) return;
		if (window.matchMedia('(prefers-reduced-motion: reduce)').matches) return;
		if (!window.matchMedia('(pointer: fine)').matches) return;

		const cv = canvas;
		const ctx = cv.getContext('2d');
		if (!ctx) return;

		let width = (cv.width = window.innerWidth);
		let height = (cv.height = window.innerHeight);

		const onResize = () => {
			width = cv.width = window.innerWidth;
			height = cv.height = window.innerHeight;
		};

		type Particle = {
			x: number;
			y: number;
			vx: number;
			vy: number;
			life: number;
			maxLife: number;
			size: number;
		};
		const particles: Particle[] = [];
		let lastSpawn = 0;
		let raf = 0;

		const onMove = (e: PointerEvent) => {
			const now = performance.now();
			if (now - lastSpawn < 16) return;
			lastSpawn = now;
			for (let i = 0; i < 3; i++) {
				if (particles.length > 220) particles.shift();
				particles.push({
					x: e.clientX + (Math.random() - 0.5) * 10,
					y: e.clientY + (Math.random() - 0.5) * 10,
					vx: (Math.random() - 0.5) * 0.6,
					vy: (Math.random() - 0.5) * 0.6 - 0.3,
					life: 0,
					maxLife: 60 + Math.random() * 40,
					size: 8 + Math.random() * 14
				});
			}
		};

		const tick = () => {
			ctx.clearRect(0, 0, width, height);
			for (let i = particles.length - 1; i >= 0; i--) {
				const p = particles[i];
				p.life++;
				p.x += p.vx;
				p.y += p.vy;
				p.size += 0.35;
				if (p.life >= p.maxLife) {
					particles.splice(i, 1);
					continue;
				}
				const t = p.life / p.maxLife;
				const alpha = 0.28 * Math.sin(Math.PI * t);
				const g = ctx.createRadialGradient(p.x, p.y, 0, p.x, p.y, p.size);
				g.addColorStop(0, `rgba(148, 163, 184, ${alpha})`);
				g.addColorStop(1, 'rgba(148, 163, 184, 0)');
				ctx.fillStyle = g;
				ctx.beginPath();
				ctx.arc(p.x, p.y, p.size, 0, Math.PI * 2);
				ctx.fill();
			}
			raf = requestAnimationFrame(tick);
		};

		window.addEventListener('resize', onResize);
		window.addEventListener('pointermove', onMove);
		raf = requestAnimationFrame(tick);

		return () => {
			cancelAnimationFrame(raf);
			window.removeEventListener('resize', onResize);
			window.removeEventListener('pointermove', onMove);
		};
	});
</script>

<canvas bind:this={canvas} class="pointer-events-none fixed inset-0 z-[60]" aria-hidden="true"
></canvas>
