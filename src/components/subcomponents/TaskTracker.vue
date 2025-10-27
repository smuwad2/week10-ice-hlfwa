<script setup>
    // TODO: add code to define necessary props
    const props = defineProps({ 
        task: Object,
        idx: Number
    })

</script>

<script>
    export default { 
        data() {
            return {
                show: false,
                desc: '',
                deadline: '',
                taskList: []
            }
        },
    }
</script>

<template>
    <!-- TODO: add your template code here --> 
    <div class="card" style="width: 18rem;display:inline-block;">
        <div class="card-body">
            <h5 class="card-title">Deadline: {{task.deadline}}</h5>
            <hr>
            <p class="card-text">{{task.desc}}</p>
            <button type="button" v-on:click="$emit('removeTask', idx)" class="btn btn-primary">Done</button>
        </div>
    </div>
</template>