<template>
  <div>
    <section class="hero">
      <div class="hero-inner">
        <h1>We deliver projects that defies all Imitations</h1>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed leo turpis consequat, commodo elementum ac eu id dictum. Dignissim vel viverra erat semper diam ornare volutpat. Id scelerisque ultricies consequat vitae, nisl enim. </p>
        <div class="_btns">
          <router-link to="contact-us" class="contact">Contact us</router-link>
          <router-link to="#service" class="service">Our services</router-link>
        </div>
      </div>
    </section>

    <section class="about">
      <div class="_inner">
        <h2>Who we are</h2>
        <p>We are a construction and project management company in Nigeria, which was incorporated to carry on the business of building construction, project management, construction management and facility management, design/build of first class building and other civil engineering services, consulting and general contracting services to clients in both the public and private sectors.</p>
        <router-link to="#">More about us</router-link>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  layout: 'light',
  components: {},
}
</script>

<style lang="scss" scoped>
.hero {
  background-image: url('../assets/img/hero-img.jpg');
  background: linear-gradient(180deg, rgba(0, 0, 0, 0.56) 0%, #000000 85.2%);
  display: block;
  margin-top: -100px;
}

.hero-inner {
  padding: 15rem 0;
  max-width: 900px;
  margin: auto;
  text-align: center;
  color: $ot-white;

  h1 {
    font-size: 3.813rem;
    line-height: 86px;
    margin-bottom: 33px;
  }

  p {
    width: 80%;
    margin: auto;
  }
}

._btns {
  display: flex;
  justify-content: space-between;
  max-width: 290px;
  margin: 36px auto 0;

  .contact {
    background-color: $ot-red;
    color: $ot-white;
    padding: 12px 24px;
    border-radius: 4px;
  }

  .service {
    color: $ot-white;
    padding: 12px 24px;
    border: 1px solid $ot-white;
    border-radius: 4px;
  }
}

.about {
  background-image: url('../assets/img/about-line-art.png');
  background-repeat: no-repeat;
  display: block;

  ._inner {
    max-width: 900px;
    margin: auto;
    text-align: center;
    padding: 50px 0;

    h2 {
      font-size: 30px;
      font-family: "Aeonik TRIAL Regular";
      font-weight: 400;
      padding-bottom: 16px;
    }

    p {
      font-size: 18px;
      padding-bottom: 30px;
      line-height: 29px;
    }
  }
}
</style>
