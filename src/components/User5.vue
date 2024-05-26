<template>
    <div className="one">
        <button @click="deleteUser(index)">Удалить</button>
        <h3><span>Имя пользователя: </span>{{ user.name }}</h3>
        <p><span>Email пользователя: </span>{{user.email}}</p>
        <p><span>Cупер секретный пароль: </span>{{user.pass}}</p>
    </div>
</template>

<script>
export default {
    props:{
        user:{
            type: Object,
            required: true
        },
        index:{
            type: Number,
            required: true
        },
        deleteUser:{
            type: Function,
            required: true
        }
    }
}
</script>

<style scoped>
.one span {
    color: #000;
  }
  button{
    border: 0;
    border-radius: 5px;
    outline: none;
    padding: 10px 15px;
    background: #d66c75;
    font-weight: bold;
    cursor: pointer;
    transition: transform 500ms ease;
    float: right;
}

button:hover{
    transform: translateY(-5px);
}


</style>
