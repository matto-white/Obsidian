1)
Dato il seguente indirizzo di rete: 192.168.15.0

Vogliamo 3 sottoreti e almeno 50 pc per sottorete

192.168.15.00000000 ->                        192.168.15.11000000
s.m. /24 -> /26 = 255.255.255.192                          00    192.168.15.0/26
                                                                                  01    192.168.15.64/26
                                                                                  10    192.168.15.128/26
                                                                                  11    192.168.15.192/26

192.168.15.0/26
	Gateway: 192.168.15.1
	Range host:
		Da: 192.168.15.2
		A: 192.168.15.62
	Broadcast: 192.168.15.63
192.168.15.64/26
	Gateway: 192.168.15.65
	Range host:
		Da: 192.168.15.66
		A: 192.168.15.126
	Broadcast: 192.168.15.127
192.168.15.128/26
	Gateway: 192.168.15.129
	Range host:
		Da: 192.168.15.130
		A: 192.168.15.190
	Broadcast: 192.168.15.191
192.168.15.192/26
	Gateway: 192.168.15.193
	Range host:
		Da: 192.168.15.194
		A: 192.168.15.254
	Broadcast: 192.168.15.255



2)
Pianificare una rete con 20 sottoreti e 80 host per sottorete.
172.16.0.0 == 172.16.00000|000.00000000/21
                                 00000
                                 00001
                                 00010
                                 00011
                                 00100
                                 00101
                                 00110 
                                 00111
                                 01000
                                 01001
                                 01010
                                 01011
                                 01100
                                 01101
                                 01110
                                 01111
                                 10000
                                 10001
                                 10010
                                 10011
                                 
S.M. = 255.255.248.0

172.16.0.0/21
	Gateway: 172.16.0.1
	Range host:
		Da: 172.16.0.2
		A: 172.16.7.254
	Broadcast: 172.16.7.255
172.16.8.0/21
	Gateway: 172.16.8.1
	Range host:
		Da: 172.16.8.2
		A: 172.16.15.254
	Broadcast: 172.16.15.255
	658 host = 00001|010.10010010 -> 172.16.10.146
172.16.16.0/21
	Gateway: 172.16.16.1
	Range host:
		Da: 172.16.16.2
		A: 172.16.23.254
	Broadcast: 172.16.23.255
172.16.24.0/21
	Gateway: 172.16.24.1
	Range host:
		Da: 172.16.24.2
		A: 172.16.31.254
	Broadcast: 172.16.31.255
172.16.32.0/21
	Gateway: 172.16.32.1
	Range host:
		Da: 172.16.32.2
		A: 172.16.39.254
	Broadcast: 172.16.39.255
172.16.40.0/21
	Gateway: 172.16.40.1
	Range host:
		Da: 172.16.40.2
		A: 172.16.47.254
	Broadcast: 172.16.47.255
172.16.48.0/21
	Gateway: 172.16.48.1
	Range host:
		Da: 172.16.48.2
		A: 172.16.55.254
	Broadcast: 172.16.55.255
172.16.56.0/21
	Gateway: 172.16.56.1
	Range host:
		Da: 172.16.56.2
		A: 172.16.63.254
	Broadcast: 172.16.63.255
172.16.64.0/21
	Gateway: 172.16.64.1
	Range host:
		Da: 172.16.64.2
		A: 172.16.71.254
	Broadcast: 172.16.71.255
172.16.72.0/21
	Gateway: 172.16.72.1
	Range host:
		Da: 172.16.72.2
		A: 172.16.79.254
	Broadcast: 172.16.79.255
172.16.80.0/21
	Gateway: 172.16.80.1
	Range host:
		Da: 172.16.80.2
		A: 172.16.87.254
	Broadcast: 172.16.87.255
172.16.88.0/21
	Gateway: 172.16.88.1
	Range host:
		Da: 172.16.88.2
		A: 172.16.95.254
	Broadcast: 172.16.95.255
172.16.96.0/21
	Gateway: 172.16.96.1
	Range host:
		Da: 172.16.96.2
		A: 172.16.103.254
	Broadcast: 172.16.103.255
172.16.104.0/21
	Gateway: 172.16.104.1
	Range host:
		Da: 172.16.104.2
		A: 172.16.111.254
	Broadcast: 172.16.111.255
172.16.112.0/21
	Gateway: 172.16.112.1
	Range host:
		Da: 172.16.112.2
		A: 172.16.119.254
	Broadcast: 172.16.119.255
172.16.120.0/21
	Gateway: 172.16.120.1
	Range host:
		Da: 172.16.120.2
		A: 172.16.127.254
	Broadcast: 172.16.127.255
172.16.128.0/21
	Gateway: 172.16.128.1
	Range host:
		Da: 172.16.128.2
		A: 172.16.135.254
	Broadcast: 172.16.135.255
172.16.136.0/21
	Gateway: 172.16.136.1
	Range host:
		Da: 172.16.136.2
		A: 172.16.143.254
	Broadcast: 172.16.143.255
172.16.144.0/21
	Gateway: 172.16.144.1
	Range host:
		Da: 172.16.144.2
		A: 172.16.151.254
	Broadcast: 172.16.151.255
172.16.152.0/21
	Gateway: 172.16.152.1
	Range host:
		Da: 172.16.152.2
		A: 172.16.169.254
	Broadcast: 172.16.159.255


172.16.123.223/21 -> 172.16.01111|011.11011111
Rete: 172.16.120.0/21
991 Host