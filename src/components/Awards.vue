<template>
    <div class="container">

        <div class="mainText">
            <h2></h2>
            <p>Cras quis nulla commodo, aliquam lectus sed, blandit augue. Cras ullamcorper bibendum bibendum. Duis
                tincidunt urna non pretium porta. Nam condimentum vitae ligula vel ornare. Phasellus at semper
                turpis. Nunc eu tellus tortor. Etiam at condimentum nisl, vitae sagittis orci. Donec id dignissim
                nunc. </p>
        </div>
        <div>
            <img src="awards.png" alt="">
            <img src="awards.png" alt="">
        </div>
        <div>
            <img src="awards.png" alt="">
            <img src="awards.png" alt="">
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
    margin-top: 125px;
    display: flex;
    background-color: white;
    border-radius: 50px 0 50px 50px;
    padding-top: 65px;
    padding-left: 69px;
}

.mainText {
    h2 {
        text-align: center;
        font-family: "proxima-nova";

        &::after {
            content: 'AWARDS';
            text-decoration-style: wavy;
            text-decoration-line: underline;
            text-decoration-color: #26C6D0;
        }
    }
}
</style>