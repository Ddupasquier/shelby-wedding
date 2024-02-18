<script>
    import ContentContainer from "$lib/components/ContentContainer.svelte";
</script>

<svelte:head>
    <title>Shelby & Ethan</title>
</svelte:head>

<ContentContainer>
    <h1>Ethan & Shelby's Commitment Ceremony</h1>
    <p class="date-location">
        October 4-6, 2024<br />
        <a href="/where">Trout Creek Wilderness Lodge, Molalla, OR</a>
    </p>

    <p class="details">
        Accommodations will be provided on site.<br />
        <span class="note">(Text Shelby with questions)</span>
    </p>

    <h2>RSVP by April 1st, 2024</h2>
</ContentContainer>

<style>
    .date-location {
        font-size: 1.25rem;
        font-weight: 600;
        margin: 1.5rem 0;
    }

    .details {
        font-size: 1rem;
        margin-bottom: 1rem;
    }

    .note {
        font-style: italic;
        font-size: 0.9rem;
    }
</style>
