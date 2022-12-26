# Abas
Trata-se de um projeto simples com HTML e CSS que cria diferentes abas, com conteúdos distintos, em uma mesma página.

## HTML
```html
<body>
    <div class="abas">
        <input type="radio" name="abas"  id="abaUm" checked="checked">
        <label for="abaUm">Primeira</label>
        <div class="aba">
            <h1>Primeira aba</h1>
            <p>Conteúdo da primeira aba</p>
        </div>
        <input type="radio" id="abaDois" name="abas"> 
        <label for="abaDois">Segunda</label>
        <div class="aba">
            <h1>Segunda aba</h1>
            <p>Conteúdo da segunda aba</p>
        </div>
        <input type="radio" id="abaTres" name="abas">
        <label for="abaTres">Terceira</label>
        <div class="aba">
            <h1>Terceira aba</h1>
            <p>Conteúdo da tarceira aba</p>
        </div>

    </div>  
</body>
```

## CSS
```css
        body{
            background-color: rgb(149, 149, 149);
            display: flex;
            align-items: center;
            justify-content: center;
            height: 100vh;
            font-family: 'poppoins',sans-serif;
        }
        .abas{
            display: flex;
            flex-wrap: wrap;
            width: 380px;
        }
        .abas label{
            order: 1;
            display: block;
            padding: 10px 15px;
            margin-right: 0.2rem;;
            cursor: pointer;
            background-color: rgb(231, 242, 106);
            font-weight: bold;
            transition:  ease 0.3s;
        }
        .abas .aba{
            order: 99;
            flex-grow:1;
            width: 100%;
            height: 280px;
            display: none;
            padding: 1rem;
            background-color: #fff;
        }
        .abas input[type="radio"]{
            display: none;
        }
        .abas input[type="radio"]:checked+label{
            background-color: #fff;
        }
        .abas input[type="radio"]:checked+label+.aba{
            display: block;
        }
```
