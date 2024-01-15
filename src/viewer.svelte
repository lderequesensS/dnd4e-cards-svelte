<script>
	export let viewer = {}; // If I don't have an empty object it breaks, why?
	export let curLang;

	var style = "background:#649769;";

	$:
		if (viewer.type == curLang.types[2]) {
			style = "background:#4c4c4e;";
		} else if (viewer.type == curLang.types[1]) {
			style = "background:#981332;";
		} else {
			style = "background:#649769;";
		}
</script>

<div class="font-vecna border-black border-2">
	<div class="grid grid-cols-5" style={style}>
		<div class="font-tool text-white text-center">
			{#if viewer.icon1 != '' && viewer.icon2 != ''}
				{viewer.icon1}{@html "&emsp;&emsp; "}{viewer.icon2}
			{:else}
				{viewer.icon1}{viewer.icon2}
			{/if}
		</div>
		<div class="col-span-3 text-center text-white">
			{viewer.name.toUpperCase()}
		</div>
		<div class="text-right text-white">
			{viewer.level}
		</div>
	</div>
	<p style="background:linear-gradient(to right, #dcddcb, #ffffff)" class="h-1 text-transparent"> a</p>
	<div> <!-- Maybe there is a beautiful way to make the 2nd line to start after the rhombus -->
		<div class="inline">
			{viewer.type.toUpperCase()}
		</div>
		<div class="font-tool inline">
			+
		</div>
		<div class="inline">
			{viewer.keywords}
		</div>
	</div>
	<!-- I divided this just to not think about sanitization -->
	<p> {viewer.action.toUpperCase()}{@html "&emsp;&emsp; "}{viewer.range} </p>

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
