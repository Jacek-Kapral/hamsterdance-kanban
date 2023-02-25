<script>
import KanbanBoard from '@/components/KanbanBoard.vue';
import KanbanTable from '@/components/KanbanTable.vue';

export default {
	name: 'AppHome',
	components: {
		KanbanBoard,
		KanbanTable
	},
};
</script>

<template>
	<KanbanTable></KanbanTable>
	<KanbanBoard></KanbanBoard>
</template>

<style>
</style>