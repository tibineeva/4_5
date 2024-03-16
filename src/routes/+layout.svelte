<nav> 
    <div class="nav-container"> 
        <a href="/" class="nav-logo" title="Back to Homepage">Имя Фамилия</a> 
        <div class="nav-links"> 
            {#each nav as link} 
            <a href={link.href} class="link">{link.title}</a> 
            {/each} 
        </div> 
    </div> 
</nav> 
<div class="container"> 
    <!-- Pages will be injected below --> 
    <slot /> 
</div> 
<script>
    const nav = [ 
    { 
        title: 'Обо мне', 
        href: '/about' 
    }, 
    { 
        title: 'Блог', 
        href: '/blog' 
    }, 
    { 
        title: 'Портфолио', 
        href: '/project' 
    }, 
    { 
        title: 'Контакты', 
        href: '/contacts' 
    }
    ] 
</script> 
  
<style>  
    .container {  
        max-width: 1400px;  
        margin: 50px auto;  
        display: grid;  
        grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));  
        gap: 20px;  
    }  
    nav {  
        background-color: #f3f3f3;  
        padding: 10px;  
        box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);  
    }  
    .nav-logo {  
        font-size: 24px;  
        font-weight: bold;  
        text-decoration: none;  
        color: #333;  
    }  
    .nav-links {  
        display: flex;  
        justify-content: flex-end;  
    }  
    .link {  
        margin-left: 10px;  
        color: #333;  
        text-decoration: none;  
    }  
</style>