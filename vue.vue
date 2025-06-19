<template>
  <div class="user-card">
    <!-- Именованный слот для аватара -->
    <slot name="avatar">
      <div class="default-avatar">
        👤
      </div>
    </slot>

    <!-- Основной контент -->
    <div class="user-info">
      <!-- Обязательный слот для имени -->
      <slot name="name"></slot>
      
      <!-- Необязательный слот для описания -->
      <slot name="description"></slot>
      
      <!-- Слот по умолчанию (для дополнительного контента) -->
      <slot></slot>
    </div>

    <!-- Слот для действий (кнопки и т.д.) -->
    <div class="actions">
      <slot name="actions"></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: 'UserCard'
}
</script>

<style scoped>
.user-card {
  border: 1px solid #ddd;
  border-radius: 8px;
  padding: 16px;
  max-width: 300px;
  margin: 10px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}
.default-avatar {
  font-size: 40px;
  text-align: center;
  margin-bottom: 10px;
}
.user-info {
  margin-bottom: 15px;
}
.actions {
  display: flex;
  gap: 8px;
}
</style>