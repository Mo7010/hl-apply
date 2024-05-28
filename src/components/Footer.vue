<script>
import { RouterLink } from 'vue-router';
</script>

<template>
<div class="footer">
    <h4>All Copyrights Receved To <span>Hl Services©</span> 2024</h4>
</div>
</template>

<style scoped>
.footer{
    width:100%;
    height:10vh;
    background:radial-gradient(circle, rgba(0,0,0,1) 0%, var(--primary) 100%);
    display:flex;
    justify-content:center;
    align-items:center;
    border-top-left-radius:25px;
    border-top-right-radius:25px;
}

.footer h4{
    color:white;
}

.footer h4 span{
    color:var(--text);
}
</style>
