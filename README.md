<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Luana Borba Studio</title>
  <!-- Fonte do Google Fonts (Exemplo) -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link 
    href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&family=Montserrat&display=swap" 
    rel="stylesheet"
  >
  <!-- Estilos CSS Internos -->
  <style>
    /* RESET BÁSICO */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html, body {
      font-family: 'Montserrat', sans-serif;
      background-color: #FFFFFF;
      color: #000000;
      scroll-behavior: smooth;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    /* CABEÇALHO */
    header {
      width: 100%;
      background-color: #FFFFFF;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1rem 2rem;
      border-bottom: 1px solid #C8A35F; /* linha dourada */
      position: fixed;
      top: 0;
      z-index: 999;
    }

    .logo {
      font-family: 'Playfair Display', serif;
      font-size: 1.5rem;
      font-weight: 700;
      color: #C8A35F; /* Dourado */
    }

    nav ul {
      list-style: none;
      display: flex;
      gap: 1.5rem;
    }

    nav ul li {
      font-weight: 600;
      transition: color 0.3s;
    }

    nav ul li:hover {
      color: #C8A35F; /* Efeito hover dourado */
      cursor: pointer;
    }

    /* SEÇÕES */
    section {
      width: 100%;
      padding: 5rem 2rem 3rem 2rem; /* Espaçamento para não ficar embaixo do header fixo */
    }

    /* BANNER INICIAL */
    #home {
      background: url('https://via.placeholder.com/1200x600/000000/FFFFFF?text=Banner+Inicial') 
                  no-repeat center center/cover;
      height: 80vh;
      display: flex;
      justify-content: center;
      align-items: center;
      position: relative;
      color: #FFFFFF;
      text-align: center;
    }

    #home::before {
      content: "";
      position: absolute;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.4); /* Camada escura para destacar o texto */
      top: 0;
      left: 0;
    }

    #home .banner-content {
      position: relative;
      z-index: 1;
    }

    #home .banner-content h1 {
      font-family: 'Playfair Display', serif;
      font-size: 3rem;
      margin-bottom: 1rem;
      color: #C8A35F;
    }

    #home .banner-content p {
      font-size: 1.2rem;
      max-width: 600px;
      margin: 0 auto;
    }

    /* SEÇÃO SOBRE */
    #sobre {
      background-color: #FFFFFF;
      color: #000000;
    }

    #sobre h2 {
      font-family: 'Playfair Display', serif;
      font-size: 2rem;
      margin-bottom: 1.5rem;
      color: #C8A35F;
      text-align: center;
    }

    .sobre-container {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 2rem;
      max-width: 1000px;
      margin: 0 auto;
    }

    .sobre-container img {
      width: 300px;
      height: auto;
      border-radius: 10px;
      border: 2px solid #C8A35F;
    }

    .sobre-container p {
      text-align: center;
      line-height: 1.5;
      max-width: 600px;
    }

    /* SEÇÃO SERVIÇOS */
    #servicos h2 {
      font-family: 'Playfair Display', serif;
      font-size: 2rem;
      margin-bottom: 1.5rem;
      color: #C8A35F;
      text-align: center;
    }

    .tabela-servicos {
      max-width: 700px;
      margin: 0 auto;
      border: 1px solid #C8A35F;
      border-radius: 5px;
      padding: 2rem;
      background-color: #FFFFFF;
    }

    .tabela-servicos h3 {
      font-size: 1.3rem;
      margin-bottom: 1rem;
      color: #000000;
      font-weight: 700;
      border-bottom: 1px solid #C8A35F;
      padding-bottom: 0.5rem;
    }

    .tabela-servicos ul {
      list-style: none;
      margin-bottom: 1.5rem;
    }

    .tabela-servicos li {
      margin: 0.5rem 0;
      font-weight: 500;
    }

    /* SEÇÃO AGENDAMENTO */
    #agendamento {
      background-color: #F8F8F8;
    }

    #agendamento h2 {
      font-family: 'Playfair Display', serif;
      font-size: 2rem;
      margin-bottom: 1.5rem;
      color: #C8A35F;
      text-align: center;
    }

    .agendamento-container {
      max-width: 700px;
      margin: 0 auto;
      text-align: center;
    }

    .agendamento-container p {
      margin-bottom: 1rem;
    }

    .agendamento-container a {
      display: inline-block;
      padding: 0.8rem 1.5rem;
      background-color: #C8A35F;
      color: #FFFFFF;
      border-radius: 5px;
      font-weight: 600;
      transition: background-color 0.3s;
    }

    .agendamento-container a:hover {
      background-color: #a07f4b;
    }

    /* SEÇÃO CONTATO */
    #contato h2 {
      font-family: 'Playfair Display', serif;
      font-size: 2rem;
      margin-bottom: 1.5rem;
      color: #C8A35F;
      text-align: center;
    }

    .contato-container {
      max-width: 700px;
      margin: 0 auto;
      display: flex;
      flex-direction: column;
      gap: 1rem;
    }

    .contato-container form {
      display: flex;
      flex-direction: column;
      gap: 1rem;
    }

    .contato-container form input,
    .contato-container form textarea {
      padding: 0.8rem;
      border: 1px solid #C8A35F;
      border-radius: 5px;
      outline: none;
    }

    .contato-container form button {
      width: fit-content;
      padding: 0.8rem 1.5rem;
      background-color: #C8A35F;
      color: #FFFFFF;
      border: none;
      border-radius: 5px;
      font-weight: 600;
      cursor: pointer;
      transition: background-color 0.3s;
    }

    .contato-container form button:hover {
      background-color: #a07f4b;
    }

    .info-contato {
      text-align: center;
      margin-top: 1rem;
      font-size: 1rem;
    }

    /* RODAPÉ */
    footer {
      background-color: #000000;
      color: #FFFFFF;
      padding: 1.5rem 2rem;
      text-align: center;
      margin-top: 2rem;
    }

    footer .social-links {
      margin-bottom: 1rem;
    }

    footer .social-links a {
      margin: 0 0.5rem;
      color: #C8A35F;
      font-weight: 600;
    }

    footer p {
      font-size: 0.9rem;
    }

    /* RESPONSIVIDADE */
    @media (max-width: 768px) {
      header {
        flex-direction: column;
        gap: 1rem;
      }

      .sobre-container {
        flex-direction: column;
        text-align: center;
      }
    }
  </style>
