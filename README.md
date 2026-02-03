# KarolDev - Portfolio Pessoal

Site pessoal de Karol Albuquerque, desenvolvedora especializada em soluções modernas e de alta performance.

## 📋 Descrição

Este é um site portfolio moderno e responsivo desenvolvido com HTML, CSS e JavaScript puro. O design segue um tema **Tech + Feminino**, combinando tons de roxo, rosa neon, azul neon e detalhes futuristas leves para criar uma experiência visual elegante e profissional.

## 🚀 Tecnologias Utilizadas

- **HTML5** - Estrutura semântica
- **CSS3** - Estilização com Flexbox, Grid e animações
- **JavaScript (Vanilla)** - Interatividade e animações de scroll
- **Google Fonts** - Tipografia Poppins

## 📁 Estrutura de Pastas

```
Site portfolio Karol/
│
├── index.html              # Página principal
├── style.css               # Estilos do site
├── script.js               # Scripts e interatividade
├── README.md               # Este arquivo
│
└── assets/                 # Arquivos estáticos
    ├── favicon.svg         # Favicon do site
    └── placeholder-profile.png  # Foto de perfil (temporária)
```

## 🌐 Deploy no GitHub Pages

Para hospedar este site no GitHub Pages, siga estes passos:

1. **Criar um repositório no GitHub**
   - Nome recomendado: `karoldev.github.io` (para URL personalizada)
   - Ou qualquer nome (será acessível em `usuario.github.io/nome-do-repo`)

2. **Enviar os arquivos para o repositório**
   ```bash
   git init
   git add .
   git commit -m "Initial commit - Portfolio site"
   git branch -M main
   git remote add origin https://github.com/SEU-USUARIO/SEU-REPOSITORIO.git
   git push -u origin main
   ```

3. **Ativar o GitHub Pages**
   - Vá em **Settings** > **Pages**
   - Em **Source**, selecione a branch `main` e pasta `/ (root)`
   - Clique em **Save**
   - Aguarde alguns minutos para o site ficar disponível

4. **Acessar o site**
   - URL: `https://SEU-USUARIO.github.io/SEU-REPOSITORIO`
   - Ou `https://karoldev.github.io` (se usar o nome especial)

## ✏️ Como Personalizar

### Substituir a Foto de Perfil

