<template>
 <div class="products_display" ref="container" @scroll="handleScroll">
    <div  v-for="item in productsList" :key="item.id">
        <div class="card">
            <img class="card-image" :src="item.image"/>
            <div class="card-body">
                <div class="card_name"> {{ item.name }}</div>
                <div class="card_price"> Rs. {{ item.price }}</div>
            </div>
        </div>
    </div>
 </div>
</template>

<script>
import axios from 'axios';

export default {
    name: 'ListofProducts',
    // productsList: null,
    data() {
        return {
            productsList: null,
        }
    },

   created(){
    axios.get('https://pim.wforwoman.com/pim/pimresponse.php/?service=category&store=1&url_key=top-wear-kurtas&page=1&count=20&sort_by=&sort_dir=desc&filter=').
    then(resp => {
        this.productsList = resp.data.result.products
        console.log("the response of API is", this.productsList)
    })
   },

   methods: {
    handleScroll() {
    //   const container = this.$refs.container;
    //   if (container.scrollHeight - container.scrollTop === container.offsetHeight) {
        this.loadMore();
    //   }
    },

    loadMore(){
        this.loading = true
        axios.get('https://pim.wforwoman.com/pim/pimresponse.php/?service=category&store=1&url_key=top-wear-kurtas&page=1&count=20&sort_by=&sort_dir=desc&filter=').
    then(resp => {
        this.productsList.push(resp.data.result.products)
    })
        this.loading = false
    }
    }



}
</script>

<style scoped>
 .products_display {
    height: 100vh-80px;
    display: inline-flex;
    flex-direction: row;
    position: relative;
    flex-wrap: wrap;
    margin-left: 30px;
    /* width: auto;
    height: auto; */
 }

 .products_display div {
    margin-left: 7px;
    margin-right: 7px;
    margin-bottom: 40px;
 }

 .card {
    height: 450px;
    width: 280px;
    /* margin: 20px; */
 }

 .card-image {
    height: 400px;
    width: 280px;
 }

 .card-body {
    display: flex;
    justify-content: flex-start;
    align-items: flex-start;
    flex-direction: column;
    flex-wrap: wrap;
    padding: 0px;
    margin: 0px;
 }

 .card-body  .card_name {
    margin-top: 10px;
    margin-bottom: 0px;
    justify-content: flex-start;
    align-items: flex-start;
 }

 .card-body .card_price {
    margin-top: 10px;
    justify-content: flex-start;
    align-items: flex-start;
 }

</style>