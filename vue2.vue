<template>
  <div class="app">
    <h1>Пользователи</h1>
    
    <!-- Простое использование -->
    <UserCard>
      <template #name>
        <h2>Иван Иванов</h2>
      </template>
      <template #description>
        <p>Frontend разработчик</p>
      </template>
    </UserCard>

    <!-- Использование с кастомным аватаром и кнопками -->
    <UserCard>
      <template #avatar>
        <img 
          src="https://randomuser.me/api/portraits/women/44.jpg" 
          alt="Аватар"
          class="custom-avatar"
        >
      </template>
      
      <template #name>
        <h2>Мария Петрова</h2>
      </template>
      
      <template #description>
        <p>UI/UX дизайнер с 5-летним опытом</p>
      </template>
      
      <p>Люблю Vue.js и кофе ☕</p>
      
      <template #actions>
        <button @click="sendMessage">Написать</button>
        <button @click="viewProfile">Профиль</button>
      </template>
    </UserCard>
  </div>
</template>

<script setup>
import UserCard from './components/UserCard.vue'

const sendMessage = () => alert('Сообщение отправлено!')
const viewProfile = () => alert('Переход в профиль')
</script>

<style>
.app {
  font-family: Arial, sans-serif;
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
}
.custom-avatar {
  width: 60px;
  height: 60px;
  border-radius: 50%;
  display: block;
  margin: 0 auto 10px;
}
button {
  padding: 6px 12px;
  background: #42b983;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}
button:hover {
  background: #3aa876;
}
</style>