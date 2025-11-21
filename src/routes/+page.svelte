<script lang="ts">
	let joke = $state('');

	const getJoke = async () => {
		const response = await fetch('https://official-joke-api.appspot.com/random_joke');
		const data = await response.json();
		joke = `${data.setup} - ${data.punchline}`;
	};
</script>

<main
	class="bg-[url(/src/img/lmao.jpeg)] bg-no-repeat bg-cover min-h-screen flex items-center justify-center flex-col gap-7"
>
	<h1 class="text-2xl font-bold font-sans text-center">Random Joke <br /> Generator</h1>
	<section
		class="p-10 bg-black rounded-md border shadow flex flex-col items-center gap-4 sm:min-w-100 sm:w-50"
	>
		<span class=" text-5xl">😂</span>
		<span class="text-white text-center font-sans">{joke}</span>
		<button
			class="px-8 py-2 bg-orange-300 font-bold cursor-pointer active:scale-95 hover:bg-blue-300 border rounded-sm text-sm"
			onclick={getJoke}
		>
			Get A Random Joke
		</button>
	</section>
</main>
<footer class="bg-gray-300 flex flex-col items-center gap-5 p-10">
	<h1 class="text-3xl text-gray-700 font-bold">Finals Activity 2</h1>
	<div class="flex flex-col sm:flex-row sm:flex gap-2 flex-wrap">
		<span class="bg-gray-800 text-white p-3 rounded-md">Eviota, Jhun Jay Mars</span>
		<span class="bg-gray-800 text-white p-3 rounded-md">Genon, Christian Owen</span>
		<span class="bg-gray-800 text-white p-3 rounded-md">Helera, Rommel Christian</span>
		<span class="bg-gray-800 text-white p-3 rounded-md">Balean, Patrick</span>
		<span class="bg-gray-800 text-white p-3 rounded-md">Berja, Alyssa</span>
	</div>
</footer>
