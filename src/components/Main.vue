<script setup>
    import miniPosters from './miniPosters.vue';
    import Meeting from './Meeting.vue';
    import Post from './Post.vue';
    import Anouncement from ".//Anouncement.vue";
</script>

<template>
    <div class="afishaPosters mt-20 mb-44">
      <img src="/poster.jpeg" alt="Poster" class="rounded-md poster">
      <div class="miniPosters">
        <miniPosters Image="/operavsoperetta.jpeg" Name="Опера VS Оперетта"/>
        <miniPosters Image="/vivaldi.jpeg" Name="Антонио Вивальди. Времена года"/>
      </div>
    </div>
    <div class="afisha">
        <div class="afishaInfo">
          <p class="afishaName text-5xl font-bold ml-1">Афиша</p>
          <div class="flex gap-4 items-center">
            <img src="/calendar.png" alt="Calendar">
            <p class="goticFont text-xl font-bold"><a href="./">Все мероприятия</a></p>
          </div>
        </div>
        <div class="allMeetings">
            <Meeting Data="3 июня" ImageSrc="/poster.jpeg" Name="Антонио Вивальди. Времена года" Info="Посвящение Фрэнку Синатре." Genre="Джаз" Time="19:00" :Age="6" Price="350"/>
            <Meeting Data="30 июня" ImageSrc="/operavsoperetta.jpeg" Name="Опера VS Оперетта" Info="Санкт-Петербургский камерный оркестр Olympic Orchestra" Genre="Классика" Time="17:00" :Age="12" Price="450"/>
        </div>
    </div>
  <div class="flex justify-center flexNewsShedule mb-28">
    <div class="news_shedule items-center justify-center">
      <div>
        <p class="goticFont text-5xl font-bold mb-12">Новости</p>
        <div class="news">
          <Post Image="/news__image.png" NamePost="Переносы / Отмена мероприятий" AboutPost="11.04.2023 г. в 19.00 час. — концерт «Опера vs. Оперетта» - ПЕРЕНОС на 05.06.2023 г. в 19.00 час."/>
          <Post Image="/news__image-2.png" NamePost="Переносы / Отмена мероприятий" AboutPost="11.04.2023 г. в 19.00 час. — концерт «Антонио Вивальди. Времена года» - ОТМЕНЯЕТСЯ с 05.06.2023 г. в 19.00 час."/>
        </div>
      </div>
      <div class="calendar mt-24">
        <p style="background-image: url('/calendar__image.png'); background-repeat: no-repeat" class="goticFont text-white text-4xl font-bold pb-8 pt-48 pl-4">Обзорные экскурсии</p>
        <div class="shedule mt-4 pt-6 pb-6">
          <div class="chooseMontDiv">
            <p class="goticFont text-3xl font-bold text-black">Июль</p>
            <div>
              <button class="chooseMonthBtn"><</button>
              <button class="chooseMonthBtn">></button>
            </div>
          </div>
          <div class="month-shedule">
            <div class="week-shedule">
              <p class="day-shedule">1</p>
              <p class="day-shedule">2</p>
              <p class="day-shedule">3</p>
              <p class="day-shedule">4</p>
              <p class="day-shedule">5</p>
              <p class="day-shedule">6</p>
              <p class="day-shedule">7</p>
            </div>
            <div class="week-shedule">
              <p class="day-shedule">1</p>
              <p class="day-shedule">2</p>
              <p class="day-shedule">3</p>
              <p class="day-shedule">4</p>
              <p class="day-shedule">5</p>
              <p class="day-shedule">6</p>
              <p class="day-shedule">7</p>
            </div>
            <div class="week-shedule">
              <p class="day-shedule">1</p>
              <p class="day-shedule">2</p>
              <p class="day-shedule">3</p>
              <p class="day-shedule">4</p>
              <p class="day-shedule">5</p>
              <p class="day-shedule">6</p>
              <p class="day-shedule">7</p>
            </div>
            <div class="week-shedule">
              <p class="day-shedule">1</p>
              <p class="day-shedule">2</p>
              <p class="day-shedule">3</p>
              <p class="day-shedule">4</p>
              <p class="day-shedule">5</p>
              <p class="day-shedule">6</p>
              <p class="day-shedule">7</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="brieflyAnons">
    <div class="flex justify-between items-center mb-20">
      <p class="goticFont text-5xl font-bold text-black">Краткие анонсы</p>
      <div class="flex gap-4 items-center">
        <img src="/calendar.png" alt="Calendar">
        <p class="goticFont text-2xl font-bold"><a href="./">Все мероприятия</a></p>
      </div>
    </div>
    <div class="anouncement-items">
      <Anouncement data="3 июня" title="ВЕК ИМЕНИ СИНАТРА"/>
      <Anouncement data="4 июня" title="Санкт-Петербургский камерный оркестр Olympic Orchestra"/>
      <Anouncement data="6 июня" title="Спектакль День Радио"/>
      <Anouncement data="8 июня" title="ВЕК ИМЕНИ СИНАТРА"/>
    </div>
  </div>
