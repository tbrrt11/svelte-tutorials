<script>
    import Anime from 'animejs/lib/anime.es.js';

    const mount = () => {
        Anime({
            targets: 'div',
            translateX: 250,
            backgroundColor: '#000',
            duration: 3000
        });
    };

</script>

<div use:mount>

</div>

<style>
    div {
        background-color: orangered;
        width: 100px;
        height: 100px
    }
</style>