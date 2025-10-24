<script>
    // TODO: Complete the code
    export default { 
        data() {
            return {
                
            }
        },
        // Hint: insert properties task (Object) and idx (Number)
        props: {
            task: Object,
            id: Number
        },
        emits: ["removeTask"]
    }
</script>

<template>
    <!-- TODO: add your template code here --> 
   <div class="card" style="width: 18rem; display:inline-block; margin-right: 10px">
        <div class="card-body">
            <h5 class="card-title">Deadline: {{ task.deadline }}</h5>
            <hr></hr>
            <p class="card-text">{{ task.desc }}</p>
            <button class="btn btn-primary" @click="$emit('removeTask', id)">Done</button>
        </div>
    </div>
</template>


