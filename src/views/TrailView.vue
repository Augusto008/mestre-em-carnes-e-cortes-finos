<template>
  <div class="trail pb-5">
    <div class="row justify-content-center my-4">
      <div class="col-auto">
        <select name="lesson" id="lesson" class="form-select" v-model="selectedLesson">
          <option v-for="(lessonItem, index) in lessonList" v-bind:key="index" :value="lessonItem[0]">
            {{ lessonItem[1] }}
          </option>
        </select>
      </div>
    </div>
    <component v-bind:is="selectedLesson"></component>
    <div class="d-flex justify-content-end">
      <button id="backStart" class="btn btn-light rounded-circle mt-5" @click="backToStart">
        <img src="..\assets\arrow-narrow-top-alignment-svgrepo-com.svg" alt="return to top" width="40px;">
      </button>
    </div>
  </div>
</template>

<style lang="scss">
  #backStart {
    position: fixed;
    bottom: 20px;
    right: 20px;
  }
</style>

<script>
  import LessonIntro from "@/components/lessons/LessonIntro.vue";
  import Lesson1 from "@/components/lessons/Lesson1.vue";
  import Lesson2 from "@/components/lessons/Lesson2.vue";
  import Lesson3 from "@/components/lessons/Lesson3.vue";
  import Lesson4 from "@/components/lessons/Lesson4.vue";
  import Lesson5 from "@/components/lessons/Lesson5.vue";
  import Lesson6 from "@/components/lessons/Lesson6.vue";
  import Lesson7 from "@/components/lessons/Lesson7.vue";
  import Lesson8 from "@/components/lessons/Lesson8.vue";
  import Lesson9 from "@/components/lessons/Lesson9.vue";
  import Lesson10 from "@/components/lessons/Lesson10.vue";
  import Lesson11 from "@/components/lessons/Lesson11.vue";
  import Lesson12 from "@/components/lessons/Lesson12.vue";

  export default {
    name: "Trail",
    components: {
      LessonIntro,
      Lesson1,
      Lesson2,
      Lesson3,
      Lesson4,
      Lesson5,
      Lesson6,
      Lesson7,
      Lesson8,
      Lesson9,
      Lesson10,
      Lesson11,
      Lesson12,
    },
    data() {
      return {
        lessonList: [
          ["LessonIntro", "Introdução"],
          ["Lesson1", "Lição 1"],
          ["Lesson2", "Lição 2"],
          ["Lesson3", "Lição 3"],
          ["Lesson4", "Lição 4"],
          ["Lesson5", "Lição 5"],
          ["Lesson6", "Lição 6"],
          ["Lesson7", "Lição 7"],
          ["Lesson8", "Lição 8"],
          ["Lesson9", "Lição 9"],
          ["Lesson10", "Lição 10"],
          ["Lesson11", "Lição 11"],
          ["Lesson12", "Lição 12"],
        ],
        selectedLesson: "LessonIntro"
      }
    },
    computed: {
      actualComponent() {
        return this.SelectedLesson
      }
    },
    methods: {
      backToStart() {
        document.body.scrollTop = 0; // For Safari
        document.documentElement.scrollTop = 0; // For Chrome, Firefox, IE and Opera
      }
    }
  }
</script>