<template>
	<main class="w-full bg-primary rounded-25 p-10 mb-20 flex-col show">
		<section class="w-full flex flex-row justify-between items-center">
			<div id="izq" class="flex flex-row items-center bg-primary">
				<img :src="item.userimg" class="w-38 rounded-full" />
				<div class="mx-8">
					<h3>{{ item.nombre }}</h3>
					<h4>{{ item.lugar }}</h4>
				</div>
			</div>
			<div id="der" class="btn hover:bg-secundary">
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
					class="btn flex flex-row items-center mr-5 hover:bg-secundary"
				>
					<img src="../assets/icons/heart.svg" class="w-22 mr-5" />
					<h3>{{ item.card.likes }}</h3>
				</div>
				<div
					class="btn flex flex-row items-center mr-5 hover:bg-secundary"
				>
					<img src="../assets/icons/chat.svg" class="w-22 mr-5" />
					<h3>{{ item.card.com }}</h3>
				</div>
				<div class="btn hover:bg-secundary mr-5">
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
	<main
		class="bg-primary rounded-30 overflow-hidden flex flex-col my-20 mx-40"
	>
		<img :src="item.thumbnailUrl" class="object-cover h-200" />
		<div class="flex flex-col p-15">
			<h1 class="text-20">{{ item.title }}</h1>
			<h2 class="text-10 text-terciary">${{ item.precio }}.00</h2>
			<button class="px-8 py-5 rounded-20 bg-azul text-15 mt-10 w-fit">
				comprar
			</button>
		</div>
	</main>
</template>

<script>
export default {
	props: ['item'],
};
</script>

<style>
.show {
	animation: show ease-in-out 0.3s;
}

@keyframes show {
	0% {
		transform: translateY(50px);
	}
}
</style>
