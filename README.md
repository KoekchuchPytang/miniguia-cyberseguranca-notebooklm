# 🔐 Miniguia de Estudos: Segurança da Informação com NotebookLM

Este repositório documenta a criação de um **Caderno Temático no NotebookLM** sobre Segurança da Informação / Cibersegurança, desenvolvido como projeto prático de um bootcamp da DIO. O objetivo foi usar a Inteligência Artificial como ferramenta de aprendizagem ativa, aliando curadoria de fontes, pensamento crítico e engenharia de prompts.

---

## 🎯 Contexto e Objetivos

O tema escolhido foi **Segurança da Informação / Cibersegurança**, por ser um assunto relevante tanto para usuários comuns quanto para profissionais de tecnologia, cobrindo desde comportamento individual até gestão de risco corporativa.

**Objetivos de estudo com este material:**
- Compreender os principais conceitos de segurança da informação, do nível básico (usuário final) ao avançado (gestão de risco organizacional).
- Entender como ameaças comuns (phishing, malware, engenharia social) se conectam a vulnerabilidades técnicas (OWASP) e frameworks de governança (NIST).
- Praticar o uso de IA generativa (NotebookLM) como ferramenta de curadoria, síntese e revisão de conteúdo técnico.
- Criar um material de consulta rápida (glossário + prompts reutilizáveis) para revisões futuras sobre o tema.

---

## 📚 Curadoria de Fontes

Foram selecionadas e carregadas no NotebookLM **5 fontes abertas**, escolhidas para cobrir três camadas complementares: comportamento do usuário, vulnerabilidades técnicas e gestão de risco organizacional.

| Fonte | Tipo | Camada | Link |
|---|---|---|---|
| Cartilha de Segurança — Golpes na Internet (CERT.br) | PDF | Usuário / Comportamental | https://cartilha.cert.br/fasciculos/golpes/fasciculo-golpes.pdf |
| Cartilha de Segurança — Códigos Maliciosos (CERT.br) | PDF | Usuário / Comportamental | https://cartilha.cert.br/fasciculos/codigos-maliciosos/fasciculo-codigos-maliciosos.pdf |
| Cartilha de Segurança — Privacidade (CERT.br) | PDF | Usuário / Dados | https://cartilha.cert.br/fasciculos/privacidade/fasciculo-privacidade.pdf |
| OWASP Top 10 (2021) | PDF | Técnico / Desenvolvimento | https://www.hhs.gov/sites/default/files/owasp-top-10.pdf |
| NIST Cybersecurity Framework (CSF) 2.0 | PDF | Estratégico / Governança | https://nvlpubs.nist.gov/nistpubs/CSWP/NIST.CSWP.29.pdf |

> As fontes foram escolhidas propositalmente para representar públicos diferentes: cidadão comum (CERT.br), desenvolvedor/técnico (OWASP) e gestor/executivo (NIST) — permitindo uma visão de 360° sobre o tema.

---

## 🧠 Engenharia de Prompts e "Cicatrizes"

Abaixo estão documentados os prompts testados no NotebookLM, as respostas obtidas e as observações de cada teste.

### Prompt 1 — Visão geral e conexões entre fontes

**Prompt utilizado:**
```
Com base nas fontes fornecidas, faça um resumo geral 
conectando os principais temas de segurança da informação 
abordados, identificando pontos em comum entre elas.
```

**Resultado:** ✅ Funcionou bem na primeira tentativa.

O NotebookLM organizou a resposta em 3 pilares (Governança/NIST, Técnico/OWASP, Humano/CERT.br) e identificou conexões concretas entre as fontes, como o "Princípio do Privilégio Mínimo" aparecendo nos três documentos com abordagens diferentes.

**Observação:** não foi necessário refinar o prompt — a resposta já veio estruturada e referenciada às fontes de origem.

---

### Prompt 2 — Comparação entre abordagens das fontes

**Prompt utilizado:**
```
Compare a abordagem da Cartilha CERT.br (mais voltada ao 
usuário comum) com a abordagem técnica do OWASP Top 10 e 
do NIST Framework (mais voltadas a profissionais/empresas). 
Quais complementos cada uma oferece?
```

