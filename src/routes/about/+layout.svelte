<!-- +layout.svelte -->
<script>
    export let title;
</script>

<header>
    <h1>{title}</h1>
    <nav>
        <ul>
            <li><a href="/">Главная</a></li>
            <li><a href="/gallery">Галерея</a></li>
            <li><a href="/about">Обо мне</a></li>
        </ul>
    </nav>
</header>

<main>
    <slot></slot>
</main>

<style>

header {
    background-color: #333;
    color: white;
    padding: 10px 0;
}

header h1 {
    margin: 0;
    padding: 0 20px;
}

nav ul {
    list-style-type: none;
    padding: 0;
    margin: 0;
}

nav ul li {
    display: inline;
    margin-right: 10px;
}

nav a {
    color: white;
    text-decoration: none;
}

main {
    padding: 20px;
}

footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 10px 0;
}

</style>
