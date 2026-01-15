[14/01/2026]
# Website Recon & Footprinting
- alvo: https://hackersploit.org/
### Comandos Kali & Ferramentas
- Aprender sobre um comando: `whatis <command>`
- `whatweb` -> fornece uma visão abrangente das tecnologias utilizadas reais no site
- HTTRack ou HDTrack -> baixar a página web (código-fonte) para analisar localmente 
	- Para instalar e usar por CLI `sudo apt-get install webhttrack`

### Plugins (add-ons) para o Mozilla
- built with -> identifica as tecnologias que estão sendo usadas no site
- wappalyzer -> identifica as tecnologias que estão sendo usadas no site

1. Descobrir o ip usando `host hackersploit.org`
Procurar por informações de um site pode começar através do `hackersploit.org/robots.txt` 
	O arquivo robots.txt é para habilitar ou desabilitar que um buscador como o **Google** indexe o site ou determinada página ou seja, deixe habilitado ou desabilitado determinada busca
	O `disallow` informa ao buscador, sempre desconsiderar a página ou diretório
	![[Pasted image 20260114213417.png]]

O Segundo arquivo bem importante é o `XML` de pontos do mapa do site, fica uma busca como por exemplo `http://hackersploit.org/sitemap.xml`

O sitemap é um arquivo que fornece aos mecanismos de pesquisa uma maneira organizada de indexar o local na rede Internet.

