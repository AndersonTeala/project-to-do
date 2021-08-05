<template>
	<div id="app">
		<h1>Tarefas</h1>
		<TaskGrid :tasks="tasks" />
	</div>
</template>

<script>
import TaskGrid from './components/TaskGrid.vue'
export default {
	components: { TaskGrid },
	data(){
		return{
			tasks: [
				{ name: 'Lavar a louça', pending: false },
				{ name: 'Comprar um celular', pending: true },
			]
		}
	}

}
</script>

<style>
	body {
		font-family: 'Lato', sans-serif;
		background: rgb(2,0,36);
		background: linear-gradient(90deg, rgba(2,0,36,1) 0%, rgba(82,72,160,1) 35%, rgba(0,212,255,1) 100%);
		color: #FFF;
	}

	#app {
		display: flex;
		flex: 1;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		height: 100vh;
	}

	#app h1 {
		margin-bottom: 5px;
		font-weight: 300;
		font-size: 3rem;
	}
</style>
