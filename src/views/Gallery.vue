<template>
    <div class="gallery-view">
      <h1>{{ title }}</h1>
      <div class="gallery">
        <div class="gallery-item" v-for="(image, index) in images" :key="index">
          <img :src="image.url" :alt="image.alt" />
        </div>
      </div>
    </div>
  </template>
  
  <script>
import MainFooter from '../components/MainFooter.vue';

export default {
  components: { MainFooter },
  data() {
    return {
      title: "Image Gallery",
      images: [
        { url: "https://lh5.googleusercontent.com/p/AF1QipM8UiBUhYFQsyyVhDUbzDjTBh6GV66nRTZyZ5at=s1941-k-no", alt: "Image 1" },
        { url: "https://lh5.googleusercontent.com/p/AF1QipNzZ78Eg9Vgi_-28rZD_Z-XjaPSO7o7Ux1dHpFs=s1455-k-no", alt: "Image 2" },
        { url: "https://lh5.googleusercontent.com/p/AF1QipP8mm_bUt1LVxzquyT6w3JHMI2cl1Mya8STQWiw=s1941-k-no", alt: "Image 3" },
        { url: "https://lh3.googleusercontent.com/p/AF1QipPrMmPi6RxOkINwTzadIjRoywaGzzDkIZs1lZma=s1360-w1360-h1020", alt: "Image 4" },
        { url: "https://lh3.googleusercontent.com/p/AF1QipOdMq4NUDN4lA38E2we8WNb-DLBIRggIwS7uJvF=s1360-w1360-h1020", alt: "Image 5" },
        { url: "https://lh3.googleusercontent.com/p/AF1QipM7rC9myfSv-UmZOE3ofNn0IvAPjyu1Nlvqb8PM=s1360-w1360-h1020", alt: "Image 6" },
        // Add more image links here
      ],
    };
  },
};
</script>

  <style scoped>
  .gallery-view {
    text-align: center;
    padding-top: 120px;
    padding-bottom: 100px;
    background-color: #ffff;
  }
  
  .gallery {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    justify-content: center;
  }
  
  .gallery-item {
    width: 500px; /* Set the desired width here */
    height: 500px; /* Set the desired height here */
    overflow: hidden;
  }
  
  .gallery-item img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
  </style>
  