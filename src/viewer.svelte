<script>
	export let viewer = {}; // If I don't have an empty object it breaks, why?
</script>

<div class="font-vecna border-black border-2">
	<div class="grid grid-cols-5 bg-green-300">
		<div>
			icon 1
			icon 2
		</div>
		<div class="col-span-2 text-center">
			{viewer.name}
		</div>
		<div class="col-span-2 text-right">
			{viewer.level}
		</div>
	</div>
	<div> <!-- Maybe there is a beautiful way to make the 2nd line to start after the rhombus -->
			{viewer.type + " ♦ " + viewer.keywords}
	</div>
	<p> {viewer.action + " " + viewer.range} </p>

	<div>
		{#each viewer.properties as property}
			{property}
		{/each}
	</div>


	<div class="text-center text-gray-500 text-lg">
		{viewer.description}
	</div>
</div>
