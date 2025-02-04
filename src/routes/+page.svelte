<script>
    export let propostas = [
        { titulo: "Educação", descricao: "Investir em escolas públicas, capacitação de professores e tecnologia educacional." },
        { titulo: "Saúde", descricao: "Melhorar a infraestrutura dos hospitais e postos de saúde, além de garantir medicamentos gratuitos." },
        { titulo: "Infraestrutura", descricao: "Reformar estradas, ampliar o transporte público e garantir saneamento básico para todos." }
    ];
</script>

<style>
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
    background: url('esc.jpg') no-repeat center center/cover;
    min-height: 90vh;
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
    max-width: 40%;
    height: auto;
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
</style>

<!-- Navbar -->
<div class="navbar">
    <div class="logo">
        <h2>Vinicius Goetten <b>48</b></h2>
    </div>
    <nav>
        <a href="#sobre">Sobre</a>
        <a href="#propostas">Propostas</a>
        <a href="#contato">Plano de Governo</a>
        <a href="#contato">Contato</a>
    </nav>
</div>

<!-- Hero Section -->
<div class="hero">
    <div class="hero-overlay"></div>
    <div class="hero-text">
        <p>O Poder do Povo em nossas mãos!</p>
        <h1>Vinicius Goetten</h1>
        <p>Candidato à Presidência</p>
        <button>Conheça minhas propostas</button>
    </div>
    <img src="favicon.png" alt="Candidato">
</div>

<!-- Sobre -->
<section id="sobre" class="py-5">
    <div class="container">
        <h2 class="text-center mb-4">Sobre mim</h2>
        <div class="row">
            <div class="col-md-6">
                <p>Sou pobre, periférico.</p>
            </div>
            <div class="col-md-6">
                <img src="favicon.png" alt="Sobre Vinicius Goetten" class="img-fluid rounded">
            </div>
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
        <p>&copy; 2023 Vinicius Goetten. Todos os direitos reservados.</p>
        <p>
            <a href="https://www.instagram.com/goetten_vinicius/" class="text-white">Instagram</a>
        </p>
    </div>
</footer>
