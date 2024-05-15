<template>
  <div class="landing">
    <div class="header">
      <img src="../assets/taxi-valenciana.png" />
    </div>
    <div class="banner">
      <h1>Reserva tu viaje<br>Desde el aeropuerto</h1>
      <p>
        Servicios de taxi a toda la comunidad Valenciana y todo España, precios económicos averigue por el suyo su consulta no molesta (posible reservar).
      </p>
      <div class="call-to-action">
        <a href="https://wa.me/34624614349" target="_blank" class="whatsapp">
          Reservar por WhatsApp
        </a>
        <a href="tel:684348692" target="_blank" class="telephone">
          Reservar por llamada
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'LandingPage',
  props: {
    msg: String
  }
}
</script>

<style scoped lang="scss">
  .landing {
    width:100%;
    height:100vh;
    background-color:#242422;
    overflow:hidden;

    &::before {
      position:absolute;
      pointer-events: none;
      content:'';
      top:0;
      left:0;
      width:200%;
      height:200vh;
      background-image:url('../assets/taxi-space.png');
      background-size: 70px auto;
      background-repeat: space;
      opacity:.03;
      transform-origin:top left;
      transform:rotate(-30deg) translateX(-50%);
    }


    .header {
      display:flex;
      align-items: center;
      padding:30px 0;
      max-width:1200px;
      margin:0 auto;

      img {
        max-width:230px;
      }
    }

    .banner {
      width:100%;
      max-width:1200px;
      margin:0 auto;
      height:400px;
      padding:40px 0;

      h1 {
        font-size: 4.5rem;
        text-align:left;
        font-weight: bold;
        margin:0;
        padding:0;
        color:#fff;
      }

      p {
        text-align: left;
        color:#fff;
        max-width: 800px;
      }

      .call-to-action {
        text-align:left;
        margin-top:60px;

        .whatsapp {
          padding:15px 20px;
          background-color:#2DD46C;
          border-radius:10px;
        }

        .telephone {
          padding:15px 20px;
          background-color:#000;
          border-radius:10px;
          color:#fff;
        }

        a {
          text-align: center;
          text-decoration: none;
          font-weight: bold;
          color:#000;
          padding:0;
          margin:0;
        }

        a:not(:last-of-type) {
          margin-right:15px;
        }
      }
    }
  }
</style>
