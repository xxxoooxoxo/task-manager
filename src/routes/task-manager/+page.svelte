<script lang="ts">
	import TaskList from '../../components/TaskList.svelte';
	import { data } from '../../lib/taskData';
</script>

<div class="p-10 h-full">
	<div class="text-white text-2xl mb-6">Some List</div>
	<button class="text-xl mb-3 text-white font-bold cursor-pointer hover:underline flex items-start">
		+ Add List
	</button>
	<div class="flex-it h-full">
		<div class="flex-it flex-row rounded-xl h-full">
			{#each data as taskList}
				<TaskList title={taskList.text} tasks={taskList.items} />
			{/each}
		</div>
	</div>
</div>
