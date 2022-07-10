<template>
  <main class="background">
    <div class="container bg-primary p-0">
      <personal-information-hero/>
      <personal-statement/>
      <div class="row px-5">
        <div class="col-12 col-xl-8 mb-3">
          <work-experience/>
          <soft-skills/>
        </div>
        <div class="col-12 col-xl-4">
          <professional-skills/>
          <education/>
          <interests/>
        </div>
      </div>
      <div class="row">
        <star-rating/>
        <user-experience-buttons/>
      </div>
    </div>
  </main>
</template>

<script>

import Education from "@/components/Education";
import Interests from "@/components/Interests";
import SoftSkills from "@/components/SoftSkills";
import StarRating from "@/components/StarRating";
import WorkExperience from "@/components/WorkExperience";
import PersonalStatement from "@/components/PersonalStatement";
import ProfessionalSkills from "@/components/ProfessionalSkills";
import UserExperienceButtons from "@/components/UserExperienceButtons";
import PersonalInformationHero from "@/components/PersonalInformationHero";

export default {
  name: 'HomeView',
  components: {
    Education,
    Interests,
    StarRating,
    SoftSkills,
    WorkExperience,
    PersonalStatement,
    ProfessionalSkills,
    UserExperienceButtons,
    PersonalInformationHero
  }
}

</script>

<style scoped>
</style>
