<template>
    <div>

        <p v-if="!dismissed">{{ notif_handler }}</p>


        <button @click="dismiss_notif">dismiss notification</button>

        <button @click="show_notif">show notifications</button>
    </div>
</template>

<script>
    export default {

    data() {
        return {

            notif_handler: undefined,

            dismissed: false,


        }
    },
    
        

        methods:{



            notification(notif){

                console.log(`notified`);

                this.notif_handler = notif;

                console.log(notif);

            },

            show_notif(){

                this.dismissed = false;

            },

            dismiss_notif(){

                this.dismissed = true;


            }


        },


        mounted(){


            this.$root.$on(`toast_notify`, this.notification);
        }

    }
</script>

<style scoped>

</style>