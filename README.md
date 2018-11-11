**Fastlane** [Working in progress]

Primeiros passos para automatização do processo de distribuição.

A primeira coisa a se fazer se checar se sua versão do **OS X** é 10.9 ou superior.

```Ex: macOS High Sierra v: 10.13.60```

A segunda coisa a se fazer é checar se sua versão de **Ruby** é 2.0 ou superior. Você deve estar pensando
que diabos vou fazer com Ruby, bom o Fastlane é baseado em uma coleção de **scripts Ruby** que facilitam
e muito a vida e por isso devemos mantê-lo atualizado.

```Ex: ruby -v```

A terceira coisa é checar se o Xcode command line tools está instalado na sua máquina.

```Ex: xcode-select --install```

- Caso você receba o erro: “command line tools are already installed, use `Software Update` to
install updates”, é sinal que o command line tools já está instalado e seu Mac.

Ao término desses 3 passos iniciais você pode executar o comando de instalação do Fastlane com segurança.

```Ex: sudo gem install -n /usr/local/bin fastlane --verbose```

- Nesse momento você terá que autorizar a instalação, então logo que necessário confirme com seu usuário e senha.

Terminado esta etapa da instalação do fastlane vamos para o terminal, agora iremos acessar a pasta do
projeto onde iremos realizar a automatização dos processos.

```Ex: cd /Documents/Estudos/Marvel```

Logo que estiver na pasta do projeto execute o seguinte comando:

```Ex: fastlane init ```

- Caso seja a primeira vez que você rode **fastlane init** será realizada uma validação para
ver se as credenciais do app já existem no iTunes Connect.

    As possíveis resposta que você pode obter ao executar este comando são: 

        Este identificador de aplicativo não existe no iTunes Connect, ele será criado para você.
        Este identificador ainda não existe no Portal Apple Developer, ele será criado para você.
        Por favor, confirme os valores acima (y / n)

        Ou

        Parece que o APP_NAME já foi utilizado por outra pessoa, por favor insira um nome alternativo:

Quando a etapa inicial de instalação do fastlane terminar abra sua pasta do projeto, nela você
irá ver uma nova pasta chamada fastlane com três arquivos dentro

        - Appfile: Responsável por armazenar seu Apple ID e o Bundle identificar
        - Deliverfile: Responsável pelas configurações de submissão para app para store
        - Fastfile: Responsável por gerenciar as lanes criadas

Dado que tudo tenha ocorrido com sucesso e os arquivos Appfile, Deliverfile e Fastfile, tenha sido criados
você também verá um pasta chamada **/metadata** que conterá alguns alguns arquivos de texto, os quais são
responsáveis pela apresentação de informações relevantes na App Store.


        - primary_category
            Ex: Entretenimento
        - primary_first_sub_category
            Ex: MZGenre.Racing
        - primary_second_sub_category
            Opcional
        - secondary_category
            Opcional
        - secondary_first_sub_category
            Opcional
        - secondary_second_sub_category
            Opcional
        - copyright
            Ex: Copyright (c) 2018 Rafael Silva Ltda


Além destes arquivos de textos que contemplam informações sobre categoria, subcategoria, copyright etc, faz necessário
a criação de um outro arquivo que deve ser criado na pasta raiz /metadata, esse arquivo será um .json chamado itunes_ratin_config.

- Essas configurações garantem que seu app tenha a classificação etária correta para ser disponibilizado na App Store. 

        - itunes_ratin_config
            {
            "CARTOON_FANTASY_VIOLENCE": 0,
            "REALISTIC_VIOLENCE": 0,
            "PROLONGED_GRAPHIC_SADISTIC_REALISTIC_VIOLENCE": 0,
            "PROFANITY_CRUDE_HUMOR": 0,
            "MATURE_SUGGESTIVE": 0,
            "HORROR": 0,
            "MEDICAL_TREATMENT_INFO": 0,
            "ALCOHOL_TOBACCO_DRUGS": 0,
            "GAMBLING": 0,
            "SEXUAL_CONTENT_NUDITY": 0,
            "GRAPHIC_SEXUAL_CONTENT_NUDITY": 0,
            "UNRESTRICTED_WEB_ACCESS": 0,
            "GAMBLING_CONTESTS": 0
            }

        
E para finalizar as configurações básicas do fastlane acesse **metadata/en-US** nesta pasta você encontra os arquivos 
referentes a informações de metadados do aplicativo exibidas na App Store como Nome, palavras chave, url de apoio entre outros.    

        - name
            Ex: Marvel
        - description
            Ex: MZGenre.Racing
        - keywords
            Marvel, herois, 
        - marketing_url
            Opcional
        - privacy_url
            http://marvel.com    
        - promotional_text
            Opcional
        - release_notes
            Ex: Lorem ipsum dolor sit amet, consectetur adipiscing elit.
        - subtitle
            Opcional
        - support_url
            http://marvel.com
