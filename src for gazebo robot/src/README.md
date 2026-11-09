// Este é o setup padrao para iniciar projetos ROS2_ com estes após instalar o ROS2_jazzy_Jalisco no Linux Ubuntu Noble 24.04
// Criar uma pasta ros2_ws e denstro desta pasta cria a pasta src.
// Estes arquivos devem estar dentro da pasta src

// Importante antes de usar os comandos baixo o gedit
// abra o seu bashrc com no terminal: gedit .bashrc

nas ultimas linhas cole estes comandos:

source /opt/ros/jazzy/setup.bash
source ~/ros2_ws/install/setup.bash
source /usr/share/colcon_argcomplete/hook/colcon-argcomplete.bash

//isso vai ajudar a rodar os programas toda vez que voce der run em um codigo, e abrir um novo terminal para rodar ele use:

source .bashrc

//isso vai configurar o terminal com o bash do ros2.

//pelo terminal entre na pasta ros2_ws e use os comandos

colcon build --package-select my_robot_interfaces
colcon build --package-select my_cpp_pkg
colcon build --package-select my_cpp_py
colcon build --package-select turtlesim_catch_them_all
colcon build --package-select my_robot_bringup

// estes comandos vão construir todos os pacotes, se eles funcionarem esta tudo certo, para confirmar que esta tudo ok
// escreva no terminal:  

ros2 launch my_robot_bringup turtlesim_catch_them_all.launch.py 

// Isso ira abrir um simulador do ros2 que tem um programa automatico dentro destes pacotes.

//Continue seu trabalho dai.

//OBs: talvez os codigos cpp mostrem erro nos includes de bibliotecas ros2 ou nas suas proprias que construir eu resolvi isso pelo proprio vscode pedindo que ele ignorese o problema.
os codigos rodam normalmente
