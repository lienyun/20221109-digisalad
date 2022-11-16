<template>
    <div class="container">
        <h2>&nbsp;&nbsp;OUR BRAND EXPERIENCE&nbsp;&nbsp;</h2>
        <div class="content">
            <p>Cras quis nulla commodo, aliquam lectus sed, blandit augue. Cras ullamcorper bibendum bibendum. Duis
                tincidunt urna non pretium porta. Nam condimentum vitae ligula vel ornare. Phasellus at semper turpis.
                Nunc
                eu tellus tortor. Etiam at condimentum nisl, vitae sagittis orci. Donec id dignissim nunc. Donec elit
                ante,
                eleifend a dolor et, venenatis facilisis dolor. In feugiat orci odio, sed lacinia sem elementum quis.
                Aliquam consectetur, eros et vulputate euismod, nunc leo tempor lacus, ac rhoncus neque eros nec lacus.
                Cras
                lobortis molestie faucibus.</p>
            <img src="client.png" alt="">

        </div>


    </div>


</template>

<style lang="scss" scoped>
$colorBlue: #26C6D0;
$colorPurple: #585880;
$colorPink: #EE6C8A;
$colorYellow: #FFBC58;

.container {
    background-color: white;
    padding-top: 435px;
    position: relative;
    z-index: 0;
    top: -50px;
}

h2 {
    text-align: center;

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

p {

    font-style: normal;
    font-weight: 400;
    font-size: 16px;
    line-height: 24px;
    text-align: center;
    letter-spacing: 1px;
    color: #262626;
}

.content {
    padding: 50px 10%;

    & img {
        margin: 0 auto;
        display: block;
        margin-top: 40px;
        width: 90%;
    }
}

@media (max-width: 1200px) {
    .container {
        padding-top: 735px;

    }
}

@media(max-width: 768px) {
    .container {
        padding-top: 800px;

        & h2 {
            line-height: 68px;
        }
    }

    .content {

        & img {
            margin: 0 auto;
            display: block;
            margin-top: 40px;
            width: 90%;
        }
    }
}
</style>