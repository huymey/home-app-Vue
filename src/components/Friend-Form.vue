<template>
    <div class="form">
        <div>
            <input type="text" placeholder="FirstName" v-model="firstName"/>
        </div>
        <div>
            <input type="text" placeholder="lastName" v-model="lastName"/>
        </div>
        <div>
            <input type="text" placeholder="Comment" v-model="comment"/>
        </div>
        <div class='btn'>
            <button @click="onAdd">Add</button>
        </div>
    </div>
    
    <FriendCard :listofCard='listofCard'/>
</template>

<script>
import FriendCard from "./Friend-Card.vue";
export default {
    components :{
        FriendCard
    },
    data(){
        return {
            firstName : '',
            lastName : '',
            comment : '',
            listofCard :[]
        }
    },
    methods : {
        onAdd(){
            let card = {firstName : this.firstName.toUpperCase(),lastName:this.lastName.toUpperCase(),comment: this.comment}
            if(this.firstName !='' && this.lastName!= '' &&this.comment !=''){
                this.listofCard.push(card)
                this.firstName=''
                this.lastName=''
                this.comment=''
            }
            }
        }
};
</script>

<style>
.form{
    box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
    width: 70%;
    margin: auto;
    padding: 10px;
    border-radius: 5px;
    
}
input{
    margin: 10px;
    width: 90%;
    border-radius: 5px;
    padding: 10px;
    border: 2px solid rgb(193, 190, 190);
}
button{
    margin: 10px;
    width: 95%;
    padding: 10px;
    background: rgb(193, 190, 190);
    border: none;
}
</style>