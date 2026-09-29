# STATUS_DO_PROJETO.md — METHA Corpus Clinic

**Documento Oficial de Registro, Arquitetura e Continuidade de Trabalho**  
*Última atualização: 29 de setembro de 2026*  
*Responsável Técnico: Thales Machado Sousa (U.AI Technologies / METHA Corpus Clinic)*  
*Cliente / Autoridade: Dr. Mateus Camargos (CRM-MG 88.462)*  
*Repositório GitHub:* `thalesmsousa10/methacorpus-clinic` (Branch `main`)

---

## 1. 📌 Resumo Executivo & Posicionamento

A **METHA Corpus Clinic** é uma clínica de medicina integrativa e de precisão especializada em emagrecimento definitivo, modulação hormonal, hipertrofia e longevidade, liderada pelo **Dr. Mateus Camargos**.

### A Grande Virada Metodológica (Playbook 2026):
A comunicação do projeto foi completamente reformulada a partir do Playbook oficial da clínica, rompendo com o discurso genérico de dieta/disciplina e adotando uma tese científica e humanizada:
- **O Acordo Oculto:** O corpo não é o problema; ele é a resposta biológica. O excesso de peso é uma solução adaptativa inconsciente que o corpo encontrou para proteger a mente de feridas e sobrecargas emocionais.
- **As 3 Funções Biológicas do Peso:**
  1. *Blindagem (Proteção):* Barreira física contra vulnerabilidade, julgamento ou invasão.
  2. *Sobrecarga (Força):* Ganho de densidade para suportar rotinas exaustivas sem pedir ajuda.
  3. *Afeto (Preenchimento):* Volume para ser visto e uso do alimento como refúgio de solidão.
- **A Metodologia dos Dois Cardápios:**
  - *Cardápio Alimentar & Metabólico (No Prato):* Manejo farmacológico moderno criterioso (tirzepatida/Mounjaro), exames de precisão, preservação de massa magra.
  - *Cardápio Emocional & Comportamental (Ao Redor do Prato):* Desmonte da função protetora do peso e desativação dos gatilhos comportamentais para cessar o efeito sanfona.
- **Telemedicina de Alto Padrão:**
  - Consultas individuais profundas (1h+ de imersão).
  - Emissão de receitas médicas digitais oficiais com assinatura digital ICP-Brasil com validade jurídica em todo o território nacional.

---

## 2. 🌐 Links Públicos Ativos (GitHub Pages)