</head>
<body>
  <!-- CABEÇALHO -->
  <header>
    <div class="logo">Luana Borba Studio</div>
    <nav>
      <ul>
        <li><a href="#home">Início</a></li>
        <li><a href="#sobre">Sobre</a></li>
        <li><a href="#servicos">Serviços</a></li>
        <li><a href="#agendamento">Agendamento</a></li>
        <li><a href="#contato">Contato</a></li>
      </ul>
    </nav>
  </header>

  <!-- SEÇÃO BANNER INICIAL -->
  <section id="home">
    <div class="banner-content">
      <h1>Luana Borba Studio</h1>
      <p>Unhas que elevam sua autoestima. Bem-vinda ao nosso espaço de beleza e bem-estar!</p>
    </div>
  </section>

  <!-- SEÇÃO SOBRE -->
  <section id="sobre">
    <h2>Quem Sou Eu</h2>
    <div class="sobre-container">
      <img src="C:\Users\gustavo cruz\Downloads\WhatsApp Image 2025-03-02 at 19.12.50 (1).jpeg"


      <p>
        Olá, sou a Luana Borba, apaixonada por realçar a beleza e a confiança das mulheres através de alongamentos de unhas impecáveis. Meu objetivo é oferecer um serviço de excelência, com produtos de alta qualidade e técnicas avançadas, para que cada cliente se sinta única e especial.
      </p>
    </div>
  </section>

  <!-- SEÇÃO SERVIÇOS -->
  <section id="servicos">
    <h2>Nossos Serviços</h2>
    <div class="tabela-servicos">
      <h3>Aplicação</h3>
      <ul>
        <li>Fibra de Vidro – R$ 100,00</li>
        <li>Unha em Gel – R$ 100,00</li>
      </ul>

      <h3>Manutenção</h3>
      <ul>
        <li>Fibra de Vidro – R$ 70,00</li>
        <li>Unha em Gel – R$ 70,00</li>
      </ul>

      <h3>Extras</h3>
      <ul>
        <li>Reposição de unha (na manutenção) – Valor incluso</li>
        <li>Reposição de unha (fora da manutenção) – R$ 10,00/unidade</li>
        <li>Remoção – R$ 30,00</li>
      </ul>
    </div>
  </section>

  <!-- SEÇÃO AGENDAMENTO -->
  <section id="agendamento">
    <h2>Agende Seu Horário</h2>
    <div class="agendamento-container">
      <p>
        Escolha o melhor dia e horário para você. Estou ansiosa para te atender!
      </p>
      <!-- Exemplo de link para Calendly ou outra plataforma de agendamento -->
         <a href="https://api.whatsapp.com/send/?phone=5511940425048&text&type=phone_number&app_absent=0"target=_black>Agendar Agora</a>
    </div>
                            
</form>
      <div class="info-contato">
        <p>Ou se preferir, fale conosco diretamente:</p>
        <p>WhatsApp: (11) 94042-5048</p>
        <p>Instagram: <a href="https://www.instagram.com/luanaborba_studio?igsh=dDcwZG4zYWNjMnA3&utm_source=qr" target="_blank">@luanaborba_studio</a></p>
        <p>Endereço: Rua João Almeida Sampaio, 143 –Osasco/SP</p>
      </div>
    </div>
    </section>


 <form>
  <!-- RODAPÉ -->
  <footer>
    <div class="social-links">
      <a href="https://www.instagram.com/luanaborba_studio?igsh=dDcwZG4zYWNjMnA3&utm_source=qr" target="_blank">Instagram</a> |
      <a href="https://api.whatsapp.com/send/?phone=5511940425048&text&type=phone_number&app_absent=0" target="_blank">WhatsApp</a>
    </div>
    <p>© 2025 Luana Borba Studio – Todos os direitos reservados.</p>
  </footer>
   
 
 <php>
  <!DOCTYPE html>
<html lang="pt-BR">

  </form>
</body>
</html>


</body>
</html>
