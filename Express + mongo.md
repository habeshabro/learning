```js
const express = require('express')//import express
const app = express() //create an instance of express server
app.use(express.json()) //to make sure that the server can use json
app.listen(3000, () => {}) //initialize server and make it listen to port 3000
app.get('/', (req,res)=> {
	res.send("hello World")
})
```
```js
const mongoose = require('mongoose');
mongoose.connect('mongodb://127.0.0.1:27017/test')
  .then(() => {
    console.log('Connected!');
    app.listen(3000, () => {
        console.log("Listening on port 3000")
    })
})
.catch(() => {
    console.log("Connection failed");
})
```
in models create product.model.js
```js
const ProductSchema = mongoose.Schema(
    {
        name: {
            type: String,
            required: [true, "Plese enter product name"]
        },
        quantity: {
            type: Number,
            required: true,
            default: 0
        },
        price: {
            type: Number,
            required: true,
            default: 0
        },
        image: {
            type: String,
            required: false,
        }
    },
    {
        timestamps: true
    }
) 
const Product = mongoose.model("Product", ProductSchema) //products collection

module.exports = Product;
```

product.controller.js
```js
const Product = require('../models/product.model')
const getProduct = async (req, res) => {
    try {
        const { id } = req.params;
        const product = await Product.findById(id);
        res.status(200).json(product)
    }
    catch (error) {
        res.status(500).json({message: error.message})
    }
}

const updateProduct = async (req, res) => {
    try {
        const { id } = req.params;
        const product = await Product.findByIdAndUpdate(id, req.body);
        const updatedProduct = await Product.findById(id)
        res.status(200).json(updatedProduct)
    }
    catch (error) {
        res.status(500).json({message: error.message})
    }
}

const deleteProduct = async (req, res) => {
    try {
        const { id } = req.params;
        const product = await Product.findByIdAndDelete(id);
        res.status(200).json({message: "Product deleted"})
    }

    catch (error) {
        res.status(500).json({message: error.message})
    }
} 

module.exports = {
    getProduct,
    updateProduct,
    deleteProduct
}
```
product.route.js
```js
const express = require("express")
const router = express.Router();
const { getProduct, updateProduct, deleteProduct } = require('../controllers/product.controller')
router.get('/:id', getProduct)
router.put('/:id', updateProduct)
router.delete('/:id', deleteProduct)
module.exports = router
```

```js
const productRoute = require('./routes/product.route')
app.use('/api/product', productRoute)

app.post('/api/products', async (req, res) => {
    try {
        const product = await Product.create(req.body);
        res.status(200).json(product)
    }
    catch (error) {
        res.status(500).json({message: error.message})
    }
})
```