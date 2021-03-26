<template>
    <div class="bg-light">
        <div class="sticky-top">
            <nav class="navbar navbar-dark bg-primary">
                <span class="navbar-brand mb-0 h1">Produtos e Marcas</span>
            </nav>        
        </div>
        <br>
        
        <div class="container">
            <div class="row bg-ligth">
                <form action="" class="col-4 py-3">
                    <div class="form-todo form-group">
                        <h4>Marcas</h4>
                        <p>
                            <label>Nome:</label>
                            <input type="text" class="form-control" >
                        </p>            
                        <button type="submit" class="btn btn-success">Adicionar</button>                        
                    </div>
                </form>

                <form action="" class="col-8 py-3">
                    <div class="form-todo form-group">                                    
                        <h4>Produtos</h4>
                        <div class="input-group mb-3">
                            <div class="input-group-prepend">
                                <label class="input-group-text" for="inputGroupSelect01">Marca</label>
                            </div>
                            <select class="custom-select" id="inputGroupSelect01">
                                <option selected>Escolha...</option>
                                <option value="1">One</option>
                                <option value="2">Two</option>
                                <option value="3">Three</option>
                            </select>
                        </div>
                        
                        <p>
                            <label>Modelo:</label>
                            <input type="text" class="form-control" >
                        </p>

                        <p>
                            <label>Tipo:</label>
                            <input type="text" class="form-control" >
                        </p>

                        <p>
                            <label>Preço:</label>
                            <input type="text" class="form-control" >
                        </p>            

                        <p>
                        <label>Descrições do produto:</label>
                        <textarea name="" class="form-control" ></textarea>
                        </p>
                        <button type="submit" class="btn btn-success">Adicionar</button>                                            
                    </div>
                </form>
            </div>
            <hr>
            <h4>Itens Salvos</h4>
            <div class="form-group">
                <table class="table table-secondary">
                <thead>
                    <tr>
                        
                        <th scope="col">Marca</th>
                        <th scope="col">Modelo</th>
                        <th scope="col">Tipo</th>
                        <th scope="col">Preço</th>
                        <th scope="col">Descrições</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>Mark</td>
                        <td>Otto</td>
                        <td>@mdo</td>
                        <td>@mdo</td>
                        <td>@mdo</td>
                    </tr>
                    
                </tbody>
                </table>
            </div>
        </div>
    </div>
    

</template>

<script>

    
    // data() {
    //     return {
    //         comments: [
    //             {
    //                 name: 'Zé',
    //                 message: 'Teste 1'
    //             }
    //         ],
    //         // Aqui guarda os valores inseridos no formulário
    //         name: '',
    //         message: ''

    //     }
    // },
    // methods: {
    //     addComment() {   
    //         if (this.name.trim() === '' || this.message.trim() === '') {
    //             return;
    //         }
            
    //         this.comments.push({
    //             name: this.name,
    //             message: this.message
    //         });
    //         // Aqui apaga os dados digitados após enviá-los ao formulário
    //         this.name = '';
    //         this.message = '';
    //     },
    //     removeComment(index) {
    //         this.comments.splice(index, 1);
    //     }
    // },
    // // Criar relação do Watch com o timestamp do BD
    // watch: {

    // }

</script>