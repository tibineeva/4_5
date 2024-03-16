<script>
    import { routes } from "./routes";
</script>

<svelte:head>
    <title>Портфолио</title>
</svelte:head>

<div class="container">
    <h1>Мои проекты</h1>
    <div class="apps">
        {#each routes as page}
            <div class="app">
                <h2>{page.title}</h2>
                <p>{page.body}</p>
                <p class="readmore">
                    <a class="link" href={`/project/apps/${page.id}`}>
                        Читать далее
                    </a>
                </p>
            </div>
        {/each}
    </div>
</div>

<style>
    .container {
    margin: 50px auto;
    max-width: 800px;
    padding: 20px;
    background-color: #f9f9f9; /* Цвет фона контейнера */
    border-radius: 10px; /* Закругление углов */
    box-shadow: 0 0 20px rgba(0, 0, 0, 0.1); /* Тень контейнера */
}

.apps {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); /* Адаптивные колонки */
    grid-gap: 20px;
    justify-content: center; /* Центрирование элементов */
}

.app {
    border: 1px solid #ddd;
    padding: 20px;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1); /* Улучшенная тень */
    border-radius: 10px; /* Закругление углов */
    background-color: #fff; /* Цвет фона блока */
    transition: transform 0.3s ease; /* Плавное изменение при наведении */
}

.app:hover {
    transform: translateY(-5px); /* Анимация при наведении */
}

.link {
    color: rgb(10, 10, 139);
    text-decoration: none;
    font-weight: bold;
}

.link:hover {
    color: rgb(10, 10, 200); /* Изменение цвета при наведении */
}
</style>
