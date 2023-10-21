<script>

export default{

    data: function(){
        return{
            name: "",
            vari: [
                {id: 1, name: "Burger", price: 200},
                {id: 2, name: "Kacci", price: 300},
                {id: 3, name: "Pizza", price: 150},
                {id: 4, name: "Choocolate", price: 50},
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
        },

    },

    computed:{
        total(){
            return this.cart.reduce((taka, variant)=> taka + variant.price, 0)
        }
    },
    
}

</script>

<template>

    <div class="container">
        <div class="row"> 
            <h1 class="text-center my-4">Favourite Food Builder</h1>
            <div class="col-4 mb-4 mt-4">
                <div class="card">
                    <div class="position1 card-body">

                        <!-- Inline css -->
                        <h5 class="card-title text-center" :style="{color :'red'}">Show Dynamic Food Name Usign For loop</h5>

                        <li :key="varient.id" v-for="varient in cart">
                            <span>{{ varient.name }}</span>
                        </li>
                    </div>
                    <span class="border"></span>

                    <!-- conditional css -->
                    <p class="text-center" :style="cart.length == 0 ? {color: 'black'} : {color: 'red'}">Total Items : {{ cart.length }}</p>

                    <p class="text-center" :style="cart.length == 0 ? {color: 'black'} : {color: 'red'}">Total Price : {{ total }}</p>
                    

                    <!-- Button trigger modal -->
                    <button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#staticBackdrop">
                    Add To Cart
                    </button>

                    <!-- Modal -->
                    <div class="modal fade" id="staticBackdrop" data-bs-backdrop="static"       data-bs-keyboard="false" tabindex="-1" aria-labelledby="staticBackdropLabel" aria-hidden="true">
                        <div class="modal-dialog">
                            <div class="modal-content">
                                <div class="modal-header">
                                    <h1 class="modal-title fs-5" id="staticBackdropLabel">Order Your Favourite Food</h1>
                                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                                </div>
                                <div class="modal-body">
                                    <div class="mb-3">
                                        <label for="exampleInputEmail1" class="form-label">First Name</label>
                                        <input type="text" class="form-control" id="aaaaaaaaaaaaaaaaaaaa" aria-describedby="emailHelp">
                                        <div id="emailHelp" class="form-text">your name here.</div>
                                    </div>

                                    <div class="mb-3">
                                        <label for="exampleInputEmail1" class="form-label">Phone Number</label>
                                        <input type="text" class="form-control" id="bbbbbbbbbbbbbbbbbbbb" aria-describedby="emailHelp">
                                        <div id="emailHelp" class="form-text">your phone number.</div>
                                    </div>

                                    <div class="mb-3">
                                        <label for="exampleInputEmail1" class="form-label">Email address</label>
                                        <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp">
                                        <div id="emailHelp" class="form-text">We'll never share your email with anyone else.</div>
                                    </div>
                                </div>
                                <div class="modal-footer">
                                    <button type="button" class="btn btn-danger" data-bs-dismiss="modal">Cancel</button>
                                    <button type="button" class="btn btn-primary" data-bs-dismiss="modal">Order</button>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="col-4 mb-4 mt-4">
                <div class="card">
                    <div class="card-body">
                        <h5 class="text-center mb-4">Select Your Food</h5>
                        <div class="foodItems" :key="varient.id" v-for="varient in vari">
                            <div >
                                <p class="mt-3">{{ varient.name }}-{{ varient.price }}</p>
                            </div>
                            <div class="mb-2">
                                
                                <a @click="addToCart(varient.id)" class="Button btn btn-primary px-4">+</a>

                                <a @click="removeToCart(varient.id)" class="Button btn btn-danger px-4">-</a>

                            </div>
                        </div>
                    </div>
                </div>
                <router-link to="/">
                    <a class="Button btn btn-primary px-4 w-100 mt-2">Back To Home</a>           
                </router-link>
            </div>

            <div class="col-4 mb-4 mt-4">
                <div class="card">
                    <div class="position1 card-body">
                        <h5 class="card-title text-center">Add Input Value</h5>

                        <input type="text" v-model="name" />
                        <a @click="inputValueSS()" class="btn btn-primary">Click</a>
                        <div class="ListItem shadow-sm" :key="varient.index" v-for="varient in arr">
                            <p>{{ varient }}</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>


</template>


<!-- External css -->
<style>
.Button{
    margin-right: 10px;
    font-size: 20px;
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

li{
    list-style-type: none;
}

.foodItems{
    display: flex;
    justify-content: space-between;
}
</style>