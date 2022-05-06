<template>
	<Uphome class="z-20" />
	<section class="flex-row flex mt-8 mb-15 overflow-x-scroll px-8">
		<UserStory />
		<Story v-for="item of items" :key="item.id" :item="item" />
	</section>
	<section class="mx-15">
		<Card v-for="item of items" :key="item.id" :item="item" />
	</section>
</template>

<script>
import Card from '../components/Card.vue';
import Uphome from '../components/Uphome.vue';
import Story from '../components/Story.vue';
import UserStory from '../components/UserStory.vue';
import { useStore } from 'vuex';
import { onMounted } from 'vue';
import { computed } from '@vue/reactivity';

export default {
	components: { Card, Uphome, Story, UserStory },

	setup() {
		const store = useStore();
		onMounted(() => {
			store.dispatch('fetchData');
		});

		const items = computed(() => store.state.items);

		return { items };
	},
};
</script>
