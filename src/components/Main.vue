<script setup>
    import miniPosters from './miniPosters.vue';
    import Meeting from './Meeting.vue';
</script>

<template>
    <div class="afishaPosters mt-20 mb-44">
      <img src="/poster.jpeg" alt="Poster" class="rounded-md poster">
      <miniPosters />
    </div>
    <div class="afisha">
        <div class="afishaInfo">
          <p class="afishaName text-5xl font-bold ml-1">Афиша</p>
          <div class="flex gap-4 items-center">
            <img src="/calendar.png" alt="Calendar">
            <p class="goticFont text-xl font-bold">Все мероприятия</p>
          </div>
        </div>
        <div class="allMeetings">
            <Meeting />
            <Meeting />
            <Meeting />
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
</style>