<template>
    <div class="form-check">
        <input class="form-check-input" v-on:click="task.status = true" type="checkbox" value id="defaultCheck1">
        <label class="form-check-label item" v-on:click="task.status = true" v-bind:class="{'item-completed':task.status}" for="defaultCheck1">{{task.name}}</label>
    </div>
</template>
<script>
    export default {
        name : "ItemTugas",
        props : ["task"],
    }
</script>
<style scoped>
    .item-completed {
        color: mediumseagreen;
    }
    .item-notcompleted {
        color: darkslateblue;
    }
</style>
