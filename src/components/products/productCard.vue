<template>
    <div class="card card-deck">
        <div class="card text-white bg-danger mb-3 " style="width: 30rem">
            <div class="center">
            <img class="card-img-top imgs p-3" style="align-items:center" :src="product.img" alt="Card image cap" />
            <div class="card-body">
                <h3 class="card-title">{{ product.name }}</h3>
                Price: ₱{{ product.price }}.00
                <br>
            </div>
            <div class="card-footer bg-dark">
                <button type="button" class="btn btn-dark text-white btn-outline-secondary" @click="$emit('viewProd', product)">View</button>
            </div>
            </div>
        </div>
    </div>
    
    
</template>

<script>
    export default {
        props: ['product'],
            // img() {
            //     return this.product.img;
            // }
    }
</script>

<style>
.imgs{
    height: 150px !important;
    width: 130px !important;
    align-items: center;
}
.center{
     display: flex;
    justify-content: center;
}
.card-deck{
    margin: 10px 10px ;
}
.card{
    padding:1px !important;
}

</style>