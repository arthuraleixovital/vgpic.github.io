<script>
    export let propostas = [
        { titulo: "Educação", descricao: "Fim das avaliações competitivas e ensino voltado para a cooperação e o pensamento crítico, em vez de apenas decorar conteúdos. Programa de alimentação escolar baseado em produção local e agroecológica, garantindo comida saudável para todos os alunos." },
        { titulo: "Saúde", descricao: "Centros de saúde em bairros periféricos funcionando 24h, com atendimento médico, odontológico e psicológico gratuitos. Produção e distribuição pública de itens de higiene e saúde, como absorventes, fraldas e medicamentos básicos." },
        { titulo: "Segurança Pública", descricao: "Sistema comunitário de segurança, onde a própria população participa da organização e mediação de conflitos, reduzindo a necessidade de policiamento armado. Formação obrigatória para agentes de segurança com foco em direitos humanos, combate ao racismo e ao uso excessivo da força." }
    ];
        // Verifica se o dispositivo é móvel
        function isMobile() {
        return /Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent);
    }

    // Se for um dispositivo móvel, redireciona para uma versão desktop
    if (isMobile()) {
        window.location.href = "https://seusite.com/versao-desktop";
    }
</script>

<style>
    :global(*) {
        box-sizing: border-box;
        margin: 0;
        padding: 0;
    }

    :global(html, body) {
        width: 100vw;
        overflow-x: hidden; /* Garante que nada cause rolagem lateral */
    }

    .navbar {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 15px 50px;
        background-color: #fff;
        box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }

    .navbar a {
        color: #333;
        margin: 0 15px;
        text-decoration: none;
        font-weight: bold;
    }

    .hero {
        position: relative;
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 50px;
        background: url('/esc.jpg') no-repeat center center/cover;
        height: 90vh; /* Altura fixa */
        max-height: 681px; /* Limite máximo */
        overflow: hidden;
    }

    .hero-overlay {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background: rgba(0, 0, 0, 0.5);
    }

    .hero-text {
        position: relative;
        max-width: 50%;
        background: rgba(0, 0, 0, 0.6);
        padding: 20px;
        border-radius: 10px;
        color: white;
    }

    .hero h1 {
        font-size: 3em;
    }

    .hero p {
        font-size: 1.2em;
    }

    .hero button {
        background-color: #ff0000;
        color: white;
        border: none;
        padding: 15px 30px;
        font-size: 1.2em;
        cursor: pointer;
        margin-top: 20px;
        border-radius: 20px;
    }

    .hero img {
        position: absolute; /* Permite ajuste manual */
        width: 40%;
        bottom: -300px; /* Ajuste a altura da imagem */
        left: 55%; /* Ajuste horizontal para mover a imagem */
    }

    .logo b {
        background: linear-gradient(270deg, #ff0000, #ff9900, #ffff00, #00ff00, #0000ff, #8b00ff, #ff0000);
        background-size: 600% 600%;
        background-clip: text;
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        animation: rainbow 10s ease infinite;
    }

    @keyframes rainbow {
        0% { background-position: 0% 50%; }
        50% { background-position: 100% 50%; }
        100% { background-position: 0% 50%; }
    }

    .sobre-container {
        position: relative;
        width: 100%;
        height: 500px;
        background: url('favicon.png') no-repeat center center/cover;
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 20px 50px;
        overflow: hidden;
    }

    .sobre-texto {
        max-width: 50%;
        color: white;
        padding: 20px;
        border-radius: 10px;
        background-color: rgba(0, 0, 0, 0.6); /* Fundo semi-transparente para melhor legibilidade */
    }

    .sobre-imagem {
        position: absolute;
        width: 30%;
        bottom: 0px;
        left: 70%;
        height: auto;
    }

    .bg-light {
        background-color: #f8f9fa !important;
    }

    .py-5 {
        padding-top: 3rem !important;
        padding-bottom: 3rem !important;
    }

    .text-center {
        text-align: center !important;
    }

    .mb-4 {
        margin-bottom: 1.5rem !important;
    }

    .card {
        position: relative;
        display: flex;
        flex-direction: column;
        min-width: 0;
        word-wrap: break-word;
        background-color: #fff;
        background-clip: border-box;
        border: 1px solid rgba(0, 0, 0, 0.125);
        border-radius: 0.25rem;
    }

    .card-body {
        flex: 1 1 auto;
        padding: 1.25rem;
    }

    .card-title {
        margin-bottom: 0.75rem;
    }

    .card-text:last-child {
        margin-bottom: 0;
    }

    .btn-primary {
        color: #fff;
        background-color: #0d6efd;
        border-color: #0d6efd;
    }

    .btn-primary:hover {
        color: #fff;
        background-color: #0b5ed7;
        border-color: #0a58ca;
    }

    .bg-dark {
        background-color: #212529 !important;
    }

    .text-white {
        color: #fff !important;
    }
</style>

<!-- Navbar -->
<div class="navbar">
    <div class="logo">
        <h2>Vinicius Goetten <b>48</b></h2>
    </div>
    <nav>
        <a href="#sobre">Sobre</a>
        <a href="#propostas">Propostas</a>
        <a href="httpwww.google.com/cuzinho">Plano de Governo</a>
        <a href="#contato">Contato</a>
    </nav>
</div>

<!-- Hero Section -->
<div class="hero">
    <div class="hero-overlay"></div>
    <div class="hero-text">
        <p>Revolução com justiça, progresso com igualdade!</p>
        <h1>Vinicius Goetten</h1>
        <p>Candidato à Presidência</p>
        <button on:click={() => document.querySelector('#propostas').scrollIntoView({ behavior: 'smooth' })}>Conheça minhas propostas</button>
    </div>
    <img src="v1.png" alt="Candidato">
</div>

<!-- Sobre -->
<section id="sobre" class="py-5">
    <div class="container">
        <h2 class="text-center mb-4">Sobre mim</h2>
        <div class="sobre-container">
            <div class="sobre-texto">
                <p>Me chamo Vinicius Goetten e tenho 36 anos de idade; nascido em Otacílio Costa - Santa Catarina! Minha incursão na política surge da revolta contra as discrepâncias sociais e da crença firme de que um Brasil mais equânime e solidário é viável! Com esse propósito em mente foi que estabeleci o Partido Igualitário Comunista (PIC), um movimento engajado na batalha pelos direitos dos trabalhadores e na promoção da democracia participativa visando o fim da exploração.
                    Ditadura nunca mais. O futuro é vermelho!</p>
            </div>
            <img src="v2.png" alt="Sobre Vinicius Goetten" class="sobre-imagem">
        </div>
    </div>
</section>

<!-- Propostas -->
<section id="propostas" class="bg-light py-5">
    <div class="container">
        <h2 class="text-center mb-4">Minhas Propostas</h2>
        <div class="row">
            {#each propostas as proposta}
                <div class="col-md-4 mb-4">
                    <div class="card h-100">
                        <div class="card-body">
                            <h5 class="card-title">{proposta.titulo}</h5>
                            <p class="card-text">{proposta.descricao}</p>
                        </div>
                    </div>
                </div>
            {/each}
        </div>
    </div>
</section>

<!-- Contato -->
<section id="contato" class="py-5">
    <div class="container">
        <h2 class="text-center mb-4">Entre em Contato</h2>
        <div class="row justify-content-center">
            <div class="col-md-6">
                <form>
                    <div class="mb-3">
                        <label for="nome" class="form-label">Nome</label>
                        <input type="text" class="form-control" id="nome" required>
                    </div>
                    <div class="mb-3">
                        <label for="email" class="form-label">E-mail</label>
                        <input type="email" class="form-control" id="email" required>
                    </div>
                    <div class="mb-3">
                        <label for="mensagem" class="form-label">Mensagem</label>
                        <textarea class="form-control" id="mensagem" rows="5" required></textarea>
                    </div>
                    <button type="submit" class="btn btn-primary">Enviar</button>
                </form>
            </div>
        </div>
    </div>
</section>

<!-- Footer -->
<footer class="bg-dark text-white py-4">
    <div class="container text-center">
        <p>&copy; 2025 Vinicius Goetten. Todos os direitos reservados.</p>
        <p>
            <a href="https://www.instagram.com/goetten_vinicius/" class="text-white">Instagram</a>
        </p>
    </div>
</footer>