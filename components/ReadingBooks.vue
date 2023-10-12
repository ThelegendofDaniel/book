<template>
	<div class="pl-5">
		<h3 class="text-lg font-bold">Continue Reading</h3>
		<div class="my-4 overflow-x-scroll flex scroll-container">
			<div
				v-for="readingBook in books"
				:key="readingBook.id"
				class="w-7/12 h-28 mx-5 cursor-pointer shadow-md justify-between inline-flex min-w-[70%]"
			>
				<img
					src="../assets//images/psychology of money.jpg"
					:alt="readingBook.title"
					class="w-20"
				/>
				<div class="ml-1 pl-2 w-8/12 flex-col justify-between flex">
					<div class="flex justify-between">
						<span
							class="px-3 font-bold inline-flex text-sm items-center bg-yellow-200 text-yellow-500 rounded-full"
						>
							<svg
								xmlns="http://www.w3.org/2000/svg"
								fill="none"
								viewBox="0 0 24 24"
								stroke-width="1.5"
								stroke="currentColor"
								class="w-5 h-5 mr-1"
							>
								<path
									stroke-linecap="round"
									stroke-linejoin="round"
									d="M11.48 3.499a.562.562 0 011.04 0l2.125 5.111a.563.563 0 00.475.345l5.518.442c.499.04.701.663.321.988l-4.204 3.602a.563.563 0 00-.182.557l1.285 5.385a.562.562 0 01-.84.61l-4.725-2.885a.563.563 0 00-.586 0L6.982 20.54a.562.562 0 01-.84-.61l1.285-5.386a.562.562 0 00-.182-.557l-4.204-3.602a.563.563 0 01.321-.988l5.518-.442a.563.563 0 00.475-.345L11.48 3.5z"
								/>
							</svg>
							{{ readingBook.stars }}</span
						>
						<div class="flex">
							<span
								class="bg-purple-400 inline-flex justify-center bookmarked items-center text-sm text-white rounded-full ml-3"
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
										d="M16.5 3.75V16.5L12 14.25 7.5 16.5V3.75m9 0H18A2.25 2.25 0 0120.25 6v12A2.25 2.25 0 0118 20.25H6A2.25 2.25 0 013.75 18V6A2.25 2.25 0 016 3.75h1.5m9 0h-9"
									/>
								</svg>
							</span>
							<span
								class="bg-yellow-100 ml-2 text-yellow-500 p-1 rounded-full"
							>
								<svg
									xmlns="http://www.w3.org/2000/svg"
									fill="none"
									viewBox="0 0 24 24"
									stroke-width="1.5"
									stroke="currentColor"
									class="w-6 h-6"
								>
									<path
										stroke-linecap="round"
										stroke-linejoin="round"
										d="M4.26 10.147a60.436 60.436 0 00-.491 6.347A48.627 48.627 0 0112 20.904a48.627 48.627 0 018.232-4.41 60.46 60.46 0 00-.491-6.347m-15.482 0a50.57 50.57 0 00-2.658-.813A59.905 59.905 0 0112 3.493a59.902 59.902 0 0110.399 5.84c-.896.248-1.783.52-2.658.814m-15.482 0A50.697 50.697 0 0112 13.489a50.702 50.702 0 017.74-3.342M6.75 15a.75.75 0 100-1.5.75.75 0 000 1.5zm0 0v-3.675A55.378 55.378 0 0112 8.443m-7.007 11.55A5.981 5.981 0 006.75 15.75v-1.5"
									/>
								</svg>
							</span>
						</div>
					</div>
					<p
						class="title font-bold whitespace-nowrap overflow-x-clip text-ellipsis"
					>
						{{ readingBook.title }}
					</p>
					<p class="text-gray-500">{{ readingBook.author }}</p>
					<div
						class="percent-container bg-gray-200 mt-2 rounded-full"
					>
						<div
							:style="{ width: readingBook.readenPercent + '%' }"
							class="bg-yellow-600 h-full rounded-full"
						></div>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>
<script>
export default {
	setup() {
		const books = [
			{
				author: "Morgan Housel",
				title: "The Psychology Of Money",
				stars: "4.4",
				isPicked: true,
				readenPercent: 70,
				id: "1",
			},
			{
				author: "Morgan Housel",
				title: "The Psychology Of Money",
				stars: "4.4",
				isPicked: true,
				readenPercent: 70,
				id: "2",
			},
			{
				author: "Morgan Housel",
				title: "The Psychology Of Money",
				stars: "4.4",
				isPicked: true,
				readenPercent: 70,
				id: "3",
			},
			{
				author: "Morgan Housel",
				title: "The Psychology Of Money",
				stars: "4.4",
				isPicked: true,
				readenPercent: 70,
				id: "4",
			},
			{
				author: "Morgan Housel",
				title: "The Psychology Of Money",
				stars: "4.4",
				isPicked: true,
				readenPercent: 70,
				id: "5",
			},
		];
		return { books };
	},
};
</script>
<style lang="scss" scoped>
.percent-container {
	position: relative;
	height: 8px;
	width: 100%;
	> div {
		position: absolute;
		left: 0;
		top: 0;
	}
}
.bookmarked {
	width: 32px;
}
.scroll-container {
	::-webkit-scrollbar {
		display: none;
	}

	/* Hide scrollbar for IE, Edge and Firefox */

	-ms-overflow-style: none; /* IE and Edge */
	scrollbar-width: none; /* Firefox */
}
</style>
