Fastlane [Working in progress]

Primeiros passos para automatização do processo de distribuição.

A primeira coisa a se fazer se checar se sua versão do OS X é 10.9 ou superior.
Ex: sobre este mac (macOS High Sierra v: 10.13.60)

A segunda coisa a se fazer é checar se sua versão de Ruby é 2.0 ou superior a isto.
Ex: ruby -v

A terceira coisa é checar se o Xcode CLT está instalado na sua máquina.
Ex: xcode-select --install

Caso você recebe um erro: “command line tools are already installed, use
" Software Update" to install updates”, é sinal que o command line tools já está instalado em seu Mac.

Ao término desses 3 passos iniciais você pode executar o comando de instalação do Fastlane com segurança.

Ex: sudo gem install -n /usr/local/bin fastlane --verbose

Nesse momento você terá que autorizar a instalação então logo que necessário confirme com     seu usuário e senha.

Terminado esta etapa da instalação do fastlane vamos para o terminal, agora iremos acessar a pasta do projeto onde iremos realizar a automatização dos processos.

Ex: cd /Documents/Estudos/Marvel

Logo que estiver na pasta do projeto execute o seguinte comando
Ex: fastlane init 

Caso necessário utilize o prefixo sudo para ter permissão de usuário root
Caso seja a primeira vez que vc rode fastlane init será realizada uma validação para ver se as credenciais do app já existem no iTunes Connect, caso não será necessário informar um nome para projeto.

Neste momento se vc abrir sua pasta do projeto você irá ver uma nova pasta chamada fastlane com três arquivos:

Appfile: Responsável por armazenar seu Apple ID e o Bundle identificar 
Deliverfile: Responsável por submeter o app para store
Fastfile:  Responsável por gerenciar as lanes criadas 


