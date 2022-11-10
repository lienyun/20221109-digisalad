<template>
    <div class="video-container">
        <iframe id="player" src="https://www.youtube.com/embed/8_4JRK4QkqU"></iframe>
    </div>
    <div class="title">
        <nav>
            <button>START YOUR PROJECT</button>
            <div class="hamburger"><img src="menu-hamburger.png" alt=""></div>
        </nav>
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
    mounted() {
        
    },
    methods: {

    }
}
</script>

<style lang="scss" scoped>
* {
    box-sizing: border-box;
    font-family: "proxima-nova";


}

.title {
    position: relative;
    background-color: rgba(black, 0.3);
    padding-top: 41px;
    height: 940px;
    padding-bottom: 75px;
    border-radius: 0 0 30px 30px;
}

h1 {
    font-style: normal;
    font-weight: 700;
    font-size: 38px;
    line-height: 70px;
    letter-spacing: 9.16667px;
    margin: 0;
    color: white;
    z-index: 99;

    &::after {
        content: '';
        display: block;
        background-color: #26C6D0;
        width: 571px;
        height: 8px;
        position: relative;
        top: -23px;
        left: -10px;
        z-index: -1;
    }
}

nav {
    display: flex;
    justify-content: end;
    align-items: center;
    margin-top: 41px;
    padding-right: 60px;
    margin: 0;

    & button {
        padding: 12px 20px;
        color: white;
        background: linear-gradient(90deg, #4EE5EA 3.94%, #26D0A8 94.73%);
        border-radius: 24px;
        border: none;
        font-style: normal;
        font-weight: 700;
        font-size: 14px;
        letter-spacing: 1.14286px;
        text-align: center;
        line-height: 17px;
        margin-right: 44px;
    }
}


.text {
    display: flex;

}

.leftText {
    font-size: 16px;
    letter-spacing: 2.22222px;
    font-weight: 700;
    padding-top: 179px;
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
    height: 940px;
    position: absolute;
    z-index: 0;
    border-radius: 0 0 30px 30px;
    overflow: hidden;

    & iframe {
        width: 100%;
        height: 940px;
    }
}

.end {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    margin-top: 259px;

    & img {
        width: 65px;
        height: 65px;
    }

    & h3 {
        margin: 0;
        font-weight: 700;
        font-size: 14px;
        letter-spacing: 2px;
        color: white;
    }
}
</style>