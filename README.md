# alura
surf

<think>
First, the user wants a program in JavaScript for functionality, with CSS for visuals, creating a website with just the homepage (tela inicial), themed around SURF. I need to provide the code as a single HTML file containing HTML, CSS, and JavaScript.


## Gathering project details  
- The task is to create a website with a single homepage themed around surfing.  
- The website needs HTML for structure, CSS for visuals, and JavaScript for functionality, all combined in one HTML file.  
- The homepage is referred to as "tela inicial," indicating a focus on the initial user experience.

## Extending project scope  
- The website must use only HTML, CSS, and JavaScript, with TailwindCSS allowed if imported via a CDN script in the head.  
- All code should be combined into a single HTML file, named index.
</think>`index.html`
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Surf Paradise - Tela Inicial</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background: linear-gradient(135deg, #87CEEB, #FFD700);
            margin: 0;
            overflow-x: hidden;
        }
        .hero {
            position: relative;
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            background-image: url('https://placehold.co/1920x1080/png?text=Ocean+Waves');
            background-size: cover;
            background-position: center;
        }
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 255, 0.3);
            z-index: 1;
        }
        .hero-content {
            z-index: 2;
        }
        .wave-animation {
            position: absolute;
            bottom: 0;
            width: 100%;
            height: 100px;
            background: url('https://placehold.co/1200x600/png?text=Curling+Waves') repeat-x bottom;
            animation: wave 5s linear infinite;
        }
        @keyframes wave {
            0% { transform: translateX(0px); }
            100% { transform: translateX(-1200px); }
        }
        .surf-board {
            transition: transform 0.3s ease;
        }
        .surf-board:hover {
            transform: rotate(5deg);
        }
        .tips {
            padding: 50px 20px;
            background: white;
            border-radius: 10px;
            margin: 20px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        footer {
            padding: 20px;
            text-align: center;
            background: #333;
            color: white;
        }
    </style>
</head>
<body>
    <div class="hero">
        <div class="hero-content">
            <h1 class="text-6xl font-bold mb-4">Bem-vindo ao Surf Paradise</h1>
            <p class="text-2xl mb-6">Descubra as ondas, o estilo de vida e as emoções do surfe!</p>
            <button id="catchWaveBtn" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">Pegue uma Onda!</button>
        </div>
        <div class="wave-animation"></div>
    </div>

    <section class="container mx-auto py-10">
        <div class="text-center mb-8">
            <h2 class="text-4xl font-semibold">Sobre o Surfe</h2>
            <p class="text-lg mt-4">O surfe é mais do que um esporte; é uma paixão, um estilo de vida que une humanos e oceano em harmonia perfeita.</p>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
            <div class="text-center">
                <img src="https://placehold.co/400x300/png?text=Surfer+Catching+Wave+in+Tropical+Beach+with+Sunny+Sky" alt="A expert surfer dressed in a black wetsuit riding a blue surfboard on a large curling wave in a tropical beach setting with blue ocean water, golden sand, and a bright sunny sky with scattered clouds" class="mx-auto rounded-lg surf-board">
                <p class="mt-4">Pegue a Wave Perfeita</p>
            </div>
            <div class="text-center">
                <img src="https://placehold.co/400x300/png?text=Pristine+Surfpole+Beach+with+Boards" alt="A pristine surf gear store with colorful surfboards arranged in racks, wet suits hanging, and a background of calm ocean waves at sunset with oranges and pinks in the sky" class="mx-auto rounded-lg surf-board">
                <p class="mt-4">Explore Equipamentos</p>
            </div>
            <div class="text-center">
                <img src="https://placehold.co/400x300/png?text=Group+of+Surfers+Laughing" alt="A group of five young surfers smiling and laughing while sitting on their surfboards on a golden sandy beach, with turquoise ocean waves in the background and a cloudless bright blue sky" class="mx-auto rounded-lg surf-board">
                <p class="mt-4">Comunidade Surfista</p>
            </div>
        </div>
    </section>

    <section class="tips mx-auto w-11/12 md:w-3/4">
        <h2 class="text-3xl font-semibold text-center mb-6">Dicas para Iniciantes no Surfe</h2>
        <ul class="list-disc list-inside text-lg">
            <li>Comece com aulas básicas para segurança e técnica.</li>
            <li>Escolha praias com ondas suaves e tenha um parceiro experiente.</li>
            <li>Invista em um bom equipamento: prancha, leash e fatos de choque.</li>
            <li>Respeite as regras locais e o meio ambiente marinho.</li>
        </ul>
        <div id="tipContainer" class="mt-6 hidden">
            <p class="text-xl font-bold">Bônus: Uma dica secreta - Visualize a onda antes de pegar!</p>
        </div>
    </section>

    <footer>
        <p>&copy; 2023 Surf Paradise. Todos os direitos reservados. Desenvolvido com paixão pelas ondas.</p>
    </footer>

    <script>
        const catchWaveBtn = document.getElementById('catchWaveBtn');
        const tipContainer = document.getElementById('tipContainer');

        catchWaveBtn.addEventListener('click', () => {
            alert('Você está pronto para surfar? Vem caçar aquela onda!');
            tipContainer.classList.toggle('hidden');
        });
    </script>
</body>
</html>
</content>
</create_file>
```

🎨 **Generating images based on descriptions...**

✅ **Images generated successfully! Here's your updated content:**

`index.html`
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Surf Paradise - Tela Inicial</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background: linear-gradient(135deg, #87CEEB, #FFD700);
            margin: 0;
            overflow-x: hidden;
        }
        .hero {
            position: relative;
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            background-image: url('https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/3de58cd3-cc34-4471-ab1a-bedeeb7d530d.png');
            background-size: cover;
            background-position: center;
        }
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 255, 0.3);
            z-index: 1;
        }
        .hero-content {
            z-index: 2;
        }
        .wave-animation {
            position: absolute;
            bottom: 0;
            width: 100%;
            height: 100px;
            background: url('https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/7b38f6ee-c4a8-4b86-a276-2f33e009b294.png') repeat-x bottom;
            animation: wave 5s linear infinite;
        }
        @keyframes wave {
            0% { transform: translateX(0px); }
            100% { transform: translateX(-1200px); }
        }
        .surf-board {
            transition: transform 0.3s ease;
        }
        .surf-board:hover {
            transform: rotate(5deg);
        }
        .tips {
            padding: 50px 20px;
            background: white;
            border-radius: 10px;
            margin: 20px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        footer {
            padding: 20px;
            text-align: center;
            background: #333;
            color: white;
        }
    </style>
</head>
<body>
    <div class="hero">
        <div class="hero-content">
            <h1 class="text-6xl font-bold mb-4">Bem-vindo ao Surf Paradise</h1>
            <p class="text-2xl mb-6">Descubra as ondas, o estilo de vida e as emoções do surfe!</p>
            <button id="catchWaveBtn" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">Pegue uma Onda!</button>
        </div>
        <div class="wave-animation"></div>
    </div>

    <section class="container mx-auto py-10">
        <div class="text-center mb-8">
            <h2 class="text-4xl font-semibold">Sobre o Surfe</h2>
            <p class="text-lg mt-4">O surfe é mais do que um esporte; é uma paixão, um estilo de vida que une humanos e oceano em harmonia perfeita.</p>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
            <div class="text-center">
                <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/428761a6-4fd4-40af-a788-fbeb0eefca33.png" alt="A expert surfer dressed in a black wetsuit riding a blue surfboard on a large curling wave in a tropical beach setting with blue ocean water, golden sand, and a bright sunny sky with scattered clouds" class="mx-auto rounded-lg surf-board">
                <p class="mt-4">Pegue a Wave Perfeita</p>
            </div>
            <div class="text-center">
                <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/22160848-ff58-4b7b-baef-1cc7c7f35daa.png" alt="A pristine surf gear store with colorful surfboards arranged in racks, wet suits hanging, and a background of calm ocean waves at sunset with oranges and pinks in the sky" class="mx-auto rounded-lg surf-board">
                <p class="mt-4">Explore Equipamentos</p>
            </div>
            <div class="text-center">
                <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/a027d7f1-bf33-4bc8-939b-476ccee9a9f9.png" alt="A group of five young surfers smiling and laughing while sitting on their surfboards on a golden sandy beach, with turquoise ocean waves in the background and a cloudless bright blue sky" class="mx-auto rounded-lg surf-board">
                <p class="mt-4">Comunidade Surfista</p>
            </div>
        </div>
    </section>

    <section class="tips mx-auto w-11/12 md:w-3/4">
        <h2 class="text-3xl font-semibold text-center mb-6">Dicas para Iniciantes no Surfe</h2>
        <ul class="list-disc list-inside text-lg">
            <li>Comece com aulas básicas para segurança e técnica.</li>
            <li>Escolha praias com ondas suaves e tenha um parceiro experiente.</li>
            <li>Invista em um bom equipamento: prancha, leash e fatos de choque.</li>
            <li>Respeite as regras locais e o meio ambiente marinho.</li>
        </ul>
        <div id="tipContainer" class="mt-6 hidden">
            <p class="text-xl font-bold">Bônus: Uma dica secreta - Visualize a onda antes de pegar!</p>
        </div>
    </section>

    <footer>
        <p>© 2023 Surf Paradise. Todos os direitos reservados. Desenvolvido com paixão pelas ondas.</p>
    </footer>

    <script>
        const catchWaveBtn = document.getElementById('catchWaveBtn');
        const tipContainer = document.getElementById('tipContainer');

        catchWaveBtn.addEventListener('click', () => {
            alert('Você está pronto para surfar? Vem caçar aquela onda!');
            tipContainer.classList.toggle('hidden');
        });
    </script>
</body>
</html>
</content>
</create_file>
```
