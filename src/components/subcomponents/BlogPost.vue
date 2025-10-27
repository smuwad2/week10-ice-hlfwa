<script>
    export default {
        computed: {
            feel() {
                return "/assets/" + this.mood.toLowerCase() + ".png"
            }
        },
        props: {
            id: String,
            subject: String,
            entry: String,
            mood: String
        }
    }
</script>

<template>
    <!-- TODO: add your template code here --> 
    <div class="card mx-auto" style="width: 24rem;">
        <img :src="feel" class="card-img-top" alt="Image cap">  
        <div class="card-body">
            <h5 class="card-title"> Blog {{ id }} Subject {{ subject }} </h5>
            <p class="card-text"> {{ entry }} </p>
            <hr size="10" noshade>
            <br />
        </div>
    </div>

</template>