</template>

<style>
.poster {
    width: 856px;
    height: 497px;
  }
  .miniAfisha {
    border-radius: 8px;
    gap: 24px;
    padding: 12px 16px 12px 16px;
    width: 416px;
    height: 104px;   
    background-color: rgba(25, 25, 25, 0.05); 
  }
  .miniAfishaImg {
    width: 80px;
    height: 80px;
    border-radius: 8px;
  }
  .afishaPosters {
    display: grid;
    grid-template-columns: 55rem 24rem;
    align-items: center;
    justify-content: center;
  }
  .afisha {
    display: grid;
    justify-content: center; 
  }
  .afishaInfo {
    display: grid;
    grid-template-columns: 68rem 14rem;
    margin-bottom: 8rem;
  }
  .miniPosters {
    display: grid;
    gap: 16px;
  }
  .allMeetings {
    display: flex;
    flex-direction: column;
  }
  .meeting {
    display: grid;
    grid-template-columns: 32rem 32rem 10rem;
    background-color: rgba(25, 25, 25, 0.05);
    border-radius: 16px;
    padding: 32px 60px 32px 60px;
    justify-content: space-between;
  }
  .meetingPhoto {
    width: 380px;
    height: 240px;
    border-radius: 8px;
  }
  .posterDiv {
    display: grid;
    grid-template-columns: 7rem 18rem;
    align-items: center;
    gap: 36px;
  }
  .infoAboutNameMeeting {
    display: grid;
    grid-template-columns: 24rem;
  }
  .littleInfoMeeting {
    display: grid;
    grid-template-columns: repeat(3, 4rem);
    align-items: center;
  }
  .afishaName {
    font-family: "Cormorant Garamond";
  }
  .littleInfo {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  .orderBtn {
    background-color: #05B093;
    border-radius: 24px;
    width: 175px;
    height: 51px;
    padding: 15px 30px 14px 30px;
    color: #FFF;
  }
  .day {
    color: #1b1b1bad;
  }
  .news_shedule {
    display: grid;
    grid-template-columns: 48rem 35rem;
    margin-left: 3rem;
  }
  .news {
    display: grid;
    grid-template-columns: 22rem 22rem;
  }
  .shedule {
    display: grid;
    grid-template-columns: 10.2rem 24rem;
    background-color: rgba(236, 236, 236, 0.49);
    width: 525px;
    position: relative;
    top: -1rem;
    border-bottom-right-radius: 12px;
    border-bottom-left-radius: 12px;
  }
  .month-shedule {
    display: grid;
  }
  .week-shedule {
    display: grid;
    grid-template-columns: repeat(7, 3rem);
  }
  .day-shedule {
    color: white;
    width: 38px;
    padding: 6px;
    margin: 8px;
    font-size: larger;
    border-radius: 4px;
    text-align: center;
    cursor: pointer;
  }
  .day-shedule:nth-child(odd) {
    background-color: rgba(25, 25, 25, 0.3);
  }
  .day-shedule:nth-child(even) {
    background-color: rgba(5, 176, 147, 1);
  }
  .chooseMonthBtn {
    color: white;
    width: 32px;
    height: 38px;
    padding: 2px;
    border-radius: 4px;
    text-align: center;
    background-color: rgba(5, 176, 147, 1);
  }
  .chooseMonthBtn:first-child {
    margin-right: 1rem;
  }
  .chooseMontDiv {
    display: flex;
    justify-content: center;
    gap: 8rem;
    flex-wrap: wrap;
  }
  .brieflyAnons {
    display: flex;
    flex-direction: column;
    align-items: stretch;
    flex-wrap: wrap;
    align-content: center;
    margin-bottom: 12rem;
  }
  .anouncement-items {
    display: grid;
    justify-content: center;
    grid-template-columns: repeat(4, 21rem);
    justify-items: center;
  }
</style>