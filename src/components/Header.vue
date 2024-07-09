<script setup>

</script>

<template>

    <nav class="main-nav">
        <ul>
            <li>
                <a class="logo" href="/">
                    <span class="logo-icon">
                        <span class="text-hidden">Honda Logo</span>
                    </span>
                </a>
            </li>
            <li>
                <a href="">Build</a>
            </li>
            <li>
                <a href="#">Models</a>
            </li>
            <li>
                <a href="#">Tools</a>
            </li>
            <li>
                <a href="#">Owners</a>
            </li>
            <li>
                <a href="#">Certified Pre Owned</a>
            </li>
            <li>
                <a href="#">Electrified</a>
            </li>
        </ul>
    </nav>

</template>

<style scoped>

@font-face{
    font-family:honda-icons;
    src:url(/fonts/honda-icons.woff2) format('woff2'),url(/fonts/honda-icons.woff) format('woff');
    font-weight:400;
    font-style:normal;
}

nav{
    align-items: center;
    background: #FFF;
    box-shadow: -0.2px 1px 1px rgba(0, 0, 0, 0.14);
    display: flex;
    height: 84px;
    width: 100%;
}

nav ul{
    align-items: center;
    display: flex;
    font-size: 14px;
    gap: 40px;
    list-style: none;
}

nav a{
    color: #1b1b1b;
    font-weight: 600;   
    text-decoration: none;
}

nav a:hover{
    text-decoration-color: #C82B21 !important;
    text-decoration: underline;
    text-decoration-thickness: 6px;
    text-underline-offset: 32px;
}

nav a.logo:hover{
    text-decoration: none !important;
}

.logo-icon{
    font-family: 'honda-icons';
    font-style: normal;
    font-weight: normal;
    font-variant: normal;
    text-transform: none;
    line-height: 1;
    -webkit-font-smoothing: antialiased;
    font-size: 30px;
}

.logo-icon:before {
    content: "\e903";
}



</style>