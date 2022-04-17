<template>
    <b-container fluid>
        <b-row>
            <b-col><h1>{{project.title}}</h1></b-col>
        </b-row>
        <b-row>
            <b-col>{{project.description}}</b-col>
            <b-col>{{project.video}}</b-col>
        </b-row>
    </b-container>
</template>

<script>
export default {
    name: "Project",
    
    props:{
        project: {
            type: Object,
            required: true
        }
    }
}
</script>

<style scoped>

</style>