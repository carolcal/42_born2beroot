# Born2beroot
## ENGLISH VERSION
### Description
Born2beroot is a virtual machine project at 42 School, where we have to create a virtual machine using Virtual Box, install an operating system, and do a bunch of configurations. As I am not able to push a Virtual Machine to github, I am going to describe on this ReadMe things I learned in this process and a resume of everything you need for the evaluation

### Project Overview
#### 1. Compare Signature.txt to .vdi
Para enviar seu projeto, você precisa gerar uma assinatura por meio do comando `shasum VirtualBox.vdi` o qual deverá ser executado no terminal na pasta onde seu vdi está presente (fora da Máquina Virtual).   
**ATENÇÃO!** Tenha certeza que realmente terminou tudo, pois sempre que algo é modificado em sua máquina virtual, esse número muda. Então ele nada mais é que uma forma de assegurar que nada foi alterado em sua máquina depois que você fechou o projeto.   
Esse número deverá ser colocado dentro de um arquivo `signature.txt` o qual deverá ser submetido no repositório da escola. Na hora da avaliação, o avaliador usará o comando `shasum VirtualBox.vdi` novamente para assegurar que a assinatura esteja igual à submetida.
#### 2. Máquina Virtual
O que é uma Máquina Virtual e para que ela serve?
> O VirtualBox é um software que permite criar uma máquina virtual, ou seja, um ambiente virtualizado dentro do computador, mas que opera de forma isolada do sistema principal. A máquina virtual possui seu próprio sistema operacional, memória, CPU, disco rígido e outros recursos configuráveis. Ela é muito útil para executar testes, pois, mesmo que ocorra um erro ou falha grave na máquina virtual, o sistema principal do computador não é afetado. Além disso, é uma solução eficiente para quem precisa usar mais de um sistema operacional, permitindo o uso de máquinas virtuais em vez de adquirir vários computadores.
