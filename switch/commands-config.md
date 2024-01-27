# Comandos para roteadores Cisco (Modo de configuração)

## "(config)#" indica o modo em que estamos, no caso o modo de configuração do equipamento.


## Banner motd
### Comando para definir uma mensagem no equipamento


### motd: usado para definir uma mensagem assim que o equipamento for iniciado/acessado


```
Switch(config)# banner motd <texto>
```

## Hostname
### Comando usado para definir um nome ao equipamento

```
(config)# hostname <nome a ser definido>
```

## Enable
### Dentro do modo de configuração, podemos definir uma senha para o modo Admin.

```
(config)# enable secret <senha>
```
### Existe a opção "password", mas o secret possui uma criptografia por padrão.

## Line
### Comando usado para configurar interfaces/terminais que dão acesso ao equipamento, por exemplo a console (interface/terminal que usamos para configurar o equipamento)

```
(config)# line console 0
```
### Dentro do modo de configuração da interface:
```
(config-line)# password <senha>
```
### Para habilitar a senha use:
```
(config-line)# login
```
### Para ativar a mensagem de inicio (motd):
```
(config-line)# motd-banner
```

## Service Password-Encryption
### Use o comando no modo de config para criptografar as senhas gravas no equipamento

```
(config)# service password-encryption
```
