# juankz-repo1-

## Red

Para esta practica configure la maquina virtual en modo **Red Interna** (Internal Network) en VirtualBox,

![Configuracion de red](https://github.com/user-attachments/assets/12771092-beae-4bc7-a5bf-d86b326f6ba0)

## Justificacion

Elegi el modo **Red Interna** porque me permite mantener la maquina virtual aislada, de forma que solo pueda comunicarse con otras VMs conectadas a esa misma red interna, sin acceso a la red domestica ni a Internet, Esto reduce significativamente la **superficie de ataque**, ya que la VM no queda expuesta a otros dispositivos de mi red local ni es alcanzable desde el exterior, Ademas, este modo permite una **segmentacion de red** clara entre el entorno de pruebas y el resto de mi infraestructura, lo cual es una buena practica de seguridad al trabajar con maquinas virtuales que puedan usarse para pruebas o analisis,

Descarte el modo **Puente (Bridged)** porque conecta la VM directamente a la red fisica, dandole una IP visible dentro de mi red domestica y reduciendo el aislamiento, Tambien descarte **Solo-Anfitrion (Host-Only)** porque, si bien aisla la VM de la red externa igual que Red Interna, permite la comunicacion directa con el Host, lo cual no era necesario para esta practica y hubiera ampliado innecesariamente la superficie de contacto entre la VM y mi maquina fisica, Por estos motivos, Red Interna fue la opcion que mejor equilibraba aislamiento y funcionalidad para el ejercicio,

## Snapshots

Tome una instantanea llamada **"Instalacion Base Limpia"** una vez instalado el sistema operativo y antes de realizar cualquier configuracion adicional, La VM estaba **apagada** en el momento de tomar el snapshot, para asegurar un estado consistente y evitar inconsistencias de disco o memoria,

![Snapshot Instalacion Base Limpia](https://github.com/user-attachments/assets/31a498f8-60ab-4fd6-a7cd-0986f64830a4)
