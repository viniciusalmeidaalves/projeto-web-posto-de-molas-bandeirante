# Posto de Molas Bandeirante — Site Corporativo (Serviços e Produtos)

Resumo rápido
------------
Aplicação PHP + MySQL para catálogo de produtos, gerenciamento de serviços, manutenção de frota, formulário de contato e área administrativa.

Tecnologias
----------
- Frontend: HTML5, CSS3, JavaScript (Vanilla)
- Backend: PHP 7.4+ (estruturado em MVC simples)
- Banco: MySQL / MariaDB
- Opcional: Composer, PHPMailer, reCAPTCHA, Google Analytics, Google Tag Manager

Arquitetura geral
-----------------
- Separar código público (DocumentRoot) do restante da aplicação para segurança.
- Camada de apresentação (HTML/CSS) isolada da lógica (PHP scripts em php/).
- Serviços reutilizáveis (DB Connection) centralizados em php/db_connect.php.
- Admin isolado para facilitar proteção por autenticação.
- Assets versionados e organizados por tipo (css, js, img, audio).

Principais arquivos e símbolos
------------------------------
- Entrada pública: index.html, sobre.html, servicos.html, produtos.html, contato.html
- Conexão DB: php/db_connect.php
- Seed de dados: php/inserir_dados_teste.php
- Estilos: css/estilos.css (importa módulos via @import)
- Módulos CSS: css/modules/ (_base.css, _header.css, _home.css, _services.css, _products.css, _about.css, _contact.css, _footer.css, _modal.css, _animations.css, _media-queries.css)
- Scripts: js/scripts.min.js
- Imagens: img/ (banners/, icones/, imagens/, logo/, nossos-servicos/, persona/)
- Áudio: audio/ (vinheta da marca)

Fluxo de dados resumido
-----------------------
1. Usuário acessa página HTML estática (index.html, servicos.html, produtos.html, etc)
2. JavaScript renderiza componentes: menu responsivo, slideshow, modal, seletor de abas
3. Formulário de contato valida dados no front → envia para backend (a implementar)
4. Página de produtos lê categorias/subcategorias do banco
5. Admin gerencia: Categorias → Subcategorias → Produtos com CRUD via PHP
6. Serviços (manutenção frota) gerenciados em servicos.html com tipos e recomendações
7. Integração com Google Maps, Analytics e Tag Manager para tracking
8. WhatsApp flutuante para contato direto

## 🖼 Prévia do Projeto 
*Página inicial do projeto Posto de Molas
<img width="1364" height="727" alt="image" src="https://github.com/user-attachments/assets/0f0d0461-1bc6-433d-989e-3c01e7a21ae3" />

## 📁 Acesso ao projeto
1. [visualizar o projeto na web](https://projeto-web-posto-de-molas-bandeirante.vercel.app/)
