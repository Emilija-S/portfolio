<template>
  <main class="container">
    <personal-information-hero/>
    <article class="bg-primary">

      <personal-statement/>

      <div class="px-5">
        <div class="row">
          <div class="col-12 col-xl-8">

            <h3 class="text-uppercase">Work Experience</h3>
            <hr/>
            <work-experience v-for="experience in workExperiences" :work-experience="experience"/>

            <h3 class="mx-3 mt-4 text-uppercase">Soft Skills</h3>
            <hr class="mb-3"/>
            <soft-skills v-for="skill in softSkills" :soft-skill="skill" class="mb-3"/>

          </div>

          <div class="col-12 col-xl-4">

            <h3 class="text-uppercase d-flex justify-content-center">Proffesional Skills</h3>
            <hr/>

            <h4 class="mt-2 ms-5 text-decoration-underline">Frontend</h4>
            <ul class="list-unstyled mt-3">
              <proffesional-skills v-for="skill in proffesionalSkillsFrontend" :proffesional-skill="skill"/>
            </ul>

            <h4 class="mt-4 ms-5 text-decoration-underline">Backend</h4>
            <ul class="list-unstyled mt-3">
              <proffesional-skills v-for="skill in proffesionalSkillBackend" :proffesional-skill="skill"/>
            </ul>

            <h3 class="text-uppercase d-flex justify-content-center mt-5 pt-5">Education
              <span class="ps-3"><i @click="isActiveEducation" class="fa fa-arrow-circle-down fa-2x btn btn-danger"/></span>
            </h3>
            <hr/>

            <ul class="list-unstyled">
              <education v-for="degree in degrees" :education-degree="degree"
                         :is-active-button-education="isActiveButtonEducation"/>
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


          <h3 class="d-flex justify-content-center text-center mt-5">RATE YOUR EXPERIENCE: </h3>
          <ul class="list-unstyled d-flex flex-row justify-content-center">
            <li  class="btn p-2"  :class="(currentNumberOfStars >= 1)? bgColor : ''" @click="rating(1)"><i class="fa fa-star-o fa-2x" aria-hidden="true"></i></li>
            <li  class="btn p-2"  :class="(currentNumberOfStars >= 2)? bgColor : ''" @click="rating(2)"><i class="fa fa-star-o fa-2x" aria-hidden="true"></i></li>
            <li  class="btn p-2"  :class="(currentNumberOfStars >= 3)? bgColor : ''" @click="rating(3)"><i class="fa fa-star-o fa-2x" aria-hidden="true"></i></li>
            <li  class="btn p-2"  :class="(currentNumberOfStars >= 4)? bgColor : ''" @click="rating(4)"><i class="fa fa-star-o fa-2x" aria-hidden="true"></i></li>
            <li  class="btn p-2"  :class="(currentNumberOfStars === 5)? bgColor : ''" @click="rating(5)"><i class="fa fa-star-o fa-2x" aria-hidden="true"></i></li>
          </ul>
          <h3 class="col-12 d-flex justify-content-center text-center">Average rating reached: {{ ratioCalculated }}</h3>

      </div>

      <user-experience-buttons/>


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
import UserExperienceButtons from "@/components/UserExperienceButtons";



export default {
  name: 'HomeView',
  components: {
    UserExperienceButtons,
    Education,
    Interests,
    SoftSkills,
    WorkExperience,
    PersonalStatement,
    ProffesionalSkills,
    PersonalInformationHero
  },

  methods: {
    isActiveInterests() {
      this.isActiveButtonInterests = !this.isActiveButtonInterests;
    },
    isActiveEducation() {
      this.isActiveButtonEducation = !this.isActiveButtonEducation;
    },
    rating(numberOfStars) {
      this.currentNumberOfStars = numberOfStars;
      this.sumOfStars += numberOfStars;
      this.ratingCounter++;
    }
  },

  computed: {
    ratioCalculated() {
      return (this.sumOfStars / this.ratingCounter).toFixed(2);
    }
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
          technologiesUsed: [
            {
              technologyName: 'JAVA',
              technologyLink: 'https://docs.oracle.com/javase/7/docs/api/'
            },
            {
              technologyName: 'HTML',
              technologyLink: 'https://developer.mozilla.org/en-US/docs/Web/HTML'
            },
            {
              technologyName: 'CSS',
              technologyLink: 'https://developer.mozilla.org/en-US/docs/Web/CSS'
            }
          ]
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
          technologiesUsed: [
            {
              technologyName: 'Django',
              technologyLink: 'https://docs.djangoproject.com/en/4.0/'
            },
            {
              technologyName: 'Python',
              technologyLink: 'https://docs.python.org/3/'
            },
            {
              technologyName: 'CSS',
              technologyLink: 'https://developer.mozilla.org/en-US/docs/Web/CSS'
            },
            {
              technologyName: 'HTML',
              technologyLink: 'https://developer.mozilla.org/en-US/docs/Web/HTML'
            }
          ]
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
          technologiesUsed: [
            {
              technologyName: 'Python',
              technologyLink: 'https://docs.python.org/3/'
            },
            {
              technologyName: 'Bootstrap',
              technologyLink: 'https://getbootstrap.com/docs/4.1/getting-started/introduction/'
            },
            {
              technologyName: 'CSS',
              technologyLink: 'https://developer.mozilla.org/en-US/docs/Web/CSS'
            },
            {
              technologyName: 'HTML',
              technologyLink: 'https://developer.mozilla.org/en-US/docs/Web/HTML'
            }
          ]
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
        'Nature',
        'Books',
        'Traveling',
        'Cycling',
        'Tennis',
        'Fitness'
      ],

      sumOfStars: 0,
      showImg: false,
      ratingCounter: 0,
      bgColor: 'bg-warning',
      currentNumberOfStars: 0,
      isActiveButtonInterests: false,
      isActiveButtonEducation: false
    }
  }
}

</script>

<style scoped>
</style>
