<template>
	<main class="w-full bg-primary rounded-25 p-10 mb-20 flex-col">
		<section class="w-full flex flex-row justify-between items-center">
			<div id="izq" class="flex flex-row items-center bg-primary">
				<img :src="item.userimg" class="w-38 rounded-full" />
				<div class="mx-8">
					<h3>{{ item.nombre }}</h3>
					<h4>{{ item.lugar }}</h4>
				</div>
			</div>
			<div id="der" class="btn hover:bg-secundary" @click="modal = true">
				<img src="../assets/icons/more.svg" class="w-15" />
			</div>
		</section>
		<img
			:src="item.card.cardimg"
			class="my-8 rounded-25 w-full max-h-[390px] object-cover"
		/>
		<section class="w-full flex flex-row justify-between items-center my-8">
			<div class="flex flex-row">
				<div
					class="btn flex flex-row items-center rounded-20 mr-5 hover:bg-secundary"
				>
					<img src="../assets/icons/heart.svg" class="w-22 mr-5" />
					<h3>{{ item.card.likes }}</h3>
				</div>
				<div
					class="btn flex flex-row items-center rounded-20 mr-5 hover:bg-secundary"
				>
					<img src="../assets/icons/chat.svg" class="w-22 mr-5" />
					<h3>{{ item.card.com }}</h3>
				</div>
				<div class="btn hover:bg-secundary rounded-20 mr-5">
					<img src="../assets/icons/send.svg" class="w-22" />
				</div>
			</div>
			<div class="btn hover:bg-secundary mr-5">
				<img src="../assets/icons/mark.svg" class="w-22" />
			</div>
		</section>
		<section class="px-8 cursor-pointer">
			<h3>{{ item.nombre }}</h3>
			<h4>
				{{ item.card.descripcion }}
			</h4>
		</section>
	</main>

	<main v-show="modal" @click="modal = false" class="screen">
		<section
			class="bg-primary rounded-20 overflow-hidden w-full h-fit show"
		>
			<div class="flex justify-center py-8">
				<div class="w-30 h-3 bg-terciary rounded-10"></div>
			</div>
			<div class="w-full p-15 hover:bg-secundary">
				<h3 class="text-rojo">Denunciar</h3>
			</div>
			<div class="w-full p-15 hover:bg-secundary"><h3>Compartir</h3></div>
			<div class="w-full p-15 hover:bg-secundary">
				<h3>Copiar enlace</h3>
			</div>
		</section>
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
