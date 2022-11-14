<template>
    <div class="container">

        <img class="left-arrow" src="arrow.png" alt="">
        <img class="right-arrow" src="arrow.png" alt="">

        <div class="bg-img"></div>
        <div class="content">
            <div class="left-side">
                <img src="project.png" alt="">
                <button>VIEW PROJECT</button>
            </div>
            <div class="text">
                <h4>HIGHLIGHTED SHOWCASE</h4>
                <h3>LP CLUB MOBILE APP</h3>
                <p>Cras quis nulla commodo, aliquam lectus sed, blandit augue. Cras ullamcorper bibendum bibendum. Duis
                    tincidunt urna non pretium porta. Nam condimentum vitae ligula vel ornare. Phasellus at semper
                    turpis.
                    Nunc eu tellus tortor. Etiam at condimentum nisl, vitae sagittis orci. Donec id dignissim nunc.
                    Donec
                    elit ante, eleifend a dolor et, venenatis facilisis dolor. In feugiat orci odio, sed lacinia sem
                    elementum quis. Aliquam consectetur, eros et vulputate euismod, nunc leo tempor lacus, ac rhoncus
                    neque
                    eros nec lacus. Cras lobortis molestie faucibus.</p>
            </div>
        </div>
    </div>
</template>

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


.left-arrow,
.right-arrow {
    position: absolute;
    top: 50%;
    z-index: 5;
    padding: 0 50px;
}

.right-arrow {
    right: 0;
    transform: rotate(180deg);
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
    padding: 10%;
}

.left-side {
    position: relative;
    flex: 1;
    // & .img-matte {
    //     width: 540px;
    //     height: 540px;
    //     overflow: hidden;
    //     border-radius: 20px;
    //     object-fit: cover;
    // }
    // & div {
    //     position: relative;
    // }

    & img {
        width: 40vw;
        min-width: 400px;
        border-radius: 20px;
    }

}

.text {
    flex: 1;
    color: white;
    padding-left: 62px;
    position: relative;
    z-index: 5;

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



button {
    position: absolute;
    // right: -10%;
    left: 60%;
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
    // padding: 60px 33px 61px 33px;
    width: 300px;
    height: 140px;
    // margin: 0 auto;
    // margin-top: 30px;
    display: flex;
    align-items: center;
    justify-content: center;


    &::after {
        content: '';
        display: inline-block;
        width: 70px;
        height: 2px;
        background-color: white;
        margin-left: 26px;
    }
}

@keyframes left-arrow-bounce {
    0% {
        left: 0;
    }

    50% {
        left: 10px
    }

    100% {
        left: 0;
    }
}

@keyframes right-arrow-bounce {
    0% {
        right: 0;
    }

    50% {
        right: 10px
    }

    100% {
        right: 0;
    }
}

.left-arrow {
    animation: left-arrow-bounce infinite;
    animation-duration: .5s;
}

.right-arrow {
    animation: right-arrow-bounce infinite;
    animation-duration: .5s;
}

@media(max-width: 1200px) {
    .content {
        flex-direction: column;

        & .left-side {
            margin-left: 20%;
        }

        & .text {
            margin-top: 100px;
            padding: 0;
        }
    }

    button {
        left: 40%;
    }

    .left-arrow,
    .right-arrow {
        padding: 0 20px;
    }

}
</style>