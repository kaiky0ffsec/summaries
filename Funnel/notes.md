target => 10.129.41.250
____

# Tasks

1. How many TCP ports are open?
	1.  2 {21,22}
	2. ![[Pasted image 20260205205538.png]]
2. What is the name of the directory that is available on the FTP server?
	1. Me conectei usando usuário anonymous e senha anonymous usando o utilitário ftp
	2. ![[Pasted image 20260205205830.png]]
	3. ![[Pasted image 20260205205855.png]]
	4. mail_backup
	5. ![[Pasted image 20260205210034.png]]
3. What is the default account password that every new member on the "Funnel" team should change as soon as possible?
	1. Acesse o diretório usando `cd mail_backup` e continha 2 arquivos dentro:
		1. ![[Pasted image 20260205210203.png]]
		2. Examinei o arquivo .pdf de politicas de senha e a informação estava lá: {funnel123#!#}
		   ![[Pasted image 20260205210329.png]]
4. Which user has not changed their default password yet?
	1. Ao ler a mensagem de boas-vindas, você pode criar uma lista de possíveis nomes de usuário: optimus, albert, andreas, christine e maria. Em seguida, você pode usar uma ferramenta como o Hydra ou o CrackMapExec para realizar um ataque de força bruta (password spraying), utilizando esses nomes de usuário e a senha padrão contra o serviço SSH.
	2. Usando Hydra, comando `hydra -C pass_funnel.txt ssh://10.129.41.250 `
	3. ![[Pasted image 20260205212127.png]]
	4. {christine}
5. Which service is running on TCP port 5432 and listens only on localhost?
	1. Após autenticar-se via SSH na máquina remota como o usuário christine, você pode usar o comando ss -tl para listar as portas em escuta na máquina remota e o serviço padrão que provavelmente está escutando nessa porta.
	2. O comando `ss -tl` é uma ferramenta usada para obter dados dos sockets e exibe informações de maneira semelhante ao `netstat`
	3. -t (TCP) -l (LISTENING) -n (numerico)![[Pasted image 20260205212918.png]]
6. Como você não consegue acessar o serviço mencionado anteriormente a partir da máquina local, será necessário criar um túnel e conectar-se a ele a partir da sua máquina. Qual o tipo correto de túnel a ser usado: encaminhamento de porta remoto ou encaminhamento de porta local?
	1. Nesse cenário, você precisa acessar um serviço que está sendo executado no servidor. Portanto, você gerará tráfego direcionado a uma porta em sua máquina local e, por sua vez, o SSH encaminhará esse tráfego para a porta remota.
	2. Criando o tunel do local para o remoto usando `ssh -L {porta}:localhost:5432{porta_descoberta} christine@10.129.41.250`
	3. ![[Pasted image 20260205213443.png]]
	4. ![[Pasted image 20260205213823.png]]
	5. acessei usando o comando `psql -U{user} christine -h localhost -p {porta que enviamos no tunel} 1234`
	6. após acessar para listar eu usei `\l`
	7. Usando **local port forwarding** para remote port forwarding
7. Você poderia usar um túnel dinâmico em vez do encaminhamento de porta local? Sim ou Não
	1. Sim
8. KEY:
	1. ![[Pasted image 20260205214338.png]]
	2. Usei comandos no postgresql como: `\l \c \dt & SELECT * FROM flag;` 

