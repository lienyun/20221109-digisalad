<template>
  <div class="container">
    <div class="bg-img"></div>

    <div class="nav">
      <img src="digisalad.png" alt="">
      <div class="cancel-matte" @click="cancel()">
        <div class="cancel"></div>
      </div>

    </div>
    <div class="buttons">
      <div class="left-btn">
        <button type="button" class="btn1" @click="aboutHandler()">
          <div class="btn-bg"></div>

          <div class="wrap-content">
            <img src="service-01.png" alt="">
            <div>
              <h4>EMPOWERING BRANDS</h4>
              <h3>ABOUT US</h3>
            </div>
          </div>
        </button>



        <button type="button" class="btn2">
          <div class="btn-bg"></div>

          <div class="wrap-content">
            <img src="service-02.png" alt="">
            <div>
              <h4>CASE STUDIES</h4>
              <h3>WORKS</h3>
            </div>
          </div>

        </button>


      </div>
      <div class="center-btn">

        <button type="button" class="btn3">
          <div class="btn-bg"></div>

          <div class="wrap-content">
            <img src="service-03.png" alt="">
            <div>
              <h4>BE COOL WITH US</h4>
              <h3>CAREERS</h3>
            </div>

          </div>

        </button>
        <button type="button" class="btn4">
          <div class="btn-bg"></div>
          <div class="wrap-content">
            <img src="service-04.png" alt="">
            <div>
              <h4>OUR STRATEGIES</h4>
              <h3>INSIGHTS</h3>
            </div>

          </div>

        </button>
      </div>
      <div class="right-btn">

        <button type="button" class="btn5" @click="serviceHandler()">
          <div class="btn-bg"></div>
          <div class="wrap-content">
            <img src="carrot.png" alt="">
            <div>
              <h4>AREAS OF EXPERTISE</h4>
              <h3>SERVICES</h3>
            </div>

          </div>
        </button>

        <button type="button" class="btn6">

          <div class="wrap-content">
            <div>
              <h4>START YOUR JOURNEY WITH US</h4>
              <h3>CONTACT</h3>
            </div>

          </div>
        </button>
      </div>

    </div>


  </div>
</template>

<script>


export default {
  name: 'SideBar',
  methods: {
    cancel() {
      this.$emit('noSidebar')
    },
    aboutHandler() {
      this.cancel()
      window.location = '#about'

    },
    serviceHandler() {
      this.cancel()
      window.location = '#service'
    }
  },
  computed: {
    getClassName(i) {
      // var id = i+1
      return `btn+${i}`
    }
  }

}
</script>


<style lang="scss" scoped>
$colorBlue: #26C6D0;
$colorPurple: #585880;
$colorPink: #EE6C8A;
$colorYellow: #FFBC58;
$colorGreen: #26D0A8;

.container {
  width: 100vw;
  height: 100vh;
  position: relative;
}

.bg-img {
  background: linear-gradient(180deg, rgba($colorPurple, 0.9) 3.61%, rgba($colorBlue, 0.9) 95.7%), url(../assets/sidebar-bg.png) no-repeat;
  mix-blend-mode: normal;
  background-size: cover;
  position: absolute;
  top: 0;
  width: 100vw;
  height: 100vh;
  border-radius: 0 0 50px 50px;

}

.nav {
  position: relative;
  z-index: 5;
  height: 100px;
  padding: 0 60px 0 80px;
  display: flex;
  justify-content: space-between;
  align-items: center;

  & img {
    width: 120px;
    height: 54px;
  }

  & .cancel-matte {
    position: relative;
    width: 45px;
    height: 45px;

    &:hover {
      cursor: pointer;
    }
  }

  & .cancel {
    position: absolute;
    top: 35%;
    left: 15%;
    width: 30px;
    height: 3px;
    border-radius: 1.5px;
    transform: rotate(45deg);
    background-color: white;
    margin-top: 7px;


    &::before {
      content: '';
      display: block;
      width: 30px;
      height: 3px;
      background-color: white;
      border-radius: 1.5px;
      transform: rotate(90deg);
    }

  }
}

