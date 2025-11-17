# Metodologia

Este projeto segue uma abordagem realista, estruturada e inspirada em padrões usados por analistas OSINT corporativos, consultorias de segurança e threat hunters.

## 1. Definição do Objetivo
Realizar um levantamento **não intrusivo** da exposição digital de uma organização real, avaliando:

- Pegada digital pública  
- Infraestrutura exposta  
- Metadados vazados  
- Interconexões tecnológicas  
- Atores humanos visíveis  
- Possíveis vetores de engenharia social  
- Riscos derivados de má configuração  

Tudo dentro de escopo passivo, sem violar Termos de Serviço ou legislação.

---

## 2. Coleta de Domínios e Infraestrutura
Técnicas utilizadas:

- WHOIS / RDAP  
- Extração de registros DNS (A, MX, NS, TXT)  
- Certificados públicos (crt.sh, Censys-like)  
- DNSDumpster  
- Resolução reversa de IP  
- Identificação de provedores (Cloudflare, Vercel, etc.)  
- Banner grabbing passivo  

Avaliação incluiu:

- Datas de criação/expiração  
- Responsáveis públicos  
- Organização vinculada  
- Serviços expostos  
- Estrutura de hospedagem  

---

## 3. Identificação de Tecnologias
Combinação de:

- Wappalyzer  
- WhatRuns  
- Inspeção de cabeçalhos HTTP  
- Fingerprinting de frameworks (Next.js, React, OpenResty, Nginx, Apache etc.)

Objetivo: entender dependências, riscos e possíveis pontos fracos (cookies inseguros, headers ausentes, serviços legados etc.)

---

## 4. Coleta de Artefatos Públicos
Inclui:

- PDFs expostos indexados  
- Documentos internos sem autenticação  
- Arquivos info.php  
- APIs retornando conteúdo público  
- Páginas administrativas acessíveis publicamente  

Nenhum acesso indevido foi realizado, análise puramente observacional.

---

## 5. Footprinting Humano
Somente dados públicos, como:

- Perfis profissionais  
- E-mails institucionais divulgados  
- Postagens públicas  
- Perfis suspeitos (impostores)  
- Materiais vazados por usuários  

Sem coleta de dados privados ou restritos.

---

## 6. Análise de Riscos
Para cada achado, foi avaliado:

- Impacto potencial  
- Possível uso por atores maliciosos  
- Vetores mais prováveis  
- Medidas de mitigação realistas  

---

## 7. Documentação
O resultado foi documentado separando:

- metodologia – **como** a coleta foi feita  
- achados – **o que** foi encontrado  
- riscos – **por que** é um problema  
- recomendações – **o que corrigir**  
