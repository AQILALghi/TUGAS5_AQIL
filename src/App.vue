<template>
  <div>
    <Navbar />
    <div class="container mt-4">
      <Carousel />
      <div class="card-container mt-4">
        <Card 
          v-for="product in products" 
          :key="product.id" 
          :title="product.name" 
          :description="product.description" 
          :url="product.url" 
        />
      </div>
    </div>
    <Footer />
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue';
import Carousel from './components/Carousel.vue';
import Card from './components/Card.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Navbar,
    Carousel,
    Card,
    Footer
  },
  data() {
    return {
      products: [
        { 
          id: 1, 
          name: 'Product1', 
          description: '52.000.000.', 
          url: 'https://wallpapercave.com/wp/AjbRDTn.jpg' 
        },
        { 
          id: 2, 
          name: 'Product2', 
          description: '60.000.000.', 
          url: 'https://wallpapercave.com/wp/wp3787846.jpg' 
        },
        { 
          id: 3, 
          name: 'Product3', 
          description: '70.000.000', 
          url: 'https://wallpapercave.com/wp/wp3787739.jpg' 
        },
        { 
          id: 4, 
          name: 'Product 4', 
          description: '65.000.000', 
          url: 'https://wallpapercave.com/wp/wp3787739.jpg' 
        },
        { 
          id: 5, 
          name: 'Product 5', 
          description: '40.000.000', 
          url: 'https://wallpapercave.com/wp/wp1941206.jpg' 
        },
        { 
          id: 6, 
          name: 'Product 6', 
          description: '35.000.000', 
          url: 'https://wallpapercave.com/wp/wp1941216.jpg' 
        }
      ]
    };
  }
};
</script>

<style>
body {
  background-color: rgb(239, 234, 234);
}

.card-container {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 16px; /* Optional: Adjust the space between cards */
}

.card {
  flex-basis: calc(33.33% - 16px); /* Atur lebar kartu dengan ketiga bagian dari wadah dikurangi jarak antar kartu */
}
</style>
