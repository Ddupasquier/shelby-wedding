<script>
    import AboveFooter from "./AboveFooter.svelte";
</script>

<AboveFooter />
<footer class="footer">
    <div>
        <p>
            Contact Shelby: (585) 545-0708
        </p>
        <p>RSVP Required by April 1st, 2024</p>
        <!-- Newsletter form could be added here -->
        <p>We can't wait to see all of you!</p>
    </div>
</footer>

<style>
    /* Basic styling for footer */
    .footer {
        position: absolute;
        bottom: 0;
        width: 100%;
        background-color: #000000;
        padding: 20px;
        text-align: center;
        font-size: 14px;
        color: white;
        z-index: 1;
    }

    .footer p {
        margin: 5px 0;
    }
</style>
