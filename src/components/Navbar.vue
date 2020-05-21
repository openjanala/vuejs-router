<template>
    <div>
        <nav>
            <ul>
                <li><router-link to="/">Home</router-link></li>
                <li><router-link to="/about">About</router-link></li>
                <li><router-link :to="{name:'contact'}">Contact</router-link></li>
                <li><router-link to="/profile">Profile</router-link></li>
            </ul>
        </nav>
        <div class="profileId">
            <ul>
                <li v-for="(id, index) in userIds" :key="index">
                    <router-link :to="{name:'profile', params:{user_id:id} }">Profile {{id}}</router-link>
                </li>
            </ul>
            <button @click="Contact">Contact</button>
            <button @click="About">About</button>

             <button @click="Back">Back</button>
            <button @click="Forward">Forward</button>
        </div>
    </div>
</template>

<script >
export default {
    name:'Navbar',
    data(){
        return{
            userIds:['1','2','3']
        }
    },
    methods:{
        Contact(){
            this.$router.push( {name:'contact'} )
        },
        About(){
            this.$router.push( {name:'about'} )
        },
        Back(){
            this.$router.go(-1)
        },
        Forward(){
            this.$router.go(1 )
        },
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
.profileId ul li{
    list-style: none;;
}


</style>
