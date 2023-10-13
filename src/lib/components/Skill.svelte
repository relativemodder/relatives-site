<script>
    export let progress;
    export let name;
    export let icon;
</script>

<div class="skill mt-4 w-100">
    <div class="skill-info w-100">
        <img alt={name} src={icon} />
        <span>{name}</span>
    </div>
    <div class="progress mt-2 w-100" role="progressbar" aria-label="Example with label" aria-valuenow={progress} aria-valuemin="0" aria-valuemax="100">
        <div class="progress-bar" style={`width: ${progress}%`}>{progress}%</div>
    </div>
</div>

<style>

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
</style>