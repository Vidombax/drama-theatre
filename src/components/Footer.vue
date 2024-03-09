<template>
    <div class="footer text-white">
      <p class="goticFont mb-8 text-3xl">Сайт Концертно - экскурсионных программ</p>
      <div>
        <p class="goticFont text-3xl mb-4">Мероприятия</p>
        <div class="activityChoice">
          <p class="activity">Экскурсии</p>
          <p class="activity">Концерты</p>
          <p class="activity">Афиша</p>
        </div>
      </div>
      <div class="contacts">
        <p class="goticFont text-3xl mb-4">Контакты</p>
        <div class="flex gap-4 flex-col">
          <p class="activity">г. Санкт-Петербург, Невский пр., д. 1</p>
          <p class="activity">text@mail.ru</p>
          <p class="activity">(812) 123-45-67</p>
        </div>  
      </div>
    </div>
    <div class="line"></div>
    <p class="pravo">Все права принадлежат драмтеатру</p>
</template>

<style>
.footer {    
    display: grid;
    grid-template-columns: 42rem 24rem 24rem; 
    justify-content: center;
    align-items: center;  
    padding-top: 2rem;
  }
  .activityChoice {
    display: flex;
    gap: 2rem;
  }
  .contacts {
    display: flex;
    flex-direction: column;
    margin-top: 4.3rem;
  }
  .activity {
    font-size: small;
  }
  .line {
    border-bottom: solid 2px #ffffff3f;
    border-radius: 2px;
    margin-top: 4rem;
    width: 1500px;
    margin-left: 10rem;
  }
  .pravo {
    color: #ffffff3f;
    font-size: large;
    display: flex;
    justify-content: center;
    margin-top: 4rem;
  }
</style>