<script>
	import Title from "./title.svelte";
	import languages from "./languages.js";
	import LanguageSelector from "./languageSelector.svelte";

	let selectedLang = 0; // Spanish as default
	let curLang = languages[selectedLang];
	let input; // Objeto??

</script>


<main>
	<Title />

	<LanguageSelector {selectedLang} {curLang}/> <!-- Check if is really necesary this props -->

	<div class="grid grid-cols-2">
		<div>
			Input
		</div>
		<div>
			Viewer
		</div>
	</div>
</main>

