<template>
  <div class="card-wrapper">
    <div v-for="service in services" :key="service.id" class="card">
      <!-- <img src="@/assets/generic/service-badge.png" alt="Service Badge" /> -->
      <h2>{{ service.name }}</h2>
      <img :src="getImageUrl(service.image)" alt="Service Image" />
      <p>{{ service.description }}</p>
    </div>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  data() {
    return {
      services: [],
    }
  },
  mounted() {
    this.fetchData()
  },
  methods: {
    async fetchData() {
      try {
        const response = await axios.get('https://api.mocki.io/v2/561baaaa')
        console.log('API Response:', response.data)
        this.services = response.data.services
      } catch (error) {
        console.error('Error fetching data:', error)
      }
    },
    getImageUrl(imagePath) {
      // Assuming the base URL is 'https://api.mocki.io/v2/561baaaa'
      const baseUrl = 'https://api.mocki.io/v2/561baaaa'
      return `${baseUrl}${imagePath}`
    },
  },
}
</script>

<style scoped>
.card-wrapper {
  max-width: 1089px;
  margin: 0 auto;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  gap: 30px;
  margin-top: 105px;
}
.card-wrapper > .card {
  max-width: 320px;
  text-align: center;
}

.card-wrapper > .card > img {
  max-width: 92px;
  height: auto;
}
.card-wrapper > .card > h2 {
  opacity: 1;
  color: #0e3757;
  font-size: 28px;
  font-weight: 400;
  letter-spacing: 0px;
  line-height: 42px;
  padding: 12px 0 10px 0;
  margin: 0;
}
.card-wrapper > .card > p {
  opacity: 1;
  color: #8d9ca8;
  font-size: 20px;
  font-weight: 400;
  letter-spacing: 0px;
  line-height: 30px;
  margin: 0;
}
@media only screen and (max-width: 630px) {
  .card-wrapper {
    flex-direction: column;
    padding: 0 15px;
    margin: 0;
  }
  .card-wrapper > .card {
    margin-top: 35px;
  }
  .card-wrapper > .card > h2 {
    font-size: 24px;
    padding: 10px 0;
    margin: 0;
  }
  .card-wrapper > .card > p {
    font-size: 18px;
    margin: 0;
  }
}
</style>
