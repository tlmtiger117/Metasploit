# 04/05/26

 - Metaspliot: Framework com diversas funções, comummente utilizado em testes de penetração(pentest) para exploração de vulnerabilidades conhecidas(CVEs)

- Função: Criado para dar acesso a algum alvo(expliot), por isso as diversas funções nessa ferramenta.

- Tipos de Metasploit:
   - CLI(open-sourcec): Essa é a ferramenta disponível ao público. Não tem interface gráfica
   - GUI(comercial):    Essa são os que as empresas usam(pago). O diferencial aqui é a interface gráfica(GUI/grafic user interface).



- Módulos Metaspotable: São pastes/scripts específicos com o objetivo de executar tarefas específicas(exploração, scanning, brute-force...):

- Esses módulos pode ser encontrados em: "/auxiliarys" no metasploit.

   - Exploit/Exploração: Utiliza Módulos(Scripts) relacionados a exploração de vulnerabilidades conhecidas no host alvo(CVEs).

   - Vulnerability:      O resultado de um Exploit(exploração) que pode resultar no acesso a informações ou execução de comandos no sistema alvo.

   - payload:            O script que será executado após a fase de Exploit e vulnerability darem certo, assim, executando o script quando já se
                         está no sistema alvo.    

      - Fluxo: Explt(Explorando uma falha no sistema)-> Vuln(o resultado da exploração(acesso ao alvo))-> payl(o que é executado quando se está no sistema)



- Encoders/codificadores: Te permite modificar o Exploit e o Pyload para evitar a detecção por sistemas de assinaturas(antivírus) que analisam o 
   comportamento dos scripts do metasploit e de outros com um banco de dados de vulnerabilidades conhecidas/comportamento.

   - Os encoders não deve ser tratados como "bypass/evasão", pois existem scripts que fazem isso com uma eficácia superior as vezes.

   - Eles são encontrados em: "/enconders" no metasploit.



- Evasion: Scripts focados em evasão(antivírus) tentam não ser detectados facilmente por programas de defesa do SO alvo.
   - Eles saõ encontrados em: "/evasion" no metasploit.



- Exploits: Scripts com a função de explorar inicialmente uma falha conhecida. Tem a função de fornecer acesso a algo do sistema alvo
   - Eles ficam em: "/exploits" no metasploit.



- NOPS: Scripts com foco em buffers(vazamentos) de dados da RAM e CPU. Isso ocorre sobrepondo dados existentes com dados muito maiores, assim vazando-os.
   - Eles ficam em: "/nops" no metasploit.



- Payloads: A "carga-útil" do metasploit, é o que vai ser executando quando já se tem acesso ao host, assim ganhando acesso a algo do sistema.
   - Quando se ganha o acesso, normalmente os pentester utilizam uma calculadora pra provar que pode executar comandos no sistema(prova de conceito);

- Tipos de Payload:

   - Adapters: Um adaptador envolve cargas úteis individuais para convertê-las em diferentes formatos. Por exemplo, uma carga útil única normal 
               pode ser envolvida dentro de um adaptador Powershell, que fará um único comando powershell que executará a carga útil





   - Singles: Cargas úteis autônomas (adicionar usuário, iniciar o notepad.exe, etc.) que não precisam baixar um componente adicional para executar.


   - Stagers: Responsável por configurar um canal de conexão entre e o sistema de destino. Útil quando se trabalha com cargas úteis encenadas.
             "Cargas úteis estagiadas” primeiro carregará um stager no sistema de destino e, em seguida, baixará o restante da carga útil (estágio).
             Isso fornece algumas vantagens, pois o tamanho inicial da carga útil será relativamente pequeno em comparação com a carga útil completa enviada
             de uma só vez.


   - Stages: Baixado pelo stager. Isso permitirá que você use cargas úteis de tamanho maior.

      - Eles ficam em: "/payloads" no metasploit.


- Post: Scripts focados em pós exploração("Blz, já tenho acesso e privilégio... o que fazer agora?")

   - Eles são encontrados em: "/payloads"
