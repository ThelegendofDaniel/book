<template>
	<div class="pl-5">
		<h3 class="text-lg font-bold">Continue Reading</h3>
		<div class="mt-4 overflow-x-scroll flex">
			<div
				v-for="readingBook in books"
				class="w-7/12 mx-2 shadow-md inline-flex min-w-[70%]"
			>
				<img
					src="../assets//images/psychology of money.jpg"
					:alt="readingBook.title"
					class="w-4/12"
				/>
				<div class="ml-1">
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
								class="w-6 h-6 mr-1"
							>
								<path
									stroke-linecap="round"
									stroke-linejoin="round"
									d="M11.48 3.499a.562.562 0 011.04 0l2.125 5.111a.563.563 0 00.475.345l5.518.442c.499.04.701.663.321.988l-4.204 3.602a.563.563 0 00-.182.557l1.285 5.385a.562.562 0 01-.84.61l-4.725-2.885a.563.563 0 00-.586 0L6.982 20.54a.562.562 0 01-.84-.61l1.285-5.386a.562.562 0 00-.182-.557l-4.204-3.602a.563.563 0 01.321-.988l5.518-.442a.563.563 0 00.475-.345L11.48 3.5z"
								/>
							</svg>
							{{ readingBook.stars }}</span
						>
						<div>
							<span
								class="bg-purple-400 inline-flex items-center text-sm text-white rounded-full ml-3"
							>
								<svg
									xmlns="http://www.w3.org/2000/svg"
									fill="none"
									viewBox="0 0 24 24"
									stroke-width="1.5"
									stroke="currentColor"
									class="w-4 h-4"
								>
									<path
										stroke-linecap="round"
										stroke-linejoin="round"
										d="M16.5 3.75V16.5L12 14.25 7.5 16.5V3.75m9 0H18A2.25 2.25 0 0120.25 6v12A2.25 2.25 0 0118 20.25H6A2.25 2.25 0 013.75 18V6A2.25 2.25 0 016 3.75h1.5m9 0h-9"
									/>
								</svg>
							</span>
						</div>
					</div>
					<p class="title">{{ readingBook.title }}</p>
					<p>{{ readingBook.author }}</p>
					<div
						class="percent-container bg-gray-200 mt-2 rounded-full"
					>
						<div
							:style="{ width: readingBook.readenPercent + '%' }"
							class="bg-yellow-300 h-full rounded-full"
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
			},
			{
				author: "Morgan Housel",
				title: "The Psychology Of Money",
				stars: "4.4",
				isPicked: true,
				readenPercent: 70,
			},
			{
				author: "Morgan Housel",
				title: "The Psychology Of Money",
				stars: "4.4",
				isPicked: true,
				readenPercent: 70,
			},
			{
				author: "Morgan Housel",
				title: "The Psychology Of Money",
				stars: "4.4",
				isPicked: true,
				readenPercent: 70,
			},
			{
				author: "Morgan Housel",
				title: "The Psychology Of Money",
				stars: "4.4",
				isPicked: true,
				readenPercent: 70,
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
</style>
