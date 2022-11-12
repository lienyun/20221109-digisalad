<template>
  <div class="container">
    <div class="bg-img"></div>

    <div class="nav">
      <img src="digisalad.png" alt="">
      <div class="cancel" @click="cancel()"></div>



    </div>
    <div class="buttons">
      <div class="left-btn">

        <button type="button" class="btn1">
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
            <h4>BE COOL WITH US</h4>
            <h3>CAREERS</h3>
          </div>

        </button>
        <button type="button" class="btn4">
          <div class="btn-bg"></div>

          <div class="wrap-content">
            <img src="service-04.png" alt="">
            <h4>OUR STRATEGIES</h4>
            <h3>INSIGHTS</h3>
          </div>

        </button>
      </div>
      <div class="right-btn">

        <button type="button" class="btn5">
          <div class="btn-bg"></div>

          <div class="wrap-content">
            <img src="carrot.png" alt="">
            <h4>AREAS OF EXPERTISE</h4>
            <h3>SERVICES</h3>
          </div>

        </button>

        <button type="button" class="btn6">

          <div class="wrap-content">
            <h4>START YOUR JOURNEY WITH US</h4>
            <h3>CONTACT</h3>
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
    }
  }

}
</script>


<style lang="scss" scoped>
.container {
  width: 100vw;
  height: 100vh;
  position: relative;
}

.bg-img {
  background: linear-gradient(180deg, rgba(#585880, 0.9) 3.61%, rgba(#26C6D0, 0.9) 95.7%), url(../assets/sidebar-bg.png) no-repeat;
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
  padding: 41px 60px 0 60px;
  display: flex;
  justify-content: space-between;

  & img {
    width: 140px;
  }

  & .cancel {
    margin: 0;
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

    &:hover {
      cursor: pointer;
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



  & .center-btn{
    flex-grow: 2;
    height: 85vh;


    & h4 {
      margin-top: 28px;
    }

    & h3 {
      margin-top: 9px;
    }
  }

  & .left-btn {

    & h3,
    h4 {
      margin-left: 20px;
    }
  }
  & .right-btn{
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
        background-color: #EE6C8A;
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

  & .btn1 {
    // height: 210px;
    flex-grow: 2;
    position: relative;
    background-color: #26C6D0;

    & .btn-bg {
      background: url(../assets/btn-1.png);
      background-size: cover;
      width: 100%;
      height: 100%;
      position: absolute;
      top: 0;
      left: 0;
    }

    & .wrap-content {
      display: flex;
      align-items: center;
      position: absolute;
      left: 10%;
      bottom: 20%;
    }
  }

  & .btn2 {
    // height: 320px;
    flex-grow: 3;

    position: relative;
    background-color: #EE6C8A;

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
      display: flex;
      align-items: center;
      position: absolute;
      text-align: left;
      left: 10%;
      bottom: 20%;

      & h3::after {
        background-color: #26C6D0;
      }
    }
  }

  & .btn3 {
    // height: 430px;
    flex-grow: 2;
    position: relative;
    background-color: #E6A94E;

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
      position: absolute;
      left: 10%;
      bottom: 20%;
      text-align: left;
    }
  }

  & .btn4 {
    // height: 282px;
    flex-grow: 1;

    position: relative;
    background-color: #26D0A8;

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
      position: absolute;
      left: 10%;
      bottom: 20%;
      text-align: left;
    }
  }

  & .btn5 {
    // height: 320px;
    flex-grow: 3;

    position: relative;
    background-color: #585880;

    & .btn-bg {
      background: url(../assets/btn-5.png);
      background-size: cover;
      width: 100%;
      height: 100%;
      position: absolute;
      top: 0;
      left: 0;
    }

    & .wrap-content {
      position: absolute;
      left: 10%;
      bottom: 20%;
      text-align: left;
    }
  }

  & .btn6 {
    // height: 210px;
    flex-grow: 2;

    background-color: white;
    text-align: left;

    & .wrap-content {
      position: absolute;
      left: 10%;
      bottom: 30%;

    }

    & h4 {
      color: #262626;
    }

    & h3 {
      color: #26C6D0;
    }
  }
}
</style>