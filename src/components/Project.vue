<template>
    <div class="container">
        <Carousel :autoplay="2000">
            <slide v-for="slide in slides" :key="slide">

                <div class="bg-img"></div>
                <div class="content">
                    <div class="left-side">
                        <img src="project.png" alt="">
                        <button class="main-btn">VIEW PROJECT</button>
                    </div>
                    <div class="text">
                        <h4>{{ slide.subtitle }}</h4>
                        <h3>{{ slide.title }}</h3>
                        <p>Cras quis nulla commodo, aliquam lectus sed, blandit augue. Cras ullamcorper bibendum
                            bibendum. Duis
                            tincidunt urna non pretium porta. Nam condimentum vitae ligula vel ornare. Phasellus at
                            semper
                            turpis.
                            Nunc eu tellus tortor. Etiam at condimentum nisl, vitae sagittis orci. Donec id
                            dignissim
                            nunc.
                            Donec
                            elit ante, eleifend a dolor et, venenatis facilisis dolor. In feugiat orci odio, sed
                            lacinia
                            sem
                            elementum quis. Aliquam consectetur, eros et vulputate euismod, nunc leo tempor lacus,
                            ac
                            rhoncus
                            neque
                            eros nec lacus. Cras lobortis molestie faucibus.</p>
                    </div>
                </div>

            </slide>
            <template #addons>
                <Navigation></Navigation>
            </template>

        </Carousel>

    </div>
</template>

<script>
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'

export default {
    name: 'App',
    data() {
        return {
            slides: [
                { id: 1, title: 'LP CLUB MOBILE APP', subtitle: 'HIGHLIGHTED SHOWCASE' },
                { id: 2, title: 'LP CLUB MOBILE APP2', subtitle: 'HIGHLIGHTED SHOWCASE2' },
                { id: 3, title: 'LP CLUB MOBILE APP3', subtitle: 'HIGHLIGHTED SHOWCASE3' },
            ]
        }
    },
    components: {
        Carousel,
        Slide,
        Pagination,
        Navigation,
    },
}

</script>

<style lang="scss" scoped>
$colorBlue: #26C6D0;
$colorPurple: #585880;
$colorPink: #EE6C8A;
$colorYellow: #FFBC58;

.container {
    margin: 0;
    position: relative;
    top: -50px;
    overflow: hidden;
    border-radius: 0 0 50px 50px;
}

.bg-img {
    filter: blur(10px);
    background: linear-gradient(0deg, rgba(0, 0, 0, 0.75), rgba(0, 0, 0, 0.75)), url(../assets/project.png);
    background-blend-mode: normal, multiply;
    background-size: cover;
    position: absolute;
    width: 100%;
    height: 100%;
    transform: scale(1.05);
}

.content {
    display: flex;
    justify-content: center;
}

.carousel__slide {
    padding: 10%;

}


.left-side {
    position: relative;
    flex: 1;

    & img {
        width: 35vw;
        min-width: 300px;
        border-radius: 20px;
    }

}

.text {
    flex: 1;
    color: white;
    padding-left: 62px;
    position: relative;
    z-index: 5;
    text-align: start;

    & h4 {
        font-style: normal;
        font-weight: 700;
        font-size: 16px;
        line-height: 19px;
        letter-spacing: 2.22222px;
    }

    & h3 {
        font-style: normal;
        font-weight: 700;
        font-size: 32px;
        line-height: 39px;
        letter-spacing: 3.63636px;

    }

    & p {
        font-style: normal;
        font-weight: 400;
        font-size: 16px;
        line-height: 24px;
        letter-spacing: 1px;
    }

}



.main-btn {
    position: absolute;
    left: 45%;
    bottom: -10%;
    font-family: "proxima-nova";
    font-style: normal;
    font-weight: 700;
    font-size: 16px;
    line-height: 19px;
    letter-spacing: 2.22222px;
    color: white;
    border: none;
    background: $colorBlue;
    border-radius: 1px;
    width: 300px;
    height: 140px;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: .5s;


    &::after {
        content: '';
        display: inline-block;
        width: 70px;
        height: 2px;
        background-color: white;
        margin-left: 26px;
        transition: .5s;

    }

    &:hover {
        cursor: pointer;
        background-color: white;
        color: $colorBlue;
        transition: .5s;

        &::after {
            background-color: $colorBlue;
            transition: .5s;

        }
    }
}



@media(max-width: 1200px) {
    .content {
        flex-direction: column;

        & .left-side {
            margin-left: 0;

            & button {
                height: 100px;
            }
        }

        & .text {
            margin-top: 100px;
            padding: 0;
        }
    }

    .main-btn {
        left: 40%;
    }


}

@media(max-width: 560px) {
    .content {
        & .left-side {
            margin: 0 auto;

            & button {
                position: relative;
                top: 0;
                left: 0;
                margin-top: 30px;
                height: 20px;
                background-color: transparent;
                z-index: 1;
                color: white;

                &::after {
                    content: '';
                    position: absolute;
                    display: block;
                    margin: 0;
                    width: 0px;
                    height: 8px;
                    background-color: $colorBlue;
                    top: 10px;
                    z-index: -1;
                }
            }
        }

        @keyframes showHighlight {
            0% {
                width: 0;
            }

            100% {
                width: 150px;
            }
        }

        & button:hover {
            cursor: pointer;

            &::after {
                animation: showHighlight forwards;
                animation-duration: .5s;
            }
        }

        & .text {
            margin-top: 50px;
        }
    }
}
</style>