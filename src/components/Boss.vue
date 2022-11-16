<template>
    <div class="container">


        <div class="content">
            <div class="boss">
                <img src="tony.png" alt="tony ng">
                <h4>Tony Ng</h4>
                <p>Founder & Creative Director</p>
            </div>
            <div class="quote">
                <img src="left-quote 1.png" alt="">
                <p>
                    A great digital work isn’t about designing beautiful pages purely. It is about context - how do we
                    <span>deliver the right experience to the right person at the right time. </span>The most important
                    thing is that
                    your work can engage customers at anytime, anywhere and let users experience an entire amazing
                    digital
                    journey.
                </p>
            </div>
        </div>

    </div>
</template>

<style lang="scss" scoped>
.container {
    position: relative;
    z-index: 1;
}

.content {
    position: absolute;
    top: -318px;
    right: 140px;
    display: flex;
    border-radius: 0 65px 65px 65px;
    background: url(../assets/boss-bg.png) no-repeat;
    background-size: cover;
}

.boss {
    padding: 100px;

    & img {
        width: 204px;
        height: 204px;
        border-radius: 50%;
    }


    & h4 {
        margin: 0;
        margin-top: 39px;
        font-style: normal;
        font-weight: 700;
        font-size: 20px;
        line-height: 24px;
        text-align: center;
        letter-spacing: 2px;
        text-transform: uppercase;
        color: white;
    }

    & p {
        margin: 0;
        margin-top: 8px;
        color: white;
        text-align: center;
        font-style: italic;
        font-weight: 400;
        font-size: 16px;
        line-height: 16px;
        letter-spacing: 2px;
    }
}

.quote {
    padding-top: 80px;
    padding-right: 100px;
    padding-left: 11px;

    & img {
        display: block;
        margin: 0 auto;
    }

    & p {
        font-style: normal;
        font-weight: 400;
        font-size: 22px;
        line-height: 48px;
        letter-spacing: 2px;
        color: white;

        & span {
            color: #FFBC58;
        }
    }

}

@media(max-width: 1200px) {
    .content {
        right: 10%;
        flex-direction: column;
        padding: 10%;

        & .boss {
            padding: 0;
            text-align: center;
            order: 2;
            padding-top: 80px;

            & div {
                margin: 0;
            }
        }

        & .quote {
            padding: 0;
            // padding-top: 80px;
            order: 1;
            & p{
                font-size: 16px;
                line-height: 36px;
            }
        }
    }
}
</style>