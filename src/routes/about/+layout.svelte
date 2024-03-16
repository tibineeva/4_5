<script>
    import { Navigation } from './Navigation.svelte';
</script>

<header class="header">
    <h1>Мой удивительный веб-сайт</h1>
    <Navigation />
</header>

<main class="main-content">
    <slot></slot>
</main>

<footer class="footer">
    <p>© 2024. Создано с любовью</p>
</footer>

<style>
    .header {
        background-color: #333;
        color: white;
        text-align: center;
        padding: 1rem;
    }

    .main-content {
        padding: 1rem;
    }

    .footer {
        background-color: #333;
        color: white;
        text-align: center;
        padding: 0.5rem;
    }
</style>
