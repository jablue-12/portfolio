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
      @sliding-end="onSlideEnd">

      <template v-for="(project,index) in items">

        <b-carousel-slide
          :key="index"
          caption="First slide"
          text="Nulla vitae elit libero, a pharetra augue mollis interdum."
          img-src="https://picsum.photos/1024/480/?image=52">
          <Project :project="project"/>
        </b-carousel-slide>
        
      </template>

    </b-carousel>
  </div>
</template>

<script>
import Project from "@/components/Project.vue"
export default {
  name: "Portfolio",

  components: {Project},

  data(){
      return {
          items: [
            {
              title: "Flappy Bird", 
              description: "Implemented a flappy bird game clone using python/pygame with sqlite3...",
              img: "image1",
              video: "video1"  
            },
            {
              title: "Memory Game", 
              description: "impelemented a memory game usign vue",
              img: "image2",
              video: "video2"  
            },
            {
              title: "Food Ordering System", 
              description: "Implemented a flappy bird game clone using python/pygame with sqlite3...",
              img: "image3",
              video: "video3"  
            },
          ],
          // project: {
          //   title: "Flappy Bird", 
          //   description: "Implemented a flappy bird game clone using python/pygame with sqlite3...",
          //   img: "image1",
          //   video: "video1"  
          // },
      }
  }
};
</script>

<style scoped></style>
