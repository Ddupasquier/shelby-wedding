<script>
    import { shelbyEthan2, shelbyEthan3 } from "$lib/images";
</script>

<div class="gallery">
    <img src={shelbyEthan2} alt="" class="photo" />
    <img src={shelbyEthan3} alt="" class="photo" />
</div>

<style>
    .gallery {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
        gap: 1rem;
        position: relative;
        overflow: hidden;
    }

    .photo {
        max-width: 40%;
        height: auto;
        border-radius: 8px;
        box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    }

    @media (max-width: 768px) {
        .gallery {
            flex-direction: column;
        }

        .photo {
            max-width: 100%;
        }
    }
</style>