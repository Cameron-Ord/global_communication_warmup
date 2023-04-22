<template>
    <div>

        <button @click="delete_button">DELETE</button>

    </div>
</template>

<script>
    export default {

        data() {
            return {
            
                notif: `sucessfully deleted!`,

            }
        },

        methods:{


            delete_button(){


                
                console.log(this.notif);

                this.$root.$emit(`toast_notify`, this.notif);
            }
        }

        
    }
</script>

<style scoped>

</style>