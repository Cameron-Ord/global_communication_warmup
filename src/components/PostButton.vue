<template>
    <div>

        <button @click="post_button">POST</button>

    </div>
</template>

<script>
    export default {
        

        data() {
            return {
                notif: `successfuly posted!`,
            }
        },

        methods:{

            post_button(){

                console.log(this.notif);

                this.$root.$emit(`toast_notify`, this.notif);
            }
        }

    }
</script>

<style scoped>

</style>