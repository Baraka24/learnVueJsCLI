<template>
    <div>
        <!-- <center>
            <input v-model="checked" type="checkbox" name="check" />
            <label for="check">{{ checked }}</label>

            <p>Tutorials:{{ tutorials }}</p>
        </center> -->
        <input v-model="tutorials" type="checkbox" value="Data Structures" name="ds">
        <label for="ds">Data Structures</label>
        <input v-model="tutorials" type="checkbox" value="Algoritms" name="al">
        <label for="al">Algoritms</label>
        <input v-model="tutorials" type="checkbox" value="Machine Learning" name="ml">
        <label for="ml">Machine Learning</label>
    </div>
</template>

<script>
export default {
data() {
	return {
	checked: '',
	tutorials: [],
	}
},
}
</script>
