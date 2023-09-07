<template>
	<div>
		<Card v-for="item in cards" :title="item.title" />
	</div>
</template>
<script>
export default {
	data() {
		return {
			cards: [
				{
					title: "item1",
				},
				{
					title: "item2",
				},
			],
		};
	},
};
</script>
