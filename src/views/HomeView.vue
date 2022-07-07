<template>
  <main class="container">
    <personal-information-hero/>
    <article class="bg-primary">

      <personal-statement/>

      <div class="px-5">
        <div class="row">
          <div class="col-12 col-lg-8">

            <h3 class="text-uppercase">Work Experience</h3>
            <hr/>
            <work-experience v-for="experience in workExperiences" :work-experience="experience"/>

            <h3 class="mx-3 mt-4 text-uppercase">Soft Skills</h3>
            <hr class="mb-3"/>
            <soft-skills v-for="skill in softSkills" :soft-skill="skill" class="mb-3"/>

          </div>

          <div class="col-12 col-lg-4">

            <h3 class="text-uppercase d-flex justify-content-center">Proffesional Skills</h3>
            <hr/>

            <h4 class="mt-2 ms-5 text-decoration-underline">Frontend</h4>
            <ul class="list-unstyled mt-3">
              <proffesional-skills v-for="skill in proffesionalSkillsFrontend" :proffesional-skill="skill"/>
            </ul>

            <h4 class="mt-4 ms-5 text-decoration-underline">Backend</h4>
            <ul class="list-unstyled mt-3">
              <proffesional-skills v-for="skill in proffesionalSkillBackend"
                                   :proffesional-skill="skill"/>
            </ul>

            <h3 class="text-uppercase d-flex justify-content-center mt-5 pt-5">Education
            <span class="ps-3"><i @click="isActiveEducation" class="fa fa-arrow-circle-down fa-2x btn btn-danger"/></span>
            </h3>
            <hr/>

            <ul class="list-unstyled">
              <education v-for="degree in degrees" :education-degree="degree" :is-active-button-education="isActiveButtonEducation"/>
            </ul>

            <h3 class="text-uppercase d-flex justify-content-center mt-5 pt-5">Interests
            <span class="ps-3"><i @click="isActiveInterests" class="fa fa-arrow-circle-down fa-2x btn btn-danger"/></span>
            </h3>

            <hr/>


            <ul class="list-unstyled mt-3">
              <interests v-for="interest in interests" :interest="interest" :is-active-button-interests="isActiveButtonInterests"/>
            </ul>

          </div>

        </div>

      </div>

      <div class="container p-5 p4-2 d-flex justify-content-center">

        <button @click="isClickedLike" class="btn btn-secondary rounded rounded-pill text-white px-3 me-3 ">LIKE
          <span class="badge px-3"> {{ likesCounter }}</span>
        </button>

        <button @click="isClickedDislike" class="btn btn-danger rounded rounded-pill text-white px-3">DISLIKE
          <span class="badge px-3"> {{ dislikesCounter }}</span>
        </button>

      </div>

    </article>

  </main>
</template>

<script>

import Education from "@/components/Education";
import Interests from "@/components/Interests";
import SoftSkills from "@/components/SoftSkills";
import WorkExperience from "@/components/WorkExperience";
import PersonalStatement from "@/components/PersonalStatement";
import ProffesionalSkills from "@/components/ProffesionalSkills";
import PersonalInformationHero from "@/components/PersonalInformationHero";


export default {
  name: 'HomeView',
  components: {
    Education,
    Interests,
    SoftSkills,
    WorkExperience,
    PersonalStatement,
    ProffesionalSkills,
    PersonalInformationHero
  },
  methods: {
    isClickedLike() {
      this.likesCounter++;
    },
    isClickedDislike() {
      this.dislikesCounter++;
    },
    isActiveInterests() {
      this.isActiveButtonInterests = !this.isActiveButtonInterests;
    },
    isActiveEducation() {
      this.isActiveButtonEducation = !this.isActiveButtonEducation;
    }
  },

  computed: {

  },

  watch: {

  },
  data() {
    return {
      workExperiences: [
        {
          title: 'Job Title 1',
          begin: 2020,
          end: 'present',
          paragraph: 'Lorem Ipsum is simply dummy text of the printing and\n' +
              '      typesetting industry. Lorem Ipsum has been the industry\'s standard dummy text ever since the 1500s, when\n' +
              '      an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived\n' +
              '      not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged.\n' +
              '      It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and\n' +
              '      more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.',
          technologiesUsed: ['JAVA', 'HTML', 'CSS']
        },
        {
          title: 'Job Title 2',
          begin: 2019,
          end: 2020,
          paragraph: 'Lorem Ipsum is simply dummy text of the printing and\n' +
              '      typesetting industry. Lorem Ipsum has been the industry\'s standard dummy text ever since the 1500s, when\n' +
              '      an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived\n' +
              '      not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged.\n' +
              '      It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and\n' +
              '      more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.',
          technologiesUsed: ['Django', 'Python', 'CSS', 'HTML']
        },
        {
          title: 'Job Title 3',
          begin: 2018,
          end: 2019,
          paragraph: 'Lorem Ipsum is simply dummy text of the printing and\n' +
              '      typesetting industry. Lorem Ipsum has been the industry\'s standard dummy text ever since the 1500s, when\n' +
              '      an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived\n' +
              '      not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged.\n' +
              '      It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and\n' +
              '      more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.',
          technologiesUsed: ['Python', 'Bootstrap', 'CSS', 'HTML']
        }
      ],
      softSkills: [
        {
          skillName: 'Excellent Communicator',
          skillDescription: 'Lorem Ipsum is simply dummy text of the printing and\n' +
              '      typesetting industry. Lorem Ipsum has been the industry\'s standard dummy text ever since the 1500s, when\n' +
              '      an unknown printer took a galley of type and scrambled it to make a type specimen book.'
        },
        {
          skillName: 'Team Player',
          skillDescription: 'Lorem Ipsum is simply dummy text of the printing and\n' +
              '      typesetting industry. Lorem Ipsum has been the industry\'s standard dummy text ever since the 1500s, when\n' +
              '      an unknown printer took a galley of type and scrambled it to make a type specimen book.'
        }
      ],
      proffesionalSkillsFrontend: [
        {
          skillName: 'HTML',
          rating: 4
        },
        {
          skillName: 'CSS',
          rating: 4
        },
        {
          skillName: 'BOOTSTRAP',
          rating: 5
        }
      ],
      proffesionalSkillBackend: [
        {
          skillName: 'PYTHON',
          rating: 4
        },
        {
          skillName: 'DJANGO',
          rating: 3
        },
        {
          skillName: 'JAVA',
          rating: 5
        }
      ],
      degrees: [
        {
          degreeName: 'Degree Name 1',
          begin: 'yearX',
          end: 'yearY'
        },
        {
          degreeName: 'Degree Name 2',
          begin: 'yearZ',
          end: 'yearT'
        },
        {
          degreeName: 'Degree Name 3',
          begin: 'yearH',
          end: 'yearP'
        }
      ],

      interests: [
        'Photography',
        'Books',
        'Traveling',
        'Cycling',
        'Tennis',
        'Fitness'
      ],
      likesCounter: 0,
      dislikesCounter: 0,
      isActiveButtonInterests: false,
      isActiveButtonEducation: false
    }
  }
}

</script>

<style scoped></style>
