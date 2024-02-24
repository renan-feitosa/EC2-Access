# Relatório de Acesso à Amazon EC2 

<div align="center">
  <sub>Imagem 1 - Amazon EC2 Logo</sub>
  <img src="./images/amazon-aws-ec2.jpg">
  <sup>Fonte: ITExperts (2022)</sup>
</div>

## Introdução
&emsp;A Amazon Elastic Compute Cloud (Amazon EC2) é um serviço de computação em nuvem que oferece capacidade de computação escalável na nuvem da Amazon Web Services (AWS). Com a EC2, os usuários podem lançar e gerenciar instâncias virtuais conforme necessário, permitindo flexibilidade e escalabilidade para atender às demandas de computação.

&emsp;Neste relatório técnico, o objetivo principal será a inicialização de uma instância na Amazon EC2 e configurar o acesso seguro a essa instância usando a ferramenta PuTTY.


## Objetivo

&emsp;O objetivo do seguinte relatório técnico consiste em compreender e seguir os passos necessários para criar e configurar uma instância na Amazon EC2, incluindo nomear a instância, criar um par de chaves, configurar as regras de segurança, e iniciar a instância Além disso, é de suma importância entender como configurar ferramentas como o PuTTY para acessar a instância de forma segura, utilizando chaves privadas para autenticação.


## Materiais
1. **Amazon EC2:** Serviço de nuvem da Amazon que permite a criação e gerenciamento de instâncias virtuais.

2. **PuTTY:** Uma ferramenta popular para acesso remoto a servidores via SSH em sistemas Windows. É utilizado para configurar e estabelecer conexões seguras com instâncias na Amazon EC2.

3. **Chaves Públicas e Privadas:** Utilizadas para autenticação durante o acesso às instâncias. A chave privada é inserida na ferramenta PuTTY para autenticação, enquanto a chave pública é armazenada na instância EC2 para permitir o acesso.

## Método

&emsp;Para inicializar uma instância na Amazon EC2, o primeiro passo é nomear a instância, como mostra a **Imagem 2**. Isso envolve atribuir um nome descritivo à instância para facilitar a identificação posterior.

<div align="center">
  <sub>Imagem 2 - Nomeando a Instância</sub>
  <img src="./images/naming-instance.png">
  <sup>Fonte: Autoria própria</sup>
</div>

&emsp;Em seguida, é necessário criar um par de chaves. Esse par de chaves consiste em uma chave pública e uma chave privada. A chave pública é usada para criptografar dados que só podem ser descriptografados pela chave privada correspondente.  Este par de chaves é crucial para autenticar e acessar a instância de forma segura.<sup>[3]</sup>

<div align="center">
  <sub>Imagem 3 - Creating Key Pair .ppk</sub>
  <img src="./images/creating-key-pair.png
  ">
  <sup>Fonte: Autoria Própria</sup>
</div>

&emsp;Após a criação do par de chaves, é necessário configurar as regras de segurança do grupo de segurança associado à instância para permitir o tráfego HTTP/HTTPS. Um grupo de segurança da AWS atua como um firewall virtual para suas instâncias EC2, controlando o tráfego de entrada e saída.<sup>[1]</sup>

<div align="center">
  <sub>Imagem 4 - Permitir Tráfego HTTP/HTTPS</sub>
  <img src="./images/allowing-http-https.png">
  <sup>Fonte: Autoria Própria</sup>
</div>


&emsp;Uma vez configuradas as regras de segurança, a instância pode ser iniciada. Isso envolve iniciar a máquina virtual na nuvem da Amazon EC2, usando as configurações especificadas, como tipo de instância, tamanho, sistema operacional, etc. Durante esse processo, a instância é provisionada e preparada para ser executada.

<div align="center">
  <sub>Imagem 5 - Instância Iniciada</sub>
  <img src="./images/instance-launched.png">
  <sup>Fonte: Autoria Própria</sup>
</div>

&emsp;Nesta imagem, é mostrada a interface de gerenciamento da Amazon EC2, mostrando uma instância que está em execução. Isso significa que a máquina virtual associada a essa instância foi inicializada com sucesso e está pronta para ser utilizada. É possível ver informações importantes, como o ID da instância, tipo, status, endereço IP público, entre outros.

<div align="center">
  <sub>Imagem 6 - Instância em Execução</sub>
  <img src="./images/running-instance.png">
  <sup>Fonte: Autoria Própria</sup>
</div>

&emsp;Esta imagem mostra o aplicativo PuTTY, uma ferramenta que dá possibilidade de acessar servidores remotos via SSH, com uma captura de tela mostrando a configuração do hostname. O hostname é o nome atribuído a um dispositivo na rede.

<div align="center">
  <sub>Imagem 7 -Adicionando Hostname no PuTTY</sub>
  <img src="./images/adding-hostname.png">
  <sup>Fonte: Autoria Própria</sup>
</div>

&emsp;Após isso, a chave privada é inserida no painel SSH/Auth para a autenticação. Com isso, o PuTTY está configurado para usar uma chave privada específica para autenticação, garantindo um acesso seguro à instância remota. 

<div align="center">
  <sub>Imagem 8 - Adicionando Pair Key no PuTTY</sub>
  <img src="./images/adding-private-key.png">
  <sup>Fonte: Autoria Própria</sup>
</div>

&emsp;Finalizando o processo, foi realizado um login através do console com "ec2-user" e a instância foi acessada com sucesso. 

<div align="center">
  <sub>Imagem 9 - Print no Console</sub>
  <img src="./images/console-login.png">
  <sup>Fonte: Autoria Própria</sup>
</div>


## Resultados
&emsp;Após seguir todos os passos descritos na seção anterior, os resultados alcançados incluem:

1. **Inicialização da Instância EC2:** A instância na Amazon EC2 é criada e configurada com sucesso, incluindo a atribuição de um nome descritivo e a definição de um par de chaves público-privado.

2. **Configuração do Acesso Seguro:** Utilizando a ferramenta PuTTY, as chaves privadas são configuradas para autenticação SSH, garantindo acesso seguro à instância remota.

3. **Acesso à Instância Remota:** Após configurar corretamente o acesso no PuTTY, o login na instância remota é realizado com sucesso.

&emsp;Logo, conclui-se que todos os objetivos propostos foram alcançados com sucesso.

## Conclusão
&emsp;A capacidade de inicializar e acessar instâncias na Amazon EC2 de forma segura e eficiente é fundamental para aproveitar os benefícios da computação em nuvem. Este relatório técnico fornece uma visão geral dos passos necessários para alcançar esse objetivo, desde a configuração inicial, no website da AWS, até o acesso remoto seguro, pelo PuTTY.

## Referências
1. CHECK POINTS SOLUTION. **What is AWS Security Groups**. Disponível em: <https://www.checkpoint.com/cyber-hub/cloud-security/what-is-aws-security-groups/#:~:text=An%20AWS%20security%20group%20acts>. Acesso em: 24 fev. 2024.  
2. ITEXPERTS. **EC2: Saiba mais sobre esta solução da Amazon AWS**. Disponível em: <https://www.itexperts.com.br/blog/tecnico/amazon-ec2/>. Acesso em: 22 fev. 2024. 
3. QUORA. **What is the purpose of key pair with Amazon AWS EC2?** Disponível em: <https://www.quora.com/What-is-the-purpose-of-key-pair-with-Amazon-AWS-EC2#:~:text=Amazon%20EC2%20uses%20public>. Acesso em: 24 fev. 2024. 