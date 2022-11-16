<template>
    <nav :class="{ scroll: isSticky }">
        <!-- <nav class="scroll"> -->
        <img class="logo" :class="{ show: isSticky }" src="digisalad-blue.png" alt="">
        <div class="right-side">
            <button>START YOUR PROJECT</button>

            <img :class="{ black: isSticky }" src="menu-hamburger.svg" alt="" @click="menu()">

        </div>

    </nav>
</template>

<script>
export default {
    name: 'Nav',
    data() {
        return {
            isSticky: false
        }
    },
    mounted() {
        window.addEventListener("scroll", this.handleScroll)
    },
    methods: {
        handleScroll() {
            this.isSticky = window.scrollY > 50 ? true : false;
        },
        menu() {
            this.$emit('openMenu')
        }
    }
}



</script>

<style lang="scss" scoped>
nav {
    position: absolute;
    z-index: 99;
    width: 100%;
    height: 100px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin: 0;
    background-color: transparent;
    top: 0;
    padding: 0 60px 0 80px;

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

        &:hover {
            cursor: pointer;
        }
    }

    .logo {
        opacity: 0;

        &.show {
            opacity: 1;
        }
    }

    & .right-side {
        display: flex;
        align-items: center;

        & img:hover {
            cursor: pointer;
        }

        & .black {
            filter: invert(50%) sepia(0%) saturate(2%) hue-rotate(94deg) brightness(91%) contrast(85%);

        }
    }
}

.scroll {
    background-color: rgba(white, 0.9);
    position: fixed;
    top: 0;
    z-index: 10;
    box-shadow: 0 0 5px rgba(black, 0.3);
}

@keyframes showNav {
    0% {
        top: -300px;
    }

    100% {
        top: 0;
    }
}

.scroll {
    animation-name: showNav;
    animation-duration: 1s;
}

@media(max-width:1200px) {
    nav button {
        display: none;
    }
    nav {
        height: 64px;
        padding: 10px 25px 10px 30px;
        & .logo {
            height: 40px;
        }
    }
}
</style>