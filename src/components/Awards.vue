<template>
    <div class="container">
        <div class="content">
            <div class="mainText">
                <h2>&nbsp;&nbsp;AWARDS&nbsp;&nbsp;</h2>
                <p>Cras quis nulla commodo, aliquam lectus sed, blandit augue. Cras ullamcorper bibendum bibendum. Duis
                    tincidunt urna non pretium porta. Nam condimentum vitae ligula vel ornare. Phasellus at semper
                    turpis. Nunc eu tellus tortor. Etiam at condimentum nisl, vitae sagittis orci. Donec id dignissim
                    nunc. </p>
            </div>
            <div class="awards">
                <img src="awards.png" alt="">
                <img src="awards.png" alt="">
            </div>
            <div class="awards">
                <img src="awards.png" alt="">
                <img src="awards.png" alt="">
            </div>
        </div>
    </div>
</template>

<script>

export default {
    name: 'Awards',
}
</script>

<style lang="scss" scoped>
* {
    // border: 1px solid black;
}

.container {
    position: relative;
    z-index: 1;
}

.content {
    position: absolute;
    // left: 10%;
    right: 0;
    width: 80vw;
    margin-top: 125px;
    display: flex;
    background-color: white;
    border-radius: 50px 0 50px 50px;
    padding: 65px;

    .mainText {
        width: 416px;
        padding-right: 37px;
    }

    .awards {
        // padding-right: 37px;
        flex-basis: 0;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;

        & :first-of-type {
            // padding-bottom: 19px;
        }
    }
}

.mainText {
    h2::after {
        content: '';
        width: 10px;
        height: 10px;
        border-radius: 50%;
        background-color: #EE6C8A;
        display: inline-block;
        margin-left: -10px;
    }

    p {
        padding-top: 31.7px;
    }
}

@media(max-width: 960px) {
    .content {
        flex-direction: column;
        text-align: center;
        justify-content: center;

        & .mainText {
            padding: 0;
            margin: 0 auto;
        }

        & .awards {
            padding: 0;

            & :first-of-type {
                padding-bottom: 0;
            }
            & img {
                padding-top: 20px;
            }
        }
    }
}
</style>