# Web Player IPTV com API Xtream

Um leitor de IPTV moderno e rico em funcionalidades, construído com HTML, Tailwind CSS e JavaScript puro, que se conecta à API Xtream Codes para fornecer uma experiência de streaming completa no navegador.


---

## 🚀 Sobre o Projeto

Este projeto foi criado para ser uma interface de front-end leve, rápida e elegante para serviços de IPTV que utilizam o painel Xtream Codes. O objetivo é oferecer uma experiência de utilizador comparável à de serviços de streaming populares, com funcionalidades como cache de conteúdo para navegação rápida, um leitor de vídeo personalizado e memorização do progresso de visualização.

Toda a lógica é contida num único ficheiro HTML, utilizando o Tailwind CSS para o estilo e JavaScript puro para a interatividade, o que o torna extremamente portátil e fácil de implementar em qualquer servidor web com PHP.

---

## ✨ Principais Funcionalidades

- **Conexão com API Xtream**: Autenticação segura de utilizador através de URL do servidor, nome de utilizador e senha.

- **Interface Moderna**: Design responsivo e limpo inspirado na paleta de cores do Gemini, utilizando Tailwind CSS.

- **Navegação por Abas**: Conteúdo claramente separado em "TV ao Vivo", "Filmes" e "Séries".

- **Leitor de Vídeo Personalizado**:
  - Interface de controlos que aparece ao passar o rato.
  - Barra de progresso interativa (scrub).
  - Controlos de volume, tempo e botão de ecrã inteiro.
  - Suporte para streams de áudio com visualizador dedicado.

- **Continuar de Onde Parou**: O player guarda o progresso de filmes e episódios no `localStorage` e pergunta se deseja continuar ao reabrir um vídeo.

- **Navegação Inteligente de Séries**:
  - Botões de próximo e anterior no leitor de vídeo.
  - Botão "Próximo Episódio" que aparece 30 segundos antes do fim.
  - Reprodução automática do episódio seguinte ao terminar o atual.

- **Pesquisa em Tempo Real**: Barra de pesquisa no cabeçalho para filtrar o conteúdo da categoria atual instantaneamente.

- **Cache de Conteúdo**: Após o primeiro login, todo o conteúdo (TV, filmes e séries) é carregado e guardado em cache para navegação entre abas instantânea.

- **Carregamento Otimizado**:
  - Lazy Loading para as imagens dos pôsteres.
  - Buffer otimizado com HLS.js para menos pausas na reprodução.

---

## 🛠️ Tecnologias Utilizadas

### Front-End:
- HTML5  
- Tailwind CSS  
- JavaScript (ES6+)

### Reprodução de Vídeo:
- HLS.js - Para reprodução de streams HLS.

### Back-End (Dependência):
- Um servidor web com PHP para executar o script da API.

---

## ⚙️ Como Configurar e Usar

### Pré-requisitos:

- Um servidor web (ex: Apache, Nginx) com PHP instalado.
- Credenciais de um serviço de IPTV que utilize a API Xtream Codes (URL do servidor, utilizador e senha).

### Configuração do Back-End:

1. Coloque o ficheiro `player_api.php` no seu servidor.
2. Certifique-se de que o script tem permissões corretas e dependências como a pasta `includes`.

### Configuração do Front-End:

1. Coloque o ficheiro `index.html` no mesmo servidor (diretório público, ex: `public_html` ou `www`).
2. A função `apiRequest` no JS já está configurada para chamar `player_api.php`. Se os ficheiros estiverem em pastas diferentes, ajuste o caminho conforme necessário.

### Acesso e Utilização:

- Acesse no navegador: `http://seusite.com/index.html`
- Insira a URL do servidor, nome de utilizador e senha para acessar o conteúdo.

---

## ⚡ Dependência do Back-End (`player_api.php`)

Este projeto é apenas o front-end. O script `player_api.php` é **essencial**, pois:

- Recebe os pedidos do web player.
- Comunica-se com o painel Xtream Codes.
- Autentica o utilizador.
- Busca e envia as listas de canais, filmes e séries em JSON.

Sem este script no servidor, o player **não funcionará**.

---

## 📈 Possíveis Melhorias

- [ ] Suporte para login com URL de lista M3U.  
- [ ] Implementação de EPG (Guia de Programação Eletrónico).  
- [ ] Secção de "Favoritos".  
- [ ] Página de configurações (tema, buffer, etc.).  
- [ ] Refatoração para framework moderno (Vue.js ou React).

---

## 📜 Licença

Distribuído sob a licença **MIT**. Veja o ficheiro `LICENSE` para mais informações.

