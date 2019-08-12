# RESET PASSWORD RB411 WITH OPENWRT 10.03 Backfire


- Ligue a RB e aguarde até que o LED verde comece a piscar;
- Quando o LED começar a piscar, aperte e segure o BOTÃO reset (não é para fechar curto nos dois terminais que exite na placa, é o próprio botão de reset mesmo);
- Após cerca de 2 segundos, o LED verde começará a piscar mais rapidamente, isso significa que a RB entrou em *safe mode*;

- Configure o IP do computador para 192.168.1.10/24
- Acesse por Telnet o IP da RB em *safemode*: 192.168.1.1
$ telnet 192.168.1.1

- Dentro da RB digite os seguintes comandos:

# mount / -o remount,rw
# passwd
(informe a nova senha)
(informe novamente a nova senha)

- Desligue a RB e ligue-a normalmente (sem pressionar botao algum);
- Coloque o IP do computador na faixa do IP da RB;
- Acesse o IP da RB via navegador WEB;
- Entre com o usuario root e senha root;

- Para acessar via ssh é necessário passar um parâmetro adicional na linha de comando, pois a versão 10.03 do OpenWRT possui uma versão desatualizada do SSH server. Alinha de comando é:
$ ssh -o KexAlgorithms=+diffie-hellman-group1-sha1 root@192.168.1.1
- No qual, 192.168.1.1 é o IP da RB.


---


