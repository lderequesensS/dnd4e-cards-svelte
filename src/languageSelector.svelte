<script>
	import languages from "./languages.js";
	export let selectedLang;
	export let curLang;
</script>

<div class="text-right font-vecna">
	{curLang.language}:
	<select
		bind:value={selectedLang}
		on:change={() => curLang = languages[selectedLang]}
	>
		{#each languages as language}
			<option value={language.idx}>
				{language.languageName}
			</option>
		{/each}
	</select>
</div>
