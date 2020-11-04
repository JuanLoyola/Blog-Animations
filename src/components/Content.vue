<template>
  <div class="container">
    <section class="info">
      <div class="info-card">
        <h2 class="container-title">
      Lorem ipsum dolor sit amet.
    </h2>
    <hr>
    <br>
    <p class="container-content">
      Lorem ipsum dolor sit amet consectetur, adipisicing elit. Aspernatur deleniti velit veniam recusandae eaque doloremque omnis quaerat eius excepturi quam vel, id amet quod numquam, assumenda officia? Sequi similique, dolorem eveniet, id iusto ipsum vero illum, quam est blanditiis sapiente debitis. Nihil necessitatibus fuga doloremque libero autem molestiae illum cupiditate ipsam ipsum explicabo harum quis recusandae accusantium incidunt eligendi.
    </p>
      </div>
    <br>
    <div class="info-card">
      <h2 class="container-title">
      Lorem ipsum dolor sit amet.
    </h2>
    <hr>
    <br>
    <p class="container-content">
      Lorem ipsum dolor sit amet consectetur, adipisicing elit. Distinctio autem iusto officiis cumque natus? Perspiciatis ea dicta, adipisci facere ipsam repudiandae magnam tempora, suscipit officia, vero iusto corrupti error excepturi blanditiis illum aperiam cumque laborum rem quam totam eligendi.
    </p>
    </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'Content'
}
</script>

<style lang="scss" scoped>
.container{
  width: 100%;
  padding: 10px 0px;
  font-size: 1rem;
  background-image: url('../assets/chalkboard.jpg');

  .info{
    display:flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    &-card{
      display:flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      width: 50%;

      border: 2px solid rgb(145, 143, 143);
      background: #f1f1f1;
    }
  }
  &-title{
    background: #f1f1f1;
    font-size: 1.3rem;
    font-weight: bold;
  }
  hr{
    margin-top: 20px;
    width: 280px;
  }
  &-content{
    text-align:start;
    font-weight: 600;
    max-width: 90%;
  }
}
@media screen and (min-width: 320px) and (max-width:1034px){
  .container{
    padding: 0px 0px;
    .info{
      &-card{
        width: 80%;
      }
    }
    &-title{
      background: #f1f1f1;
      font-size: 1.2rem;
      font-weight: bold;
    }
    hr{
      margin-top: 20px;
      width: 130px;
    }
    &-content{
      text-align:start;
      font-weight: 600;
      max-width: 80%;
    }
  }
}
</style>
