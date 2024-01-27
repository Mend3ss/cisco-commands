# Comandos para gerenciar VLANs em Switches Cisco

## name

### Comando usado para definir o nome da VLAN

```
Switch(config)# vlan <numero da vlan>

Switch(config-vlan)# name <nome>
```

## description

### Comando usado para definir uma descrição para a VLAN

```
Switch(config)# interface vlan <numero da vlan>

Switch(config-if) description <texto>
```

## show vlan brief

### Comando usado para verificar as configurações de VLANs atuais

```
Switch# show vlan brief
```

## switchport

### Comando usado para configurar interfaces em VLANs

## switchport mode

### temos três modos:

### • access (a interface irá acessar uma VLAN especifica)

### • dynamic (o modo padrão que vem configurado.. a interface irá acessar de forma dinâmica, mas a padrão é a VLAN 1)

### • trunk (a interface com este modo é capaz de se comunicar com todas as outras VLANs.. Por exemplo, a VLAN 10 e 20 podem passar por essa interface para chegar a um destino)

## Definindo uma interface para o modo access

```
Switch(config)# interface <interface>

Switch(config-if)# switchport mode access
```
### definindo que VLAN a interface deve acessar

```
Switch(config-if)# switchport access vlan <numero da vlan>
```

## Definindo uma interface para o modo trunk

```
Switch(config)# interface <interface>

Switch(config-if)# switchport mode trunk
```

### Definindo quais VLAN estão permitidas na interface

```
Switch(config-if) switchport trunk
```
### Temos duas opções, allowed e native.

### • allowed, permite apenas as VLANs especificadas.

### • native, define uma vlan como padrão para a interface (por exemplo 10). Assim todo tráfego de VLANs 10 serão liberados.

```
Switch(config-if) switchport trunk allowed vlan <VLAN ou VLANs (10,20,30)>
```