# Comandos para roteadores Cisco (Modo de configuração)

## Configure (deve ser usado a partir do modo Admin/Enable)
### Comando usado para entrar no modo de configuração, no nosso caso o modo terminal

```
configure <selecione o modo de configuracao desejado>
```

## Banner
### Comando para definir uma mensagem no equipamento contendo duas opções: login e motd

### login: usado para definir uma mensagem para usuarios que forem logar no equipamento

```
banner login LINE
```
### Defina a mensagem e insira "L" para terminar e sair, exemplo:

```
Uso restrito, somente pessoal autorizado L
```

### motd: usado para definir uma mensagem assim que o equipamento for iniciado/acessado

### Defina a mensagem e insira "L" para terminar e sair, exemplo:

```
Uso restrito, somente pessoal autorizado L
```

## Hostname
### Comando usado para definir um nome ao equipamento

```
hostname <nome a ser definido>
```

## Enable
### Dentro do modo de configuração, podemos definir uma senha para o modo Admin.

```
enable secret <senha>
```
### Existe a opção "password", mas o secret possui uma criptografia por padrão.

## Line
### Comando usado para configurar interfaces/terminais que dão acesso ao equipamento, por exemplo a console (interface/terminal que usamos para configurar o equipamento)

```
line console 0
```
### Dentro do modo de configuração da interface:
```
password <senha>
```
### Para habilitar a senha use:
```
login
```
### Para ativar a mensagem de inicio (motd):
```
motd-banner
```
