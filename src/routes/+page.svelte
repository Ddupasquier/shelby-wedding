<script>
    import ContentImageLeft from "$lib/components/ContentImageLeft.svelte";
    import ContentImageRight from "$lib/components/ContentImageRight.svelte";
    import Gallery from "$lib/components/Gallery.svelte";
    import {
        shelbyEthan1,
        shelbyEthan2,
        shelbyEthan3,
        shelbyEthan4,
    } from "$lib/images";
</script>

<svelte:head>
    <title>Shelby & Ethan</title>
</svelte:head>

<div class="content">
    <ContentImageLeft photo={shelbyEthan4}>
        <p class="info-text large-text">
            October 4-6, 2024<br />
            <a href="/where" class="info-link"
                >Trout Creek Wilderness Lodge
                <br />
                Molalla, OR</a
            >
        </p>

        <p class="info-text">
            Accommodations will be provided on site.<br />
            <span class="additional-note">(Text Shelby with questions)</span>
        </p>

        <h2 class="section-title">RSVP by April 1st, 2024</h2>
    </ContentImageLeft>

    <ContentImageRight photo={shelbyEthan1}>
        <a
            href="https://docs.google.com/forms/d/1QJ_RZ3UR32VgYGapmpBj3AgBBWJJ_dykjbQqoREp90Q/edit?ts=65d7f5c7"
            class="button"
            target="_blank"
            rel="noopener noreferrer">RSVP HERE</a
        >
    </ContentImageRight>

    <Gallery />
</div>

<style>
    .info-text {
        font-size: 1rem;
        margin-bottom: 1rem;
    }

    .large-text {
        font-size: 1.25rem;
        font-weight: 600;
        margin: 1.5rem 0;
    }

    .additional-note {
        font-style: italic;
        font-size: 0.9rem;
    }

    .content {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 2rem;
    }
    .button {
        padding: 1rem 2rem;
        font-size: 1.25rem;
        font-weight: 600;
        border-radius: 8px;
        background-color: darkgreen;
        color: #ffffff;
        border: none;
        cursor: pointer;
        transition: background-color 0.2s;
        font-family: "Playfair Display", serif;
    }
</style>
