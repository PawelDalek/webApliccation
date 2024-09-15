<template>
  <v-container fluid class="container-class">
    <v-row justify="center">
      <v-col cols="12" sm="6" md="3" lg="2">
        <v-btn class="accountButton" block>
          Dane osobowe
        </v-btn>
      </v-col>
      <v-col cols="12" sm="6" md="3" lg="2">
        <v-btn class="accountButton" block>
          Moja firma
        </v-btn>
      </v-col>
      <v-col cols="12" sm="6" md="3" lg="2">
        <v-btn class="accountButton" block @click="navigateToActivepackage">
          Aktywny pakiet
        </v-btn>
      </v-col>
      <v-col cols="12" sm="6" md="3" lg="2">
        <v-btn class="accountButton" block>
          Statystyki
        </v-btn>
      </v-col>
    </v-row>
  </v-container>
</template>
<style scoped lang="scss">
.container-class {
  max-width: 100%;
  margin: 0 auto;
}

.accountButton {
  font-size: 1rem; /* Domyślna wielkość tekstu */
  border-radius: 8px;
  padding: 10px 15px; /* Wygodniejsze paddingi */
  transition: background-color 0.3s ease, color 0.3s ease;
  width: 100%; /* Przyciski rozciągają się na pełną szerokość */
  text-align: center; /* Wyśrodkowanie tekstu */
}

@media (max-width: 768px) {
  .accountButton {
    font-size: 0.9rem; /* Zmniejszanie tekstu na urządzeniach mobilnych */
  }
}
</style>