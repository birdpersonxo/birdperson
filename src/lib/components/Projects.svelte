<script lang="ts">

</script>
<div class="projects-container">
    <div class="projects-wrapper">
        <div class='projects'>
            {@render project("/k2.png")}
            {@render project("/k1.png")}
            {@render project("/k2.png")}
        </div>
        <div class="project-content">
            <div class="temp">
                2D Global Illumination in COP
            </div>
            <div class="text">
                In contrast to the interaction-heavy home page, the case studies feature a clean and elegant content structure designed for ease of browsing and user familiarity. Each case study concludes with an interactive element that introduces additional pieces from Peter’s portfolio, echoing the homepage experience.
            </div>
        </div>
    </div>
    <div class="footer">
        <div class="footer-left">© Deepak Rajan. All rights reserved. </div>
        <div class="footer-right">
            <a href="https://www.youtube.com/@DeepakRajan">Youtube</a>
            <a href="https://www.linkedin.com/in/deepakrajanxo/">LinkedIn</a>
            <a href="https://www.instagram.com/deepak_rajan_/">Instagram</a>
            <a href="https://github.com/birdpersonxo/">Github</a>
            <a href="https://www.youtube.com/@DeepakRajan">Email</a>
        </div>
    </div>
</div>
{#snippet project(img: string)}
    <div class="project">
        <div class="img">
            <img src={img} alt="hero"/>
        </div>
        <div class="heading">
            <div class="main">
                2D Global Illumination in COPs
            </div>
            <div class="sub">
                After learning more about real-time lighting techniques, I wanted to tackle 2D Screen-Space Global Illumination (GI).
            </div>
        </div>
    </div>
{/snippet}

<style lang='scss'>
    .footer-right{
        display: flex;
        gap: 8px;
        a:hover{
            text-decoration: underline;
        }
    }
    .projects-container {
        display: flex;
        flex-direction: column;
        height: 100%;
        width: 100%;
    }


    .projects-wrapper {
        flex: 1;
        min-height: 0;
        width: 100%;
        display: flex;
        flex-direction: column;
        gap: 20px;
        .projects{
            display: flex;
            gap: 40px;
            justify-content: space-between;
            // padding: 20px;

        }

        .project-content{
            padding: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-direction: column;
            gap: 20px;
            height: 100%;

            .temp{
                font-size: 60px;
            }

            .text{
                width: 800px;
            }
        }
    }


    .footer {
        flex-shrink: 0;
        height: 60px;
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 0 20px;
        box-sizing: border-box;
        border-top: 1px solid var(--text-color);
    }

    .project {
        flex: 1;
        min-width: 0;

        .img {
            width: 100%;
            aspect-ratio: 16 / 7;

            img {
                width: 100%;
                height: 100%;
                object-fit: cover;
            }
        }

        .heading {
            .main {
                font-size: 22px;
            }
        }
    }
</style>
