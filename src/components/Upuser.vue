<template>
	<main class="up flex-row justify-between">
		<section
			@click="modal = true"
			class="flex flex-row items-center hover:bg-primary rounded-15 py-5"
		>
			<h2 class="ml-5">Cambiar</h2>
			<img src="../assets/icons/abajo.svg" class="w-15 mx-5" />
		</section>
		<section class="flex flex-row">
			<div class="btn hover:bg-primary ml-8">
				<img src="../assets/icons/mas-cuadrado.svg" class="w-22" />
			</div>
			<div class="btn hover:bg-primary ml-8">
				<img src="../assets/icons/mark.svg" class="w-22" />
			</div>
		</section>
	</main>
	<main v-show="modal" @click="modal = false" class="screen">
		<section
			class="bg-primary rounded-20 overflow-hidden w-full h-fit show"
		>
			<div class="flex justify-center py-8">
				<div class="w-30 h-3 bg-terciary rounded-10"></div>
			</div>

			<div class="m-10">
				<div
					class="flex flex-row w-full p-5 rounded-20 overflow-hidden bg-secundary items-center"
				>
					<img
						src="../assets/user.jpg"
						class="w-40 rounded-50 mr-8"
					/>
					<h2>usuario xd</h2>
				</div>
			</div>

			<div class="m-10">
				<div
					class="flex flex-row w-full p-5 rounded-20 overflow-hidden items-center"
				>
					<img
						src="../assets/user.jpg"
						class="w-40 rounded-50 mr-8"
					/>
					<h2>usuario xd</h2>
				</div>
			</div>

			<div class="m-10">
				<div
					class="flex flex-row w-full p-5 rounded-20 overflow-hidden items-center"
				>
					<div
						class="w-40 h-40 p-8 rounded-50 bg-trans border border-solid border-blanco mr-8"
					>
						<img src="../assets/icons/mas.svg" />
					</div>
					<h2>Agregar otra cuenta</h2>
				</div>
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
