<template>
    <div class="container">

        <h2 id="service">&nbsp;&nbsp;OUR INGRADIENTS&nbsp;&nbsp;</h2>
        <p>
            Cras quis nulla commodo, aliquam lectus sed, blandit augue. Cras ullamcorper bibendum bibendum. Duis
            tincidunt
            urna non pretium porta. Nam condimentum vitae ligula vel ornare. Phasellus at semper turpis. Nunc eu tellus
            tortor. Etiam at condimentum nisl, vitae sagittis orci. Donec id dignissim nunc. Donec elit ante, eleifend a
            dolor et, venenatis facilisis dolor. In feugiat orci odio, sed lacinia sem elementum quis. Aliquam
            consectetur,
            eros et vulputate euismod, nunc leo tempor lacus, ac rhoncus neque eros nec lacus. Cras lobortis molestie
            faucibus.
        </p>
        <button class="service-btn">OUR SERVICES</button>
        <div class="services">
            <div class="service-col">
                <div class="service" v-for="service in services">

                    <div class="circle">
                        <img :src=service.img alt="">
                    </div>

                    <h4>{{ service.title }}</h4>
                    <p>Cras quis nulla commodo, aliquam lectus sed, blandit augue. Cras ullamcorper bibendum bibendum.
                        Duis
                        tincidunt urna non pretium porta. Nam condimentum vitae ligula vel ornare.</p>
                    <button>VIEW MORE</button>
                </div>
            </div>

        </div>
        <a href="#">VIEW MORE DIGISALAD’S INGRADIENTS</a>
    </div>
</template>

<script>
export default {
    name: 'service',
    data() {
        return {
            services: [
                { id: 1, img: 'service-01.png', title: 'UX Design' },
                { id: 2, img: 'service-02.png', title: 'UI Design' },
                { id: 3, img: 'service-03.png', title: 'website development' },
                { id: 4, img: 'service-04.png', title: 'mobile app development' },
                { id: 5, img: 'service-05.png', title: 'ecommerce' },
                { id: 6, img: 'service-06.png', title: 'customer loyalty' },
                { id: 7, img: 'service-07.png', title: 'digital transformation' },
                { id: 8, img: 'service-08.png', title: 'digital marketing' },
                { id: 9, img: 'service-09.png', title: 'BRANDING' }
            ]
        }
    }
}

</script>

<style lang="scss" scoped>
$colorBlue: #26C6D0;
$colorPurple: #585880;
$colorPink: #EE6C8A;
$colorYellow: #FFBC58;

.container {
    background-color: $colorBlue;
    border-radius: 50px;
    padding-top: 320px;
    margin-top: 286px;
    padding: 320px 10%;
    padding-bottom: 500px;
    text-align: center;
    position: relative;
    z-index: 0;


    &>p {
        color: white;
        text-align: center;
        font-family: 'Proxima Nova';
        font-style: normal;
        font-weight: 400;
        font-size: 16px;
        line-height: 28px;
        letter-spacing: 1px;
        margin-top: 50px;
        margin-bottom: 30px;
    }
}

h2 {
    text-align: center;
    color: white;
    text-decoration-style: wavy;
    text-decoration-line: underline;
    text-decoration-thickness: 3px;
    text-decoration-color: $colorPurple;
    text-underline-offset: 10px;

    &::after {
        content: '';
        width: 10px;
        height: 10px;
        border-radius: 50%;
        background-color: $colorPink;
        display: inline-block;
        margin-left: -10px;
    }
}

.services {
    margin-top: 85px;
    margin-bottom: 102px;
}

.service-col {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}

.service {
    width: 33%;
    padding: 30px 25px;

    & div,
    button {
        display: block;
        margin: 0 auto;
    }

    & h4 {
        margin: 0;
        margin-top: 20px;
        color: white;
        font-style: normal;
        font-weight: 700;
        font-size: 20px;
        line-height: 24px;
        text-align: center;
        letter-spacing: 2px;
        text-transform: uppercase;
    }

    & p {
        color: white;
        text-align: center;
        font-family: 'Proxima Nova';
        font-style: normal;
        font-weight: 400;
        font-size: 16px;
        line-height: 28px;
        letter-spacing: 1px;
        margin: 0;
        margin-top: 15px;
    }

    & button {
        background-color: transparent;
        border: 2px solid white;
        color: white;
        border-radius: 30px;
        padding: 21px 34px 20px 35px;
        font-style: normal;
        font-weight: 700;
        font-size: 14px;
        line-height: 17px;
        letter-spacing: 2.22222px;
        margin-top: 30px;
        transition: .5s;



        &:hover {
            cursor: pointer;
            border: 2px solid transparent;
            background-color: white;
            color: $colorBlue;
            transition: .5s;

        }

    }
}



.circle {
    width: 108px;
    height: 108px;
    background-color: white;
    border-radius: 50%;
    position: relative;


    & img {
        display: block;
        position: absolute;
        left: 50%;
        top: 50%;
        transform: translateX(-50%) translateY(-50%)
    }

}

.service-btn {
    font-family: "proxima-nova";
    font-style: normal;
    font-weight: 700;
    font-size: 16px;
    line-height: 19px;
    letter-spacing: 2.22222px;
    color: white;
    border: none;
    background: $colorPurple;
    border-radius: 1px;
    padding: 33px 24.53px 34px 24.53px;
    margin: 0 auto;
    margin-top: 30px;
    display: flex;
    align-items: center;
    transition: .5s;


    &::after {
        content: '';
        display: inline-block;
        width: 52.03px;
        height: 2px;
        background-color: white;
        margin-left: 15px;
    }

    &:hover {
        cursor: pointer;
        background-color: $colorYellow;
        transition: .5s;
    }
}

a {
    font-style: normal;
    font-weight: 700;
    font-size: 18px;
    line-height: 22px;
    letter-spacing: 2px;
    text-transform: uppercase;
    text-decoration: none;
    color: white;

    &::after {
        content: '';
        display: block;
        background-color: $colorYellow;
        width: 0;
        height: 8px;
        margin: 0 auto;
        position: relative;
        top: -10px;
        z-index: -1;
    }
}

@keyframes showHighlight {
    0% {
        width: 0;
    }

    100% {
        width: 416px;
    }
}

a:hover {
    &::after {
        animation: showHighlight forwards;
        animation-duration: .5s;
    }
}
@media(max-width: 1200px) {
    .container{
        padding-top: 420px;
    }
}
@media(max-width: 960px) {
    .container {
        margin-top: 800px;
        padding-top: 300px;
        padding-bottom: 400px;

        & h2 {
            line-height: 68px;
        }


        & .service {
            width: 100%;
        }
    }
}
</style>