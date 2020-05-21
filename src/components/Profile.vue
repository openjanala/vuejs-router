<template>
    <div class="profile">
        <h2>Profile User Id = ( {{userId}} )</h2>
    </div>
</template>


<script>
export default {
   name:'Profile',
   data(){
        return {
            userId: this.$route.params.user_id
        }
    },
    methods:{
        updateId(){
            this.userId = this.$route.params.user_id
        }
    },
    watch:{
        $route:'updateId'
    }
}
</script>




<style scoped>

</style>

