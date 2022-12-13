# psi3542-Projeto
# Casa inteligente
## O projeto
O nosso projeto tem a intenção de integrar algumas funcionalidades que deseja-se facilitar algumas tarefas diárias através de dispositivos de IOT. Para isso criamos algumas funcionalidades que foram baseadas em tarefas realizadas na disciplina de PSI-3542 ao longo do semestre, cuja implementação foi feita usando o ESP32 e a *Raspberry Pi*.
O projeto conta com duas interfaces de interação entre o usuário e os dispositivos, a primeira é por meio do aplicativo criado no *MIT App Inventor* que permite a interação via smartphone. A segunda é por meio de comandos de voz que são processados e executados dentro do *Raspberry Pi* através de um assistente virtual, o Guilherme (nome dado em homenagem aos seus criadores que carregam mesmo nome), cujas ações foram todas criadas por nós através de envio e recebimento *mqtt* e todas controladas por lógicas de funções desenvolvidas especialmente para as diversas ações que o Guilherme pode fazer.
O ambiente em que foi realizado o projeto foi o aplicativo *Node Red*, que dispõe de uma vasta gama de conteúdo disponível na internet além de extensões para praticamente qualquer aplicação. Ele permite uma visualização fácil do tráfego de dados através da sua estrutura de diagrama de blocos além de permitir que criemos funções lógicas em seu interior por meio da linguagem *JavaScript*, todos feitos dentro da *Raspberry* que será o *HUB* da nossa aplicação.
Para os dispositivos periféricos utilizamos os microcontroladores Esp32, que permitem conexão Wi-fi para nos conectarmos ao *broker* chamado *HiveMq* de forma que podemos controlar o status dos nossos componentes além de controlar as ações através do *HUB*. E para a configuração dos dispositivos Esp32 usamos um *open source* chamado *Tasmota*, que nos permitiu manusear os diferentes periféricos que serão de fato aqueles que farão as ações. São eles: Relé, LED, Sensor MQ-2 e Buzzer.
## O aplicativo

## O assistente de voz

## Node red e Tasmota


