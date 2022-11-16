<template>
  <div class="container">

    <h2 id="about">&nbsp;&nbsp;ABOUT DIGISALAD&nbsp;&nbsp;</h2>

    <div class="video-container">
      <img src="video-thumbnail.png" alt="video">
    </div>
    <div class="text-container">
      <p>Cras quis nulla commodo, aliquam lectus sed, blandit augue. Cras ullamcorper bibendum bibendum. Duis tincidunt
        urna
        non pretium porta. Nam condimentum vitae ligula vel ornare. Phasellus at semper turpis. Nunc eu tellus tortor.
        Etiam
        at condimentum nisl, vitae sagittis orci. Donec id dignissim nunc. Donec elit ante, eleifend a dolor et,
        venenatis
        facilisis dolor. In feugiat orci odio, sed lacinia sem elementum quis. Aliquam consectetur, eros et vulputate
        euismod, nunc leo tempor lacus, ac rhoncus neque eros nec lacus. Cras lobortis molestie faucibus.</p>
    </div>
    <button>VIEW MORE</button>
  </div>
</template>

<script>

export default {
  name: 'About',
}
</script>

<style lang="scss" scoped>

$colorBlue: #26C6D0;
$colorPurple: #585880;
$colorPink: #EE6C8A;
$colorYellow: #FFBC58;
* {
  font-family: "proxima-nova";
}

.container {
  margin-top: 125px;
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


.video-container {
  display: flex;
  justify-content: center;
  margin-top: 72.7px;

  & img {
    width: 80%;
  }
}

.text-container {
  margin: 0 auto;
  width: 80%;
  margin-top: 30px;

  & p {
    font-size: 16px;
    text-align: center;
    letter-spacing: 1px;
    line-height: 28px;
    font-weight: 400;
  }
}

button {
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
  padding: 33px 24.53px 34px 24.53px;
  margin: 0 auto;
  margin-top: 30px;
  display: flex;
  align-items: center;
  transition: .5s;


  &::after {
    content: '';
    display: inline-block;
    width: 52.03px;
    height: 2px;
    background-color: white;
    margin-left: 15px;

  }

  &:hover {
    cursor: pointer;
    background-color: white;
    color: $colorBlue;
    transition: .5s;

    &::after {
      background-color: $colorBlue;
      transition: .5s;

    }
  }

}
</style>