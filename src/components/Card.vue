<template>
	<main
		class="bg-primary rounded-20 overflow-hidden flex flex-row my-15"
		@click="modal = true"
	>
		<img :src="item.thumbnailUrl" class="h-200 w-full object-cover" />
		<div class="px-30 flex flex-col justify-center items-end w-200">
			<h1 class="text-30">{{ item.title }}</h1>
			<h2 class="text-15 text-terciary">${{ item.precio }}.00</h2>
			<button class="px-5 py-2 rounded-20 bg-azul text-15 mt-15 w-fit">
				comprar
			</button>
		</div>
	</main>
</template>

<script>
export default {
	props: ['item'],
	data() {
		return {
			modal: false,
		};
	},
};
</script>
