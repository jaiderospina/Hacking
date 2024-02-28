
## Instalación de Docker sobre Kali Linux

1.	Actualización del sistema operativo:
sudo apt update
2.	Instalación Docker. En Kali Linux, el paquete se llama docker.io:
sudo apt install -y docker.io
3.	Habilita Docker para que se inicie al arrancar el sistema:
sudo systemctl enable docker --now
4.	Para verificar la instalación, puedes ejecutar el comando docker:
docker
5.	Si deseas usar Docker sin sudo, puedes agregar tu usuario al grupo docker:
sudo usermod -aG docker $USER
6.	Finalmente, cierra la sesión y vuelve a iniciarla para que los cambios tengan efecto1.
Si prefieres instalar Docker CE (Community Edition), puedes seguir estos pasos adicionales:
1.	Agrega el repositorio de Docker CE a tu lista de fuentes de APT:
printf '%s\\n' "deb [arch=amd64] https://download.docker.com/linux/debian bullseye stable" | sudo tee /etc/apt/sources.list.d/docker-ce.list
2.	Importa la clave GPG de Docker:
curl -fsSL https://download.docker.com/linux/debian/gpg | sudo gpg --dearmor -o /etc/apt/trusted.gpg.d/docker-ce-archive-keyring.gpg
3.	Actualiza nuevamente la lista de paquetes disponibles:
sudo apt update
4.	Finalmente, instala Docker CE:
sudo apt install -y docker-ce docker-ce-cli containerd.io

