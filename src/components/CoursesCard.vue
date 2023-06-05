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
              v-model="model"
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
        <div>Feature <q-badge color="primary">v1.0.0+</q-badge></div>
      </q-card-section>
    </q-card>
  </div>
</template>

<script>
import { ref } from "vue";
import { defineComponent } from "vue";

export default defineComponent *
  {
    name: "CoursesCard",
    props: {
      card: {
        type: Object,
        required: True,
      },
    },
    setup() {
      return {
        model: ref(score),
      };
    },
  };
</script>
