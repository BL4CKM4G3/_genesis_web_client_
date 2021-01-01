<template>
  <section>
    <button
      :class="'nes-btn ' + color"
      @click="document.getElementById(`dialog-${name}`).showModal()"
    >
      {{ name }}
    </button>
    <dialog :class="'nes-dialog ' + color" :id="`dialog-${name}`">
      <p :class="'title ' + title.color">{{ title.text }}</p>
      <form method="dialog">
        <button
          v-for="action in actions"
          :key="action.id"
          type="button"
          :class="'nes-btn ' + action.color"
        >
          {{ action.text }}
        </button>
      </form>
    </dialog>
  </section>
</template>

<script>
export default {
  props: {
    name: String,
    color: String,
    actions: Array,
    title: Object,
    subtitle: String,
  },
  methods: {
    setAction(action) {
      return action.method();
    },
  },
};
</script>

<style>
</style>