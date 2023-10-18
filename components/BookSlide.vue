<template>
	<div class="scroll-container pl-5">
		<div
			class="flex items-center genres text-sm overflow-x-scroll whitespace-nowrap my-5 font-bold"
		>
			<span class="mr-5 cursor-pointer active">All Genre</span
			><span class="mx-5 cursor-pointer">Comedy</span
			><span class="mx-5 cursor-pointer">Fiction</span
			><span class="mx-5 cursor-pointer">Romance</span
			><span class="mx-5 cursor-pointer">Biography</span
			><span class="mx-5 cursor-pointer">Novel</span
			><span class="mx-5 cursor-pointer">Non-Fiction</span
			><span class="mx-5 cursor-pointer">Thriller</span
			><span class="mx-5 cursor-pointer">Mystery</span
			><span class="mx-5 cursor-pointer">Fantasy</span>
		</div>
		<div class="overflow-x-scroll books-container min-w-full flex mb-10">
			<Card
				class="w-5/12 min-w-[180px] mx-5"
				v-for="book in books"
				:title="book.title"
				:author="book.author"
				:stars="book.stars"
				:isPicked="book.isPicked"
			/>
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
			},
			{
				author: "Morgan Housel",
				title: "The Psychology Of Money",
				stars: "4.4",
				isPicked: true,
			},
			{
				author: "Morgan Housel",
				title: "The Psychology Of Money",
				stars: "4.4",
				isPicked: true,
			},
			{
				author: "Morgan Housel",
				title: "The Psychology Of Money",
				stars: "4.4",
				isPicked: true,
			},
			{
				author: "Morgan Housel",
				title: "The Psychology Of Money",
				stars: "4.4",
				isPicked: true,
			},
		];
		return { books };
	},
};
</script>
<style lang="scss" scoped>
.genres,
.books-container {
	::-webkit-scrollbar {
		display: none;
	}

	/* Hide scrollbar for IE, Edge and Firefox */

	-ms-overflow-style: none; /* IE and Edge */
	scrollbar-width: none; /* Firefox */
}
.genres {
	span.active {
		color: rgb(251 146 60);
	}
}
// .scroll-container {
// 	/* Hide scrollbar for Chrome, Safari and Opera */
// 	::-webkit-scrollbar {
// 		display: none;
// 	}

// 	/* Hide scrollbar for IE, Edge and Firefox */

// 	-ms-overflow-style: none; /* IE and Edge */
// 	scrollbar-width: none; /* Firefox */

// }
</style>
