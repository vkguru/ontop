<template>
  <div>
    <section class="hero">
      <div class="hero-inner">
        <h1>We deliver projects that defies all Imitations</h1>
        <p>
          We have considerable experience in giving outstanding services in the
          areas of Real Estate Construction, and civil engineering services. We
          provide excellent consultancy and project management expertise in the
          areas of Sales and procurement of building materials, construction of
          Borehole, Landscaping services, and importation of building materials
          amongst others. We have a depth of project type experience (schools,
          governmental, office, industrial, retail, parking structures,
          multi-unit residential on pile foundation, swimming pools, resorts
          among others)
        </p>
        <div class="_btns">
          <router-link to="contact-us" class="contact">Contact us</router-link>
          <router-link to="#service" class="service">Our services</router-link>
        </div>
      </div>
    </section>

    <section class="about">
      <div class="_inner">
        <h2>Who we are</h2>
        <p>
          We are a construction and project management company in Nigeria, which
          was incorporated to carry on the business of building construction,
          project management, construction management and facility management,
          design/build of first class building and other civil engineering
          services, consulting and general contracting services to clients in
          both the public and private sectors.
        </p>
        <router-link to="/about-us" class="ot-cta">More about us</router-link>
      </div>
    </section>

    <section class="why">
      <h2>Why Ontop Builders?</h2>
      <div class="_inner">
        <div class="img">
          <img
            id="__ser"
            src="~/assets/img/ontop-services.png"
            alt="two construction engineers on a project"
          />
          <div id="__strip">
            <img src="~/assets/img/service-stripe.png" alt="multiple stripes" />
          </div>
        </div>
        <div class="text">
          <div class="_card top">
            <div class="content">
              <img src="~/assets/img/safety.png" alt="safety icon" />
              <h3>Safety</h3>
              <p>
                We recognize the paramount importance of the safety of our
                employees, clients and the general public.
              </p>
            </div>
          </div>

          <div class="_card top">
            <div class="content">
              <img src="~/assets/img/environment.png" alt="environment icon" />
              <h3>Environmental protection</h3>
              <p>
                We recognize the paramount importance of the protection of the
                environment, and pay key attention to it during the course of
                carrying out our business or operations.
              </p>
            </div>
          </div>

          <div class="_card">
            <div class="content">
              <img src="~/assets/img/standard.png" alt="standard" />
              <h3>Standard</h3>
              <p>
                We ensure that all aspects of our operations comply with our
                clients’ standards as well as all Government rules and
                regulations affecting our business and operations.
              </p>
            </div>
          </div>

          <div class="_card">
            <div class="content">
              <img src="~/assets/img/quality.png" alt="quality" />
              <h3>Quality</h3>
              <p>
                We understand the Quality Assurance requirements of our clients
                and are totally committed to quality in completion and cost as
                primary objectives.
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="service">
      <h2>What we do</h2>
      <p>
        The strength of this company is in its ability to bring together more
        than 20 active individual professionals in the construction industry
        which includes a former project manager of a multinational company in
        Qatar, professional Site Engineers, Civil Engineers, Senior Architect,
        and Quality Surveyor, and a Chartered Accountant all with many years of
        experience in their chosen field. Here are our areas of expertise, and
        what we offer
      </p>
      <div class="_inner ot-container">
        <ServiceCard
          :title="`Building construction`"
          :info="`We follow best practices in all our building projects. We can handle any kind of projects regardless of the size`"
          :img="`building-construction.png`"
        />
        <ServiceCard
          :title="`Roads & Drainage`"
          :info="`We build roads and drainages that are qualid and durable.`"
          :img="`roads-drainages.png`"
        />
        <ServiceCard
          :title="`City infrastructure & civil engineering works`"
          :info="`Our team of professionals are experts in designing and developing quality infrastructures and engineering works`"
          :img="`city-infrastructure.png`"
        />
        <ServiceCard
          :title="`Architectural & structural designs`"
          :info="`Architectural designs includes; Production of working drawing for buildings, factories, office blocks, residential apartments, hotels, schools, hostels, hospitals, landscaping services and so on.`"
          :img="`arch-design.png`"
        />
        <ServiceCard
          :title="`Project management & procurement`"
          :info="`Our project management and procurement approach is second to none in the industry`"
          :img="`project-management.png`"
        />
        <ServiceCard
          :title="`International trade Logistics`"
          :info="`We provide international trade logistics`"
          :img="`international-logistics.png`"
        />

        <ServiceCard
          :title="`Real Estate Development`"
          :info="`We pride ourselves with our robust knowledge in the Real Estate sector to develop quality projects`"
          :img="`Real-estate-development.png`"
        />
      </div>
    </section>

    <section class="project">
      <header class="ot-container">
        <div class="text">
          <h2>Our Most Recent Projects</h2>
          <p>
            We pride ourselves in the delivery of industry standard projects. We
            follow international best practices to make this happen.
          </p>
        </div>
        <div class="link">
          <router-link to="/portfolio" class="ot-cta"
            >View all projects</router-link
          >
        </div>
      </header>

      <div class="ot-container">
        <div class="ctrl lt">
          <img src="~/assets/img/arrow-right.png" @click="moveCarousel(-1)" />
        </div>
        <div class="hid">
          <div
            class="row"
            :style="{
              transform: 'translateX' + '(' + currentOffset + 'px' + ')',
            }"
          >
            <PreviewProjects
              v-for="(project, index) in projects"
              :key="index"
              :image="project.img"
              :title="project.title"
              :location="project.location"
            />
          </div>
        </div>
        <div class="ctrl rt">
          <img src="~/assets/img/arrow-right.png" @click="moveCarousel(1)" />
        </div>
      </div>
    </section>

    <section>
      <PreFooter />
    </section>
  </div>
