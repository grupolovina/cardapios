# Sistema de Cardápios Multi-idioma

Um sistema simples e responsivo para exibir cardápios de restaurantes em múltiplos idiomas, desenvolvido com HTML e CSS puro.

## 🎨 Características

- Design minimalista com foco em mobile
- Cores personalizadas (#003448 e #ede9da)
- Suporte a múltiplos restaurantes (4 restaurantes incluídos)
- Suporte a múltiplos idiomas (Português, Inglês, Espanhol)
- Redirecionamento direto para Google Drive
- Totalmente responsivo
- **Apenas HTML e CSS puro - extremamente fácil de entender e modificar**

## 📁 Estrutura de Arquivos

```
.
├── index.html                          # Página inicial - seleção de restaurante
├── language-fullano-praia.html         # Seleção de idioma - Fullano Praia
├── language-golfinho-bar.html          # Seleção de idioma - Golfinho Bar
├── language-lovina-ponta.html          # Seleção de idioma - Lovina Ponta
├── language-lovina-seixas.html         # Seleção de idioma - Lovina Seixas
├── css/
│   └── style.css                       # Todos os estilos do site
└── public/
    └── restaurant-logo.png             # Logo do restaurante
```

## 🔗 Como Configurar os Links do Google Drive

Cada botão de idioma nas páginas `language-*.html` possui um link placeholder que você precisa substituir pelo seu link real do Google Drive:

```html
<!-- ANTES (placeholder) -->
<a href="https://drive.google.com/file/d/SEU_LINK_AQUI_PT/view" target="_blank" class="menu-button">

<!-- DEPOIS (com seu link real) -->
<a href="https://drive.google.com/file/d/1AbCdEfGhIjKlMnOpQrStUvWxYz/view" target="_blank" class="menu-button">
```

### Passo a passo para obter o link do Google Drive:

1. Faça upload do PDF do cardápio para o Google Drive
2. Clique com o botão direito no arquivo e selecione "Compartilhar"
3. Altere as permissões para "Qualquer pessoa com o link pode visualizar"
4. Copie o link compartilhado
5. Substitua `SEU_LINK_AQUI_PT`, `SEU_LINK_AQUI_EN` ou `SEU_LINK_AQUI_ES` pelo ID do arquivo do Google Drive

**Importante**: O link do Google Drive tem este formato: `https://drive.google.com/file/d/[ID_DO_ARQUIVO]/view`

## ➕ Como Adicionar um Novo Restaurante

### Passo 1: Adicionar na Página Inicial
Abra `index.html` e adicione um novo botão dentro de `.buttons-container`:

```html
<a href="language-novo-restaurante.html" class="menu-button">
    <svg class="icon" xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
        <line x1="4" x2="20" y1="12" y2="12"/>
        <line x1="4" x2="20" y1="6" y2="6"/>
        <line x1="4" x2="20" y1="18" y2="18"/>
    </svg>
    Nome do Novo Restaurante
</a>
```

### Passo 2: Criar Página de Seleção de Idioma
Copie um dos arquivos `language-*.html` e renomeie para `language-novo-restaurante.html`. Atualize:
- O título no `<head>`
- O título `<h1>` com o nome do restaurante
- Os links dos botões de idioma com os links do Google Drive para cada idioma

### Passo 3: Upload dos PDFs no Google Drive
- Faça upload dos PDFs (português, inglês, espanhol) no Google Drive
- Configure as permissões para "Qualquer pessoa com o link pode visualizar"
- Copie os links e substitua nos botões da página de idioma

## 🌍 Como Adicionar um Novo Idioma

Para adicionar um novo idioma (exemplo: Francês):

### Passo 1: Atualizar Páginas de Idioma
Em cada arquivo `language-*.html`, adicione um novo botão:

```html
<a href="https://drive.google.com/file/d/SEU_LINK_AQUI_FR/view" target="_blank" class="menu-button">
    <svg class="icon" xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
        <path d="m5 8 6 6"/>
        <path d="m4 14 6-6 2-3"/>
        <path d="M2 5h12"/>
        <path d="M7 2h1"/>
        <path d="m22 22-5-10-5 10"/>
        <path d="M14 18h6"/>
    </svg>
    Français
</a>
```

### Passo 2: Adicionar os PDFs no Google Drive
- Faça upload do PDF em francês no Google Drive
- Configure as permissões
- Substitua `SEU_LINK_AQUI_FR` pelo link real do arquivo

## 🚀 Como Usar o Site

1. Abra `index.html` no navegador
2. Escolha um dos 4 restaurantes disponíveis
3. Selecione o idioma preferido (Português, Inglês ou Espanhol)
4. O cardápio será aberto no Google Drive em uma nova aba
5. Use o botão "Voltar" para escolher outro restaurante ou idioma

## 🎨 Personalização de Cores

Para alterar as cores do site, edite o arquivo `css/style.css`:

```css
body {
  background-color: #003448;  /* Cor de fundo principal */
  color: #ede9da;            /* Cor do texto */
}

.logo-circle {
  border: 4px solid #ede9da; /* Cor da borda do logo */
}

.menu-button {
  border: 2px solid #ede9da; /* Cor da borda dos botões */
  color: #ede9da;            /* Cor do texto dos botões */
}

.menu-button:hover {
  background-color: #ede9da; /* Cor de fundo ao passar o mouse */
  color: #003448;            /* Cor do texto ao passar o mouse */
}
```

## 📱 Responsividade

O site é totalmente responsivo e se adapta a diferentes tamanhos de tela:
- **Desktop**: Layout amplo com botões grandes
- **Tablet**: Layout otimizado para toque
- **Mobile**: Design focado em mobile-first, com tamanhos ajustados

## 🔧 Tecnologias

- **HTML5**: Estrutura semântica e simples
- **CSS3**: Estilos modernos com flexbox
- **SVG**: Ícones vetoriais inline
- **Google Drive**: Hospedagem e visualização dos PDFs

## 📝 Notas Importantes

- Não é necessário hospedar os PDFs localmente - tudo via Google Drive
- O logo deve estar em `public/restaurant-logo.png`
- Todos os arquivos HTML devem estar na raiz do projeto
- O site funciona sem necessidade de servidor - pode abrir diretamente no navegador
- Para hospedar online, basta fazer upload de todos os arquivos para um servidor web ou Netlify/Vercel
- Os PDFs são abertos em uma nova aba usando o visualizador do Google Drive
