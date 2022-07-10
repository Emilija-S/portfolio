<template>
  <section>
    <h3 class="text-uppercase">Work Experience</h3>
    <hr/>
    <div v-for="workExperience in workExperiences">
      <h4 class="mx-3">{{ workExperience.title }}</h4>
      <p class="mx-3 fs-6">{{ workExperience.begin }} - {{ workExperience.end }}</p>
      <p class="fs-5">
        {{ workExperience.paragraph }}
      </p>
      <p class="mx-3 fs-5 fw-bolder">Technologies used</p>
      <ul class="list-inline mb-3">
        <li class="list-inline-item m-2" v-for="technology in workExperience.technologiesUsed">
          <a :href="technology.technologyLink" target="_blank"><span class="badge bg-secondary badge-pill fs-5">
          {{ technology.technologyName }}
        </span></a>
        </li>
      </ul>
      <hr class="hr-dashed">
    </div>
  </section>
</template>

<script>
export default {
  name: "WorkExperience",
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
      ]
    }
  }
}
</script>

<style scoped>
</style>