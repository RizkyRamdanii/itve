<script lang="ts">
	import { reveal } from 'svelte-reveal';
	import SectionWrapper from './SectionWrapper.svelte';
	import Modal from '$lib/Modal.svelte';

	let showModal = false;
</script>

<SectionWrapper id="Hero">
	<section class="min-h-svh">
		<div class="flex items-start md:items-center justify-between flex-col-reverse md:flex-row">
			<div class="w-full md:w-1/2 self-start md:self-center md:py-36 md:px-5">
				<h1
					use:reveal={{
						preset: 'slide',
						x: -60,
						easing: 'easeOutBack',
						duration: 2200,
						reset: true
					}}
					class="text-7xl md:text-9xl font-bold tracking-widest"
				>
					ITVE
				</h1>
				<p
					use:reveal={{ preset: 'fly', y: -40, duration: 2200, reset: true }}
					class="text-xl md:text-3xl font-normal md:px-2"
				>
					All Your Problems,<br /> We Are the Solution
				</p>
				<div class="transition ease-in-out delay-150">
					<!-- svelte-ignore a11y-invalid-attribute -->
					<a
						on:click={() => (showModal = true)}
						href="#"
						use:reveal={{ preset: 'scale', duration: 2100, reset: true }}
						class="btn text-black hover:text-white hover:-translate-y-1 hover:scale-110 bg-transparent hover:bg-green-500 duration-300 rounded-3xl my-4 md:my-7 md:mx-2"
					>
						<svg
							class="absolute me-36 md:me-[175px] h-5 w-10 md:h-8 md:w-14"
							style="fill-rule:evenodd;clip-rule:evenodd;stroke-linejoin:round;stroke-miterlimit:2;"
							version="1.1"
							viewBox="0 0 512 512"
							xml:space="preserve"
							xmlns="http://www.w3.org/2000/svg"
							xmlns:xlink="http://www.w3.org/1999/xlink"
							><path
								d="M373.295,307.064c-6.37,-3.188 -37.687,-18.596 -43.526,-20.724c-5.838,-2.126 -10.084,-3.187 -14.331,3.188c-4.246,6.376 -16.454,20.725 -20.17,24.976c-3.715,4.251 -7.431,4.785 -13.8,1.594c-6.37,-3.187 -26.895,-9.913 -51.225,-31.616c-18.935,-16.89 -31.72,-37.749 -35.435,-44.126c-3.716,-6.377 -0.397,-9.824 2.792,-13c2.867,-2.854 6.371,-7.44 9.555,-11.16c3.186,-3.718 4.247,-6.377 6.37,-10.626c2.123,-4.252 1.062,-7.971 -0.532,-11.159c-1.591,-3.188 -14.33,-34.542 -19.638,-47.298c-5.171,-12.419 -10.422,-10.737 -14.332,-10.934c-3.711,-0.184 -7.963,-0.223 -12.208,-0.223c-4.246,0 -11.148,1.594 -16.987,7.969c-5.838,6.377 -22.293,21.789 -22.293,53.14c0,31.355 22.824,61.642 26.009,65.894c3.185,4.252 44.916,68.59 108.816,96.181c15.196,6.564 27.062,10.483 36.312,13.418c15.259,4.849 29.145,4.165 40.121,2.524c12.238,-1.827 37.686,-15.408 42.995,-30.286c5.307,-14.882 5.307,-27.635 3.715,-30.292c-1.592,-2.657 -5.838,-4.251 -12.208,-7.44m-116.224,158.693l-0.086,0c-38.022,-0.015 -75.313,-10.23 -107.845,-29.535l-7.738,-4.592l-80.194,21.037l21.405,-78.19l-5.037,-8.017c-21.211,-33.735 -32.414,-72.726 -32.397,-112.763c0.047,-116.825 95.1,-211.87 211.976,-211.87c56.595,0.019 109.795,22.088 149.801,62.139c40.005,40.05 62.023,93.286 62.001,149.902c-0.048,116.834 -95.1,211.889 -211.886,211.889m180.332,-392.224c-48.131,-48.186 -112.138,-74.735 -180.335,-74.763c-140.514,0 -254.875,114.354 -254.932,254.911c-0.018,44.932 11.72,88.786 34.03,127.448l-36.166,132.102l135.141,-35.45c37.236,20.31 79.159,31.015 121.826,31.029l0.105,0c140.499,0 254.87,-114.366 254.928,-254.925c0.026,-68.117 -26.467,-132.166 -74.597,-180.352"
								id="WhatsApp-Logo"
							/></svg
						>
						<span class="text-lg capitalize">contact us</span></a
					>

					<Modal bind:showModal>
						<div class="container">
							<h2 class="flex justify-center items-center text-2xl">What do u Need?</h2>
							<div class="top-5">
								<p class="font-normal text-base">Your Name:</p>
								<input
									type="text"
									placeholder="Example: Mulyono"
									class="input input-bordered w-full max-w-xs"
								/>
								<p class="font-normal text-base">Needs?</p>
								<textarea
									class="textarea textarea-bordered w-full"
									placeholder="Example: Buy Software bla-bla..."
								></textarea>
								<button
									class="relative w-20 h-16 left-48 bg-slate-900 rounded-xl text-white hover:bg-blue-500"
									>Send</button
								>
							</div>
						</div>
					</Modal>
				</div>
			</div>
			<div class="w-full md:w-1/2">
				<div class="relative right-2 md:left-3 md:top-1">
					<enhanced:img
						src="../images/it.png"
						alt="it-logos"
						use:reveal={{ preset: 'fade', reset: true }}
						class="logo h-[256px] w-[450px] md:h-[336px] md:w-[490px]"
					></enhanced:img>
				</div>
			</div>
		</div>
	</section>
</SectionWrapper>

<style>
	.logo {
		transform: translateY(-2%);
		animation: floater 1.8s infinite;
		transition: ease 2s;
	}

	@keyframes floater {
		0% {
			transform: translateY(-2%);
			transition: ease 2s;
		}
		50% {
			transform: translateY(2%);
			transition: ease 2s;
		}
	}

	.btn {
		width: 246px;
		height: 64px;
	}

	@media only screen and (max-width: 600px) {
		.btn {
			width: 200px;
			height: 60px;
		}
	}
</style>
