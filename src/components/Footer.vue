<template>
    <footer>
        <p>Copyright &copy; 2021</p>
        <router-link to="/about">About</router-link>
        <!-- by using anchor tag whole page is reloading, thats why use router-link to avoid it -->
        <!-- <a href="/about">About</a> -->
    </footer>
</template>

<style scoped>
a {
    color: #333;
}

footer {
    margin-top: 30px;
    text-align: center;
}
</style>