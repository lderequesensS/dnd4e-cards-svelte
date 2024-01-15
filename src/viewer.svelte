<script>
	export let viewer = {}; // If I don't have an empty object it breaks, why?
	export let curLang;

	var style = "background:#4c4c4e;";

	$:
		if (viewer.type == curLang.types[0]) {
			style = "background:#649769;";
		} else if (viewer.type == curLang.types[1]) {
			style = "background:#981332;";
		} else {
			style = "background:#4c4c4e;";
		}
</script>

<div class="font-vecna border-black border-2">
	<div class="grid grid-cols-5" style={style}>
		<div>
			icon 1
			icon 2
		</div>
		<div class="col-span-2 text-center text-white">
			{viewer.name}
		</div>
		<div class="col-span-2 text-right text-white">
			{viewer.level}
		</div>
	</div>
	<div> <!-- Maybe there is a beautiful way to make the 2nd line to start after the rhombus -->
			{viewer.type + " ♦ " + viewer.keywords}
	</div>
	<p> {viewer.action + " " + viewer.range} </p>

	<div>
		{#each viewer.properties as property, idx}
			{#if viewer.gradients[idx]}
				<p style="background:linear-gradient(to right, #dcddcb, #ffffff)">
					{property}
				</p>
			{:else}
				<p>
					{property}
				</p>
			{/if}
		{/each}
	</div>


	<div class="text-center text-gray-500 text-lg">
		{viewer.description}
	</div>
</div>
