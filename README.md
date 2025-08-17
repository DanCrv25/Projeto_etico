# Projeto_etico
projeto de finalização de modulo do curso de Cybersecurity.

Este projeto é exclusivamente educacional e destinado a fins de estudo em segurança da informação.
O uso de técnicas de engenharia social, clonagem de sites, varreduras com Nmap ou ferramentas como o Social Engineering Toolkit (SET) para coletar dados de usuários sem consentimento é ilegal, antiético e viola leis de proteção de dados (como a LGPD no Brasil e o GDPR na Europa).

Este README tem como objetivo ensinar como identificar e se proteger contra ataques de engenharia social, não promovê-los.

Ao usar este conteúdo, você concorda em não utilizá-lo para fins maliciosos. Qualquer uso indevido é de inteira responsabilidade do usuário. 


📚 Sumário
1-Objetivo do Projeto
2-Ferramentas Utilizadas
3-Ambiente de Teste 
4-Passo a Passo do Ataque
5-Como se Proteger
6-Considerações Finais
7-Referências


1-Objetivo do Projeto
Este projeto tem como finalidade demonstrar como um ataque de engenharia social pode ser conduzido, especificamente por meio da clonagem de uma página de login do XXXXXXX, utilizando ferramentas como o Social Engineering Toolkit (SET) e Nmap. O foco é educacional, com o intuito de entender as vulnerabilidades humanas e técnicas, e não promover o uso indevido dessas ferramentas.

2-Ferramentas Utilizadas
Kali Linux - Sistema operacional com ferramentas de segurança pré-instaladas
Social Engineering Toolkit (SET) - Criação de páginas falsas (phishing) e coleta de credenciais
Nmap - Varredura de rede (para fins de reconhecimento ético)
Apache2 / ngrok - Hospedagem da página clonada e exposição segura via túnel
Metasploit Framework - Demonstração de exploração

3-Ambiente de Teste (Fundamental)
Máquina virtual (VirtualBox)
Rede local sem acesso externo
Utilizado com meu login

4-Passo a Passo do Ataque (Somente em Ambiente Controlado)
    a. Atualize o sistema (Kali Linux) - "sudo apt update && sudo apt upgrade -y"
    b. Instale o Social Engineering Toolkit (SET) - "sudo apt install setoolkit"
    c. Inicie o SET - "setoolkit"
          Navegue pelas opções: 'Social-Engineering Attacks'
                                'Website Attack Vectors'
                                'Credential Harvester Attack Method'
                                'Site Cloner'
    d. Configure o clonador de site
      Insira o IP da sua máquina (ou use ngrok – ver passo 6)
      URL a ser clonada: https://www.xxxxxx.com/login/
      ⚠️ Apenas para simulação. Em produção real, isso violaria termos de serviço e leis. 
    e. Inicie o servidor web local
      O SET inicia automaticamente o Apache. Verifique:
     'sudo systemctl status apache2'
    f. Baixe e inicie o ngrok:
      './ngrok http 80'
          so gera um link público (ex: https://abc123.ngrok.io) que você pode usar em testes controlados. 
    g. Simule o ataque (apenas com consentimento)
      Acesse o link clonado em outro dispositivo ou navegador anônimo
        Digite credenciais falsas (ex: teste@exemplo.com / senha123)

Veja as credenciais capturadas no terminal do SET
✅ As credenciais aparecerão no console do SET, demonstrando como o ataque coleta dados. 

  h. (Opcional) Use Nmap para análise de rede
   'nmap -sV 1x2.xxx.1.1/24' - Isso mostra dispositivos na rede e serviços abertos – útil para reconhecimento ético. 


Atenção: Este projeto é apenas para fins educacionais.
Não autoriza, promove ou apoia atividades ilegais.

    
        



