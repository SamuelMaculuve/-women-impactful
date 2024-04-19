<script setup>

</script>

<template>
  <div v-for="(item, index) in sortedItems" :key="index" class="item">
    <div class="col">
      <div class="card card-hover border-0 bg-transparent">
        <div class="position-relative">
          <img :src="item.photo" class="rounded-3" alt="Ralph Edwards">
          <div class="card-img-overlay d-flex flex-column align-items-center justify-content-center rounded-3">
            <span class="position-absolute top-0 start-0 w-100 h-100 bg-primary opacity-35 rounded-3"></span>
            <div class="position-relative d-flex zindex-2">
              <a href="#" class="btn btn-icon btn-secondary btn-linkedin btn-sm bg-white me-2" aria-label="LinkedIn">
                <i class="bx bxl-linkedin"></i>
              </a>
              <a href="#" class="btn btn-icon btn-secondary btn-linkedin btn-sm bg-white" aria-label="LinkedIn" data-bs-toggle="modal" :data-bs-target="'#staticWomanDialog' + index">
                <i class='bx bxs-door-open'></i>
              </a>
            </div>
          </div>
        </div>
        <div class="card-body text-center p-3">
          <h3 class="fs-lg fw-semibold pt-1 mb-2">{{ item.name }}</h3>
          <p class="fs-sm mb-0">{{ item.role }}</p>
        </div>
      </div>
    </div>

    <!-- Modal -->
    <div class="modal fade" :id="'staticWomanDialog' + index" data-bs-backdrop="static" data-bs-keyboard="false" tabindex="-1" aria-labelledby="staticWomanDialogLabel" aria-hidden="true">
      <div class="modal-dialog modal-dialog-centered">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title" id="staticWomanDialogLabel">{{ item.name }}</h5>
            <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
          </div>
          <div class="modal-body">
            <p>{{ item.description }}</p>
          </div>
          <div class="modal-footer">
            <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Fechar</button>
          </div>
        </div>
      </div>
    </div>

  </div>

</template>
<script>
export default {
  data() {
    return {
      items: [
        {
          name: 'Suely Pereira',
          role: 'Engenheira Informática',
          linkedin_link: '#',
          photo: 'src/assets/img/impactulwomen/suely-pereira.webp',
          description: 'Suely Pereira é uma engenheira informática dedicada, com uma trajetória profissional que abrange mais de uma década na vanguarda das tecnologias, destacando-se nos últimos três anos em papéis de liderança.\n' +
              '\n' +
              'Sua jornada é alimentada pela crença firme de que a dedicação total é essencial para transcender qualquer desafio.\n' +
              '\n' +
              'Como líder, Suely cultiva um ambiente de trabalho onde o comprometimento e a colaboração são mais do que valorizados — são pilares essenciais para construir equipas de alto desempenho.\n' +
              '\n' +
              'Sua liderança não se resume à gestão de projectos, mas se estende ao desenvolvimento de talentos e à inspiração de uma cultura de excelência e inovação contínua na engenharia informática'
        },
        {
          name: 'Andre Doe',
          role: 'Designer',
          linkedin_link: 'Developer',
          photo: 'src/assets/img/impactulwomen/24.jpg',
          description: 'Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.'
        },
      ]
    };
  },
  computed: {
    sortedItems() {
      // Use slice() to create a copy of the original array
      return this.items.slice().sort((a, b) => {
        // Compare item names alphabetically
        return a.name.localeCompare(b.name);
      });
    }
  }
};
</script>