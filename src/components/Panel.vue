<template>
    <div class="container">
        <h1>Produtos</h1>
        <hr>

        <div class="form-todo form-group">



        </div>

        <hr>
        <div class="form-todo form-group">
            <p>
                <input type="text" placeholder="Nome" name="nome" class="form-control" >
            </p>
            <p>
                <textarea placeholder="Comente aqui" name="message" class="form-control" ></textarea>
            </p>
            <button type="submit" class="btn btn-primary">Enviar</button>
        </div>
        <div class="list-group" >
            
        </div>
        <hr>
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