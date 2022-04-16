<template>
    <div>
    <b-carousel
      v-model="slide"
      :interval="4000"
      controls
      indicators
      background="#ababab"
      img-width="1024"
      img-height="480"
      style="text-shadow: 1px 1px 2px #333;"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
      <!-- Text slides with image -->
      <b-carousel-slide
        caption="First slide"
        text="Nulla vitae elit libero, a pharetra augue mollis interdum."
        img-src="https://picsum.photos/1024/480/?image=52"
      >
        <b-card bg-variant="primary">test</b-card>
      </b-carousel-slide>

      <!-- Slides with custom text -->
      <b-carousel-slide img-src="https://picsum.photos/1024/480/?image=54">
        <h1>Hello world!</h1>
      </b-carousel-slide>


    </b-carousel>
  </div>
</template>

<script>
export default {
  name: "Portfolio",
  data(){
      return {
          fields: [
              {key: "name", label: "Name", sortable: true},
              {key: "age", label: "Age", sortable: true},
          ],
          items: [
              {"name": "Jareed", "age":22},
              {"name": "Jablue", "age":25},
              {"name": "Tesst", "age":22},
              {"name": "Fruit Punch", "age":18},
              {"name": "Linux User", "age":27},
          ]
      }
  }
};
</script>

<style scoped></style>
