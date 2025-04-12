<template>
  <div class="col-md-4 mb-4">
    <div class="card">
      <img :src="icon_url" alt="Chuck Norris" class="card-img-top">
      <div class="card-body">
        <p class="card-text">{{ value }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ChuckCard',
  props: {
    icon_url: {
      type: String,
      required: true
    },
    value: {
      type: String,
      required: true
    }
  }
}
</script>

<style scoped>
.card {
  border: 1px solid #ddd;
  border-radius: 8px;
}

.card-img-top {
  max-height: 200px;
  object-fit: cover;
  border-bottom: 1px solid #ddd;
}

.card-body {
  background-color: #f9f9f9;
}

.card-text {
  font-size: 1rem;
  color: #333;
}
</style>
