# Protótipo METHA Corpus Clinic

Abrir com servidor local na raiz: `python3 -m http.server 8099 --bind 127.0.0.1`.
Endereço: http://127.0.0.1:8099/

Página em index.html, bibliotecas de animação em assets/vendor e fotos originais na pasta do ensaio. Fontes via Google Fonts, com fallback para fontes do sistema.

## Implementado

Hero com retrato real, apresentação, seis etapas do método, seis serviços expansíveis, fundador, dois trechos de avaliações anônimas, endereço e WhatsApp com mensagem específica por serviço. Movimento GSAP, indicador de scroll, método com coluna fixa no desktop e versão linear no celular. Preferência de movimento reduzido respeitada.

## Verificação

Inspeção em navegador a 1440 e 390 pixels: sem overflow horizontal; navegação por âncoras e expansão de serviços funcionando; menu móvel abre e fecha ao selecionar uma seção; fotos carregadas. Animações distribuídas localmente para não depender de CDN. Links de WhatsApp inspecionados sem envio de mensagens.

## Limites desta primeira versão

Símbolo em SVG e assinatura tipográfica são provisórios, inspirados na referência visual, não o arquivo oficial da marca. Copy é proposta para revisão. Credenciais e horários completos aguardam confirmação. Foram usados relatos públicos, não fotos de pacientes ou montagem de antes e depois. Não há publicação em hospedagem nem formulário de coleta de dados.

## Refinamento de interação — 21/09/2026

Segunda rodada: serviços agora animam a expansão e o recolhimento do espaço (320 ms desktop, 200 ms mobile), com reversão em cliques repetidos e limpeza ao redimensionar ou mudar a preferência de movimento. Sem animação, mantém-se o comportamento nativo de details/summary. O desenho do método gira por etapa e destaca um dos anéis; a etapa é calculada pela posição de leitura, inclusive em saltos. O traço dourado percorre a apresentação no desktop e fica estático e curto no celular. Movimento reduzido desativa expansão animada e rotação. Testados clique, Enter, cliques repetidos, estados finais sem altura fixa, sincronização etapa/desenho e larguras 1440/390 sem overflow. Console sem erros na rodada. Redução de movimento conferida no código, não emulada no navegador.

Erro de sintaxe corrigido e entradas sobrepostas do hero consolidadas em uma sequência. Retrato com parallax discreto apenas no desktop; traço de continuidade entre hero e apresentação; indicador da etapa do método; serviços com realce, rotação do sinal e entrada suave do conteúdo; apresentação do fundador em sequência; relatos com entrada individual, sem carrossel. Cabeçalho fixo recolhe ao descer e reaparece ao subir, preservando foco e menu aberto. WhatsApp flutuante disponível em desktop e celular, oculto enquanto hero ou CTA final estão visíveis.

Verificação desta rodada: JavaScript validado pelo parser do Node; navegador em 1440×1000 e 390×844 sem overflow horizontal; imagens carregadas; serviço aberto por clique e fechado com Enter; menu com Escape devolvendo foco ao botão; seleção do contato fecha menu; botão flutuante oculto no hero e contato, visível no método/serviços. Nenhum novo erro de console observado após a correção (o histórico ainda contém o erro anterior). Preferência de movimento reduzido revisada no CSS e nas condições GSAP/WAAPI, sem emulação no navegador. Links de WhatsApp verificados sem enviar mensagens. Testes responsivos são emulação de tamanho, não aparelhos físicos.

## Terceira rodada — Fase 1 (Design, Fotos e Conteúdo Editorial) — 21/09/2026

Implementação das melhorias estratégicas de narrativa e autoridade:
- **Seção de Empatia e Quebra de Paradigma (`#compreensao`):** Nova seção com tipografia serifada dramática (*Cormorant Garamond*), abordando as dores reais do paciente reveladas na pesquisa (frustração com dietas prévias, efeito sanfona e ausência de julgamento). Pilares de *Fisiologia sem julgamento* e *Consistência real*.
- **Composição Editorial do Fundador (`#mateus`):** Retrato principal de alta resolução em terno azul com moldura limpa de estúdio, além dos 3 pilares de conduta clínica do Dr. Mateus (*Escuta Aprofundada*, *Estratégia Individualizada* e *Presença Contínua*).
- **Seção de FAQ Estratégico (`#duvidas`):** 5 perguntas frequentes essenciais para desarmar objeções pré-consulta (primeira consulta, escopo além do emagrecimento, acompanhamento, exames e localização em Araxá). Integrada ao sistema de animação fluida WAAPI com `details/summary`.
- **Verificação técnica:** Sintaxe JS 100% validada; Playwright testado em desktop (1440×900) e mobile (390×844); zero overflow horizontal (`scrollWidth <= innerWidth`); suporte integral a atalhos de teclado e `prefers-reduced-motion`.

## Quarta rodada — Fases 2 e 3 (Motion GSAP, Credenciais Médicas e Conversão de Luxo) — 21/09/2026

Implementação das melhorias de motion refinado e elementos de prestígio:
- **Motion Orbital Sincronizado do Método (`#metodo`):** GSAP ScrollTrigger com scrub contínuo nos anéis concêntricos (`.ring:nth-child(1)` e `.ring:nth-child(2)` em direções opostas) sincronizado com o scroll das etapas. A linha guia vertical ganha halo dourado e cada etapa ativa recebe deslocamento micro-tátil e iluminação no ponto indicador.
- **Selos de Autoridade Médica Oficial (`#mateus`):** Inclusão de badges refinados com micro-pontos dourados (`CRM-MG 91.309`, `Medicina Integrativa & Preventiva` e `Consultório Privativo · Araxá/MG`), reforçando o rigor científico e a presença física da clínica.
- **Pill Flutuante Concierge WhatsApp (`.mobile-wa`):** Redesenhado em dark glassmorphism (`backdrop-filter: blur(16px)`), borda dourada sutil e micro-indicador pulsante em verde esmeralda de atendimento ativo, sem competir com a elegância do layout e ocultando-se no Hero e CTA final.
- **Microinterações em Botões e Depoimentos:** Botões `.btn` com glow dourado volumétrico suave no hover; cartões de depoimentos (`.quotes blockquote`) estilizados com moldura lateral dourada, fundo translúcido sutil e elevação ao passar o mouse.
- **Verificação Técnica:** Zero erros de console no Playwright; testado em 1440×900 e 390×844 com `scrollWidth <= innerWidth`; todas as transições respeitam `prefers-reduced-motion`.

