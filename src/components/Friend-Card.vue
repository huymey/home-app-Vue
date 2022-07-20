<template>
    <div class="form" v-for=" item in listofCard" :key="item">
        <div><h1>{{item.firstName}}  {{item.lastName}}</h1></div>
        <div><p>{{item.comment}}</p></div>
    </div>
</template>

<script>
export default {
    props :["listofCard"]
}
</script>

<style>
.form{
    box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
    width: 70%;
    margin: auto;
    padding: 10px;
    border-radius: 5px;
    margin-top: 20px;
}
</style>