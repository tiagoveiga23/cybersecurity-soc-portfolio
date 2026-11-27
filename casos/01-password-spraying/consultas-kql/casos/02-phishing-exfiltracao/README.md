Caso 2 — Investigação de phishing e possível exfiltração de dados

1. Objetivo

Investigar uma possível infeção causada por um anexo de phishing, analisar a atividade do endpoint e avaliar indícios de transferência de dados para um destino externo.

Tipo de exercício: Simulação educativa
Ambiente: Windows
Severidade estimada: Alta

2. Cenário

Um utilizador recebeu um email suspeito com um documento Word com extensão .docm.

Após a abertura do documento, foram identificados os seguintes acontecimentos:

winword.exe iniciou powershell.exe.

O PowerShell executou comandos suspeitos.

Foi criado um ficheiro chamado upload.exe.

O processo estabeleceu uma ligação a um endereço IP externo.

Foram transmitidos aproximadamente 18,4 MB de dados através da porta 443.

3. Evidências

Evidência

Interpretação

Anexo .docm

Documento Word que suporta macros

winword.exe → powershell.exe

Cadeia de processos suspeita

upload.exe

Ficheiro criado durante a atividade

IP 185.220.101.25

Destino externo suspeito

Porta 443

Comunicação através de HTTPS/TLS

18,4 MB transmitidos

Transferência de dados a investigar

4. Análise

A execução de PowerShell a partir do Microsoft Word é um comportamento suspeito que pode indicar exploração de um documento malicioso.

A criação de upload.exe, seguida de uma ligação externa e da transmissão de 18,4 MB, aumenta a suspeita de comprometimento.

No entanto, a quantidade de dados transmitidos não permite, por si só, confirmar que ocorreu exfiltração de informação sensível.

É necessário investigar o conteúdo transferido, o hash do ficheiro, o processo responsável e o destino da comunicação.

5. Ações recomendadas

Isolar o endpoint, seguindo os procedimentos da organização.

Preservar os logs e as evidências.

Investigar o documento recebido e o ficheiro upload.exe.

Recolher e analisar o hash do ficheiro.

Investigar o endereço IP externo.

Rever a atividade da conta do utilizador.

Escalar para a equipa N2 / Incident Response.

6. Conclusão

As evidências indicam uma possível infeção iniciada através de phishing, seguida de execução suspeita de processos e comunicação com um destino externo.

A transmissão de dados representa um possível indicador de exfiltração, mas o conteúdo transferido ainda não foi confirmado.

O incidente deve ser investigado e escalado para determinar o impacto real.

Nota: Simulação educativa com dados fictícios. Não representa experiência profissional real.
