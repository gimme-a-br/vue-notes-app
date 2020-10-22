<template>
  <div class="note-selector" v-bind:class="{active: note.id === selectedNoteId}" v-on:click="selectNote()">
    <p class="note-selector-title">{{ note.body }}</p>
    <p class="note-selector-timestamp">{{ note.timestamp }}</p>
  </div>
</template>

<script>
export default {
  props: ["note", "selectedNoteId"],
  methods: {
    selectNote: function () {
      console.log("This note is selected", this.note.body);
      // this.selectedNoteId = this.note.id;
      this.$emit("selectNote", this.note);
    },
  },
};
</script>
