<template>
    <div>
        <nav>
            <ul>
                <li><router-link to="/">Home</router-link></li>
                <li><router-link to="/About">About</router-link></li>
                <li><router-link :to="{name:'Contact'}">Contact</router-link></li>
                <li><router-link to="/Profile">Profile</router-link></li>
            </ul>
        </nav>
    </div>
</template>

<script >
export default {
    name:'Navbar',
    data(){
        return{

        }
    }
}
</script>



<style scoped>
nav{
    text-align: center;
}
nav ul{
    padding:0;
}
nav li{
    display:inline-block;
    padding:20px 10px;
     
}
nav a {
    text-transform: uppercase;
    text-decoration: none;
}
</style>
