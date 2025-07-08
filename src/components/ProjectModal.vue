<!-- <template>
    <div v-if="show" class="modal-overlay" @click.self="close">
      <div class="modal-content">
        <button class="close-btn" @click="close">X</button>
        <h3>{{ title }}</h3>
        <img :src="imgSrc" alt="" class="modal-img" />
        <p>{{ details }}</p>
      </div>
    </div>
  </template>
  
  <script setup>
  import { defineProps, defineEmits } from 'vue';
  
  const props = defineProps({
    show: Boolean,
    title: String,
    imgSrc: String,
    details: String
  });
  
  const emit = defineEmits(['close']);
  function close() {
    emit('close');
  }
  </script>
  
  <style scoped>
  .modal-overlay {
    position: fixed;
    top: 0; left: 0; right: 0; bottom: 0;
    background: rgba(0, 0, 0, 0.5);
    display: flex; justify-content: center; align-items: center;
    z-index: 1000;
  }
  .modal-content {
    background: #fff;
    border-radius: 10px;
    max-width: 500px;
    padding: 1.5rem;
    position: relative;
    text-align: center;
  }
  .close-btn {
    position: absolute;
    top: 10px; right: 10px;
    background: none;
    border: none;
    font-size: 1.2rem;
    cursor: pointer;
  }
  .modal-img {
    width: 100%;
    max-height: 200px;
    object-fit: contain;
    margin-bottom: 1rem;
  }
  </style>   -->