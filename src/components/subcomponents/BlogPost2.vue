<script>
export default {
    // Add code if/as necessary
    // Hint: Add properties subject, entry and mood
    props: {
        subject: String,
        entry: String,
        mood: String
    },
    computed: {
        moodImage() {
            return `/assets/${this.mood.toLowerCase()}.png`
        }
    }
}
</script>


<template>
    <!-- TODO: add your template code here. Use boostrap card -->
    <div class="card mb-2" style="width: 18rem;">
        <img :src="moodImage" class="card-img-top" :alt="mood">
        <div class="card-body">
            <h5 class="card-title">{{ subject }}</h5>
            <p class="card-text">{{ entry }}</p>
        </div>
        <slot></slot>
    </div>
</template>
