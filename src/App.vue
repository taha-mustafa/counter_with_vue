<template>
  <main>
      <div class="counter">
        <h1 class="main-header">The Number now is...</h1>
        <h1 class="count-header">{{ count }}</h1>
        <div class="buttons">
          <button @click="count--"><i class="fa-solid fa-minus"></i></button>
          <button @click="count++"><i class="fa-solid fa-plus"></i></button>
        </div>
      </div>
    </main>
</template>

<script setup>
import { ref } from 'vue'

const count = ref(0);
</script>

<style scoped>
  /* Start Styling The Count Area */
main {
  position: absolute;
  background-color: #c7ced4;
  width: 100vw;
  height: 100vh;
}
.counter {
  position: absolute;
  background-color: #bac6d0;
  width: 400px;
  height: 430px;
  transform: translate(-50%, -50%);
  top: 50%;
  left: 50%;
  border-radius: 10px;
  border: 2px solid #00ad9c;
  text-align: center;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  flex-direction: column;
  padding: 1rem;
  transition: 0.4s;
}
@media (min-width: 351px) and (max-width: 500px) {
  .counter {
    width: 300px;
    height: 330px;
    padding: 0.3rem;
  }
}
@media (max-width: 350px) {
  .counter {
    width: 235px;
    height: 330px;
    padding: 0.3rem;
  }
}
.counter:hover {
  border-color: #fff;
}
.counter .main-header {
  font-size: 33px;
  color: #00ad9c;
}
@media (max-width: 500px) {
  .counter .main-header {
    font-size: 22px;
  }
}
.counter .count-header {
  font-size: 4rem;
  color: #00ad9c;
}
@media (max-width: 500px) {
  .counter .count-header {
    font-size: 3rem;
  }
}
.buttons {
  display: flex;
  gap: 5rem;
  align-items: center;
}
@media (max-width: 500px) {
  .buttons {
    gap: 3rem;
  }
}
.buttons button {
  border: none;
  background-color: #00ad9c;
  color: #fff;
  border-radius: 50%;
  width: 50px;
  height: 50px;
  cursor: pointer;
}
@media (max-width: 500px) {
  .buttons button {
    width: 40px;
    height: 40px;
  }
}
.buttons button > i {
  font-size: 2rem;
}
@media (max-width: 500px) {
  .buttons button > i {
    font-size: 1.5rem;
  }
}
/* End Styling The Count Area */
</style>