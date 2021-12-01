<template>
    <div>
        <h3>{{para}}</h3>
        <p>{{name}}</p>
        <p>{{job}}</p>
    </div>
</template>

<script>
    export default {
        name: 'Carousel',
        props: {
            para: String,
            name: String,
            job: String,
        }
    }
</script>