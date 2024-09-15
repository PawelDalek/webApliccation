<template>
  <aside>
    <div class="logo">
      <span class="material-icons user-icon">account_circle</span>
      <span class="username">Jan Kowalski</span>
    </div>
    <div class="buttonMenu">
      <v-btn class="sidebarButton" small>
        <span class="material-icons">home</span>
        Panel główny
      </v-btn>
      <v-btn class="sidebarButton" small>
        <span class="material-icons">devices</span>
        Urządzenia
      </v-btn>
      <v-btn class="sidebarButton" text small @click="goToActivePackage">
        <span class="material-icons">message</span>
        Wiadomości
      </v-btn>
      <v-btn class="sidebarButton" small>
        <span class="material-icons">people</span>
        Przyjaciele
      </v-btn>
      <v-btn class="sidebarButton" small>
        <span class="material-icons">calendar_today</span>
        Kalendarz
      </v-btn>
    </div>
  </aside>
</template>

<script setup>
import { ref } from 'vue'
</script>

<style lang="scss" scoped>
aside {
  display: flex;
  flex-direction: column;
  width: 25%; /* Szerokość paska bocznego */
  min-height: 100vh;
  padding: 1rem;
  background-color: var(--blue);
  color: var(--light);

  .logo {
    display: flex;
    align-items: center; /* Wyrównuje ikonę i tekst w jednej linii */
    margin-bottom: 2rem; /* Większy odstęp między sekcją użytkownika a menu */
  
    .user-icon {
      font-size: 36px; /* Powiększa ikonę użytkownika */
      margin-right: 12px; /* Większy odstęp między ikoną a tekstem */
    }

    .username {
      font-size: 1.2rem; /* Powiększa tekst użytkownika */
    }
  }

  .buttonMenu {
    margin-top: 10%;
    display: flex;
    flex-direction: column; /* Ustawienie przycisków jeden pod drugim */
    justify-content: flex-start;
    align-items: stretch; /* Przyciski na pełną szerokość */

    .sidebarButton {
      margin-bottom: 1rem; /* Dodatkowy odstęp między przyciskami */
      display: flex;
      align-items: center; /* Wyrównuje ikonę i tekst w jednej linii */
      width: flex; /* Przyciski na pełną szerokość */
      justify-content: flex-start; /* Ustawienie tekstu obok ikony */
      text-align: left; /* Tekst wyrównany do lewej */
      padding: 8px 16px; /* Padding dostosowany do przycisków */
    }

    @media (max-width: 768px) {
      position: fixed;
      z-index: 99;
      width: 100%; /* Pełna szerokość na małych ekranach */
    }
  }

  .sidebarButton {
    .material-icons {
      font-size: 24px; /* Wielkość ikony */
      margin-right: 12px; /* Większy odstęp między ikoną a tekstem */
    }
    font-size: 1rem;
    border-radius: 5px;
    padding: 6px 12px; /* Padding wewnętrzny przycisków */
    display: flex;
    align-items: center; /* Wyrównuje ikonę i tekst w jednej linii */
    justify-content: flex-start; /* Ustawienie tekstu obok ikony */
  }
}
</style>