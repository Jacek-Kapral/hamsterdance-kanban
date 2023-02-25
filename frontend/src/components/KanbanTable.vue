<script>
import axios from 'axios'

export default {
	name: 'KanbanTable',
	data() {
		return {
			kanbanTable: "Table"
		}
	},
	methods:{
		async getKanbanTableName() {
			this.kanbanTable = await axios.get(process.env.VUE_APP_BACKEND_URL + '/table')
			if (!this.kanbanTableName) this.kanbanTableName = "Table"
		}
	}
};
</script>

<template>
	<section class="table-name">
		{{ kanbanTable.name ? kanbanTable.name : "Table1" }}
	</section>
</template>

<style>
	.table-name {
	font-size: xx-large;	
	font-family: Avenir, Helvetica, Arial, sans-serif; 
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	}
</style>
