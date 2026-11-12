# -SIMULADO-PR-TICO-INTEGRADO-COMPUTA-O-EM-NUVEM
**P2 | Simulado prático integrado**  

simulado-nuvem# Simulado Prático Integrado — Computação em Nuvem
Aluno: Elywelton Ferreira nunes
Turma: 5° Semestre 
Professora: Simone Tatiane do Canto
Data: 11/11/2026

Objetivo
Implementar uma aplicação web no Kubernetes utilizando ConfigMap, Secret, RBAC, Deployment, Service, probes, escala, rollback, Job e CronJob.

Atividades realizadas
Preparação do cluster e namespace.
Configuração externa com ConfigMap.
Criação de Secret fictício.
Controle de acesso com RBAC.
Publicação Nginx com duas réplicas.
Testes HTTP e monitoramento.
Escala e autorrecuperação.
Atualização da página e rollback.
Execução de Job e CronJob.
Respostas
1. Diferença entre contêiner, Pod e Deployment
Contêiner é a unidade que executa a aplicação. Pod é a menor unidade implantável do Kubernetes e pode conter um ou mais contêineres. Deployment gerencia os Pods e mantém a quantidade desejada de réplicas.

2. Diferença entre ConfigMap e Secret
ConfigMap armazena configurações não confidenciais. Secret armazena informações sensíveis, como tokens e senhas. Ambos permitem separar a configuração do código da aplicação.

3. Diferença entre readiness e liveness
Readiness verifica se a aplicação está pronta para receber requisições. Liveness verifica se a aplicação continua funcionando. Se a liveness falhar repetidamente, o Kubernetes reinicia o contêiner.

4. O que ocorreu após a exclusão do Pod?
O Deployment identificou que havia menos Pods do que o desejado e criou outro Pod automaticamente, mantendo duas réplicas.

5. O que o rollback recuperou? A página voltou à versão 1?
O rollback recuperou a revisão anterior do Deployment, incluindo a imagem válida. Entretanto, não reverteu o ConfigMap. Por isso, a página permaneceu na versão 2.

6. Diferença entre Deployment, Job e CronJob
Deployment mantém aplicações em execução e gerencia réplicas. Job executa uma tarefa até sua conclusão. CronJob agenda a execução periódica de Jobs.

Evidências
As saídas dos comandos executados estão em evidencias/resultados.md.

Arquivos
manifests/: manifestos YAML.
scripts/: comandos utilizados.
evidencias/: resultados dos testes.
