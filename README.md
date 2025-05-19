# Born2beroot
(Readme in progress...)
## EN VERSION
### Description
Born2beroot is a virtual machine project at 42 School, where we have to create a virtual machine using Virtual Box, install an operating system, and do a bunch of configurations. As I am not able to push a Virtual Machine to github, I am going to describe on this ReadMe things I learned in this process and a resume of everything you need for the evaluation.

## PT-BR VERSION
### Descrição
Born2beroot é um projeto de máquina virtual da Escola 42, cujo objetivo é criar uma máquina virtual usando Virtual Box, instalar um sistema operacional e fazer algumas outras configurações. Como não consigo subir uma máquina virtual no github, irei descrever neste ReadMe coisas que aprendi neste processo e um resumo do que é preciso saber para a avaliação. Já aviso de antemão que eu era completamente leiga e praticamente tudo foi novidade para mim. Foi neste projeto, por exemplo, que descobri que Linux NÃO é um sistema operacional e sim um kernel e também foi nesse projeto que descobri o que é um kernel...rs. Para quem não sabe, assim como eu não sabia, kernel é responsável pela comunicação entre o hardware (parte física do computador) e o software, e é sobre ele que é construído o sistema operacional. Então sem mais delongas, vamos para os conceitos aprendidos neste projeto e tudo que você precisa saber para responder as perguntinhas da régua.
### Conceitos
#### Signature
Para enviar seu projeto, você precisa gerar uma assinatura por meio do comando `shasum VirtualBox.vdi` o qual deverá ser executado no terminal na pasta onde seu vdi está presente (fora da Máquina Virtual).   
**ATENÇÃO!** Tenha certeza que realmente terminou tudo, pois sempre que algo é modificado em sua máquina virtual, esse número muda. Então ele nada mais é que uma forma de assegurar que nada foi alterado em sua máquina depois que você fechou o projeto.   
Esse número deverá ser colocado dentro de um arquivo `signature.txt` o qual deverá ser submetido no repositório da escola. Na hora da avaliação, o avaliador usará o comando `shasum VirtualBox.vdi` novamente para assegurar que a assinatura esteja igual à submetida.
#### O que é uma Máquina Virtual e para que ela serve?
O VirtualBox é um software que permite criar uma máquina virtual, ou seja, um ambiente virtualizado dentro do computador, mas que opera de forma isolada do sistema principal. A máquina virtual possui seu próprio sistema operacional, memória, CPU, disco rígido e outros recursos configuráveis. Ela é muito útil para executar testes, pois, mesmo que ocorra um erro ou falha grave na máquina virtual, o sistema principal do computador não é afetado. Além disso, é uma solução eficiente para quem precisa usar mais de um sistema operacional, permitindo o uso de máquinas virtuais em vez de adquirir vários computadores. <

#### Qual foi a escolha do sistema operacional e porque? Qual a diferença entre Rocky e Debian?
O sistema operacional escolhido por mim foi o Debian por ele ser o mais indicado para usuários físicos e iniciantes. A diferença é que o Rocky é voltado mais para empresas, para o ambiente corporativo por conta das exigencias de segurança e por isso ele é mais complicado de atualizar. Além disso o Rocky é mantido por uma empresa enquanto o Debian é open-source e o OS mais antigo e robusto do Linux. Existe desde 1993 servindo de base para sistemas operacionais como Ubuntu que vieram depois.

#### O que é SSH?
SSH significa Secure Shell Host e é um protocolo de rede criptográfico, possibilitando operar serviços de rede de forma segura em uma rede insegura. Permite conectar e controlar um computador remotamente e é usado para administrar servidores, acessar sistemas remotamente e realizar transferências seguras de arquivos.

#### O que é UFW?
É um Firewall avançado do Linux. Projetado para facilitar a configuração  do firewall mesmo para quem não é especialista em redes. Controla e filtra o tráfego de rede para proteger contra acessos não autorizad

#### Sobre `sudo` e `sudoers`
`sudo` é um comando no Linux para que usuários comuns tenham privilégios de administrador. Para uso o `sudo` é preciso definir no arquivo `sudoers` que fica em `arquivo/etc/sudoers` quais usuários tem a permissão, quais computadores e os comandos que poderão ser executados por eles.

#### Qual a diferença entre `apt` e `aptitude`?
Ambos são gerenciadores de pacores com funcionalidades de instalar, atualizar e remover pacotes. Neste projeto usamos `apt`.   
`aptitude` sabe o que deve ser instalado como dependência quando instala um pacote e lembra quais são as dependências de cada pacote para que, ao desinstalar um pacote, ele desinstale também as dependências.   
`apt` somente fará o que foi explicitamente requisitado na linha de comando.

#### O que é APPArmor?
É um sistema de segurança do Linux com a função de prover segurança MAC (Mandatory Access Control) e vem junto com o Debian por padrão. Ele permite que o administrador restrinja as ações que os processos podem performar. Para checar se ele está executando, basta rodar `aa-status`.