.buttons {
  position: relative;
  z-index: 5;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 0 90px;

  & .left-btn,
  .center-btn,
  .right-btn {
    display: flex;
    flex-direction: column;
  }

  & .left-btn,
  .right-btn {
    flex-grow: 3;
    height: 75vh;

    & h3 {
      margin-top: 9px;
    }
  }

  & .center-btn {
    flex-grow: 2;
    height: 85vh;

    & .wrap-content {
      display: flex;
      flex-direction: column;
      align-items: start;
    }

    & h4 {
      margin-top: 28px;
    }

    & h3 {
      margin-top: 9px;
    }
  }

  & .left-btn,
  .right-btn {
    & .wrap-content {
      & div {
        margin-left: 20px;

      }
    }
  }

  & .right-btn {
    & h4 {
      margin-top: 28px;
    }

    & h3 {
      margin-top: 9px;
    }
  }

  & button {
    border-radius: 30px;
    border: none;
    box-shadow: 0 0 5px rgba(black, 0.3);
    overflow: hidden;
    margin: 20px;
    position: relative;


    & h3,
    h4 {
      margin: 0;
    }

    & h3 {
      font-style: normal;
      font-weight: 700;
      font-size: 32px;
      line-height: 39px;
      letter-spacing: 3.63636px;
      color: #FFFFFF;

      &::after {
        content: '';
        display: inline-block;
        background-color: $colorPink;
        width: 10px;
        height: 10px;
        border-radius: 50px;
        margin-left: 11px;

      }
    }

    & h4 {
      font-style: normal;
      font-weight: 400;
      font-size: 16px;
      line-height: 19px;
      letter-spacing: 1.8px;
      color: #FFFFFF;
    }
  }

  & .wrap-content {
    display: flex;
    align-items: center;
    position: absolute;
    left: 10%;
    bottom: 20%;

    & div {
      text-align: left;
    }
  }

  & .btn1 {
    flex-grow: 2;
    position: relative;
    background-color: $colorBlue;

    &:hover {
      cursor: pointer;
    }

    & .btn-bg {
      background: url(../assets/btn-1.png);
      background-size: cover;
      width: 100%;
      height: 100%;
      position: absolute;
      top: 0;
      left: 0;
    }
  }

  & .btn2 {
    flex-grow: 3;
    position: relative;
    background-color: $colorPink;

    &:hover {
      cursor: pointer;
    }

    & .btn-bg {
      background: url(../assets/btn-2.png);
      background-size: cover;
      width: 100%;
      height: 100%;
      position: absolute;
      top: 0;
      left: 0;
    }

    & .wrap-content {
      & h3::after {
        background-color: $colorBlue;
      }
    }
  }

  & .btn3 {
    flex-grow: 2;
    position: relative;
    background-color: #E6A94E;

    &:hover {
      cursor: pointer;
    }

    & .btn-bg {
      background: url(../assets/btn-3.png);
      background-size: cover;
      width: 100%;
      height: 100%;
      position: absolute;
      top: 0;
      left: 0;
    }

    & .wrap-content {
      left: 15%;
      bottom: 10%;
      text-align: left;
    }
  }

  & .btn4 {
    flex-grow: 1;
    min-height: 200px;
    position: relative;
    background-color: #26D0A8;

    &:hover {
      cursor: pointer;
    }

    & .btn-bg {
      background: url(../assets/btn-4.png);
      background-size: cover;
      width: 100%;
      height: 100%;
      position: absolute;
      top: 0;
      left: 0;
    }

    & .wrap-content {
      left: 15%;
      bottom: 10%;
      text-align: left;

      & h4 {
        margin-top: 15px;
      }
    }
  }

  & .btn5 {
    flex-grow: 3;

    position: relative;
    background-color: $colorPurple;

    &:hover {
      cursor: pointer;
    }

    & .btn-bg {
      background: url(../assets/btn-5.png);
      background-size: cover;
      width: 100%;
      height: 100%;
      position: absolute;
      top: 0;
      left: 0;
    }
  }

  & .btn6 {
    flex-grow: 2;
    background-color: white;
    text-align: left;

    & .wrap-content {
      & div {
        margin: 0;
      }
    }

    &:hover {
      cursor: pointer;
    }

    & h4 {
      color: #262626;
      margin: 0;
    }

    & h3 {
      color: $colorBlue;
    }
  }
}

.RWD-buttons {
  display: none;
}

.btn1:hover,
.btn2:hover,
.btn3:hover,
.btn4:hover,
.btn5:hover,
.btn6:hover {
  animation: shakeBtn infinite linear;
  animation-duration: .5s;
}

@keyframes shakeBtn {
  0% {
    transform: rotate(0deg);
  }

  25% {
    transform: rotate(-5deg);

  }

  50% {
    transform: rotate(0deg);

  }

  75% {
    transform: rotate(5deg);
  }

  100% {
    transform: rotate(0deg);
  }

}

@media(max-width: 1200px) {

  .nav {
    height: 64px;
    padding: 10px 25px 10px 30px;

    & img {
      width: 88.8px;
      height: 40px;
    }

  }

  .container {
    width: 100%;
    height: 100%;
  }

  .bg-img {
    width: 100%;
    height: 100%;
  }

  .buttons {
    flex-direction: column;
    padding: 0;

    & .left-btn,
    .center-btn,
    .right-btn {
      width: 100%;
      height: 500px;
    }

    & .btn1,
    .btn2,
    .btn3,
    .btn4,
    .btn5,
    .btn6 {
      flex-grow: 1;
    }

    & .wrap-content {
      display: flex;
      left: 5%;
    }

    & .btn3,
    .btn4 {
      & .wrap-content {
        flex-direction: row;
        align-items: center;
        left: 5%;
        bottom: 20%;

        & div {
          margin-left: 20px;
        }

        & h4 {
          margin: 0;
        }
      }
    }
  }
}

@media(max-width: 560px) {
  .buttons {

    & .left-btn,
    .center-btn,
    .right-btn {
      width: 100%;
      height: 350px;
    }

    & .center-btn{
      & .btn4{
        min-height: auto;
      }
    }

    & .wrap-content {
      left: 10%;
    }
  }
}
</style>