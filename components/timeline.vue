<template>

  <v-timeline   align-top
    :dense="$vuetify.breakpoint.smAndDown">
    <v-timeline-item
      v-for="(year, i) in years"
      :key="i"
      :color="year.color"
      small
    >
      <template>
        <span
          :class="`headline font-weight-bold ${year.color}--text`"
          v-text="year.year"
        ></span>
      </template>
      <v-col>
        <v-row justify="center" align="center" class="py-4">
          <h2 :class="` font-weight-bold mb-4 ${year.color}--text`">
            {{ year.text }}
          </h2>
          <v-row justify="center" align="center" class="btn-class">
            {{ year.about }}
            <v-btn
              :color="`${year.color}`"
              outlined
              class="button-style ma-3"
              :href="year.path"
              >Visit Website</v-btn
            >
          </v-row>
        </v-row>
      </v-col>
    </v-timeline-item>
  </v-timeline>
</template>
 
<script>
export default {
  data: () => ({
    years: [
      {
        text: "Capgemini",
        color: "amber",
        path: "https://www.capgemini.com/br-pt/",
        year: "2019 - até o momento",
        about:
          "Atuo no Projeto do Bradesco, como desenvolvedor, um dos projetos de grande importância para o Bradesco o PIX (Pagamento Instântaneo), desenvolvendo na linguagem Java, Node, Angular, HTML e CSS3.",
      },
      {
        text: "Grupo Géia",
        color: "green",
        path: "https://www.geia.com.br/",
        year: "2018",
        about:
          "Trabalhei no departamento de TI da empresa, onde atuava com desenvolvimento, com melhorias contínuas do site interno da empresa, quanto a questão interna, com a plataforma direta que o cliente utilizava.",
      },

      {
        text: "Bureau Translations",
        color: "purple",
        path: "https://www.bureauworks.com/",
        year: "2018",
        about:
          "Atuava na área de TI da empresa, realizando manutenções do site da empresa e melhorias contínuas em Java, HTML, CSS e JavaScript",
      },
      {
        text: "Quimicryl S/A",
        color: "deep-orange",
        path: "http://quimicryl.com.br/",
        year: "2018",
        about:
          "Auxiliar de Produção, auxiliava nas demandas da empresa para a produção de impermeabilizante na áea da construção civil",
      },
    ],
  }),
};
</script>
<style scoped>
.btn-class {
  display: flex;
  flex-direction: column;
}
.button-style {
  width: 200px;
}
</style>