<template>
    <div class="container">
        <div class="row">
            <div class="col-md-6">
                <img src="../assets/bg.jpg" width="500px" height="400px" />
            </div>
            <div class="col-md-4 top-merge">
                <form v-on:submit.prevent="Login">
                    <h3>Login</h3>
                    <p>Bem-vindo à nossa pequena demonstração do Vue com o CometChat. Faça login com o nome de usuário 
                        "superhero" ou "superhero 2" e teste o chat. Para criar seu próprio usuário, <a href="/register">Click Aqui</a>
                    </p>
                    <div class="form-wrapper">
                        <label>Usuário</label>
                        <input type="text" name="username" id="username" v-model="username" placeholder="Digite o Usuário" class="form-control" required>
                    </div>
                </form>
            </div>
        </div>
    </div>
</template>