| Versão | Descrição | Link de Visualização |
|---|---|---|
| **Site de Produção Atual** | Versão anterior preservada (estável na raiz) | [Acessar Produção](https://thalesmsousa10.github.io/methacorpus-clinic/) |
| **Proposta Dark Luxury** | Nova copy completa, Leitura Corporal e Dois Cardápios (fundo escuro) | [Acessar Proposta Dark](https://thalesmsousa10.github.io/methacorpus-clinic/proposta.html) |
| **Proposta Light Linen** | Versão em linho nobre suave, cards alvos e ouro bronze de alto contraste | [Acessar Proposta Light](https://thalesmsousa10.github.io/methacorpus-clinic/proposta-light.html) |

> **Nota:** As páginas `proposta.html` e `proposta-light.html` contam com um **alternador de temas em pílula integrado no cabeçalho** (`☀️ Versão Clara` / `🌙 Versão Escura`), permitindo testar a experiência visual com 1 toque no celular ou desktop.

---

## 3. 📂 Arquitetura de Arquivos no Repositório

```text
/Users/machado/Downloads/Site METHACORPUS - Antigravity/
├── index.html                    # Site estável em produção no GitHub Pages
├── proposta.html                 # Nova proposta com copy agressiva e tema Dark Luxury
├── proposta-light.html           # Nova proposta em tema Light Linen (alta legibilidade)
├── STATUS_DO_PROJETO.md          # Este documento (guia executivo de continuidade)
├── PROTOTIPO.md                  # Diário cronológico detalhado de todas as 9 rodadas de engenharia
├── README.md                     # Visão geral do repositório
├── favicon.svg                   # Favicon vetorial com o monograma da marca em alta definição
├── favicon.ico                   # Favicon multi-camada (16x16, 32x32, 48x48)
│
├── assets/
│   ├── favicon.svg               # Cópia para caminho relativo
│   ├── favicon.ico               # Cópia para caminho relativo
│   ├── favicon-16x16.png         # Ícone 16x16 antialiased
│   ├── favicon-32x32.png         # Ícone 32x32 antialiased
│   ├── apple-touch-icon.png      # Ícone oficial para iOS e Android (180x180 px)
│   │
│   ├── images/
│   │   ├── og-preview.jpg        # Open Graph Card oficial para WhatsApp/Redes (1200x630 px)
│   │   ├── og-preview.png        # Versão PNG do card de compartilhamento
│   │   ├── hero-mateus.webp      # Retrato principal do Dr. Mateus em WebP
│   │   ├── hero-mateus.jpg       # Fallback JPEG para navegadores antigos
│   │   ├── founder-mateus.webp   # Retrato secundário da seção sobre o médico
│   │   └── founder-mateus.jpg    # Fallback JPEG
│   │
│   └── vendor/
│       ├── gsap.min.js           # GreenSock Animation Platform (local, zero dependência CDN)
│       └── ScrollTrigger.min.js  # Plugin ScrollTrigger para animações de scroll
│
├── Fotos Dr Mateus Camargos/     # Fotos originais do ensaio profissional
└── pesquisa/                     # Base da marca, transcrições e documentos de referência
```

---

## 4. ⚖️ Decisões Estratégicas & Diretrizes Médicas (Compliance)

1. **CFM (Conselho Federal de Medicina):**
   - Proibido prometer prazos fixos de emagrecimento ("perca 10 kg em 30 dias"). Todo resultado apresentado é rotulado como resposta biológica individual.
   - Proibida a publicação de fotos de "antes e depois" sem contexto ou como garantia de resultado futuro.
2. **Playbook da METHA Corpus:**
   - Proibido citar jargões internos dos 5 traços de caráter (como *oral*, *masoquista*, *esquizoide*, etc.). O paciente não precisa saber nomes técnicos de psicanálise; ele precisa ter sua dor traduzida com clareza funcional (blindagem, sobrecarga, afeto).
   - Proibido mencionar nomes de terceiros ou escolas externas (como Elton Euler / O Corpo Explica). Toda a autoridade é atribuída ao **Método METHACORPUS** e ao **Dr. Mateus Camargos**.
3. **Registro Profissional Unificado:**
   - Padronizado rigorosamente em **CRM-MG 88.462** em todos os metadados, títulos, micro-chancelas e rodapé.
4. **Mensagens Dinâmicas de WhatsApp:**
   - Os botões de agendamento disparam mensagens já contextualizadas com:
     > *"Olá! Conheci a METHA Corpus Clinic pelo site e gostaria de agendar uma consulta para Leitura Corporal e avaliação médica com o Dr. Mateus."*
   - As especialidades no accordion enviam o nome do serviço clicado diretamente na mensagem.

---

## 5. 🎨 Identidade Visual & Compartilhamento Social

- **Open Graph Card Oficial (`og-preview.jpg` — 1200 × 630 px):**
  - Card institucional com a logo oficial da METHA Corpus reluzente no centro, tipografia imperial *METHA CORPUS · CLINIC* e chancela médica.
  - Safe zone centralizada: funciona perfeitamente tanto no preview retangular tradicional quanto no recorte quadrado (1:1) do WhatsApp.
- **Favicons de Alta Definição:**
  - Vetores e PNGs com amostragem Lanczos, eliminando qualquer pixelização nas abas do Chrome, Safari, Firefox e atalhos de celular.

---

## 6. 🚀 Como Retomar o Trabalho na Próxima Sessão

### Para rodar o ambiente localmente:
Abra o terminal na pasta do projeto e inicie o servidor:
```bash
cd "/Users/machado/Downloads/Site METHACORPUS - Antigravity"
python3 -m http.server 8096 --bind 127.0.0.1
```
Acesse no navegador:
- Dark: `http://127.0.0.1:8096/proposta.html`
- Light: `http://127.0.0.1:8096/proposta-light.html`
- Produção: `http://127.0.0.1:8096/index.html`

### Para promover uma das propostas para produção (`index.html`):
Assim que o Dr. Mateus Camargos validar e aprovar a versão favorita:
- **Se a versão escolhida for a Dark:**
  ```bash
  cp proposta.html index.html
  git add index.html
  git commit -m "feat: promove proposta dark para versao final oficial index.html"
  git push origin main
  ```
- **Se a versão escolhida for a Light:**
  ```bash
  cp proposta-light.html index.html
  git add index.html
  git commit -m "feat: promove proposta light para versao final oficial index.html"
  git push origin main
  ```

---

*Repositório sincronizado e pronto para continuidade imediata.*