1. Substitua o arquivo `assets/placeholder-profile.png` pela sua foto
2. **Importante**: Mantenha o mesmo nome do arquivo (`placeholder-profile.png`) ou atualize a referência no `index.html` (linha 58)
3. Recomendações:
   - Formato: PNG ou JPG
   - Tamanho: 400x400 pixels (ou proporção quadrada)
   - Peso: Otimize para web (< 200KB)
   - Use um editor online como [TinyPNG](https://tinypng.com/) para comprimir a imagem

### Alterar Textos

1. Abra o arquivo `index.html`
2. Edite os textos nas seguintes seções:
   - **Hero**: Linhas 31-33 (título e subtítulo)
   - **Sobre Mim**: Linhas 43-53 (textos sobre você)
   - **Serviços**: Linhas 62-88 (descrições dos serviços)
   - **Portfólio**: Linhas 97-133 (projetos e descrições)
   - **Contato**: Linha 145 (texto de contato)

### Personalizar Cores

As cores estão definidas como variáveis CSS no início do arquivo `style.css`:

```css
:root {
    --color-primary: #8B5CF6;      /* Roxo principal */
    --color-secondary: #EC4899;    /* Rosa neon */
    --color-accent: #06B6D4;       /* Azul neon */
    --color-dark: #1E1B2E;         /* Preto/Violeta escuro */
    --color-darker: #0F0B1A;       /* Preto mais escuro */
}
```

Para alterar as cores:
1. Abra `style.css`
2. Localize as variáveis `:root` (linhas 9-16)
3. Altere os valores hexadecimais conforme sua preferência
4. Os gradientes serão ajustados automaticamente

### Atualizar Links de Contato

1. **WhatsApp**: Edite a linha 185 em `index.html`
   ```html
   <a href="https://wa.me/5562982287887" ...>
   ```
   Substitua `5562982287887` pelo seu número (formato: código do país + DDD + número)

2. **LinkedIn**: Edite a linha 189 em `index.html`
   ```html
   <a href="https://www.linkedin.com/in/karoline-albuquerque-7b59b253/" ...>
   ```
   Substitua pela sua URL do LinkedIn

### Configurar Formulário de Contato (EmailJS)

O formulário de contato usa **EmailJS** para enviar mensagens diretamente para seu e-mail. Siga estes passos:

1. **Criar conta no EmailJS**
   - Acesse [https://www.emailjs.com/](https://www.emailjs.com/)
   - Crie uma conta gratuita (plano gratuito permite 200 emails/mês)

2. **Configurar Serviço de Email**
   - No dashboard, vá em **Email Services**
   - Clique em **Add New Service**
   - Escolha seu provedor (Gmail, Outlook, etc.)
   - Siga as instruções para conectar sua conta de email
   - **Anote o Service ID** gerado

3. **Criar Template de Email**
   - Vá em **Email Templates**
   - Clique em **Create New Template**
   - Use este template básico:
     ```
     Assunto: {{subject}}
     
     Nova mensagem do portfolio:
     
     Nome: {{from_name}}
     Email: {{from_email}}
     Assunto: {{subject}}
     
     Mensagem:
     {{message}}
     ```
   - **Anote o Template ID** gerado

4. **Obter Public Key**
   - Vá em **Account** > **General**
   - Copie sua **Public Key**

5. **Configurar no Código**
   - Abra o arquivo `script.js`
   - Localize as linhas 5-7 e substitua:
     ```javascript
     const EMAILJS_SERVICE_ID = 'YOUR_SERVICE_ID'; // Cole seu Service ID aqui
     const EMAILJS_TEMPLATE_ID = 'YOUR_TEMPLATE_ID'; // Cole seu Template ID aqui
     const EMAILJS_PUBLIC_KEY = 'YOUR_PUBLIC_KEY'; // Cole sua Public Key aqui
     ```

6. **Testar**
   - Envie uma mensagem de teste pelo formulário
   - Verifique se chegou no seu email

**Pronto!** Agora todas as mensagens do formulário serão enviadas para seu email automaticamente.

### Adicionar Mais Projetos ao Portfólio

1. No arquivo `index.html`, localize a seção `portfolio__grid` (linha 103)
2. Copie um dos blocos `portfolio__card`
3. Altere título, descrição e tags conforme necessário

## 🎨 Características do Design

- ✅ Design responsivo (Desktop, Tablet e Mobile)
- ✅ Animações suaves de fade-in ao rolar a página
- ✅ Menu mobile com animação
- ✅ Efeitos hover interativos
- ✅ Gradientes e sombras neon
- ✅ Tipografia moderna (Poppins)
- ✅ Código limpo e comentado

## 📱 Compatibilidade

O site foi testado e é compatível com:
- Chrome/Edge (últimas versões)
- Firefox (últimas versões)
- Safari (últimas versões)
- Navegadores mobile (iOS Safari, Chrome Mobile)

## 🔧 Melhorias Futuras (Opcional)

Algumas sugestões para expandir o projeto:
- Adicionar formulário de contato funcional (ex: Formspree, EmailJS)
- Implementar modo escuro/claro
- Adicionar mais seções (certificados, depoimentos, etc.)
- Integrar com API de GitHub para mostrar repositórios
- Adicionar blog ou artigos

## 📝 Licença

Este projeto é de uso pessoal. Sinta-se livre para usar como inspiração para seus próprios projetos.

## 🔗 Link do Repositório

Repositório: [Adicione o link do seu repositório aqui]

---

**Desenvolvido com 💜 por Karol Albuquerque**

