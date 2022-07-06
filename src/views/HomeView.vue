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
          <p>Phone: 070-871-460</p>
          <p>E-mail: ivanadimitrova23@gmail.com</p>
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
          <p>Software engineer with thorough hands-on experience in all levels of testing,including preformance,functional,integration,system, and user acceptance testing.</p>
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
        <card-for-work v-for="experience in workExperience":experience="experience"/>
      </div>
    </section>
    <!--skils-->
    <section class="mb-5 container">
      <div class="row">
        <div class="col col-md-3 text-md-end fs-5 order-md-1 order-2 text-center">
          <i class="fa fa-desktop me-2" aria-hidden="true" ></i>
          <span>SKILLS</span>
        </div>
        <div class="col col-md-9 bg-danger order-md-2 line col-12 order-1 mb-3"></div>
      </div>
      <div class="row mt-3">
        <div class="col col-md-3"></div>
        <div class="col col-md-9 text-md-start col-12 text-center">
          <ul>
            <li>Preformance and scalability optimisation</li>
            <li>SharePoint</li>
            <li>API design</li>
            <li>Data warehousing and analytics</li>
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
        <card-for-school v-for="school in schools":school="school"/>
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
    <!--last red line-->
    <section>
      <div class="row py-2 bg-danger"></div>
    </section>
  </main>
</template>

<script>
import CardForWork from "../components/layout/CardForWork";
import CardForSchool from "../components/layout/CardForSchool";
export default {
  name: "HomeView",
  components: {
    CardForWork,
    CardForSchool
  },
  data(){
    return{
      workExperience: [
        {
          role:'SOFTWARE ENGINEER',
          companyName:'Hi Solutions (2020-present)',
          workDone1:'Direct software design',
          workDone2:'Evaluate interface between hardware and software',
          workDone3:'Advice customers regarding maintenance of software system'
        },
        {
          role:'JUNIOR SOFTWARE ENGINEER',
          companyName:'RealPro Software(2017-2020)',
          workDone1:'Prepared detailed reports',
          workDone2:'Stored,retrieved, and manipulated data',
          workDone3:' Modified existing softwares to correct errors'
        }
      ],
      schools: [
        {
          schoolDegree:'Bachelor degree',
          schoolName:'Ss. Cyril and Methodius University in Skopje (2020-present)'
        },
        {
          schoolDegree:'High School',
          schoolName:'Ljupco Santov in Kocani (2016-2020)'
        },{
          schoolDegree:'Elementary School',
          schoolName:'Ss. Cyril and Methodius in Kocani (2012-2016)'
        }
      ]
    }
  }
}
</script>


<!--
<div class="container py-5">
//false/NaN/[].length//0
<div v-if="0">test</div>
</div>

<div class="container py-5 ">
<div v-for="i in 4">
  <div class="col-4 bg-danger" v-if="i % 2 ===0">test {{ i }}</div>
</div>
</div>
-->