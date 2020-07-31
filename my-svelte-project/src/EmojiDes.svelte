<script>
    let description = '';
    $: character = description.length;
    $: words = description.split(' ').length;

    $: if( description.length >= 10 ){
        console.log('-----');
        console.log('Description : ${ description }')
    }
</script>

<style>
    div {
        margin-bottom: 1em;
        margin-top: 1em;
    }
</style>

<div>
    <p>{ description }</p>
    <textarea bind:value={ description } cols="30" rows="10"></textarea>
    <p>Characters count : { character }</p>
    <p>word count : { words }</p>
</div>