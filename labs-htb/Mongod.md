OS: Linux
IP => 10.129.228.30
___
Task1 - How many TCP ports are open on the machine?
	![[Pasted image 20260120213844.png]] 2 portas TCP abertas
- 22/tcp | ssh
- 27017/tcp | mongod
___
Which service is running on port 27017 of the remote host?
`nmap -sS -p 27017 -sV -T5 10.129.228.30`
![[Pasted image 20260120213949.png]]
- MongoDB 3.6.8
___
What type of database is MongoDB? (Choose: SQL or NoSQL)
- NoSQL (NÃO RELACIONAL)

What command is used to launch the interactive MongoDB shell from the terminal?
	mongosh

What is the command used for listing all the databases present on the MongoDB server? (No need to include a trailing ;)
	- show dbs

What is the command used for listing out the collections in a database? (No need to include a trailing ;)
	show collections

What command is used to dump the content of all the documents within the collection named `flag`?
	db.flag.find()



## **Enumeração**

Começamos com uma **simples varredura inicial de enumeração** com **o nmap** . Usamos o comando: **`nmap -sV -oA initial_nmap_scan $target_ip`** . A opção **`-sV`** instrui o nmap a detectar a **versão** dos **serviços** encontrados nas **portas abertas** . A opção **`-oA`** **salvará** a **saída da varredura do nmap** em **todos os formatos de arquivo suportados pelo nmap** .