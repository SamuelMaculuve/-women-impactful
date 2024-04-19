<script setup>

</script>

<template>
  <div v-for="(item, index) in sortedItems" :key="index" class="item">
    <div class="col">
      <div class="card card-hover border-0 bg-transparent">
        <div class="position-relative">
          <img :src="item.photo" class="rounded-3" :alt="item.name">
          <div class="card-img-overlay d-flex flex-column align-items-center justify-content-center rounded-3">
            <span class="position-absolute top-0 start-0 w-100 h-100 bg-primary opacity-35 rounded-3"></span>
            <div class="position-relative d-flex zindex-2">
              <a :href="item.linkedin_link" target="_blank" class="btn btn-icon btn-secondary btn-linkedin btn-sm bg-white me-2" aria-label="LinkedIn">
                <i class="bx bxl-linkedin"></i>
              </a>
              <a href="#" class="btn btn-icon btn-secondary btn-linkedin btn-sm bg-white" aria-label="LinkedIn" data-bs-toggle="modal" :data-bs-target="'#staticWomanDialog' + index">
                <i class='bx bx-window-open' ></i>
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
      <div class="modal-dialog modal-dialog-centered modal-lg">
        <div class="modal-content bg-wtm">
          <div class="modal-header">
            <h5 class="modal-title text-white" id="staticWomanDialogLabel">{{ item.name }}</h5>
            <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
          </div>
          <div class="modal-body">
            <div class="text-center" v-if="!item.description">
               <img  :src="defaultImage" alt="Default Image" class="defaultImage"  />
                <p class="text-white"><b>Sem biografia</b></p>
            </div>
            <p class="text-white " v-else>{{ item.description }}</p>
          </div>

        </div>
      </div>
    </div>

  </div>

