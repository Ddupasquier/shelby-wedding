<script>
    import ContentContainer from "$lib/components/ContentContainer.svelte";
    import { Loader } from "mysvelte-ui";
    import { onMount } from "svelte";

    let isIframeLoading = true;

    function handleIframeLoad() {
        isIframeLoading = false;
    }
</script>

<svelte:head>
    <title>Where</title>
</svelte:head>

<ContentContainer>
    {#if isIframeLoading}
        <div class="spinner">
            <Loader color="#D9822F" />
        </div>
    {/if}

    <iframe
        on:load={handleIframeLoad}
        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2817.581086716331!2d-122.4875865224496!3d45.07400837107024!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x54bfdbc36f89b80d%3A0xe26e69d5eb2eaba2!2sTrout%20Creek%20Wilderness%20Lodge!5e0!3m2!1sen!2sus!4v1708246647351!5m2!1sen!2sus"
        width="600"
        height="450"
        style="border:0; border-radius: 8px;"
        allowfullscreen
        loading="lazy"
        referrerpolicy="no-referrer-when-downgrade"
        title="Trout Creek Wilderness Lodge"
    ></iframe>
</ContentContainer>

<style>
    .spinner {
        position: absolute;
        width: 50px;
        height: 50px;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        display: flex;
        justify-content: center;
        align-items: center;
    }
</style>