**Resultado:** ✅ Resposta muito bem estruturada.

O NotebookLM organizou a comparação em 3 camadas de público-alvo (usuário final, desenvolvedor, gestor) e trouxe uma síntese sobre complementaridade: NIST dá a estratégia, OWASP preenche a lacuna técnica, e a Cartilha atua na "linha de frente" comportamental.

**Observação:** pedir explicitamente "quais complementos cada uma oferece" ajudou a IA a não apenas listar diferenças, mas explicar o valor único de cada fonte.

---

### Prompt 3 — Cenário de ataque aplicado

**Prompt utilizado:**
```
Crie um cenário de ataque de engenharia social (phishing) 
e explique, com base nas fontes, como cada camada de defesa 
mencionada (usuário, aplicação, gestão) poderia ter evitado 
o incidente.
```

**Resultado:** ✅ Resposta muito completa e bem referenciada.

A IA criou um cenário fictício e realista ("recadastramento de token bancário/corporativo") e explicou como cada camada poderia evitá-lo, citando inclusive códigos técnicos exatos das normas (ex: OWASP A07:2021, NIST PR.AT, GV.PO, RS.MA).

**Observação:** o uso de referências técnicas específicas (não apenas texto genérico) validou a qualidade da curadoria de fontes escolhida.

---

### Prompt 4 — Glossário de conceitos

**Prompt utilizado:**
```
Liste os 15 termos técnicos mais importantes mencionados 
nas fontes, com definição curta de cada um, organizados 
em ordem alfabética.
```

**Resultado:** ✅ Resposta completa e bem organizada, praticamente pronta para uso direto no miniguia final (ver seção Glossário abaixo).

**Observação:** o glossário misturou termos de nível básico (Firewall, Backup) com termos técnicos avançados (CWE, Injection), refletindo o equilíbrio das fontes escolhidas.

---

### Prompt 5 — Roteiro de estudo progressivo

**Prompt utilizado:**
```
Crie um roteiro de estudo em tópicos, do nível básico ao 
avançado, para alguém que quer entender segurança da 
informação do zero até conceitos de gestão de risco (NIST) 
e vulnerabilidades técnicas (OWASP).
```

**Resultado:** ✅ Resposta muito bem estruturada, organizada em 3 fases progressivas (básico → intermediário → avançado).

**Observação geral sobre os 5 testes:** nenhum prompt precisou de refinamento ou re-tentativa. Isso indicou que, neste caderno, a "engenharia de prompt" foi mais decisiva na **fase de curadoria das fontes e na formulação clara da pergunta inicial** do que em ajustes reativos de troubleshooting — uma boa fonte bem selecionada tende a gerar respostas precisas de primeira.

**Dificuldade real encontrada:** o principal desafio não foi na obtenção das respostas, mas sim na **etapa de curadoria** — havia mais de 20 fascículos disponíveis do CERT.br, e foi necessário filtrar e escolher apenas os mais relevantes (golpes, códigos maliciosos e privacidade) para não sobrecarregar o caderno com fontes redundantes e manter o foco do estudo.

---

## 📖 Miniguia de Estudo (Entrega Final)

### Resumo Estruturado

A segurança da informação pode ser entendida em **três camadas complementares**:

**1. Camada Comportamental (Usuário)**
O ser humano é frequentemente o elo mais explorado em ataques cibernéticos. Golpes de engenharia social manipulam emoções como medo, urgência e curiosidade para induzir vítimas a fornecer dados sensíveis ou instalar códigos maliciosos. Boas práticas incluem: verificação de canais oficiais, uso de autenticação multifator, atenção a sinais de phishing e cuidados com privacidade em redes sociais.

**2. Camada Técnica (Desenvolvimento e Aplicações)**
O OWASP Top 10 cataloga as vulnerabilidades mais críticas em aplicações web, como falhas de controle de acesso, criptografia inadequada, injeção de código e configurações incorretas. A prevenção depende de práticas de desenvolvimento seguro (SDLC), atualização de componentes e monitoramento contínuo de logs.

