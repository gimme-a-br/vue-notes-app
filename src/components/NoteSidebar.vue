<template>
  <div class="note-selectors">
    <NoteSelector/>
    <NoteSelector/>
    <NoteSelector/>
  </div>
</template>

<script>
import NoteSelector from "./NoteSelector";

export default {
  components: {
    NoteSelector,
  },
};
</script>
