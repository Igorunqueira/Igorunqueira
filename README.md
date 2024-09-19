# Projeto AWS

Este projeto tem como objetivo avaliar os conhecimento adquiridos durante aos aprendizados da Compass-UOL 

 Esta documentação fornece um guia passo a passo para a instalação de um servidor com o Sistema Operacional Linux, onde serão instalados os serviços Apache e NFS (Network File System) em um Servidor Cloud hospedado na Amazon AWS.

Configuração do Servidor Utilizado:

Servidor Cloud hospedado no Amazon WS
Amazon Linux 2 AMI (HVM) - Kernel 5.10, Tipo de volume SSD
Instância EC2 da Família t3.small (2vCPU, Memória 2GB)
16 GB SSD de Uso Geral (gp3)
IP elástico
Portas de Comunicação Liberadas: 22/TCP, 80/TCP, 111/TCP e UDP, 443/TCP e 2049/TCP.

Conecte-se à Instância EC2 via SSH e atualize o sistema:

Para Amazon Linux 2 ou RHEL:

sudo yum update - y

Parte Prática:

Gerar chave de acesso é preciso Gerar uma chave pública para acessar o ambiente AWS.
Já a Configuração da Instância EC2 Crie uma instância EC2 com o sistema operacional Amazon Linux 2 (t3.small, 16 GB SSD). Associar um Elastic IP à instância.
Configuração de Segurança: Liberar as seguintes portas de comunicação para acesso público: 22/TCP: Acesso SSH. 111/TCP/UDP: Utilizado pelo NFS. 2049/TCP/UDP: Utilizado pelo NFS. 80/TCP: Acesso HTTP. 443/TCP: Acesso HTTPS.
Para a Configuração do NFS Configure o sistema de arquivos NFS. Crie um diretório no NFS com o seu nome para armazenar os resultados do monitoramento.
Na parte de Implementação do Apache Instale e configure o servidor Apache, garantindo que ele esteja rodando e acessível publicamente.
Já no Monitoramento de Serviço Crie um script para validar o status do serviço Apache e gerar um log. O script deve: Exibir Data e Hora, Nome do Serviço, Status (ONLINE/OFFLINE) e uma mensagem personalizada. Gerar dois arquivos de saída: Um para quando o serviço estiver ONLINE. Outro para quando estiver OFFLINe
Na parte de Automação Automatize a execução do script a cada 5 minutos utilizando o cron.
Para finalizar a parte do Versionamento Versionar o projeto utilizando o sistema de controle de versões Git.Documentação: Inclui uma documentação clara e detalhada, explicando o processo de instalação e configuração dos serviços no Linux.

Problemas:

. Automação do script de monitoramento

Autor:

Igor phyllip Junqueira de Souza 



