<script setup>
  defineProps({
    Data: String,
    ImageSrc: String,
    Name: String,
    Info: String,
    Genre: String,
    Time: String,
    Age: Number
  })
</script>
<template>
    <div class="meeting mb-8">
        <div class="posterDiv">
            <p class="goticFont font-bold text-5xl text-center w-26 day">{{ Data }}</p>
            <img :src="ImageSrc" alt="MeetingPhoto" class="meetingPhoto">
        </div>
    <div class="grid items-center">
        <div class="infoAboutNameMeeting gap-2">
            <p class="goticFont text-3xl font-bold">{{ Name }}</p>
            <p class="mb-6">{{ Info }}</p>
        </div>            
        <div class="littleInfoMeeting gap-12">
            <div class="littleInfo">
                <img src="/music.png" alt="Music">
                <p>{{ Genre }}</p>
            </div>                
            <div class="littleInfo">
                <img src="/time.png" alt="Time">
                <p>{{ Time }}</p>
            </div>                
            <div class="littleInfo">
                <img src="/age.png" alt="Age">
                <p>{{ Age }}+</p>
            </div>                
        </div>
    </div>
    <div class="grid items-center">
        <button class="orderBtn">Заказать билет</button>
    </div>
</div>
</template>