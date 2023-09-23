<template>
	<div class="p-5 creating-slider">
		<Swiper
			:modules="[SwiperAutoplay, SwiperEffectCreative, SwiperPagination]"
			:slides-per-view="1"
			:loop="true"
			:effect="'creative'"
			:autoplay="{
				delay: 8000,
				disableOnInteraction: true,
			}"
			:pagination="{
				enabled: true,
				clickable: true,
				dynamicBullets: true,
				paginationDisabledClass: '123',
				bulletActiveClass: 'swiper-pagination-bullet-active',
			}"
			:creative-effect="{
				prev: {
					shadow: false,
					translate: ['-20%', 0, -1],
				},
				next: {
					shadow: false,

					translate: ['100%', 0, 0],
				},
			}"
		>
			<SwiperSlide v-for="slide in 3" :key="slide">
				<div
					class="item cursor-pointer border-2 border-gray-300 bg-neutral-200 h-44 rounded-md pl-3 pr-1 pt-4 flex"
				>
					<div class="w-1/2">
						<div
							class="inline-flex px-4 text-orange-400 py-0.5 text-sm bg-white rounded-3xl"
						>
							<svg
								xmlns="http://www.w3.org/2000/svg"
								fill="none"
								viewBox="0 0 24 24"
								stroke-width="1.5"
								stroke="currentColor"
								class="w-5 h-5"
							>
								<path
									stroke-linecap="round"
									stroke-linejoin="round"
									d="M15.362 5.214A8.252 8.252 0 0112 21 8.25 8.25 0 016.038 7.048 8.287 8.287 0 009 9.6a8.983 8.983 0 013.361-6.867 8.21 8.21 0 003 2.48z"
								/>
								<path
									stroke-linecap="round"
									stroke-linejoin="round"
									d="M12 18a3.75 3.75 0 00.495-7.467 5.99 5.99 0 00-1.925 3.546 5.974 5.974 0 01-2.133-1A3.75 3.75 0 0012 18z"
								/>
							</svg>

							<span class="ml-1">Popular</span>
						</div>
						<p class="text-xl my-2 font-bold text-black">
							The Psychology Of Money
						</p>
						<p class="text-neutral-500 text-sm">MORGAN HOUSEL</p>
						<a href="#" class="text-orange-400 font-bold"
							>Read More</a
						>
					</div>
					<img
						class="mx-auto mb-0.5 pointer-events-none"
						src="../assets/images/psychology of money.jpg"
					/>
				</div>
			</SwiperSlide>
		</Swiper>
	</div>
	<BookSlide />
</template>

<style lang="scss">
.creating-slider {
	.swiper-pagination-bullet-active {
		background-color: rgb(68 64 60);
	}
}
</style>
