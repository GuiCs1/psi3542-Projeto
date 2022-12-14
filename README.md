# psi3542-Projeto
# Casa inteligente
## O projeto
O nosso projeto tem a intenção de integrar algumas funcionalidades que deseja-se facilitar algumas tarefas diárias através de dispositivos de IOT. Para isso criamos algumas funcionalidades que foram baseadas em tarefas realizadas na disciplina de PSI-3542 ao longo do semestre, cuja implementação foi feita usando o ESP32 e a *Raspberry Pi*.

O projeto conta com duas interfaces de interação entre o usuário e os dispositivos, a primeira é por meio do aplicativo criado no *MIT App Inventor* que permite a interação via smartphone. A segunda é por meio de comandos de voz que são processados e executados dentro do *Raspberry Pi* através de um assistente virtual, o Guilherme (nome dado em homenagem aos seus criadores que carregam mesmo nome), cujas ações foram todas criadas por nós através de envio e recebimento *mqtt* e todas controladas por lógicas de funções desenvolvidas especialmente para as diversas ações que o Guilherme pode fazer.

O ambiente em que foi realizado o projeto foi o aplicativo *Node Red*, que dispõe de uma vasta gama de conteúdo disponível na internet além de extensões para praticamente qualquer aplicação. Ele permite uma visualização fácil do tráfego de dados através da sua estrutura de diagrama de blocos além de permitir que criemos funções lógicas em seu interior por meio da linguagem *JavaScript*, todos feitos dentro da *Raspberry* que será o *HUB* da nossa aplicação.

Para os dispositivos periféricos utilizamos os microcontroladores Esp32, que permitem conexão Wi-fi para nos conectarmos ao *broker* chamado *HiveMq* de forma que podemos controlar o status dos nossos componentes além de controlar as ações através do *HUB*. E para a configuração dos dispositivos Esp32 usamos um *open source* chamado *Tasmota*, que nos permitiu manusear os diferentes periféricos que serão de fato aqueles que farão as ações. São eles: Relé, LED, Sensor MQ-2 e Buzzer.
## O aplicativo
O aplicativo foi desenvolvido na plataforma *MIT App Inventor* e será uma das interfaces de interação entre usuário e os dispositivos. 

Primeiro, ao abrir o aplicativo temos a página principal. A partir dela será possível acessar todos os ambientes da casa.


Temos por exemplo o ambiente da cozinha, nele podemos visualizar o botão que liga e desliga a lâmpada LED e que por sua vez muda de cor dependendo do estado em que a luz se encontra. Logo a baixo vemos os botões que controlam a relé para que se abra ou feche a porta. Além disso, na cozinha há o sensor MQ-2 que manda continuamente quantas partículas por milhão há de compostos produzidos na combustão. Com isso podemos analisar em tempo real a situação em que a cozinha se encontra, para a visualização deste valor em ppm é necessário ativar o botão que inicializa a contagem do sensor. Outra funcionalidade do aplicativo é que a partir de um certo valor considerado perigoso é gerado um alerta na tela sobre o perigo. 

Os outros ambientes são iguais, porém eles são desprovidos de sensores de fumaça.
## O assistente de voz
O assistente de voz é a segunda interface de interação entre usuário e a casa inteligente. O dispositivo *Raspberry Pi* contém o microfone e eles ficam localizados na sala por questão de configuração da casa que privilegia a sala por esta estar no núcleo da planta. 

O assistente chamado Guilherme é ativado assim que for chamado por alguém. Primeiramente ao ser chamado o Guilherme responde por meio dos alto-falantes que devem estar distribuídos pela casa, e ele responde perguntando de que forma ele pode ajudar. Com isso é ativado um temporizador de 7 segundos de duração que espera o usuário dar as ordens para ele distribuir as ações em uma árvore de funções que foi criada manualmente para melhor atender às necessidades do seu dono. Com isso há a possibilidade de fazer qualquer pedido igualmente é feito via aplicativo, mas a diferença principal além do meio ser a voz é que ele te responde.
## Node red e Tasmota


