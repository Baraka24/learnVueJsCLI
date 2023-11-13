<template>
    <h1>My select</h1>
    Programming language : {{ language }} <br>
    <select v-model="language" multiple>
        <option value="Java">Java</option>
        <option value="C++">C++</option>
        <option value="Python">Python</option>
        <option value="Javascript">Javascript</option>
    </select>
</template>

<script>
export default {
  data() {
    return {
      category: '',
      language: '',
    }
  },
}
</script>
