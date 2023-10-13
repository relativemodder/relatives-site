<script>
    import Skill from "./Skill.svelte";
    import jsSvg from "../../icons/js.svg";
    import htmlSvg from "../../icons/html.svg";
    import cssSvg from "../../icons/css.svg";
    import pythonSvg from "../../icons/python.svg";
    import csharpImg from "../../icons/csharp.png";
    import svelteSvg from "../../icons/svelte.svg";
    import reactSvg from "../../icons/react.svg";
    import phpSvg from "../../icons/php.svg";
    import sqlSvg from "../../icons/sql.svg";
    import bicepsSvg from "../../icons/biceps.svg";
</script>

<div class="card my-3">
    <div class="card-body d-flex skills-info">
        <h2 class="d-flex align-items-center">
            <img class="biceps me-2" src={bicepsSvg} alt="biceps" />
            My skills
        </h2>
        <div class="skills-container w-100">
            <Skill name="HTML" icon={htmlSvg} progress="91" />
            <Skill name="CSS" icon={cssSvg} progress="77" />
            <Skill name="JavaScript" icon={jsSvg} progress="56" />
            <Skill name="Svelte" icon={svelteSvg} progress="56" />
            <Skill name="React" icon={reactSvg} progress="45" />
            <Skill name="C#" icon={csharpImg} progress="55" />
            <Skill name="Python" icon={pythonSvg} progress="59" />
            <Skill name="PHP" icon={phpSvg} progress="85" />
            <Skill name="SQL" icon={sqlSvg} progress="35" />
        </div>
    </div>
</div>

<style>
    .skills-info {
        align-items: center;
        justify-content: center;
        flex-direction: column;
    }

    .biceps {
        width: 30px;
        height: 30px;
        object-fit: cover;
    }

    .skills-info .skills-container {
        margin-left: 2.5em;
        margin-right: 2.5em;
    }
</style>