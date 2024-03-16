<svelte:head>
    <title>Блог</title>
</svelte:head>
<div class="container">
    <h1>Мои статьи</h1>
    <div class="blogposts">
        {#each routes as page}
            <div class="post">
                <h2>{page.title}</h2>
                <p>{page.body}</p>
                <p class="readmore">
                    <a class="link" href={`/blog/posts/${page.id}`}>
                        Читать далее
                    </a>
                </p>
            </div>
        {/each}
    </div>
</div>
<script>
    import {routes} from './routes'
</script>
<style>
.container {
    margin: 50px auto;
    max-width: 800px;
    padding: 0 20px;
    background-color: #9265e6; /* Добавлено для более яркого фона */
    border-radius: 10px; /* Добавлено для закругления углов */
    box-shadow: 0 0 20px rgba(0, 0, 0, 0.1); /* Улучшен тень блока */
}

.blogposts {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); /* Адаптивные колонки */
    gap: 20px;
}

.post {
    border: 1px solid #ddd;
    padding: 10px;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1); /* Улучшенная тень для постов */
    border-radius: 5px; /* Добавлено для закругления углов */
}

.link {
    color: rgb(10, 10, 139);
    text-decoration: none; /* Убрано подчеркивание у ссылок */
    font-weight: bold; /* Жирный шрифт для ссылок */
}

.link:hover {
    color: rgb(10, 10, 200); /* Изменение цвета при наведении */
}
</style>
