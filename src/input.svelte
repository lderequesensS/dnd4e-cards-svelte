<script>
	export let input;
	export let curLang;

	function addProperty() {
		input.properties.push('');
		input.gradients.push(false);
		input = input;
	}

	function removeProperty(idx) {
		input.properties.splice(idx, 1)
		input.gradients.splice(idx, 1)
		input = input
	}
</script>


<div class="grid grid-cols-2">
	<div class="relative w-full min-w-[200px] h-10">
		<input
			id="name"
			class="peer w-full border-b focus:outline-none focus:border-red-600 transition-colors"
			placeholder=" "
			bind:value={input.name}/>
		<label for="name"
			class="absolute left-0 -top-4 text-gray-600 text-sm peer-placeholder-shown:text-base peer-placeholder-shown:text-gray-400 peer-placeholder-shown:top-0.5 peer-focus:-top-4 peer-focus:text-sm peer-focus:text-gray-600 transition-all">{curLang.name}
		</label>
	</div>
	<div class="relative w-full min-w-[200px] h-10">
		<input
			id="level"
			class="peer w-full border-b focus:outline-none focus:border-red-600 transition-colors"
			placeholder=" "
			bind:value={input.level}/>
		<label for="level"
			class="absolute left-0 -top-4 text-gray-600 text-sm peer-placeholder-shown:text-base peer-placeholder-shown:text-gray-400 peer-placeholder-shown:top-0.5 peer-focus:-top-4 peer-focus:text-sm peer-focus:text-gray-600 transition-all">{curLang.level}
		</label>
	</div>

	<div class="col-span-2 h-3">
	</div>

	<div class="relative">
		<select id="icon1"
			class="peer w-full border-b focus:outline-none focus:border-red-600 transition-colors bg-white text-center"
			bind:value={input.icon1}
		>
			{#each curLang.iconsLetters as letter, idx}
				<option value={letter}>{curLang.iconsDescriptions[idx]}</option>
			{/each}
		</select>
		<label for="icon1"
			class="absolute left-0 -top-4 text-gray-600 text-sm peer-placeholder-shown:text-base peer-placeholder-shown:text-gray-400 peer-placeholder-shown:top-0.5 peer-focus:-top-4 peer-focus:text-sm peer-focus:text-gray-600 transition-all"> {curLang.icon + " " + 1}
		</label>
	</div>
	<div class="relative">
		<select id="icon2"
			class="peer w-full border-b focus:outline-none focus:border-red-600 transition-colors bg-white text-center"
			bind:value={input.icon2}
		>
			{#each curLang.iconsLetters as letter, idx}
				<option value={letter}>{curLang.iconsDescriptions[idx]}</option>
			{/each}
		</select>
		<label for="icon2"
			class="absolute left-0 -top-4 text-gray-600 text-sm peer-placeholder-shown:text-base peer-placeholder-shown:text-gray-400 peer-placeholder-shown:top-0.5 peer-focus:-top-4 peer-focus:text-sm peer-focus:text-gray-600 transition-all"> {curLang.icon + " " + 2}
		</label>
	</div>

	<div class="col-span-2 h-3">
	</div>

	<div class="col-span-2">
		<div class="grid grid-cols-5">
			<div class="relative h-10 col-span-2">
				<select id="type"
					class="peer w-full border-b focus:outline-none focus:border-red-600 transition-colors bg-white"
					bind:value={input.type}
				>
					{#each curLang.types as type}
						<option value={type}>{type}</option>
					{/each}
				</select>
				<label for="type"
					class="absolute left-0 -top-4 text-gray-600 text-sm peer-placeholder-shown:text-base peer-placeholder-shown:text-gray-400 peer-placeholder-shown:top-0.5 peer-focus:-top-4 peer-focus:text-sm peer-focus:text-gray-600 transition-all"> {curLang.type}
				</label>
			</div>
			<div class="relative h-10 col-span-3">
				<input
					id="keywords"
					class="peer w-full border-b focus:outline-none focus:border-red-600 transition-colors"
					placeholder=" "
					bind:value={input.keywords}/>
				<label for="keywords"
					class="absolute left-0 -top-4 text-gray-600 text-sm peer-placeholder-shown:text-base peer-placeholder-shown:text-gray-400 peer-placeholder-shown:top-0.5 peer-focus:-top-4 peer-focus:text-sm peer-focus:text-gray-600 transition-all">{curLang.keywords}
				</label>
			</div>
		</div>
	</div>

	<div class="col-span-2 h-3">
	</div>

	<div class="col-span-2">
		<div class="grid grid-cols-5">
			<div class="relative h-10 col-span-2">
				<select id="action"
					class="peer w-full border-b focus:outline-none focus:border-red-600 transition-colors bg-white"
					bind:value={input.action}
				>
					{#each curLang.actions as action}
						<option value={action}>{action}</option>
					{/each}
				</select>
				<label for="action"
					class="absolute left-0 -top-4 text-gray-600 text-sm peer-placeholder-shown:text-base peer-placeholder-shown:text-gray-400 peer-placeholder-shown:top-0.5 peer-focus:-top-4 peer-focus:text-sm peer-focus:text-gray-600 transition-all"> {curLang.action}
				</label>
			</div>
			<div class="relative h-10 col-span-3">
				<input
					id="range"
					class="peer w-full border-b focus:outline-none focus:border-red-600 transition-colors"
					placeholder=" "
					bind:value={input.range}/>
				<label for="range"
					class="absolute left-0 -top-4 text-gray-600 text-sm peer-placeholder-shown:text-base peer-placeholder-shown:text-gray-400 peer-placeholder-shown:top-0.5 peer-focus:-top-4 peer-focus:text-sm peer-focus:text-gray-600 transition-all"> {curLang.range}
				</label>
			</div>
		</div>
	</div>

	<div class="col-span-2 h-3">
	</div>

	<div class="relative h-10 min-w-[200px] col-span-2">
		<input
			id="description"
			class="peer w-full border-b focus:outline-none focus:border-red-600 transition-colors"
			placeholder=" "
			bind:value={input.description}/>
		<label for="description"
			class="absolute left-0 -top-4 text-gray-600 text-sm peer-placeholder-shown:text-base peer-placeholder-shown:text-gray-400 peer-placeholder-shown:top-0.5 peer-focus:-top-4 peer-focus:text-sm peer-focus:text-gray-600 transition-all"> {curLang.description}
		</label>
	</div>

	{#each input.properties as property, idx}
		<!-- space -->
		<div class="col-span-2 h-3">
		</div>

		<div class="relative col-span-2 grid grid-cols-5">
			<input
			id="property-{idx}"
			class="peer border-b focus:outline-none focus:border-red-600 transition-colors col-span-3"
			placeholder=" "
			bind:value={input.properties[idx]}/>
			<label for="property-{idx}"
				class="absolute left-0 -top-4 text-gray-600 text-sm peer-placeholder-shown:text-base peer-placeholder-shown:text-gray-400 peer-placeholder-shown:top-0.5 peer-focus:-top-4 peer-focus:text-sm peer-focus:text-gray-600 transition-all"> {curLang.property + " " + (idx + 1)}
			</label>
			<div class="flex justify-center">
				<button on:click={() => removeProperty(idx)} class="align-middle">
					<img src="/icons8-trash-30.svg" alt="delete" >
				</button>
			</div>
			<div class="flex justify-end">
				<input id="checkbox-{idx}" type="checkbox" bind:checked={input.gradients[idx]} class="h-5 w-5 align-middle" />
				<label for="checkbox-{idx}"
				class="absolute right-0 -top-5 text-gray-600 text-sm transition-all"> {curLang.gradient}
				</label>
			</div>
		</div>
	{/each}

	<div class="col-span-2 h-3">
	</div>

	<div class="col-span-2 grid grid-cols-3">
		<div>
		</div>
		<button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full" on:click={addProperty}>
			{curLang.add}
		</button>
	</div>

</div>

