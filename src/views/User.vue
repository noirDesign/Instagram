<template>
	<Upuser />
	<main class="flex flex-col mx-15 mt-10 show">
		<section class="flex flex-row justify-between items-center">
			<img src="../assets/user.jpg" class="w-80 h-80 rounded-30" />
			<div class="flex flex-row rounded-20 overflow-hidden mx-20">
				<div
					class="flex flex-col hover:bg-primary px-8 py-20 items-center"
				>
					<h2>50</h2>
					<h4>publicacio...</h4>
				</div>

				<div
					class="flex flex-col hover:bg-primary px-8 py-20 items-center"
				>
					<h2>50</h2>
					<h4>seguidores</h4>
				</div>

				<div
					class="flex flex-col hover:bg-primary px-8 py-20 items-center"
				>
					<h2>50</h2>
					<h4>seguidos</h4>
				</div>
			</div>
		</section>
		<section class="flex flex-col w-full my-12">
			<h3>Nombre User</h3>
			<h4>holaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa</h4>
		</section>
		<section class="flex flex-row justify-between my-5">
			<div class="deg2 py-[6px] px-15 rounded-15">
				<h3>Editor perfil</h3>
			</div>

			<div class="bg-primary py-[6px] px-15 rounded-15">
				<h3>Promociones</h3>
			</div>

			<div class="bg-primary py-[6px] px-15 rounded-15">
				<h3>Estadisticas</h3>
			</div>
		</section>
	</main>
</template>

<script>
import Upuser from '../components/Upuser.vue';
export default {
	components: { Upuser },
};
</script>
