<template>
    <div>
        <h2>{{title}}</h2>
        <h2>{{displayName}}</h2>
        <h2>{{objectType}}</h2>
        <h2>{{published}}</h2>
    </div>
</template>

<script>
export default{
    props: ['id', 'title', 'displayName', 'objectType', 'published']
}
</script>

<style>
h2{
    background: #f4f4f4;
    padding: 8px;
    border-radius: 10px;
    margin: 10px auto;
    max-width: 700px;
    color: #444;
    text-align: left;
}

h2:hover {
    background: #ddd;
}
</style>