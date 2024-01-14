<script>
	export let viewer = {}; // If I don't have an empty object it breaks, why?
	export let curLang;
</script>

<div class="grid grid-cols-1 font-vecna">
	This is viewer
	<div>
		{viewer.name}
	</div>
</div>
