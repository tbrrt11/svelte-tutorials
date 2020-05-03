<script>
    import { onMount } from 'svelte';
    import Anime from 'animejs/lib/anime.es.js';

    onMount(async () => {
        Anime({
            targets: 'div',
            translateX: 250,
            backgroundColor: '#000',
            duration: 3000
        });
    });

</script>

<div>

</div>

<style>
    div {
        background-color: orangered;
        width: 100px;
        height: 100px
    }
</style>