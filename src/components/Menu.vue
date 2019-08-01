<template>
    <div class="col-sm-2 menu">

        <h3>Menu</h3>
        <ul class="nav nav-pills flex-column">
            <li><a @click="$emit('incrementar')" class="nav-item nav-link active" href="#">Usuarios A</a></li>
            <li><a class="nav-item" href="#">Usuarios B</a></li>
        </ul>
      
    </div>
</template>

<script>
export default {
    name: "Menu"
}
</script>

<style scoped>
.menu {
    float:left;
    background:#f1f1f1;
    height:1000px!important;
    padding-top:10px;
    padding-bottom:10px;
}

ul li a {
    padding:10px;
    display:block;
}

</style>
