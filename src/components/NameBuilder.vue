<script>

export default{

    data: function(){
        return{
            name: "",
            vari: [
                {id: 1, name: "Bangladesh"},
                {id: 2, name: "India"},
                {id: 3, name: "Soudi"},
                {id: 4, name: "Pakistan"},
            ],
            cart:[],
            arr:[],
        }
    },
    methods:{
        addToCart(varientId){
            this.cart.push(this.vari.find(vari => vari.id === varientId))
        },
        removeToCart(varientId){
            let position = this.cart.findIndex(vari => vari.id === varientId)
            this.cart.splice(position, 1)
        },
        inputValueSS(){
            this.arr.push(this.name)
        }
    }
}
</script>

<template>

    <div class="container">
        <div class="row"> 
            <div class="col-4 mb-4 mt-4">
                <div class="card">
                    <div class="position1 card-body">
                        <h5 class="card-title text-center">Show Dynamic Country Name Usign For loop</h5>

                        <li :key="varient.id" v-for="varient in cart">
                            <span>{{ varient.name }}</span>
                        </li>
                    </div>
                    <span class="border"></span>
                    <p class="text-center">Total Items : {{ cart.length }}</p>
                </div>
            </div>
            
            <div class="col-4 mb-4 mt-4">
                <div class="card">
                    <div class="card-body">
                        <h5 class="text-center mb-4">Add Country Name</h5>
                        <div :key="varient.id" v-for="varient in vari">

                            <div class="position mb-2">
                                <a @click="addToCart(varient.id)" class="Button btn btn-primary px-4">+</a>
                                <a @click="removeToCart(varient.id)" class="Button btn btn-danger px-4">-</a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="col-4 mb-4 mt-4">
                <div class="card">
                    <div class="position1 card-body">
                        <h5 class="card-title text-center">Add Input Value</h5>

                        <input type="text" v-model="name" />
                        <button @click="inputValueSS()">CLick</button>
                        <div class="ListItem shadow-sm" :key="varient.index" v-for="varient in arr">
                            <p>{{ varient }}</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>


</template>

<style>
.Button{
    margin-right: 10px;
    font-size: 20px;
}
.position{
    display: flex;
    justify-content: center;
}
.position1{
    margin: auto;
}
.border{
    width: 100%;
    height: 2px;

}
.ListItem{
    background-color: rgb(226, 226, 226);
    color: black;
    padding: 1px 7px;
    margin-bottom: 5px;
    margin-top: 10px;
    text-align: center;
    
}
</style>