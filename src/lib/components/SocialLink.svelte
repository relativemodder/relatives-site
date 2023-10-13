<script>
    export let href;
    export let icon;
</script>

<a class="soc-link mt-3" href={href} target="_blank">
    <i class={"bi bi-" + icon}></i>
    <slot />
</a>

<style>
    .soc-link {
        display: flex;
        align-items: center;
        color: var(--bs-tertiary-color);
        text-decoration: none;
        transition: 0.3s;
        font-size: 14pt;
        margin-right: 1em;
    }

    .soc-link .bi {
        transition: 0.2s;
        font-size: larger;
        margin-right: 0.4em;
    }

    .soc-link:hover {
        color: var(--bs-body-color);
    }

    .soc-link:hover .bi {
        scale: 1.1;
        margin-right: 0.6em;
    }

    @media screen and (max-width: 600px) {
        .soc-link {
            justify-content: center;
            margin-right: 0px;
        }
    }
</style>