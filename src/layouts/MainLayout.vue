<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated class="bg-white" no-caps>
      <q-toolbar>
        <q-avatar>
          <img src="https://cdn.quasar.dev/logo-v2/svg/logo-mono-black.svg" />
        </q-avatar>
        <q-toolbar-title> Quasar Courses </q-toolbar-title>

        <q-tabs v-model="tab" class="absolute-center text-primary">
          <q-tab name="Available" label="Available Courses" />
          <q-tab name="Education" label="Continuing Education" />
          <q-tab name="Courses" label="My Courses" />
          <q-tab name="Community" label="Community" />
        </q-tabs>
        <q-btn color="accent" text-color="white" label="Register or Login" />
      </q-toolbar>
    </q-header>
    <q-footer elevated>
      <q-toolbar>
        <q-tabs v-model="tab" class="absolute-center text-white" no-caps>
          <label>© 2021 NCoding®</label>
          <q-tab name="Information" label="Regularoty Information" />
          <q-tab name="Terms" label="Terms of Use & Privacy Policy" />
          <q-tab name="Careers" label="Careers" />
        </q-tabs>
      </q-toolbar>
    </q-footer>
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from "vue";
export default defineComponent({
  name: "MainLayout",

  components: {},

  setup() {},
});
</script>
