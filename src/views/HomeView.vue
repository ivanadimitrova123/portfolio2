<template>
  <main>
    <!--first red line-->
    <section>
      <div class="row py-2 bg-danger"></div>
    </section>
    <!--image and info-->
    <section class="container mb-lg-3">
      <div class="row py-lg-5 pt-4">
        <div class="col col-lg-3 d-flex justify-content-center col-7">
          <img alt="profile picture" src="../assets/images/profile-picture.jpg">
        </div>
        <div class="col col-lg-3 col-5">
          <p class="name text-dark fs-1">Ivana</p>
          <p class="name text-danger fs-1">Dimitrova</p>
          <p class="fs-4">Software engineer</p>
        </div>
        <div class="col col-lg-4 text-lg-end py-lg-5 col-12 text-center pt-5">
          <p class="pe-lg-5 pt-lg-4">Phone: 070-871-460</p>
          <a href="mailto:ivanadimitrova23@gmail.com">
            <i class="fa fa-envelope me-4 fa-2x social" aria-hidden="true"></i>
          </a>
          <a href="https://www.facebook.com/ivana.dimitrova23/">
            <i class="fa fa-facebook me-4 fa-2x social" aria-hidden="true"></i>
          </a>
          <a href="https://www.instagram.com/ivana.dimitrovva/">
            <i class="fa fa-instagram me-4 fa-2x social" aria-hidden="true"></i>
          </a>
          <a href="https://www.linkedin.com/in/ivana-dimitrova-19ba46170/">
            <i class="fa fa-linkedin-square me-4 fa-2x social" aria-hidden="true"></i>
          </a>
          <a href="https://github.com/ivanadimitrova123">
            <i class="fa fa-github fa-2x social" aria-hidden="true"></i>
          </a>
        </div>
        <div class="col col-lg-2"></div>
      </div>
    </section>
    <!--profile-->
    <section class="mb-5 container">
      <div class="row">
        <div class="col col-md-3 text-md-end fs-5 order-md-1 order-2 text-center">
          <i class="fa fa-user-o me-2" aria-hidden="true"></i>
          <span>PROFILE</span>
        </div>
        <div class="col col-md-9 bg-danger order-md-2 line col-12 order-1 mb-3"></div>
      </div>
      <div class="row">
        <div class="col col-md-3"></div>
        <div class="col col-md-6 text-md-start col-12 text-center">
          <p>Software engineer with thorough hands-on experience in all levels of testing,including
            preformance,functional,integration,system, and user acceptance testing.</p>
        </div>
        <div class="col col-3"></div>
      </div>
    </section>
    <!--employment-->
    <section class="mb-5 container">
      <div class="row">
        <div class="col col-md-3 text-md-end fs-5 order-md-1 order-2 text-center mb-3 mb-md-5">
          <i class="fa fa-briefcase me-2" aria-hidden="true"></i>
          <span>EMPLOYMENT</span>
        </div>
        <div class="col col-md-9 bg-danger order-md-2 line col-12 order-1 mb-3"></div>
      </div>
      <div>
        <card-for-work v-for="experience in workExperience" :experience="experience"/>
      </div>
    </section>
    <!--skils-->
    <section class="mb-5 container">
      <div class="row">
        <div class="col col-md-3 text-md-end fs-5 order-md-1 order-2 text-center">
          <i class="fa fa-desktop me-2" aria-hidden="true"></i>
          <span>SKILLS</span>
        </div>
        <div class="col col-md-9 bg-danger order-md-2 line col-12 order-1 mb-3"></div>
      </div>
      <div class="row mt-3">
        <div class="col col-md-3"></div>
        <div class="col col-md-9 text-md-start col-12 text-center">
          <ul>
            <li>API design</li>
            <li>SharePoint</li>
            <li>Data warehousing and analytics</li>
            <li>Preformance and scalability optimisation</li>
          </ul>
        </div>
      </div>
    </section>
    <!--education-->
    <section class="mb-5 container">
      <div class="row">
        <div class="col col-md-3 text-md-end fs-5 order-md-1 order-2 text-center mb-3 mb-md-5">
          <i class="fa fa-university me-2" aria-hidden="true"></i>
          <span>EDUCATION</span>
        </div>
        <div class="col col-md-9 bg-danger order-md-2 line col-12 order-1 mb-3"></div>
      </div>
      <div>
        <card-for-school v-for="school in schools" :school="school"/>
      </div>
    </section>
    <!--language-->
    <section class="mb-3 container">
      <div class="row">
        <div class="col col-md-3 text-md-end fs-5 order-md-1 order-2 text-center">
          <i class="fa fa-language me-2" aria-hidden="true"></i>
          <span>LANGUAGES</span>
        </div>
        <div class="col col-md-9 bg-danger order-md-2 line col-12 order-1 mb-3"></div>
      </div>
      <div class="row mt-3">
        <div class="col col-md-3"></div>
        <div class="col col-md-9 text-md-start col-12 text-center">
          <p>Macedonian</p>
          <progress value="100" max="100"></progress>
        </div>
      </div>
      <div class="row">
        <div class="col col-md-3"></div>
        <div class="col col-md-9 text-md-start col-12 text-center">
          <p>English</p>
          <progress value="70" max="100"></progress>
        </div>
      </div>
    </section>
    <!--rate my cv-->
    <section class="mb-5 container">
      <div class="row">
        <div class="col col-md-3 text-md-end fs-5 order-md-1 order-2 text-center mb-3 mb-md-5">
          <i class="fa fa-smile-o me-2" aria-hidden="true"></i>
          <span>RATE MY CV</span>
        </div>
        <div class="col col-md-9 bg-danger order-md-2 line col-12 order-1 mb-3"></div>
      </div>
      <div>
        <card-for-rating v-for="rate in rateing" :rate="rate" :variable="variable" @updateCounter="variable = $event"/>
      </div>
      <div class="row">
        <div class="col-md-3"></div>
        <div class="col col-xl-4 text-center my-3 py-1 fs-5 bg-danger text-white col-md-5 col-12">
          <span>Overall you like my CV </span>
          <span> {{ (variable / 15 * 100).toFixed(2) }} %</span>
        </div>
      </div>
    </section>
    <!--last red line-->
    <section>
      <div class="row py-2 bg-danger"></div>
    </section>
  </main>
