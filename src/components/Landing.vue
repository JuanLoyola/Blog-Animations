<template>
  <div class="container">
        <div class="container__moon">
          <img class="moon-img" src="@/assets/Luna.svg" alt="Luna">
        </div>
        <div class="container__center">
          <div>
            <p class="container__center__info">
              Use hyper-speed on all your devices to<br>
              enjoy the full power of your internet
            </p>
            <div>
              <a class="container__center__btn" href="#">
                <p class="container__center__btn__text">Read more</p>
              </a>
            </div>
            <img class="rocket" src="@/assets/Cohete.svg" alt="Rocket">
          </div>
        </div>
      <div class="clouds">
            <img src="@/assets/cloud1.png"  style="--i:1;" alt="cloud1">
            <img src="@/assets/cloud2.png"  style="--i:2;" alt="cloud2">
            <img src="@/assets/cloud3.png"  style="--i:3;" alt="cloud3">
            <img src="@/assets/cloud4.png"  style="--i:4;" alt="cloud4">
            <img src="@/assets/cloud5.png"  style="--i:5;" alt="cloud5">
      </div>
  </div>
</template>

<style lang="scss" scoped>
*{
  margin: 0;
  padding: 0;
}
.container{
  color: #f1f1f1;
  background-image: url('../assets/simplebg.svg');
  background-size: cover;
  background-repeat: no-repeat;
  background-position: bottom;
  width: 100%;
  max-width: 100%;
  height: 100vh;
  position: relative;

  a{
    text-decoration: none;
    color:#f1f1f1;
    margin: 10px;
  }

  &__moon{
    display: flex;
    justify-content: flex-end;
  }
  .moon-img{
    width: 9%;
    margin-top: 55px;
    margin-right: 55px;
    animation: spin 55s linear infinite;
  }
  @keyframes spin {
    0%   {
        -webkit-transform: rotate(0deg);
        -ms-transform: rotate(0deg);
        transform: rotate(0deg);
    }
    100% {
        -webkit-transform: rotate(360deg);
        -ms-transform: rotate(360deg);
        transform: rotate(360deg);
    }
}
  &__center{
    display:flex;
    justify-content: space-evenly;

    &__info{
      font-family: 'Poppins';
      font-weight: bold;
      font-size: 18px;
      display: flex;
    }
    &__btn{
      display: flex;
      margin-top: 10px;
      padding: 5px 5px;
      background: rgba(255, 255, 255, 0.1);
      border: 1px solid #FFFFFF;
      box-sizing: border-box;
      border-radius: 5px;
      justify-content: center;
      &__text{
        font-family: 'Bebas Neue';
        font-size: 18px;
        line-height: 22px;
      }
    }
    &__btn:hover{
      background: rgba(255, 255, 255, 0.4);
      color: #e9b935;
    }
  }
  .rocket{
    width: 10%;
    animation: MoveUpDown 6s linear infinite;
    position: absolute;
  }
  @keyframes MoveUpDown {
    0%, 100% {
      bottom: 0;
    }
    50% {
      bottom: 100px;
    }
  }
  .container .clouds{
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    overflow: hidden;
  }
  .clouds img{
    position: absolute;
    bottom: 0;
    left: 0;
    max-width: 50%;
    animation: animate calc(12s * var(--i)) linear infinite;
  }
  @keyframes animate {
    0% {
      transform: translateX(-100%);
    }
    100% {
      transform: translateX(100%);
    }
  }
}
@media screen and (min-width: 320px) and (max-width:1034px){
  .container{
    .moon-img{
      width: 160px;
    }
    &__center{
      display:flex;
      justify-content: center;
      font-size: 0.8rem;

      &__info{
        font-family: 'Poppins';
        font-weight: bold;
        font-size: 0.8rem;
        display: flex;
      }
    }
    .rocket{
      width: 30%;
      display:flex;
      justify-content: center;
      align-items: center;
    }
    .container .clouds{
      position: absolute;
      top: 0;
      left: 0;
      width: 110%;
      height: 100%;
      overflow: hidden;
    }
    .clouds img{
      position: absolute;
      bottom: 0;
      left: 0;
      max-width: 50%;
      height: 15%;
      overflow:hidden;
    }
    @keyframes animate {
      0% {
        transform: translateX(-100%);
      }
      100% {
        transform: translateX(100%);
      }
    }
  }
}
</style>

<script>
export default {
  name: 'Landing'
}
</script>
