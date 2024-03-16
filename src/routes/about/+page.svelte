<!-- +page.svelte -->
<script>
    let pageTitle = "Обо мне";
    let pageContent = 
        <p>Привет! Меня зовут [Ваше имя] и я рад приветствовать вас на моей странице.</p>
        <p>Я увлекаюсь [Ваше хобби] и люблю проводить время [Ваши интересы].</p>
        <p>На этой странице вы найдете немного информации обо мне и моих увлечениях. Приятного чтения!</p>
    ;
</script>

<h1>{pageTitle}</h1>

<div class="about-me">
    {@html pageContent}
</div>

<style>

.about-me {
    margin-top: 20px;
    padding: 20px;
    background-color: #f9f9f9;
    border: 1px solid #ccc;
    border-radius: 5px;
}

.about-me p {
    margin-bottom: 10px;
}

</style>
