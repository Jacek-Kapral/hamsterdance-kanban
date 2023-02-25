<script>
export default {
	name: 'KanbanBoard',
};
</script>

<template>
	<section>
		<div class="outer-board">
			<div class="inner-board">

			</div>
		</div>
	</section>
</template>

<style>
	.outer-board {
		position: relative;
		height: 90vh;
		width: 90%;
		margin-left: 5%;
		margin-right: 5%;
		margin-bottom: 5%;
		background: #BF6523;
		border-radius: 40px;
	}
	.inner-board {
		position: relative;
		transform: translate(-50%, -50%);
		height: 90%;
		width: 93%;
		top: 50%;
		left: 50%;
		background: #47A726;
		border-radius: 40px;
	}
</style>
