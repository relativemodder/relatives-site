<script>
    export let href;
    export let icon;
</script>

<a class="soc-link mt-3" href={href} target="_blank">
    <i class={"me-2 bi bi-" + icon}></i>
    <slot />
</a>

<style>
    .soc-link {
        display: flex;
        align-items: center;
        color: var(--bs-body-color);
        text-decoration: none;
        transition: 0.3s;
        font-size: 14pt;
        margin-right: 1em;
    }

    .soc-link .bi {
        font-size: larger;
    }

    .soc-link:hover {
        color: var(--bs-tertiary-color);
    }

    @media screen and (max-width: 600px) {
        .soc-link {
            justify-content: center;
            margin-right: 0px;
        }
    }
</style>