<template>
    <div class="profile">
        <h2>Profile | User Id = ( {{UserId}} )</h2>
    </div>
</template>


<script>
export default {
   name:'Profile',
   data(){
        return {
            UserId: this.$route.params.user_id
        }
    }
}
</script>




<style scoped>

</style>

