<script>
    import IntersectionObserver from "./IntersectionObserver.svelte";

    export let progress;
    export let name;
    export let icon;

</script>

<IntersectionObserver let:intersecting once={false} top="-80">
    <div class={"skill mt-4 w-100" + (intersecting ? " visible" : "")}>
        <div class="skill-info w-100">
            <img alt={name} src={icon} />
            <span>{name}</span>
        </div>
        <div class="progress mt-2 w-100" role="progressbar" aria-label="Example with label" aria-valuenow={progress} aria-valuemin="0" aria-valuemax="100">
            <div class="progress-bar" style={`width: ${progress}%`}>{progress}%</div>
            <div class="progress-text-mobile">{progress}%</div>
        </div>
    </div>
</IntersectionObserver>

<style>

    .skill {
        opacity: 0.0;
        transition: 0.5s;
    }

    .skill.visible {
        opacity: 1.0;
    }

    .skill:not(
        .skill.visible
    ) .progress-bar {
        width: 0px!important;
    }

    .skill-info img {
        margin-right: 0.3em;
        width: 30px;
        height: 30px;
        object-fit: cover;
        border-radius: 8px;
    }

    .skill-info {
        margin-right: 1.4em;
    }

    .progress-text-mobile {
        display: none;
        margin-left: 0.5em;
        margin-right: 0.5em;
    }

    @media screen and (max-width: 600px) {
        .skill-info {
            text-align: center;
        }

        .progress-text-mobile {
            display: block;
        }

        .progress-bar {
            color: transparent;
        }
    }
</style>