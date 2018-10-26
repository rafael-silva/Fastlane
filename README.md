Fastlane 

Primeiros passos para automatização do processo de distribuição.

A primeira coisa a se fazer se checar se sua versão do OS X é 10.9 ou superior
Ex: sobre este mac (macOS High Sierra v: 10.13.60)

A segunda coisa a se fazer é checar se sua versão de Ruby é 2.0 ou superior a insto
Ex: ruby -v


A terceira coisa e checar se o Xcode CTL esta instalado na sua maquina.
Ex: xcode-select --install

Caso você recebe um erro: “command line tools are already installed, use "Software Update" to install updates”, é sinal que o command line tools ja esta instalado em seu Mac.

Ao termino destes 3 passos iniciais você pode executar o comando de instalação do Fastlane com segurança.

Ex: sudo gem install -n /usr/local/bin fastlane --verbose

Nesse momento você terá que autorizar a instalação então logo que necessário confirme com     seu usuário e senha.

Terminado esta etapa da instalação do fastlane vamos para o terminal, agora iremos acessar a pasta <br>do projeto onde iremos realizar a automatização dos processos.

Ex: cd /Documents/Estudos/Marvel

Logo que estiver na pasta do projeto execute o seguinte comando
Ex: fastlane init 

Caso necessário utilize o prefixo sudo para ter permissão de usuário root
Caso sena a primeira vez que vc rode fastlane init será realizada uma validação para ver se as     credencias do app ja existem no iTunes Connect, caso não será necessário informar um nome     para projeto.

Neste momento se vc abrir sua pasta do projeto você ira ver uma nova pasta chamada fastlane com três arquivos dentro 
Appfile: Responsável por armazenar seu Apple ID e o Bundle identificar 
Deliverfile: Responsável por submeter o app para store
Fastfile:  Responsavel por gerencias as lanes criadas 









