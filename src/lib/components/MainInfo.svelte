<script>
    import { assets } from '$app/paths';
    import SocialLink from './SocialLink.svelte';

    function calculateAge(birthDate) {
        const dateOfBirth = new Date(birthDate);
        const currentDate = new Date();

        const ageInMilliseconds = currentDate - dateOfBirth;

        const ageInYears = Math.floor(ageInMilliseconds / (1000 * 60 * 60 * 24 * 365.25));

        return ageInYears
    }
</script>

<div class="card my-3">
    <div class="card-body d-flex main-info">
        <img alt="my-icon" src={assets + "/my-icon.png"} />
        <div class="main-text">
            <h2>Hello, I'm Relative!</h2>
            <p>
                <span>
                    <i class="bi bi-person me-2"></i>
                    Andrey, { calculateAge("2006-10-23") } y.o.
                </span>
                <br />
                <span>
                    <i class="bi bi-backpack4 me-2"></i>
                    <a href="https://mrsu.ru/en/" target="_blank">MRSU</a>
                    <span> Student</span>
                </span>
                <br />
                <span>
                    <i class="bi bi-braces me-2"></i>
                    Full-Stack Dev
                </span>
            </p>

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
        margin-left: 3em;
    }

    .main-info img {
        width: 180px;
        height: 180px;
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