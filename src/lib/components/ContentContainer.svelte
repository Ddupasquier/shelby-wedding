<script>
    import containerBg from "$lib/images/shelby-content-container.png";
</script>

<div class="content-container" style="background-image: url({containerBg});">
    <div class="text-container">
        <slot />
    </div>
</div>

<style>
    .content-container {
        position: relative;
        background-size: 100% 100%;
        background-position: center center;
        background-repeat: no-repeat;
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 16vh 15vw;
    }

    .text-container {
        padding: 2rem;
        border-radius: 10px;
        max-width: 800px;
        width: 100%;
        font-family: "Source Sans Pro", sans-serif;
        text-align: center;
    }

    @media (max-width: 768px) {
        .text-container {
            padding: 3rem;
            max-width: 90%;
        }

        .content-container {
            padding: 10vh 5vw;
        }
    }
</style>