</template>

<script>
export default {
  layout: "light",
  components: {},
  data() {
    return {
      projects: [
        {
          img: "supermarket.jpg",
          title: "Supermarket",
          location: "Prince Ebeano supermarket",
        },
        {
          img: "church-building.jpg",
          title: "Church building",
          location: "RCCG Maryland",
        },
        {
          img: "estate.jpg",
          title: "Estate building construction",
          location: "Osborne offshore estate",
        },
        {
          img: "supermarket.jpg",
          title: "Supermarket",
          location: "Prince Ebeano supermarket",
        },
        {
          img: "church-building.jpg",
          title: "Church building",
          location: "RCCG Maryland",
        },
        {
          img: "estate.jpg",
          title: "Estate building construction",
          location: "Osborne offshore estate",
        },
        {
          img: "supermarket.jpg",
          title: "Supermarket",
          location: "Prince Ebeano supermarket",
        },
        {
          img: "church-building.jpg",
          title: "Church building",
          location: "RCCG Maryland",
        },
      ],
      currentOffset: 0,
      windowSize: 3,
      paginationFactor: 220,
    };
  },
  computed: {
    atEndOfList() {
      return (
        this.currentOffset <=
        this.paginationFactor * -1 * (this.projects.length - this.windowSize)
      );
    },
    atHeadOfList() {
      return this.currentOffset === 0;
    },
  },
  methods: {
    moveCarousel(direction) {
      // Find a more elegant way to express the :style. consider using props to make it truly generic
      if (direction === 1 && !this.atEndOfList) {
        this.currentOffset -= this.paginationFactor;
      } else if (direction === -1 && !this.atHeadOfList) {
        this.currentOffset += this.paginationFactor;
      }
    },
  },
};
</script>

<style lang="scss" scoped>
.hero {
  background-image: url("../assets/img/hero-img.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  display: block;
  margin-top: -100px;
}

.hero-inner {
  padding: 25rem 3rem 15rem;
  max-width: 1000px;
  margin: auto;
  text-align: center;
  color: $ot-white;

  h1 {
    font-size: 3.813rem;
    line-height: 86px;
    margin-bottom: 33px;
  }

  p {
    font-size: 18px;
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
  background-image: url("../assets/img/about-line-art.png");
  background-repeat: no-repeat;
  background-size: cover;
  display: block;
  padding: 50px 0 100px;
  margin-bottom: 100px;

  ._inner {
    max-width: 1000px;
    margin: auto;
    text-align: center;
    padding: 50px 20px;

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
    max-width: 40%;
    position: relative;

    // #__ser {
    //   width: 100%;
    // }

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
          content: "";
          display: block;
          height: 2px;
          width: 55%;
          background-color: #c4c4c4;
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

#service {
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

  & .ot-container {
    position: relative;
    & .hid {
      overflow: scroll;

      &::-webkit-scrollbar {
        width: 0;
        height: 0;
      }
    }

    & .ctrl {
      position: absolute;
      top: 170px;
      z-index: 9;

      & img {
        cursor: pointer;
      }

      &.rt {
        right: 0;
      }

      &.lt {
        transform: rotate(180deg);
      }
    }
  }

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
        line-height: 40px;
      }
    }

    & .link {
      margin-top: 50px;
    }
  }

  & .row {
    display: flex;
    justify-content: space-between;
    column-gap: 30px;
    margin: 50px 0;
    max-width: 1200px;
    transition: 0.5s ease-in-out;
  }
}

@media screen and (max-width: 768px) {
  p {
    font-size: 16px !important;
  }

  .hero-inner {
    padding: 16rem 1.58rem 8rem;

    & h1 {
      font-size: 3rem;
      line-height: 60px;
    }
  }

  .about {
    padding-bottom: 50px;
    margin-bottom: 0;
  }

  .why {
    & ._inner {
      text-align: center;
      flex-direction: column;
      & .img {
        display: none;
      }
      & .text {
        width: 90%;
        grid-template-columns: repeat(1, 1fr);
        & ._card {
          max-width: 100%;
          & .content {
            padding-bottom: 0;
          }

          &:nth-child(4) {
            .content {
              padding-top: 30px;
            }
          }

          &.top {
            &::after {
              display: none;
            }
          }
        }
      }
    }
  }

  #service {
    padding: 0 20px;
  }

  .project {
    padding: 80px 0 0;
    .ot-container {
      flex-direction: column;
      .text {
        max-width: 100%;
      }
      .link {
        margin-right: auto;
      }
    }
  }
}

@media screen and (max-width: 320px) {
  ._btns {
    flex-direction: column;

    .contact {
      margin-bottom: 20px;
    }
  }
}
</style>
