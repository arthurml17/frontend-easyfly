<template>

<div class="formLogin" v-if="this.haveAccount == true">
    <!-- <h3 class="title">Sign in</h3> -->
    <img class="logo" src="..\assets\images\logoEasy1.png" alt="logo">

    <div class="input-container input1">
        <input placeholder="Email" type="email" class="input" id="email">
    </div>

    <div class="input-container input2">
        <input placeholder="Password" type="password" class="input" id="password">
    </div>

    <button class="btn btnSignIn">Entrar</button>

    <button class="btn btnCreateAccount" @click="changeHaveAccount(false)">Criar conta</button>
</div>

<div class="formCreateAccount" v-if="this.haveAccount == false">
    <img class="logo" src="..\assets\images\logoEasy1.png" alt="logo">

    <div class="input-container input1">
        <input placeholder="Name" type="name" class="input" id="text">
    </div>

    <div class="input-container input2">
        <input placeholder="Email" type="email" class="input" id="email">
    </div>

    <div class="input-container input3">
        <input placeholder="Password" type="password" class="input" id="password">
    </div>

    <button class="btn btnCreateAccount">Criar conta</button>

    <button class="btn btnSignIn" @click="changeHaveAccount(true)">Entrar</button>
</div>

</template>

<style scoped>

.formLogin {
    background-color: #e2e2e9;
    border-radius: 20px;
    box-sizing: border-box;
    height: 70vh;
    width: 23vw;
    background: #e2e2e9;
    box-shadow:  22px 22px 100px #5d5d60,
             -22px -22px 100px #ffffff;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

.formCreateAccount{
    background-color: #e2e2e9;
    border-radius: 20px;
    box-sizing: border-box;
    height: 80vh;
    width: 23vw;
    background: #e2e2e9;
    box-shadow:  22px 22px 100px #5d5d60,
             -22px -22px 100px #ffffff;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

.logo{
    width: 12vw;
    margin-top: -8vh;
}

.title {
    color: #dc2f55;
    font-family: sans-serif;
    font-size: 36px;
    font-weight: 600;
}

.input-container {
    height: 6.5vh;
    width: 17vw;
}

.input1 {
    margin-top: 0px;
}

.input2 {
    margin-top: 30px;
}

.input3 {
    margin-top: 30px;
    margin-bottom: 2vh;
}

.input {
    background-color: #ffffff;
    border-radius: 12px;
    border: 0;
    box-sizing: border-box;
    color: #15172b;
    font-size: 18px;
    height: 100%;
    outline: 0;
    padding: 4px 20px 0;
    width: 17vw;
    box-shadow: inset 5px 5px 8px #acacb1,
            inset -5px -5px 8px #ffffff;
}

.btn {
    border-radius: 12px;
    border: 0;
    box-sizing: border-box;
    cursor: pointer;
    font-size: 18px;
    height: 6.5vh;
    width: 17vw;
    margin-top: 38px;
    text-align: center;
    transition: letter-spacing 1s;
    box-shadow:  11px 11px 22px #bebec4,
                -11px -11px 22px #ffffff;
}

.btnSignIn{
    background-color: #dc2f55;
    color: #ffffff;
    margin-top: 3vh;
}

.btnSignIn:hover{
    letter-spacing: 4px;
    transition: letter-spacing .5s;
}

.btnCreateAccount{
    margin-top: 3vh;
    border: 2px solid #04387D;
    background-color: #e2e2e9;
    border-color: #04387D;
    color: #04387D;
    transition: background-color .8s;
}

.btnCreateAccount:hover{
    transition: color .3s;
    color: white;
    transition: background-color .3s;
    background-color: #04387D;
}

</style>

<script>

export default{
    name: 'login',
    data(){
        return{
            haveAccount: true
        }
    },
    methods: {
        changeHaveAccount(param){
            if(param == true){
                this.haveAccount = true;
            }else{
                this.haveAccount = false;
            }
        }
    }
}

</script>