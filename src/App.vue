<template>
    <div id="app">
        <router-view />
    </div>
</template>

<script>
import { CometChat } from '@cometchat-pro/chat';
import './App.css';

export default {
    created() {
        this.initializeComet()
    },
    methods: {
        initializeComet() {
            const APP_ID = 'APP_ID';
                const REGION = 'REGION';
                const appSetting = new CometChat.AppSettingBuilder()
                    .subscribePresenceForAllUsers()
                    .setRegion(REGION)
                    .build();
                CometChat.init(APP_ID, appSetting).then(
                    () => {
                        console.log('Inicialização concluída com sucesso ');
                        // Chamar a função de login
                    },
                    (error) => {
                        console.log('A inicialização falhou com erro:', error);
                        // Verificar o motivo do erro e tomar as medidas adequadas 
                    }
                );
        }
    }
}
</script>
<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}
</style>
