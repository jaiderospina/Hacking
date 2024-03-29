
## Instalación de Docker sobre Kali Linux

1.	Actualización del sistema operativo:

sudo apt update

2.	Instalación Docker. En Kali Linux, el paquete se llama docker.io:
   
sudo apt install -y docker.io

4.	Habilitar Docker para que se inicie al arrancar el sistema:

sudo systemctl enable docker --now

4.	Para verificar la instalación, ejecutar el comando docker:
docker

5.	Si se desea usar Docker sin sudo, se debe su usuario al grupo docker:
   
sudo usermod -aG docker $USER

7.	Finalmente, cierra la sesión y vuelve a iniciarla para que los cambios tengan efecto.

## Docker CE (Community Edition), seguir estos pasos adicionales:

1.	Agregar el repositorio de Docker CE a tu lista de fuentes de APT:

printf '%s\\n' "deb [arch=amd64] https://download.docker.com/linux/debian bullseye stable" | sudo tee /etc/apt/sources.list.d/docker-ce.list

2.	Importar la clave GPG de Docker:

curl -fsSL https://download.docker.com/linux/debian/gpg | sudo gpg --dearmor -o /etc/apt/trusted.gpg.d/docker-ce-archive-keyring.gpg

3.	Actualizar nuevamente la lista de paquetes disponibles:

sudo apt update

4.	Finalmente, instalar Docker CE:

sudo apt install -y docker-ce docker-ce-cli containerd.io

