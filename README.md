A segunda coisa a se fazer é checar se sua versão de Ruby é 2.0 ou superior a insto
``` > Ex: ruby -v```\n\n


A terceira coisa e checar se o Xcode CTL esta instalado na sua maquina.\n
``` > Ex: xcode-select --install```\n

	> Caso você recebe um erro: “command line tools are already installed, use "Software Update" to \n	install updates”, é sinal que o command line tools ja esta instalado em seu Mac.\n\n

Ao termino destes 3 passos iniciais você pode executar o comando de instalação do Fastlane com segurança.\n

``` > Ex: sudo gem install -n /usr/local/bin fastlane --verbose```\n
	
	Nesse momento você terá que autorizar a instalação então logo que necessário confirme com \n	seu usuário e senha.\n\n

Terminado esta etapa da instalação do fastlane vamos para o terminal, agora iremos acessar a pasta <br>do projeto onde iremos realizar a automatização dos processos.\n

``` > Ex: cd /Documents/Estudos/Marvel```\n

Logo que estiver na pasta do projeto execute o seguinte comando:\n

``` > Ex: fastlane init ```\n\n
	
	> Caso necessário utilize o prefixo sudo para ter permissão de usuário root\n
	> Caso sena a primeira vez que vc rode fastlane init será realizada uma validação para ver se as \n	credencias do app ja existem no iTunes Connect, caso não será necessário informar um nome \n	para projeto.\n\n

Neste momento se vc abrir sua pasta do projeto você ira ver uma nova pasta chamada fastlane com três arquivos dentro 
	>Appfile: Responsável por armazenar seu Apple ID e o Bundle identificar \n
	>Deliverfile: Responsável por submeter o app para store\n
	>Fastfile:  Responsavel por gerencias as lanes criadas \n
