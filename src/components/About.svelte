<script>
	import { reveal } from 'svelte-reveal';
	import SectionWrapper from './SectionWrapper.svelte';
</script>

<SectionWrapper id="About">
	<section class="min-h-svh">
		<div class="flex justify-center items-center ms-1 md:ms-2">
			<div class="hero bg-blue-200 min-h-screen rounded-lg">
				<div class="hero-content flex-col lg:flex-row">
					<enhanced:img
						use:reveal={{ preset: 'slide', duration: 1300, reset: true }}
						src="../images/abt-grafis.png"
						class="img-abt max-w-md rounded-lg shadow-2xl"
					/>
					<div use:reveal={{ preset: 'fly', duration: 1300, reset: true }}>
						<h1 class="text-5xl font-bold text-center md:text-start">About Us!</h1>
						<p class="py-6 whitespace-normal">
							sebuah organisasi community IT yang layaknya seperti keluarga dan dijadikanlah sebuah
							bisnis oleh para petinggi yang bergerak dibidang Teknologi yang menawarkan jasa atau
							produk. &#40 harusnya ini bahasa enggres cuma bingung ey kata-katanya apa yach &#41
						</p>
					</div>
				</div>
			</div>
		</div>
	</section>
</SectionWrapper>

<style>
	.img-abt {
		width: 200px;
		height: 280px;
		aspect-ratio: auto;
	}
</style>
