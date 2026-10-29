# Kazan — Landing Page Institucional

Landing page institucional para a **Kazan Indústria e Comércio Ltda.**, fabricante de bolsas de alto padrão em couro legítimo, acrílico, sintéticos e tecidos para grandes marcas do mercado nacional.

## 🛠️ Tecnologias
- [Astro 5](https://astro.build/)
- CSS3 Moderno (Variáveis, Grid & Flexbox, Estética Editorial Monocromática)
- Tipografia: Museo Sans (com fallback para Nunito Sans)

## 📁 Estrutura de Arquivos
```
├── public/
│   ├── images/
│   │   └── logo-kazan.png     # Logo oficial da Kazan
│   └── fonts/                 # Espaço para os arquivos .woff2 da Museo Sans
├── src/
│   ├── components/
│   │   ├── Header.astro       # Navegação com menu responsivo
│   │   ├── Hero.astro         # Seção de abertura com composição fotográfica
│   │   ├── Historia.astro     # História e linha do tempo com foto sticky no scroll
│   │   ├── Proposito.astro    # Missão, Visão e Valores em cards interativos
│   │   ├── Produtos.astro     # Acordeão expansível no hover (4 materiais) + esteira de etapas
│   │   ├── Fotos.astro        # Mosaico da fábrica
│   │   ├── Vagas.astro        # Vagas e carreiras (Google Sheets automático + banco de talentos)
│   │   ├── Contato.astro      # Informações de contato, formulário e rodapé
│   │   └── Photo.astro        # Componente reutilizável de imagem com legenda discreta
│   ├── layouts/
│   │   └── Layout.astro       # Layout base com meta tags e animações suaves
│   ├── pages/
│   │   └── index.astro        # Página principal
│   └── styles/
│       └── global.css         # Paleta oficial Kazan e estilos globais
```

## 🚀 Como Executar Localmente
```bash
# Instalar dependências
npm install

# Rodar servidor de desenvolvimento
npm run dev

# Gerar build de produção
npm run build
```

## 📋 Gestão Automática de Vagas (Google Sheets)
Para que o próprio RH da Kazan atualize as vagas sem necessidade de mexer no código:
1. Crie uma planilha no Google Sheets com as colunas: `Cargo`, `Setor`, `Tipo`, `Status`.
2. Vá em **Arquivo > Compartilhar > Publicar na Web > Escolha o formato CSV**.
3. Copie o link e cole na constante `GOOGLE_SHEETS_CSV_URL` em `src/components/Vagas.astro`.
4. As vagas abertas serão carregadas dinamicamente na página!
