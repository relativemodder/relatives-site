<script>
    import { assets } from '$app/paths';
    import '../css/styles.css';
</script>

<svelte:head>
    <meta name="og:title" content="Relative's Bio" />
    <meta name="og:description" content="Just a programmer" />
    <meta name="og:image" content={assets + "/my-icon.png"} />
</svelte:head>

<slot />