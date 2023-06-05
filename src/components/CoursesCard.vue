<template>
  <div class="q-pa-md row items-start q-gutter-md">
    <q-card class="my-card">
      <img src="{{imageSrc}}" />

      <q-card-section>
        <div class="text-h6">{{ name }}</div>
      </q-card-section>

      <q-card-section class="q-pt-none">
        {{ desciption }}
      </q-card-section>
      <q-card-section>
        <div id="q-app" style="min-height: 100vh">
          <div class="q-pa-md">
            <q-rating
              :value="score"
              max="5"
              size="3.5em"
              color="yellow"
              icon="star_border"
              icon-selected="star"
              icon-half="star_half"
              no-dimming
            ></q-rating>
          </div>
        </div>
      </q-card-section>
      <q-card-section>
        <div>
          <q-avatar></q-avatar> <q-badge color="primary">v1.0.0+</q-badge>
        </div>
      </q-card-section>
    </q-card>
  </div>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "CoursesCard",
  props: {
    name: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      default: "",
    },
    score: {
      type: Number,
      default: 0,
    },
    duration: {
      type: String,
      default: "",
    },
    tag: {
      type: String,
      default: "",
    },
    imageSrc: {
      type: String,
      default: "",
    },
  },
});
</script>
