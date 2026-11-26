Caso 1 — Password Spraying e comprometimento de conta privilegiada

1. Objetivo

Investigar uma atividade suspeita de autenticação, identificar possíveis indicadores de comprometimento e recomendar medidas de resposta.

Tipo de exercício: Simulação educativa
Ambiente: Windows Active Directory
Severidade estimada: Crítica

2. Cenário

Foi detetada atividade suspeita proveniente do endereço IP fictício 91.210.15.40.

A investigação identificou:

Tentativas de autenticação falhadas contra várias contas.

Um início de sessão bem-sucedido na conta joao.

A conta joao pertencia ao grupo Domain Admins.

Execução de PowerShell com ExecutionPolicy Bypass.

Criação de um ficheiro suspeito numa pasta pública.

Comunicação com um endereço IP externo.

Atividade semelhante noutros computadores.

3. Evidências relevantes

Evidência

Interpretação

Event ID 4625

Tentativas de autenticação falhadas

Event ID 4624

Início de sessão bem-sucedido

Event ID 4672

Privilégios especiais atribuídos à sessão

PowerShell com ExecutionPolicy Bypass

Execução suspeita a investigar

Ficheiro suspeito em pasta pública

Possível presença de malware

Ligação a IP externo

Possível comunicação com infraestrutura externa

4. Análise

A sequência de tentativas falhadas contra várias contas, seguida de um início de sessão bem-sucedido, é compatível com um possível ataque de Password Spraying.

O facto de a conta afetada pertencer ao grupo Domain Admins aumenta significativamente o impacto potencial.

A execução suspeita de PowerShell, a criação de um ficheiro e a comunicação externa reforçam a suspeita de comprometimento.

5. Ações recomendadas

Revogar as sessões da conta comprometida.

Bloquear temporariamente a conta, seguindo os procedimentos da organização.

Alterar a palavra-passe e verificar os métodos MFA.

Isolar os computadores afetados, se confirmado e autorizado.

Preservar os logs e recolher evidências.

Investigar o ficheiro suspeito, o seu hash e os destinos de rede.

Escalar o incidente para a equipa N2 / Incident Response.

6. Conclusão

As evidências são consistentes com um possível ataque de Password Spraying seguido de comprometimento de uma conta privilegiada.

A presença de atividade suspeita em vários computadores indica que o âmbito do incidente poderá ser alargado.

É necessária investigação adicional para determinar o alcance total e confirmar quais os dados eventualmente afetados.

Nota: Este caso é uma simulação educativa com dados fictícios. Não representa experiência profissional real.
