<template>
    <div id="loginForm" class="loginForm">
        
        <h1>Sign up</h1>
            
            <input id="email" v-model="email" type="email" name="email" placeholder="Email"/>
            <input id="username" v-model="username" type="text" name="username" placeholder="Username" @blur="validName" />
            
            <input id="password" v-model="password" type="password" name="password" placeholder="Password" @blur="validPassword"/>
            
            <input id="confirmPassword" v-model="password" type="password" name="confirmPassword" placeholder="Confirm Password"/>
            <span class="checkboxGroup">
            <input type="checkbox"  name="termsConditions"> 
            <span class="termsAndConds">By checking this box, I agree to Terms &amp; Conditions of the site.</span><br/>
            </span>
            <button type="submit" @click="submitForm">Join now</button>
        
    </div>
</template>

<script>
export default {
    name: 'LoginForm', 
    data(){
        return {
            email: '',
            username:'',
            password:'',
        }
    },
    methods:{
        validName: function (username) {
            const user = document.getElementById('username');
            const re = /^[a-zA-Z]{4,12}$/;
            console.log(re.test(username.target.value));            
            return re.test(username.target.value);
        },
        validPassword: function (password) {
            const user = document.getElementById('password');
            const re = /^(?=.*\d)(?=.*[a-z])(?=.*[A-Z])[0-9a-zA-Z]{6,12}$/;
            console.log(re.test(password.target.value));
            return re.test(password.target.value);
        },
        submitForm: function() {
            const form = document.getElementById('loginForm')
            form.innerHTML = "";
            form.innerHTML = `<h1 class='readyToPlay'>“You’re ready to play!
            In order to play with real money, you will need to 
            provide more information. You can do so now, if you 
            wish, or skip and do it at a later time.”</h1>
            <button class='continueRegistration'>Continue Registration</button>
            <button class='skip'><a href="http://www.casino.com/">Skip</a></button>`
        }
    }
}
</script>

<style lang="scss">
.loginForm {
    position: fixed;
    top: 13%;
    width: 22%;
    left: 69%;
    height: 54%;
    border-radius: 0.5em;
    background: rgba(1, 1, 1, 0.6);
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-around;
    input, button {
        width: 96%;
        background: rgba(1, 1, 1, 0.8);
        border: 2px solid black;
        border-radius: 0.4em;
        font-family: 'Montserrat', sans-serif;
        font-size: 1em;
        color: white;
        &:focus {
            outline: 0;
        }
    }
    button {
        background: #6CB21A;
        border: 0;
        font-weight: 800;
        cursor: pointer;
        a {
            color: inherit; 
            text-decoration: inherit;
        }
    }
}
    input[type="checkbox"] {
            width: 5%;
            display: flex;
    }

    .checkboxGroup {
    display: flex;
}

h1 {
    font-size: 2.5em;
    display: flex;
    justify-content: center;
    color: #F18B2F;
}
.readyToPlay {
    font-size: 1em;
    height: 50%;
    width: 90%;
    text-align: justify;
}
</style>
