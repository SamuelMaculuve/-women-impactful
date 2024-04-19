<script setup>
import WelcomeItem from './WelcomeItem.vue'
import DocumentationIcon from './icons/IconDocumentation.vue'
import ToolingIcon from './icons/IconTooling.vue'
import EcosystemIcon from './icons/IconEcosystem.vue'
import CommunityIcon from './icons/IconCommunity.vue'
import SupportIcon from './icons/IconSupport.vue'
</script>

<template>
  <!-- Video + Title split section -->
  <section class="container-fluid position-relative px-0 pt-5 mt-3 mt-lg-4">
    <div class="row g-0">
      <div class="col-xl-7 col-lg-6 pe-lg-5">
        <div class="d-flex h-100 pe-xl-4">
          <video class="w-100" autoplay muted loop style="object-fit: cover;">
            <source :src="'src/assets/assets/img/landing/conference/hero-video.mp4'" type="video/mp4">
          </video>
        </div>
      </div>
      <div class="col-xl-5 col-lg-6 position-relative py-5">
        <img :src="'src/assets/assets/img/landing/conference/hero-bg.png'" class="position-absolute top-50 translate-middle-y ms-lg-n4" width="866" alt="Background shapes">
        <div class="position-relative zindex-5 text-center text-lg-start px-3 px-lg-0 py-xl-4 py-xxl-5 mt-lg-3 mx-auto mx-lg-0" style="max-width: 530px;">
          <h1 class="display-1 pb-lg-3 mb-3">Mulheres Impactantes em Moçambique</h1>
        </div>
      </div>
    </div>
    <div class="position-absolute d-none d-lg-block bottom-0 start-0 w-100 zindex-5 pb-xxl-5">
      <div class="container pb-4 mb-3 mb-xxl-0">
        <a href="#speakers" class="d-table text-light opacity-80 text-decoration-none w-auto py-4" data-scroll data-scroll-offset="70">
              <span class="d-flex align-items-center">
                Scroll para ver mais
                <i class="bx bx-down-arrow-circle fs-3 ms-2"></i>
              </span>
        </a>
      </div>
    </div>
  </section>
  <hr>
  <!-- Speakers -->
  <section id="speakers" class="container my-2 my-md-4 my-lg-5">
    <div class="d-md-flex align-items-center justify-content-between text-center text-md-start pt-md-1 pt-lg-3">
      <h2 class="h1 mb-4 mb-md-0 me-md-3">Mulheres Impactantes</h2>
    </div>
    <div class="row row-cols-1 row-cols-sm-2 row-cols-md-3 row-cols-lg-4 g-4 mt-2 mt-lg-4">

      <!-- Item -->
      <div class="col">
        <div class="card card-hover border-0 bg-transparent">
          <div class="position-relative">
            <img :src="'src/assets/assets/img/team/24.jpg'" class="rounded-3" alt="Ralph Edwards">
            <div class="card-img-overlay d-flex flex-column align-items-center justify-content-center rounded-3">
              <span class="position-absolute top-0 start-0 w-100 h-100 bg-primary opacity-35 rounded-3"></span>
              <div class="position-relative d-flex zindex-2">
                <a href="#" class="btn btn-icon btn-secondary btn-facebook btn-sm bg-white me-2" aria-label="Facebook">
                  <i class="bx bxl-facebook"></i>
                </a>
                <a href="#" class="btn btn-icon btn-secondary btn-linkedin btn-sm bg-white me-2" aria-label="LinkedIn">
                  <i class="bx bxl-linkedin"></i>
                </a>
                <a href="#" class="btn btn-icon btn-secondary btn-twitter btn-sm bg-white me-2" aria-label="Twitter">
                  <i class="bx bxl-twitter"></i>
                </a>
                <a href="#" class="btn btn-icon btn-secondary btn-linkedin btn-sm bg-white" aria-label="LinkedIn" data-bs-toggle="modal" data-bs-target="#staticWomanDialog">
                  <i class='bx bxs-door-open'></i>
                </a>
              </div>
            </div>
          </div>
          <div class="card-body text-center p-3">
            <h3 class="fs-lg fw-semibold pt-1 mb-2">Ralph Edwards</h3>
            <p class="fs-sm mb-0">Founder &amp; CEO, Uber</p>
          </div>
        </div>
      </div>


    </div>
  </section>

  <section class="container pb-5 mb-2 mb-md-4 mb-lg-5 mt-n3 mt-lg-0">
    <div class="row pt-xl-2 pb-md-3">
      <div class="col-lg-5 mb-4 mb-lg-0">
        <h2 class="h1 text-center text-sm-start mb-4">Women Techmakers Maputo🤩💙</h2>
        <p class="pb-2 pb-lg-4 pb-xl-5 mb-3">Et, morbi at sagittis vehicula rutrum. Lacus tortor, quam arcu mi et, at lectus leo nunc. Mattis cras auctor vel pharetra tempor. Rhoncus pellentesque habitant ac tempor. At aliquam euismod est in praesent ornare etiam id. Faucibus libero sit vehicula sed condimentum. Vitae in nam porttitor rutrum sed aliquam donec sed. Sapien facilisi lectus.</p>
      </div>
      <div class="col-xl-6 col-lg-7 offset-xl-1 position-relative">

        <!-- Ticket card -->
        <div class="position-relative">
          <div class="position-relative overflow-hidden bg-gradient-primary rounded-3 zindex-5 py-5 px-4 p-sm-5">
            <span class="position-absolute top-50 start-0 translate-middle bg-light rounded-circle p-4"></span>
            <span class="position-absolute top-0 start-0 w-100 h-100 bg-repeat-0 bg-position-center-end bg-size-cover" style="background-image: url(assets/img/landing/conference/price-card-pattern.png);"></span>
            <div class="px-md-4 position-relative zindex-5">
              <div class="d-sm-flex align-items-start justify-content-between">
                <div class="text-center text-sm-start me-sm-4">
                  <h3 class="h1 text-light">Conheces uma mulher inspiradora?</h3>
                </div>
                <div class="d-table bg-white rounded-3 p-4 flex-shrink-0 mx-auto mx-sm-0">
                  <img :src="'assets/img/landing/conference/qr.png'" width="102" alt="QR Code">
                </div>
              </div>
              <div class="d-flex flex-column flex-sm-row align-items-center pt-4 mt-2">
                <a href="#" class="btn btn-light btn-lg mb-3 mb-sm-0 me-sm-3">partilhar aqui</a>
                <div class="d-flex align-items-center">
                </div>
              </div>
            </div>
            <span class="position-absolute top-50 end-0 translate-middle-y bg-light rounded-circle p-4 me-n4"></span>
          </div>
          <span class="position-absolute bg-gradient-primary opacity-60 bottom-0 mb-n2 d-dark-mode-none" style="left: 1.5rem; width: calc(100% - 3rem); height: 5rem; filter: blur(.625rem);"></span>
        </div>

        <!-- Arrow -->
        <div class="position-absolute bottom-0 text-primary d-none d-lg-block ms-xl-n5 mb-lg-5 mb-xl-4 pb-3">
          <div class="ms-xl-n4">
            <svg width="95" height="100" viewBox="0 0 95 100" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M78.8361 25.0939C91.1514 40.6379 81.8802 63.3086 61.7212 64.3539C60.7119 64.447 59.5832 64.3477 58.6105 64.2848C58.7669 50.9978 52.4534 36.5276 41.6324 32.847C31.8669 29.5776 26.5235 39.0204 30.5663 47.0383C35.4083 56.5589 43.9198 64.4699 54.2628 67.3808C53.4517 75.7446 49.4008 83.1867 40.4191 85.693C25.2817 89.8859 9.48935 75.832 7.25928 61.4938C7.12064 59.981 4.79 60.0942 4.92864 61.607C5.83171 80.8987 28.9103 96.1621 46.7792 87.3441C53.6867 83.8595 57.3887 76.5003 58.3558 68.173C69.2212 69.5612 79.5859 63.2659 85.1681 54.2081C91.5844 43.7002 88.5763 31.9764 81.257 23.1926C80.1091 21.7727 77.8441 23.7109 78.8361 25.0939ZM39.1221 52.6568C36.2753 49.3596 33.1435 45.1733 32.7276 40.635C32.275 36.2527 38.2211 36.1619 40.7539 36.5897C43.9108 37.163 46.2067 40.0025 47.9151 42.5401C51.7632 47.8805 54.3289 55.8821 54.5172 63.4926C48.5423 61.6026 43.3094 57.2542 39.1221 52.6568Z" fill="currentColor"/><path d="M75.1096 15.0312C74.0848 19.3973 73.3354 23.9923 73.4392 28.4577C73.5047 30.2821 76.0279 30.0497 76.1186 28.2613C76.2997 24.6849 77.2976 21.1349 78.2588 17.7408C80.2501 18.3708 82.3978 19.0372 84.3528 19.8231C85.8397 20.4997 87.9238 22.1382 89.7035 21.5672C90.5937 21.2818 90.7767 20.5022 90.6474 19.6495C90.3065 17.596 87.0302 16.8302 85.3872 16.1172C82.6885 14.993 80.073 14.2174 77.2645 13.561C76.3289 13.3423 75.3292 14.0956 75.1096 15.0312Z" fill="currentColor"/></svg>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Modal -->
  <div class="modal fade" id="staticWomanDialog" data-bs-backdrop="static" data-bs-keyboard="false" tabindex="-1" aria-labelledby="staticWomanDialogLabel" aria-hidden="true">
    <div class="modal-dialog modal-dialog-centered">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title" id="staticWomanDialogLabel">Glória dos Anjos Arnaldo</h5>
          <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
        </div>
        <div class="modal-body">
          <p>
            Lorem Ipsum is simply dummy text of the printing and typesetting industry.
            Lorem Ipsum has been the industry's standard dummy text ever since the 1500s,
            when an unknown printer took a galley of type and scrambled it to make a type specimen book.
            It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged.
            It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.
          </p>
        </div>
        <div class="modal-footer">
          <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Fechar</button>
        </div>
      </div>
    </div>
  </div>

</template>
