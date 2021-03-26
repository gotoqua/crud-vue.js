<template>
    <div class="bg-light">
        <div class="sticky-top">
            <nav class="navbar navbar-dark bg-info">
                <span class="navbar-brand mb-0 h1">Produtos e Marcas</span>
            </nav>        
        </div>
        <br>
        
        <div class="container">
            <div class="row bg-ligth">
                <form class="col">
                    <div class="form-todo form-group">                                    
                        <h4>Insira as informações do Produto</h4>                       
                        <p>
                            <label>Marca:</label>
                            <input id="input-brand" v-model="brand" type="text" required class="form-control" >
                        </p>                    
                        <p>
                            <label>Modelo:</label>
                            <input id="input-model" v-model="model" type="text" required class="form-control" >
                        </p>
                        <p>
                            <label>Tipo:</label>
                            <input id="input-type" v-model="type" type="text" required class="form-control" >
                        </p>
                        <p>
                            <label>Preço:</label>
                            <input id="input-price" v-model="price" type="text" required class="form-control" >
                        </p>            
                        <p>
                        <label>Descrições do produto:</label>
                        <textarea id="input-description" v-model="description" name="" class="form-control" ></textarea>
                        </p>
                        <div class="btn-group">
                            <button v-on:click="addProduct" type="submit" class="btn btn-success">Salvar</button>                            
                        </div>
                    </div>
                </form>
            </div>
            <hr>
            <h4>Itens Salvos</h4>
            <div class="list-group" v-for="(product, index) in products" v-bind:key="index">
                <table class="table table-secondary">
                <thead>
                    <tr>
                        <th scope="col">Marca</th>
                        <th scope="col">Modelo</th>
                        <th scope="col">Tipo</th>
                        <th scope="col">Preço</th>
                        <th scope="col">Descrições</th>
                        <th scope="col">Opções</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>{{ product.brand }}</td>
                        <td>{{ product.model }}</td>
                        <td>{{ product.type }}</td>
                        <td>{{ product.price }}</td>
                        <td>{{ product.description }}</td>
                        <td class="btn-group">
                            <!-- <button v-show="update" v-on:click="onUpdate" class="btn btn-sm btn-primary" type="button">Atualizar</button> -->
                            <button title="Deletar" v-on:click.prevent="removeProduct(index)" class="btn btn-sm btn-danger" type="button">Deletar</button>
                        </td>
                    </tr>                    
                </tbody>
                </table>
            </div>
        </div>
    </div>
    

</template>

<script>
export default {
    data() {
        return {
            products: [
                {                    
                    brand: 'Dell',
                    model: 'Inspiron 7559',
                    type: 'Notebook',
                    price: '3000',
                    description: 'Bom custo x benefício'
                }
            ],
            brand: '',
            model: '',
            type: '',
            price: '',
            description: ''
        }
    },

    methods: {
        addProduct() {   
            if (this.brand.trim() === '' || this.model.trim() === '' || this.type.trim() === ''
            || this.price.trim() === '' || this.description.trim() === '') {
                return;
            }
            
            this.products.push({
                brand: this.brand,
                model: this.model,
                type: this.type,
                price: this.price,
                description: this.description
            });
            // Aqui apaga os dados digitados após enviá-los ao formulário
            this.brand = '';
            this.model = '';
            this.type = '';
            this.price = '';
            this.description = '';
        },
        removeProduct(index) {
            this.products.splice(index, 1);
        }
    },
}

</script>