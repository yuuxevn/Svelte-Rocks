<script>
	// import
	import EmojiDisplay from './EmojiDisplay.svelte'
	import EmojiDes from './EmojiDes.svelte'

	let currentEmoji = 'A';
	const emojis = [ 'B', 'C', 'D', 'E' ];
	
	function randomizeEmoji() {
		return emojis[ Math.floor( Math.random() * emojis.length ) ]
	}
	function randomButton() {
		currentEmoji = randomizeEmoji();
	}

</script>
	
<style>
	div {
		margin: 5em;
	}
	button {
		background-color: #8bd3dd;
		padding: 0.75em;
		border-radius: 0.25em;
		border: 2px solid #000;
		box-shadow: 0.4rem 0.4rem #222;
	}
	button:hover {
		box-shadow: 0.25rem 0.25rem #222;
		transition: all 0.4 ease 0s;
		background-color: #8bd;
	}
</style>

<h1>Randomize Emoji</h1>
<EmojiDisplay { currentEmoji } />
<EmojiDes />
<button on:click={ randomButton } >Button</button>