</template>
<script>
import suelyPereira from '@/assets/img/impactulwomen/suely-pereira.webp';
import sheilanhabanga from '@/assets/img/impactulwomen/sheila-nhabanga.webp';
import ceciliaTivir from '@/assets/img/impactulwomen/ceciliaTivir.webp';
import gloriaGovene from '@/assets/img/impactulwomen/gloriaGovene.webp';
import elisabethVeloso from '@/assets/img/impactulwomen/ElisabethVeloso.webp';
import aminaluciliajamal from '@/assets/img/impactulwomen/aminaluciliajamal.webp';
import margaridaMoga from '@/assets/img/impactulwomen/MargaridaMoga.webp';
import valquiriaBarros from '@/assets/img/impactulwomen/valquiriaBarros.webp';
import gabrielaPaul from '@/assets/img/impactulwomen/gabrielaPaul.webp';
import vanessaGoetsa from '@/assets/img/impactulwomen/vanessaGoetsa.webp';
import narcisiaCossa from '@/assets/img/impactulwomen/narcisiaCossa.webp';
import anchaPedro from '@/assets/img/impactulwomen/anchaPedro.webp';
import defaultImage from '@/assets/img/404/defaultImage.png';
export default {
  data() {
    return {
      defaultImage:defaultImage,
      items: [
        {
          name: 'Suely Pereira',
          role: 'Engenheira Informática',
          linkedin_link: '#',
          photo: suelyPereira,
          description: 'Suely Pereira é uma engenheira informática dedicada, com uma trajetória profissional que abrange mais de uma década na vanguarda das tecnologias, destacando-se nos últimos três anos em papéis de liderança.\n' +
              '\n' +
              'Sua jornada é alimentada pela crença firme de que a dedicação total é essencial para transcender qualquer desafio.\n' +
              '\n' +
              'Como líder, Suely cultiva um ambiente de trabalho onde o comprometimento e a colaboração são mais do que valorizados — são pilares essenciais para construir equipas de alto desempenho.\n' +
              '\n' +
              'Sua liderança não se resume à gestão de projectos, mas se estende ao desenvolvimento de talentos e à inspiração de uma cultura de excelência e inovação contínua na engenharia informática'
        },
        {
          name: 'Sheila Nhabanga',
          role: 'Gestora Estratégica de negócios',
          linkedin_link: 'http://linkedin.com/in/sheilanhabanga',
          photo: sheilanhabanga,
          description: 'Auto-motivada, apaixonada por impulsionar crescimento e criação de valor, e extremamente empenhada em entregar resultados com excelência.\n' +
              '\n' +
              'A mais recente formação é na área de gestão estratégica de negócios, sendo licenciada em engenharia informática e de telecomunicações, pós graduada em gestão de projectos, e certificada em gestão de produtos.\n' +
              '\n' +
              'Possui um sólido historial no desenvolvimento e execução de estratégias que produzem resultados tangíveis; através de identificação de oportunidades no âmbito corporativo, criação de equipas de alta-performance e promoção de ambientes de colaboração com vista a atingir objectivos organizacionais.'
        },
        {
          name: 'Cecilia Tivir',
          role: 'Senior Project Coordinator',
          linkedin_link: 'https://www.linkedin.com/in/ctivir',
          photo: ceciliaTivir,
          description: 'Apaixonada pela diversidade no sector tecnológico.\n' +
              'Co-fundadora da Associação Moçambicana Mulheres na Tecnologia. É co-organizadora do Django Girls e membro da PyLadies. Actualmente é pesquisadora na área de Inteligência Artificial e Educação com foco na Mineração de Dados Educacionais',
        },
        {
          name: 'Glória Govene',
          role: 'Specialist configuration engineer',
          linkedin_link: 'https://www.linkedin.com/in/gl%C3%B3ria-govene-41085620b/',
          photo: gloriaGovene,
          description: 'Glória, nascida com uma paixão pela tecnologia, iniciou sua jornada aos 15 anos, fascinada pelo desenvolvimento web, passando os tempos livres criando sites. Seu interesse pela programação a levou a participar do Django Girls pela primeira vez, um evento dedicado a mulheres na área de tecnologia, onde rapidamente se destacou e se tornou treinadora e posteriormente organizadora do evento.\n' +
              '\n' +
              'Com um desejo ardente de compartilhar conhecimento, Glória ingressou na Vodacom como treinadora do curso Code Like a Girl primeira edição, promovendo a inclusão de mulheres nas áreas de STEM (Ciência, Tecnologia, Engenharia e Matemática). \n' +
              '\n' +
              'Sua paixão por ensinar e sua habilidade em tecnologia chamaram a atenção, abrindo portas para sua entrada na Vodacom como estagiária no departamento de Negócios da Vodacom , com serviços de valor acrescentado. \n' +
              '\n' +
              'Seu compromisso com o avanço da tecnologia e sua dedicação em melhorar a vida das pessoas são evidentes em seus projetos na Vodacom, onde atualmente atua como engenheira especialista em configurações do M-Pesa.\n' +
              '\n' +
              'Sua jornada profissional inclui passagens pela Blueteki e pelo Reteiller, onde desenvolveu suas habilidades em desenvolvimento web, aplicações e gestão de redes sociais e teve a oportunidade de trabalhar em projetos desafiadores, aprimorando ainda mais suas habilidades técnicas e sua capacidade de resolver problemas.\n' +
              '\n' +
              'Determinada a continuar evoluindo e impactando positivamente o mundo através da tecnologia, Glória é uma fonte de inspiração para todos que a conhecem.',
        },
        {
          name: 'Elisabeth Veloso',
          role: 'Projects and IT Business Partner Supervisor',
          linkedin_link: 'https://www.linkedin.com/in/elisabeth-veloso-37a9911a/',
          photo: elisabethVeloso,
          description: 'Quem é Elisabeth Veloso? Elisabeth é uma profissional apaixonada e dedicada, com formação em Engenharia Informática e Telecomunicações, e um MBA em Gestão de Negócios. Nos momentos de lazer, ela busca aprender constantemente, gosta de estar a par sobre tecnologias , tem interesses por agricultura , adora ler, e participa também em projetos sociais na área de STEM que envolvem mulheres. Com 14 anos de experiência profissional, Elisabeth trabalhou em empresas estrangeiras e multinacionais, atuando em regiões da África e do Oriente Médio.\n' +
              '\n' +
              'Atualmente, ela é Líder está em Business Solutions (Business Partner, Projectos, End User), onde sua principal responsabilidade é garantir que a tecnologia desempenhe um papel estratégico no apoio à visão da empresa. Elisabeth liderou  vários projetos durante a sua carreia de implementação e roll out de sistemas de Tecnologia.',
        },
        {
          name: 'Amina Jamal',
          role: 'Electrical Reliability Engineer',
          linkedin_link: 'https://www.linkedin.com/in/aminaluciliajamal',
          photo: aminaluciliajamal,
          description: '',
        },
        {
          name: 'Margarida Antónia Mogas',
          role: 'Postpaid Billing Engineer',
          linkedin_link: 'https://www.linkedin.com/in/margarida-ant%C3%B3nia-mogas-7160b7170',
          photo: margaridaMoga,
          description: '',
        },
        {
          name: 'Valquíria Pondja',
          role: 'Code For Change Academy Founder',
          linkedin_link: 'https://www.linkedin.com/in/valqu%C3%ADria-pondja',
          photo: valquiriaBarros,
          description: 'Valquíria Pondja is a Computer Scientist, Social Activist, Women TechMakers Ambassador, Google Developers Group Organizer & Code For Change’s founder, an academy focused in teaching homeless children and involved in hazard condition jobs, programming skills (JS, CSS, Python, ML)\n' +
              'She fights for a world where more women can thrive in tech',
        },
        {
          name: 'Gabriela Paul',
          role: 'UX-UI Designer',
          linkedin_link: 'https://www.linkedin.com/in/gabrielapaulrl',
          photo: gabrielaPaul,
          description: 'Conheça Gabriela Paul, uma apaixonada UX-UI Designer Júnior, nascida no Brasil, criada em Moçambique e atualmente estudante de Design Global em Lisboa. Sua paixão por soluções sociais e tecnologia a impulsionou desde a infância. Como freelancer, busca constantemente novas oportunidades no campo das soluções sociais, com experiência em soluções urbanas e um foco contínuo na resolução de más experiências do usuário. Além disso, é uma entusiasta da fotografia e do design visual. Ela valoriza críticas construtivas mais do que elogios. Não perca a chance de ouvir sua experiência no evento!',
        },
        {
          name: 'Vanessa Goetsa',
          role: 'Web developer',
          linkedin_link: 'https://www.linkedin.com/in/vanessa-goetsa-6525821ba',
          photo: vanessaGoetsa,
          description: '',
        },
        {
          name: 'Narcísia Cossa',
          role: 'Flow catalyst na ideialab',
          linkedin_link: 'https://www.linkedin.com/in/narc%C3%ADsia-cossa-509140204/',
          photo: narcisiaCossa,
          description: 'Tem trabalhado com jovens no âmbito do empreendedorismo acerca de 4 anos  apoiando-os na jornada empreendedora facilitando conhecimento , ferramentas fundamentais para a criação e desenvolvimento de negócio\n' +
              'É uma das poucas mulheres moçambicanas com certificação em PI training (Treinamento focado em desenvolver habilidades das pessoas em tomar iniciativa ,assumir responsabilidades e agir de forma proactiva) \n' +
              'Foi gestora de programas de pré-incubação no Orange Corners tendo contribuído para formação de mais 8 mil empreendedores',
        },
        {
          name: 'Ancha Pedro',
          role: 'Frontend Developer',
          linkedin_link: 'https://www.linkedin.com/in/anchapedro/',
          photo: anchaPedro,
          description: '',
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
<style>
  .defaultImage{
    width: 50% !important;
  }
  .bg-wtm{
    background-color: rgb(79,143,241) !important;
    text-align: left;
  }
</style>