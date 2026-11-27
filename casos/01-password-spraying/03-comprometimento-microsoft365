# Caso 3 — Comprometimento de conta Microsoft 365

**Tipo:** Simulação educativa  
**Ambiente:** Microsoft 365 / Microsoft Entra ID  
**Severidade atribuída:** Alta  
**Conta afetada:** ana.silva

## 1. Cenário

Foi identificado um possível comprometimento da conta Microsoft 365 `ana.silva`.

Durante a investigação foram encontrados:
- Login bem-sucedido a partir de um IP desconhecido.
- Notificação MFA não reconhecida pela utilizadora.
- Registo de um novo método MFA.
- Criação de uma regra de encaminhamento de emails para um endereço externo.
- Autorização de uma aplicação OAuth com a permissão `Mail.Read`.

## 2. A minha análise

Identifiquei vários indicadores de possível comprometimento da conta:

- O IP desconhecido sugere um possível acesso não autorizado.
- A notificação MFA inesperada pode indicar uma tentativa de MFA fatigue ou aprovação indevida.
- O novo método MFA pode permitir ao atacante manter acesso à conta.
- A regra de encaminhamento pode permitir receber emails fora da organização.
- A aplicação OAuth com `Mail.Read` pode permitir acesso continuado aos emails.

A investigação confirmou que a aplicação acedeu a emails e que documentos financeiros foram transferidos para um servidor externo.

## 3. Impacto identificado

A investigação confirmou a exposição de dados pessoais e financeiros de aproximadamente 200 clientes.

Entre os dados identificados estavam:
- Nomes e moradas.
- Números de identificação.
- Dados bancários.

A transferência para um servidor externo confirma a ocorrência de exfiltração de dados neste cenário.

## 4. A minha resposta como analista SOC N1

Recomendei as seguintes medidas:

1. Bloquear temporariamente o acesso à conta.
2. Revogar as sessões ativas.
3. Alterar a palavra-passe.
4. Remover o método MFA não autorizado.
5. Investigar e revogar as permissões da aplicação OAuth suspeita.
6. Preservar as evidências da regra de encaminhamento antes de a remover.
7. Investigar os registos de acesso e atividade da caixa de correio.

## 5. Escalamento

Recomendei o escalamento para:

- **N2 / Incident Response:** investigação técnica, contenção e erradicação.
- **DPO:** avaliação da violação de dados pessoais e das obrigações do RGPD.

A organização deverá avaliar a necessidade de notificação à CNPD e aos titulares dos dados, conforme os requisitos do RGPD.

## 6. Conclusão

Classifiquei o incidente como de severidade alta, devido ao comprometimento de uma conta e à exfiltração confirmada de dados pessoais e financeiros de aproximadamente 200 clientes.

A aplicação OAuth representava um risco adicional, porque a permissão `Mail.Read` podia permitir acesso aos emails mesmo após a alteração da palavra-passe.

O incidente exigia contenção imediata, preservação de evidências e escalamento para as equipas responsáveis.

---

**Nota:** Caso prático simulado, com dados fictícios. Não representa experiência profissional real.

**Competências demonstradas:** investigação de identidade, análise de MFA, OAuth, Microsoft 365, resposta a incidentes, avaliação de impacto e escalamento SOC N1.
