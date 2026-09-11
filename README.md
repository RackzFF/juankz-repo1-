# juankz-repo1-

## red

para esta practica configure la maquina virtual en modo **red interna (internal network)** en virtualbox.

![configuracion de red](https://github.com/user-attachments/assets/12771092-beae-4bc7-a5bf-d86b326f6ba0)

## justificacion

elegi el modo **red interna** porque permite que la maquina virtual se mantenga aislada y solo pueda comunicarse con otras maquinas virtuales que esten conectadas a la misma red interna. de esta forma, la vm no tiene acceso a internet ni a la red domestica.

esto ayuda a reducir la **superficie de ataque**, por que la maquina virtual no queda expuesta a los dispositvios de mi red ni a otras conexiones , ademas separa la parte de pruebas del resto de la red, cosa que es una buena forma de asegurarse trabajando con las vm

descarte el modo **puente (bridged)** porque conecta la vm directamente a la red fisica. esto haria que la vm tenga una ip dentro de mi red domestica y tendria un menor nivel de aislamiento.

tambien descarte el modo **solo-anfitrion (host-only)** porque, aunque mantiene a la vm aislada de internet y de la red externa, permite que se comunique directamente con el equipo anfitrion, para esta practica esa comunicacion no era necesaria, por lo que preferi mantener un aislamiento mayor

por estos motivos, elegi **red interna**, ya que era la opcion que mejor se adaptaba a lo que necesitaba

## snapshots

tome una instantanea llamada **"instalacion base limpia"**
la maquina virtual estaba **apagada** al momento de crear el snapshot, para guardar un estado limpio y estable de la vm y poder volver a ese punto en caso de ser necesario.

![snapshot instalacion base limpia](https://github.com/user-attachments/assets/31a498f8-60ab-4fd6-a7cd-0986f64830a4)
