<template>
	<div class="cursor-pointer">
		<div class="pic relative rounded-md overflow-hidden">
			<img
				class="w-full h-full"
				src="../assets/images/psychology of money.jpg"
				alt=""
			/>
			<span
				class="absolute top-1 right-1 bg-green-50 rounded-full"
			></span>
		</div>
		<div>
			<p
				class="text-ellipsis font-bold whitespace-nowrap overflow-x-clip my-1"
			>
				{{ title }}
			</p>
			<p class="font-semibold">{{ author }}</p>
		</div>
		<div class="flex mt-2 items-center">
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
				{{ stars }}</span
			>
			<span
				class="bg-purple-400 inline-flex items-center text-sm text-white rounded-full px-4 ml-3"
				v-if="isPicked"
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
						d="M16.5 3.75V16.5L12 14.25 7.5 16.5V3.75m9 0H18A2.25 2.25 0 0120.25 6v12A2.25 2.25 0 0118 20.25H6A2.25 2.25 0 013.75 18V6A2.25 2.25 0 016 3.75h1.5m9 0h-9"
					/>
				</svg>
				Picked</span
			>
		</div>
	</div>
</template>
<script>
export default {
	props: ["title", "author", "stars", "isPicked"],
};
</script>
