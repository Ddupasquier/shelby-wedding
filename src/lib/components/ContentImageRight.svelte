<script>
    import containerBg from "$lib/images/shelby-content-container.png";

    export let photo = "";
</script>

<div class="container">
    <div class="text-container">
        <img src={containerBg} alt="" class="container-bg" />
        <div class="text">
            <slot />
        </div>
    </div>

    {#if photo}
        <img src={photo} alt="" class="photo" />
    {/if}
</div>

<style>
    .container {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        position: relative;
        overflow: hidden;
    }

    .photo {
        max-width: 40%;
        height: auto;
        border-radius: 8px;
        box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    }

    .text-container {
        display: flex;
        align-items: center;
        justify-content: center;
        flex-grow: 1;
        position: relative;
    }

    .container-bg {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        z-index: 0;
        filter: sepia(100%);
    }

    .text {
        position: relative;
        z-index: 1;
        color: #000000;
        font-size: 16px;
        line-height: 1.5;
        margin: 8rem;
    }

    @media (max-width: 768px) {
        .container {
            flex-direction: column;
        }

        .photo {
            max-width: 100%;
            order: 1;
        }
        
        .text-container {
            order: 2;
        }

        .text {
            margin: 4rem;
        }
    }
</style>
