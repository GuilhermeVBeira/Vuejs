<template>
	<div id="app">
		<h1>Tarefas</h1>
		<Taskgrid :tasks="tasks"/>
	</div>
</template>

<script>
import Taskgrid from './components/TaskGrid.vue'

export default {
	components: {Taskgrid},
	data() {
		return {
			tasks: [
				{name: "Lavar a louça", pending: false},
				{name: "Passar no mercado", pending: true},
			]
		}	
	}
}
</script>

<style>
	body {
		font-family: 'Lato', sans-serif;
		background: linear-gradient(to right, rgb(22, 34, 42), rgb(58, 96, 115));
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
