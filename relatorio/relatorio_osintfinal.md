# Relatório OSINT - Estudo do Setor Educacional

## Objetivo
Este relatório apresenta um estudo OSINT completamente passivo, ético e desidentificado, simulando a análise de uma organização do setor educacional.  
Nenhuma informação sensível, nenhum dado real e nenhum domínio específico aparece aqui.  
O objetivo é demonstrar capacidade técnica sem prejudicar terceiros.

---

## Escopo
A análise cobre:

- estrutura de domínio
- tecnologias públicas
- superfície exposta
- fluxos de comunicação abertos
- riscos teóricos
- hipóteses de exploração não-intrusivas
- recomendações técnicas

Tudo foi feito utilizando apenas informações que um atacante poderia coletar publicamente.

---

## Metodologia
A coleta seguiu exclusivamente métodos OSINT passivos, incluindo:

- consulta pública a WHOIS  
- fingerprinting de tecnologias via ferramentas open source  
- enumeração passiva de subdomínios  
- identificação de padrões de e-mail públicos  
- pesquisas abertas em redes sociais profissionais  
- análise de exposição digital pública  

Nenhuma interação com sistemas internos foi realizada.

---

## Infraestrutura Geral (Desidentificada)

### WHOIS
O estudo identificou as seguintes características comuns entre empresas do setor:

- registros contendo pessoa física ou jurídica atrelada ao domínio  
- e-mails institucionais usados como contato administrativo  
- uso de Cloudflare ou provedores equivalentes  
- DNS distribuído em múltiplos servidores  

Impacto:  
Informações administrativas expostas em WHOIS ajudam adversários a construir engenharia social altamente direcionada.

---

## 5. Tecnologias Identificadas (Estrutura Genérica)
As empresas educacionais geralmente utilizam:

- frameworks modernos de frontend (como React, Next.js)  
- servidores de aplicação baseados em Linux  
- hospedagem em plataformas cloud  
- CDN com mitigação de DDoS  
- APIs acessíveis por subdomínios separados  
- múltiplos serviços externos integrados (analytics, identidade, pagamentos)

Riscos comuns:

1. endpoints expostos sem autenticação suficiente  
2. ambientes de teste acessíveis publicamente  
3. versões desatualizadas de servidores web  
4. vazamento indireto via headers ou respostas de erro  

---

## Superfície de Exposição Comum

###  Subdomínios
Ambientes típicos encontrados em organizações educacionais:

- portals de alunos
- sistemas administrativos
- APIs
- ambientes de teste
- intranet exposta parcialmente
- painéis com autenticação simples

Impacto:  
Ambientes internos expostos ampliam a superfície de ataque.

---

##  Análise de Funcionários (Fontes Públicas)
De maneira desidentificada, foram observados padrões comuns:

- funcionários publicam cargos e unidades em redes sociais  
- e-mails institucionais seguem um padrão previsível  
- materiais de treinamento frequentemente circulam de forma pública  

Riscos:

- spear-phishing direcionado  
- coleta de perfis sociais para engenharia social  
- ataques de personificação  

---

##  Hipóteses de Exploração (Somente Teóricas)
Estas hipóteses são padrões encontrados geralmente em ambientes educacionais:

1. Painéis administrativos com autenticação fraca  
2. APIs retornando respostas completas demais  
3. Subdomínios abandonados propensos a takeover  
4. Serviços expostos com versões antigas de servidores web  
5. Documentos internos vazados publicamente  
6. E-mails institucionais facilmente enumeráveis  

Nenhum teste invasivo foi realizado.

---

##  Recomendações Gerais de Segurança

- Implementar MFA em todos os sistemas  
- Minimizar dados pessoais no WHOIS  
- Reforçar rate limiting em painéis  
- Ocultar endpoints de desenvolvimento  
- Separar ambientes (produção, homologação)  
- Conduzir varreduras periódicas de subdomínios  
- Revisar documentação exposta publicamente  