**3. Camada Estratégica (Governança e Gestão de Risco)**
O NIST Cybersecurity Framework 2.0 organiza a segurança em seis funções: Governar, Identificar, Proteger, Detectar, Responder e Recuperar. Essa camada conecta a tecnologia aos objetivos de negócio, definindo políticas, treinamentos, gestão de fornecedores e planos de resposta a incidentes.

**Síntese:** a defesa robusta em cibersegurança exige a integração dessas três camadas — o NIST fornece a estratégia, o OWASP preenche as lacunas técnicas, e a educação do usuário (CERT.br) atua como linha de frente contra manipulações.

---

### Glossário

| Termo | Definição |
|---|---|
| **Antivírus (Antimalware)** | Ferramentas que detectam, previnem e removem códigos maliciosos de dispositivos. |
| **Autenticação Multifator (MFA)** | Mecanismo que exige identificação adicional além da senha para proteger o acesso. |
| **Backdoor** | Programa que permite o retorno de um invasor a um dispositivo já comprometido. |
| **Backup** | Cópia de segurança de dados para permitir recuperação após perda ou ataque. |
| **Botnet** | Rede de dispositivos infectados ("zumbis") usada para potencializar ataques em larga escala. |
| **Criptografia** | Tecnologia que cifra dados para que só possam ser lidos por quem tem autorização. |
| **CWE (Common Weakness Enumeration)** | Catálogo comunitário de fraquezas comuns em software e hardware. |
| **Engenharia Social** | Manipulação psicológica que explora emoções para obter dados ou ações da vítima. |
| **Firewall** | Mecanismo que monitora o tráfego de rede e bloqueia acessos indevidos. |
| **Injeção (Injection)** | Falha em que dados não confiáveis são enviados a um interpretador (ex: SQL Injection). |
| **Malware (Código Malicioso)** | Termo genérico para programas criados para executar ações danosas em dispositivos. |
| **Princípio do Privilégio Mínimo** | Diretriz que recomenda conceder apenas o nível de acesso estritamente necessário. |
| **Ransomware** | Malware que torna dados inacessíveis (geralmente via criptografia) e exige resgate. |
| **Rootkit** | Conjunto de técnicas que esconde a presença contínua de um invasor em um sistema. |
| **Spyware** | Software espião que monitora atividades e envia dados a terceiros sem autorização. |

---

### Prompts Reutilizáveis para Revisões Futuras

```
1. Resumo geral e conexões entre fontes:
"Com base nas fontes fornecidas, faça um resumo geral 
conectando os principais temas de [ASSUNTO] abordados, 
identificando pontos em comum entre elas."

2. Comparação entre abordagens:
"Compare a abordagem de [FONTE A] com a de [FONTE B]. 
Quais complementos cada uma oferece?"

3. Cenário aplicado:
"Crie um cenário prático de [SITUAÇÃO] e explique, com 
base nas fontes, como diferentes camadas de defesa/atuação 
poderiam lidar com esse caso."

4. Glossário rápido:
"Liste os 15 termos técnicos mais importantes mencionados 
nas fontes, com definição curta de cada um, organizados 
em ordem alfabética."

5. Roteiro de estudo progressivo:
"Crie um roteiro de estudo em tópicos, do nível básico ao 
avançado, sobre [ASSUNTO], cobrindo desde conceitos 
introdutórios até tópicos avançados de [ÁREA ESPECÍFICA]."
```

---

## 🛠️ Ferramentas Utilizadas

- [NotebookLM](https://notebooklm.google.com) — criação do caderno temático e testes de prompts
- [GitHub](https://github.com) — versionamento e publicação do projeto

---

## ✅ Conclusão

Este projeto demonstrou como o NotebookLM pode ser usado como ferramenta de aprendizagem ativa, permitindo sintetizar múltiplas fontes técnicas em um material de estudo coeso. A principal lição foi que a **qualidade da curadoria de fontes** impacta diretamente a qualidade das respostas geradas — prompts bem formulados sobre fontes bem selecionadas tendem a gerar resultados precisos já na primeira tentativa.
