<template>
    <div class="video-container">

        <video autoplay loop muted type="video/mp4" src="DigiSalad Website Videov3_1080p.mp4"></video>
    </div>
    <div class="title">
        <div class="text">
            <div class="leftText">
                <h5>DIGITAL AGENCY</h5>
            </div>
            <div class="mainText">
                <img src="digisalad.png" alt="">
                <h1>WE CREATE
                    <br>
                    AMAZING
                    <br>
                    DIGITAL EXPERIENCES
                    <div class="dot"></div>
                </h1>
            </div>
            <div class="mainText-RWD">
                <img src="digisalad.png" alt="">
                <h1>WE CREATE
                    <br>
                    AMAZING
                    <br>
                    DIGITAL
                    <br>
                    EXPERIENCES
                    <div class="dot"></div>
                </h1>
            </div>

        </div>
        <div class="end">
            <img src="salad.png" alt="">
            <h3>TASTE US NOW!</h3>
        </div>

    </div>
</template>

<script>
export default {
    name: 'FirstPart',
}
</script>

<style lang="scss" scoped>

$colorBlue: #26C6D0;
$colorPurple: #585880;
$colorPink: #EE6C8A;
$colorYellow: #FFBC58;

* {
    box-sizing: border-box;
    font-family: "proxima-nova";
}

.title {
    position: relative;
    background-color: rgba(black, 0.3);
    width: 100%;
    height: 100vh;
    border-radius: 0 0 50px 50px;
    display: flex;
    justify-content: space-around;
    flex-direction: column;
}

h1 {
    position: relative;
    font-style: normal;
    font-weight: 700;
    font-size: 38px;
    line-height: 70px;
    letter-spacing: 9.16667px;
    margin: 0;
    color: white;
    z-index: 1;

    &::after {
        content: '';
        display: block;
        background-color: $colorBlue;
        height: 8px;
        position: relative;
        top: -25px;
        left: -10px;
        z-index: -1;
        margin: 0;
        animation: showHighLight forwards;
        animation-duration: .5s;
    }
}

@keyframes showHighLight {
    0% {
        width: 0px;
    }

    100% {
        width: 580px;
    }
}

.dot {
    width: 10px;
    height: 10px;
    border-radius: 50%;
    background-color: $colorPink;
    display: inline-block;
    margin-left: -10px;
}




.text {
    display: flex;
}

.leftText {
    font-size: 16px;
    letter-spacing: 2.22222px;
    font-weight: 700;
    padding-top: 100px;
    padding-left: 62.5px;

    & h5 {
        margin: 0;
        writing-mode: vertical-rl;
        transform: rotate(180deg);
        color: white;
        display: flex;
        flex-direction: row-reverse;
        align-items: center;

        &::after {
            content: '';
            display: block;
            margin-bottom: 24.5px;
            // border-top: 2px white solid;
            background-color: white;
            width: 2px;
            height: 113px;
        }
    }
}

.mainText {
    padding-top: 111px;
    padding-left: 138.5px;

    & img {
        margin-bottom: 34px;
    }
}

.video-container {
    background-color: black;
    width: 100%;
    height: 100vh;
    position: absolute;
    border-radius: 0 0 50px 50px;
    overflow: hidden;

    & video {
        z-index: -2;
    }
}

.end {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;


    & img {
        width: 65px;
        height: 65px;
        margin-bottom: 11px;
    }

    & h3 {
        margin: 0;
        font-weight: 700;
        font-size: 14px;
        letter-spacing: 2px;
        color: white;
    }
}

.mainText-RWD {
    display: none;
}
@media(max-width:960px){
    .mainText {
        margin: 0 auto;
        padding: 100px 0;
    }
    .leftText {
        display: none;
    }
}
@media(max-width:768px) {
    .mainText {
        display: none;
    }

    .mainText-RWD {
        display: block;
        margin: 0 auto;
        margin-top: 100px;

        & h1 {
            font-size: 30px;
            line-height: 50px;

            &::after {
                top: -20px;
                animation: showHighLight-rwd forwards;
                animation-duration: .5s;
            }
        }

        & img {
            margin-bottom: 30px;
            width: 150px;
        }
    }

    .leftText {
        display: none;
    }
}

@keyframes showHighLight-rwd {
    0% {
        width: 0px;
    }

    100% {
        width: 300px;
    }
}
</style>