<script>
    import { assets } from '$app/paths';
    import SocialLink from './SocialLink.svelte';
</script>

<div class="card">
    <div class="card-body d-flex main-info">
        <img alt="my-icon" src={assets + "/my-icon.png"} />
        <div class="main-text">
            <h2>Hello, I'm Relative!</h2>
            <p>I'm the programmer, so...</p>

            <div class="soc-links mt-4">
                <SocialLink href="https://github.com/relativemodder" icon="github">
                    My GitHub
                </SocialLink>
                <SocialLink href="https://t.me/notrlt" icon="telegram">
                    My Telegram
                </SocialLink>
            </div>
        </div>
    </div>
</div>

<style>
    .main-info {
        flex-direction: row;
        align-items: center;
        justify-content: start;
    }

    .main-info .main-text {
        margin-left: 2em;
    }

    .main-info img {
        width: 200px;
        height: 200px;
        object-fit: cover;
    }

    .soc-links {
        display: flex;
        flex-direction: row;
    }

    @media screen and (max-width: 600px) {
        .main-info {
            flex-direction: column;
            text-align: center;
        }
        .main-info img {
            width: 150px;
            height: 150px;
            object-fit: cover;
        }
        .soc-links {
            flex-direction: column;
        }
        .main-info .main-text {
            margin-top: 1.3em;
            margin-left: 0px;
        }
    }
</style>