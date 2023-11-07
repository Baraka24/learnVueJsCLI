<template>
    <div>
        <form @submit.prevent="addItem">
            <p>Add item</p>
            <p>Item name: <input type="text" v-model="itemName" required></p>
            <p>How many: <input type="number" v-model="itemNumber"></p>
            <button type="submit">Add item</button>
        </form>
        <p>Shopping list</p>
        <ul>
            <li v-for="(item, index) in shoppingList" :key="index">
                {{ item.name }}, {{ item.number }}
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    data() {
        return {
            shoppingList: [],
            itemName: null,
            itemNumber: null
        }
    },
    methods: {
        addItem() {
            let item = {
                name: this.itemName,
                number: this.itemNumber
            }
            this.shoppingList.push(item);
            this.itemName = null; // Reset the item name input
            this.itemNumber = null; // Reset the item number input
        }
    }
}
</script>
