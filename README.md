# firewall
Firewall baseado em IPTABLES para DEBIAN

O iptables é um programa escrito em C, sendo utilizado como ferramenta que configura regras para o protocolo de Internet IPv4/IPv6 na tabela de filtragem de pacotes, também conhecido como modelo OSI para transmissão e recepção sendo arquivados no kernel Linux (versão 2.3.15 ou posteiro).

O software para proteção de rede conhecido por "pfsense" em sua grande parte o mesmo trabalha com IPTABLES e , é segura por ter seu código aberto.

Agora que sabemos o que é o IPTABLES é essencial entender que muitas vezes ele é mais seguro que antivírus pagos, tendo consciência que o ideal seria dropar tudo e só liberar o que a empresa ou a pessoa tem necessidade.

-----------

# Para que não exista comflito entre regras de FIREWALL - IPTABLES, ele :

* Limpando as Chains
* Zerando contadores
* Define politicas padrao ACCEPT
* Ativando resposta do ping
* Removendo regras de proteção

# Ativa protecão na rede:

* Abilitar o uso de syncookies (muito útil para evitar SYN flood attacks)
* desabilita o "ping" (Mensagens ICMP) para sua máquina
* Não aceite redirecionar pacotes ICMP
* Ative a proteção contra respostas a mensagens de erro falsas
* Evita a peste do Smurf Attack e alguns outros de redes locais

# Politica Padrão

* INPUT DROP
* OUTPUT DROP
* FORWARD DROP

# Loga/Adiciona/Descarta hosts da lista "CRIMINOSO PROCURADO" 

* tcp "firewall [ftp]"
* tcp "firewall [ssh]"
* icmp "firewall [ping]"
* udp "firewall [ftp]"
* udp "firewall [ssh]"

# Permitindo loopback/dns/conexões 

* Permitindo loopback
* Permite o estabelecimento de novas conexões iniciadas por você
* Libera o acesso do DNS 


* 
