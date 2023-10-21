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
    }
},

computed:{
    total(){
        return this.cart.reduce((taka, variant)=> taka + variant.price, 0)
    }
}
}
</script>