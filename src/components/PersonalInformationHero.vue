<template>
  <section class="container">
    <div class="row background">
      <div class="col-12 col-xl-3 p-0 m-0">
        <div class="ratio ratio-292x350">
          <img class="object-fit-cover" src="../assets/images/291770709_3339692369600221_5753835680248884173_n.jpg" alt="Profile picture">
        </div>
      </div>
      <div class="col-12 col-xl-9 text-white">
        <div class="row ps-0">
          <div class="col-12 col-xl-8 d-flex flex-column align-items-start text-white ps-sm-5">
            <p class="h3  pt-4 ps-2">EMILIJA SIMONOSKA</p>
            <h5 class="title ps-2">Full Stack Developer</h5>
            <ul class="list-unstyled pt-4 ps-2">

              <li class="my-2 d-flex flex-column flex-sm-row"><i class="fa fa-envelope mx-2" aria-hidden="true"></i>
                <a href="https://www.facebook.com/emilijaes/" target="_blank"
                   class="text-decoration-none">emilija.simonoska@hotmail.com</a>
              </li>

              <li class="my-2 d-flex flex-column flex-sm-row"><i class="fa fa-mobile fa-2x mx-2" aria-hidden="true"></i>
                (+389) 71374292
              </li>

              <li class="my-2 d-flex flex-column flex-sm-row"><i class="fa fa-compass mx-2" aria-hidden="true"></i>
                Macedonia, Ohrid
              </li>
            </ul>
          </div>
          <div class="col-12 col-xl-3 d-flex align-items-start">
            <ul class="list-unstyled  ms-0 ms-sm-4 ps-0 ps-sm-3 pt-5">
              <li class="mb-2 d-flex align-items-sm-center pt-3"><i class="fa fa-github mx-2" aria-hidden="true"></i>
                <a href="#" class="text-decoration-none">linkedin.com/username</a>
              </li>
              <li class="my-2 d-flex align-items-sm-center"><i class="fa fa-quora mx-2" aria-hidden="true"></i>
                <a href="#" class="text-decoration-none">quora.com/username</a>
              </li>
              <li class="my-2 d-flex align-items-sm-center"><i class="fa fa-youtube mx-2" aria-hidden="true"></i>
                <a href="#" class="text-decoration-none">youtube.com/username</a>
              </li>
              <li class="my-2 d-flex align-items-sm-center">
                <i class="fa fa-linkedin-square mx-2" aria-hidden="true"></i>
                <a href="#" class="text-decoration-none">linkedin.com/username</a>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "PersonalInformationHero"
}
</script>

<style scoped>
.background {
  background: rgb(66,148,23);
  background: linear-gradient(90deg, rgba(66,148,23,1) 37%, rgba(18,32,180,1) 69%, rgba(7,12,66,1) 95%);
}
</style>