</template>

<script>
import CardForWork from "../components/layout/CardForWork";
import CardForSchool from "../components/layout/CardForSchool";
import CardForRating from "../components/layout/CardForRating";

export default {
  name: "HomeView",
  components: {
    CardForRating,
    CardForWork,
    CardForSchool
  },
  data() {
    return {
      variable: 0,
      workExperience: [
        {
          role: 'SOFTWARE ENGINEER',
          companyName: 'Hi Solutions (2020-present)',
          workDone1: 'Direct software design',
          workDone2: 'Evaluate interface between hardware and software',
          workDone3: 'Advice customers regarding maintenance of software system'
        },
        {
          role: 'JUNIOR SOFTWARE ENGINEER',
          companyName: 'RealPro Software(2017-2020)',
          workDone1: 'Prepared detailed reports',
          workDone2: 'Stored,retrieved, and manipulated data',
          workDone3: ' Modified existing softwares to correct errors'
        }
      ],
      schools: [
        {
          schoolDegree: 'Bachelor degree',
          schoolName: 'Ss. Cyril and Methodius University in Skopje (2020-present)'
        },
        {
          schoolDegree: 'High School',
          schoolName: 'Ljupco Santov in Kocani (2016-2020)'
        }, {
          schoolDegree: 'Elementary School',
          schoolName: 'Ss. Cyril and Methodius in Kocani (2012-2016)'
        }
      ],
      rateing: [
        {
          rateFor: 'Interesting',
          clickText: 'Click on the star multiple times to rate if my CV was interesting',
        },
        {
          rateFor: 'Informative',
          clickText: 'Click on the star multiple times to rate if my CV was informative',
        },
        {
          rateFor: 'Easy to navigate',
          clickText: 'Click on the star multiple times to rate if my CV was easy to navigate',
        }
      ]
    }
  }
}
</script>