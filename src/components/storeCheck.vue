<template>
    <div>
        <div class="itemCard">
            <div class="items" v-for="item in jeanLists" :key="item.id">
                <img :src="item.image" class="image-top">
                <div class="text-incard">
                    <p>{{ item.name }}</p>
                    <span> {{ item.price }}</span>
                    <button class="fas fa-cart-plus" @click="onSelect(item)"></button>
                    <button class="fas fa-trash-can" @click="deleteItem(item.index)"></button>
                </div>
            </div>
        </div>

        <p> สินค้าในตะกร้า {{ showNameOfProduct }} </p>
        <p> total price{{ checkPrice }} bath</p>
        <p>จำนวน {{ numberOfProduct }} </p>



    </div>
</template>

<script>
import jeans from "../assets/jeans"
export default {
    data() {
        return {
            jeanLists: jeans,
            cartItems: []
        }
    },
    methods: {
        onSelect(item) { 
            console.log(this.cartItems)
            let index = undefined 
            this.cartItems.forEach((el, count) => {
                if (el.id === item.id) {
                    
                    index = count
                }
            }) 
            if (index === undefined) {
                this.cartItems.push({ 
                    ...item,
                    amount: 1, 
                })
            }
            else {
                this.cartItems[index].amount++ 
            }
        },
        deleteItem(index) {
            this.cartItems.splice(index, 1)
        }
    },
    computed: {
        showNameOfProduct() {
            let product = " ";
            this.cartItems.forEach((item) => {
                product += item.name;
            })
            return product;
        },
        checkPrice() {
            let total = 0;
            this.cartItems.forEach((item) => {
                total += item.price * item.amount;
            });
            console.log(total)
            return total;
        },
        numberOfProduct() {
            let count = 0;
            this.cartItems.forEach((item) => {
                count++
            })
            return count;
        }

    }
}
</script>

<style lang="scss" scoped>

</style>