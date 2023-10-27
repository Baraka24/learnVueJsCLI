<template>
<div class="danger">
    <h2>Learning Vue JS is funny</h2>
    <h1>{{ header }}</h1>
    <p><strong>Success!</strong> {{ text }}.</p>
    <slot></slot>
    <div class="actions">
      <slot name="links"></slot>
    </div>
</div>
</template>

<style>
.danger {
  background-color: #0e871e;
  border-left: 6px solid #343333;
}

</style>
<script>
export default {
    props: ['header', 'text', 'theme']
}
</script>