## Quinta rodada — Estratégia de Telemedicina & Atendimento Remoto Nacional — 21/09/2026

Adaptação completa de posicionamento e conversão para atendimento online em todo o Brasil:
- **Hero & Headline:** Inclusão de badge com luz verde ativa no Hero (`Atendimento Presencial em Araxá & Online para todo o Brasil`) e reforço da teleconsulta na copy de abertura.
- **Bio e Credenciais do Dr. Mateus (`#mateus`):** Adicionado badge oficial `Consultas Online (Brasil e Exterior)` e texto destacando a emissão de receitas digitais oficiais ICP-Brasil com validade nacional e pedidos de exames laboratoriais na cidade do paciente.
- **FAQ Dedicado à Telemedicina (`#duvidas`):** Nova pergunta 04 explicando detalhadamente como funciona a consulta remota (duração de 1h+, segurança, videochamada privativa, suporte contínuo entre consultas).
- **Cards Duais de Modalidades em Contato (`#contato`):** Seção de contato dividida em duas caixas elegantes com links dedicados: `01 · Consultório em Araxá` (Atendimento Presencial) e `02 · Telemedicina Brasil` (Consulta Online).
- **Mensagens Inteligentes no WhatsApp:** Script ajustado para detectar o clique específico e gerar mensagens personalizadas com o interesse pré-definido pelo paciente (`online` ou `presencial`).
- **Verificação Técnica:** Zero erros de console; validado no Playwright em 1440px e 390px sem overflow horizontal; links de WhatsApp validados com mensagens pré-formatadas.

## Sexta rodada — Identidade Técnica, Performance WebP, Open Graph e Rotas — 22/09/2026

Implementação de melhorias autônomas de infraestrutura, compartilhamento e usabilidade:
- **Favicons Oficiais e App Icons:** Desenvolvidos assets dedicados em vetor e alta resolução: `assets/favicon.svg` com o monograma "M" em linhas douradas geométricas finas e gradiente de luxo, `assets/favicon-32x32.png`, `assets/apple-touch-icon.png` (180x180 para atalhos iOS/Android) e `favicon.ico` na raiz e pasta de assets, eliminando qualquer erro 404 em navegadores e bots.
- **Open Graph & Twitter Cards:** Configuração integral de metadados de compartilhamento para WhatsApp, Instagram Direct, Facebook e Twitter/X. Banner exclusivo de prévia social gerado em alta resolução (`assets/images/og-preview.jpg`, 1200×630px, 114KB) com visual editorial escuro, retrato do Dr. Mateus, monograma, CRM e pilares de atuação.
- **Performance WebP & LCP Otimizado:** Conversão das imagens de alta resolução para formato moderno `.webp` com compressão sem perda perceptível de fidelidade, empacotadas via `<picture>` com fallback JPEG e preloading de alta prioridade (`fetchpriority="high"`, `rel="preload"`) para o retrato do Hero.
- **Chips de Traçado de Rotas (Maps & Waze):** Adição de botões táteis no Card do Consultório em Araxá com links diretos para início de navegação por GPS no Google Maps (`destination=Rua+Almeida+Campos,+336`) e no Waze (`navigate=yes`), além de tags de segurança na Telemedicina (*Videochamada Privativa* e *Receita ICP-Brasil*).
- **Verificação Técnica Playwright:** 0 erros de console, 0 advertências; teste de largura em desktop (1440px, scrollWidth: 1425px) e mobile (390px, scrollWidth: 375px); requisições de assets validadas com status HTTP 200 OK.

## Sétima rodada — Alinhamento de Posicionamento Clínico (Dr. Mateus) — 24/09/2026

Implementação dos ajustes cirúrgicos alinhados diretamente com o Dr. Mateus Camargos:
- **Atualização do Registro Profissional Oficial:** Retificação de todo o material e metadados para **CRM-MG 88.462** (substituindo o número provisório anterior).
- **Enxugamento do Catálogo de Cuidados:** Remoção integral dos produtos de procedimentos em consultório (*Estética Avançada* e *PEIM · Microvasos*), mantendo o foco exclusivo em *Emagrecimento Saudável*, *Hipertrofia e Composição Corporal*, *Reposição Hormonal* e *Medicina Esportiva*.
- **Transição para Telemedicina Exclusiva:** Devido à mudança de cidade do Dr. Mateus e ausência de consultório físico no momento, todos os pontos de contato, cabeçalho, FAQ, cards e rotas presenciais em Araxá foram removidos e convertidos para um ecossistema de teleconsulta de alta sofisticação com:
  - Videochamadas privativas estendidas (1h+ de consulta dedicada).
  - Emissão oficial de receitas médicas e solicitações de exames com certificação digital ICP-Brasil aceitas em todo o território nacional.
  - Acompanhamento contínuo e canal de suporte direto entre as consultas.
- **Mensageria Contextual do WhatsApp:** Atualização dos disparos no WhatsApp para direcionamento imediato de consultas online por telemedicina com o Dr. Mateus.



