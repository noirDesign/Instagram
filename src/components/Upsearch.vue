<template>
	<main class="up flex-col justify-between">
		<section
			class="bg-primary flex flex-row px-15 rounded-20 w-full justify-between overflow-hidden"
		>
			<input
				type="text"
				placeholder="Buscar"
				class="bg-primary text-15 w-full h-40"
			/>
			<img src="../assets/icons/search.svg" class="w-22" />
		</section>
		<section class="flex flex-row mt-10 justify-between w-full show">
			<div
				class="flex flex-row items-center bg-primary py-5 px-10 rounded-15"
			>
				<img src="../assets/icons/category.svg" class="w-22 mr-5" />
				<h3>Todo</h3>
			</div>

			<div
				class="flex flex-row items-center bg-primary py-5 px-10 rounded-15"
			>
				<img src="../assets/icons/short.svg" class="w-22 mr-5" />
				<h3>Reels</h3>
			</div>

			<div
				class="flex flex-row items-center bg-primary py-5 px-10 rounded-15"
			>
				<img src="../assets/icons/tv1.svg" class="w-22 mr-5" />
				<h3>Ig Tv</h3>
			</div>

			<div
				class="flex flex-row items-center bg-primary py-5 px-10 rounded-15"
			>
				<img src="../assets/icons/cart1.svg" class="w-22 mr-5" />
				<h3>Tienda</h3>
			</div>
		</section>
	</main>
</template>
