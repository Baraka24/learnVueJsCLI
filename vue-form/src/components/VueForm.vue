<template>
    <div>
        <form v-on:submit.prevent="addItem">
            <p>Add item</p>
            <p>Item name: <input type="text" required></p>
            <p>How many: <input type="number"></p>
            <button type="submit">Add item</button>
        </form>
        <p>Shopping list</p>
        <ul v-for="item in shoppingList" v-bind:key="item">
            <li>{{ item.name }}, {{ item.number }}</li>
        </ul>
    </div>
</template>

<script>
export default {
    data() {
        return {
            shoppingList : []
        }
    },
    methods: {
        addItem() {
            let item = {
                name: this.itemName,
                Number: this.itemNumber
            }
            this.shoppingList.push(item);
            /* this.itemName = null
            this.itemNumber = null */
        }
    }
}
</script>
