FTP sends data in the clear, without any encryption. What acronym is used for a later protocol designed to provide similar functionality to FTP but securely, as an extension of the SSH protocol?:
	**SFTP** (_Secure File Transfer Protocol_)

What is username that is used over FTP when you want to log in without having an account?
	anonymous

What is the response code we get for the FTP message 'Login successful'?
	For an FTP message "Login successful," the standard positive completion response code is in the **2xx range**, most commonly **230 User logged in, proceed** or similar (like 200 OK for successful connection/command), indicating the action (login) was completed successfully, allowing the user to proceed with FTP commands. 

Here's a breakdown of common codes related to login:

- **220** Service ready for new user (initial welcome)
- **230** User logged in, proceed (after successful USER/PASS).
- **200 OK** (Command successful, general success).

What is the command used to download the file we found on the FTP server?
	get
ao usar get no ftp em um (txt) por exemplo, ele baixa na máquina do atacante (minha) após isso só dar quit e ver dentro da minha maquina
