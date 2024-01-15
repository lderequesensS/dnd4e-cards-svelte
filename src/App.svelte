<script>
	import Title from "./title.svelte";
	import languages from "./languages.js";
	import LanguageSelector from "./languageSelector.svelte";
	import Input from "./input.svelte";
	import Viewer from "./viewer.svelte";

	let selectedLang = 0; // Spanish as default
	let curLang = languages[selectedLang];
	let input = {
		name: '',
		level: '',
		type: curLang.types[0],
		action: curLang.actions[0],
		description: '',
		range: '',
		keywords: '',
		properties: [''],
		gradients: [false],
		icon1: 'a',
		icon2: '',
	}

</script>


<main>
	<Title />

	<LanguageSelector {selectedLang} bind:curLang={curLang}/>

	<div class="grid grid-cols-1 lg:grid-cols-2 space-x-2 space-y-3">
		<div>
			<Input bind:input={input} {curLang}/>
		</div>
		<div>
			<Viewer viewer={input} {curLang}/>
		</div>
	</div>
</main>

