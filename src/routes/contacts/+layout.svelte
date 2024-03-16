<script>
</script>
<header>
    <h1>Мой сайт</h1>
    <nav>
        <ul>
            <li><a href="/">Главная</a></li>
            <li><a href="/about">Обо мне</a></li>
            <li><a href="/contacts">Контакты</a></li>
        </ul>
    </nav>
</header>

<main>
    {#if $page}
        {#each $page.children as child}
            {#if child.slug === $subPage}
                {#await import(./${child.slug}.svelte)}
                    <p>Загрузка...</p>
                {:then page}
                    <svelte:component this={page.default} />
                {:catch error}
                    <p>Ошибка загрузки страницы: {error.message}</p>
                {/await}
            {/if}
        {/each}
    {:else}
        <p>Выберите страницу в меню навигации</p>
    {/if}
</main>

<footer>
    &copy; {new Date().getFullYear()} Мой сайт
</footer>

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
