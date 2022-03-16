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
        <router-link to="#" class="ot-cta">More about us</router-link>
      </div>
    </section>

    <section class="why">
      <h2>Why Ontop builders?</h2>
      <div class="_inner">
        <div class="img">
          <img id="__ser" src="~/assets/img/ontop-services.png" alt="two construction engineers on a project" />
          <div id="__strip">
            <img src="~/assets/img/service-stripe.png" alt="multiple stripes" />
          </div>
        </div>
        <div class="text">
          <div class="_card top">
            <div class="content">
              <img src="~/assets/img/safety.png" alt="safety icon" />
              <h3>Safety</h3>
              <p>We recognize the paramount importance of the safety of our employees, clients and the general public.</p>
            </div>
          </div>

          <div class="_card top">
            <div class="content">
              <img src="~/assets/img/environment.png" alt="environment icon" />
              <h3>Environmental protection</h3>
              <p>We recognize the paramount importance of the protection of the environment, and pay key attention to it during the course of carrying out our business or operations.</p>
            </div>
          </div>

          <div class="_card">
            <div class="content">
              <img src="~/assets/img/standard.png" alt="standard" />
              <h3>Standard</h3>
              <p>We ensure that all aspects of our operations comply with our clients’ standards as well as all Government rules and regulations affecting our business and operations.</p>
            </div>
          </div>

          <div class="_card">
            <div class="content">
              <img src="~/assets/img/quality.png" alt="quality" />
              <h3>Quality</h3>
              <p>We understands the Quality Assurance requirements of our clients and are totally committed to quality in completion and cost as primary objectives.</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="service">
      <h2>What we do</h2>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed leo turpis consequat, commodo elementum ac eu id dictum.</p>
      <div class="_inner ot-container">
        <ServiceCard 
          :title="`Building construction`"
          :info="`Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.`" 
          :img="`building-construction.png`" 
        />
        <ServiceCard 
          :title="`Roads & Drainage`"
          :info="`Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.`" 
          :img="`roads-drainages.png`" 
        />
        <ServiceCard 
          :title="`City infrastructure & civil engineering works`"
          :info="`Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.`" 
          :img="`city-infrastructure.png`" 
        />
        <ServiceCard 
          :title="`Architectural & structural designs`"
          :info="`Architectural designs includes; Production of working drawing for buildings, factories, office blocks, residential apartments, hotels, schools, hostels, hospitals, landscaping services and so on.`" 
          :img="`arch-design.png`" 
        />
        <ServiceCard 
          :title="`Project management & procurement`"
          :info="`Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.`" 
          :img="`project-management.png`" 
        />
        <ServiceCard 
          :title="`International trade Logistics`"
          :info="`Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.`" 
          :img="`international-logistics.png`" 
        />
        
        <ServiceCard 
          :title="`Real Estate Development`"
          :info="`Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.`" 
          :img="`Real-estate-development.png`" 
        />
      </div>
    </section>

    <section class="project">
      <header class="ot-container">
        <div class="text">
          <h2>Our Most Recent Projects</h2>
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed leo turpis consequat, commodo elementum ac eu id dictum</p>
        </div>
        <div class="link">
          <router-link to="/potfolio" class="ot-cta">View all projects</router-link>
        </div>
      </header>
    </section>

    <section>
      <PreFooter />
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
  background-repeat: no-repeat;
  background-size: cover;
  display: block;
  margin-top: -100px;
}

.hero-inner {
  padding: 25rem 0 15rem;
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

    &:hover {
      background-color: $ot-white;
      color: $ot-red;
    }
  }

  .service {
    color: $ot-white;
    padding: 12px 24px;
    border: 1px solid $ot-white;
    border-radius: 4px;

    &:hover {
      background-color: $ot-red;
      color: $ot-white;
      border: 1px solid $ot-red;
    }
  }
}

.about {
  background-image: url('../assets/img/about-line-art.png');
  background-repeat: no-repeat;
  background-size: cover;
  display: block;
  padding: 50px 0 100px;
  margin-bottom: 100px;

  ._inner {
    max-width: 900px;
    margin: auto;
    text-align: center;
    padding: 50px 0;

    h2 {
      font-size: 30px;
      font-family: "Aeonik TRIAL";
      font-weight: 400;
      padding-bottom: 16px;
    }

    p {
      font-size: 18px;
      padding-bottom: 60px;
      line-height: 29px;
    }

    .cta {
      color: $ot-red;
      padding: 12px 24px;
      border: 1px solid $ot-red;
      border-radius: 4px;
    }
  }
}

.why {
  h2 {
    font-family: "Aeonik TRIAL";
    font-size: 30px;
    font-weight: 400;
    text-align: center;
  }

  ._inner {
    margin-top: 100px;
    padding-bottom: 100px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    column-gap: 200px;
  }

  .img {
    width: 40%;
    position: relative;

    #__ser {
      width: 100%;
    }

    #__strip {
      position: absolute;
      top: 415px;
      right: -130px;
      z-index: -1;
    }
  }

  .text {
    width: 980px;
    display: grid;
    grid-template-columns: repeat(2, 1fr);

    ._card {
      max-width: 348px;

      .content {
        position: relative;
        height: 100%;
        padding-bottom: 30px;
      }

      &.top {
        margin-bottom: 50px;
        &::after {
          content: '';
          display: block;
          height: 2px;
          width: 55%;
          background-color: #C4C4C4;
          opacity: 0.3;
        }
      }

      img {
        padding-bottom: 20px;
      }

      h3 {
        line-height: 30px;
        padding-bottom: 10px;
      }
    }
  }
}

.service {
  padding: 150px 0;

  h2 {
      font-size: 30px;
      font-family: "Aeonik TRIAL";
      font-weight: 400;
      padding-bottom: 16px;
      text-align: center;
    }

    p {
      font-size: 18px;
      padding-bottom: 60px;
      line-height: 29px;
      text-align: center;
      max-width: 870px;
      margin: auto;
    }

    ._inner {
      display: flex;
      justify-content: flex-start;
      align-items: center;
      flex-wrap: wrap;
      column-gap: 35px;
      grid-row-gap: 35px;
    }
}

.project {
  padding: 80px 0;
  
  & header {
    display: flex;
    justify-content: space-between;
    align-items: center;

    & .text {
      max-width: 550px;

      & h2 {
        font-family: "Aeonik TRIAL";
        font-weight: 400;
        padding-bottom: 16px;
        font-size: 30px;
      }
    }

    & .link {
      margin-top: 50px;
    }
  }
}
</style>
