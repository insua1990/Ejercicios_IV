#### Ejercicio 1
Consultar en el catálogo de alguna tienda de informática el precio de un ordenador tipo servidor y calcular su coste de amortización a cuatro y siete años.Consultar este artículo en Infoautónomos sobre el tema.

###### Enlace
https://www.pccomponentes.com/hp-proliant-bl460c-gen9-e5-2620v3

> Especificaciones:

**Procesador**

Socket de procesador LGA 2011-v3
Familia de procesador Intel Xeon
Número de procesadores soportados* 2
System bus data transfer rate 8 GT/s
Intel® ® Xeon ® serie E5-2600
Procesador compatible Xeon

**Memoria**

tipos de memoria compatibles DDR4-SDRAM
Número de ranuras DIMM 16
Medios de almacenaje
Número de discos duros soportados 2
Interfaces de unidad de disco duro soportadas SAS,Serial ATA
Hot-swap Bahía para disco duro

**Red**

Ethernet LAN, velocidad de transferencia de datos 10, 100, 1000, 10000 Mbit/s
Ethernet

**Puertos e Interfaces**

Ethernet LAN (RJ-45) cantidad de puertos 2
Ranuras de expansión
Versión de entradas de PCI Express 3.0
Color negro

 Precio : 1782,64€ Sin iva

**Amortizacion a 4 años:**
> 1782.64 x 0.25 = 445.66 € cada año con amortización máxima.

**Amortizacion a 7 años:**

    Primer año: 1782.64 * 0.30 = 534.792 €
    Segundo año: 1782.64 * 0.25 = 612.60 €
    Tercer año: 1782.64 * 0.15 = 267.396 €
    Cuarto año: 1782.64 * 0.15 = 267.396 €
    Quinto año: 1782.64 * 0.05 = 89.132 €
    Sexto año: 1782.64 * 0.05 = 89.132 €
    Séptimo año: 1782.64 * 0.05 = 89.132 €

#### Ejercicio 2
Usando las tablas de precios de servicios de alojamiento en Internet y de proveedores de servicios en la nube, Comparar el coste durante un año de un ordenador con un procesador estándar (escogerlo de forma que sea el mismo tipo de procesador en los dos vendedores) y con el resto de las características similares (tamaño de disco duro equivalente a transferencia de disco duro) en el caso de que la infraestructura comprada se usa sólo el 1% o el 10% del tiempo.

> He seleccionado el servidor del ejercicio 1 frente a una maquina virtual en Azure con las siguientes caracteristicas:
>- 2 nucleos
>- 14 GB RAM
>- 135 GB espacio en disco
>- Precio / hora = 0.287 €/h = 213.32 € mes

**Si se usa el 1% del tiempo:**

Servidor dedicado : 1782.64 € / 12 = 148.55 €/mes
Máquina virtual : 213.32 €/mes x 0.01 = 2.1332 €/mes

**Si se usa el 10% del tiempo**

Servidor dedicado : 1782.64 € / 12 = 148.55 €/mes
Máquina virtual : 213.32 €/mes x 0.1 = 21.332 €/mes

El uso de máquinas virtuales en la nube es mucho más barato.

#### Ejercicio 3
a. ¿Qué tipo de virtualización usarías en cada caso? Comentar en el foro
b. Crear un programa simple en cualquier lenguaje interpretado para Linux, empaquetarlo con CDE y probarlo en diferentes distribuciones.

a)
**Virtualización plena** para ejecutar máquinas virtuales con sistemas operativos diferentes.
**Virtualización de entornos de desarrollo** para ejecutar lenguajes evitando conflictos.
**Virtualización de aplicaciones** para empaquetar aplicaciones y que se ejecuten de forma independiente mediante emuladores.

b)
** Contenido del fichero : **
#!/usr/bin/env python
print "Hello World!!"

> root@insua-HP-Pavilion-g6-Notebook-PC:/home/insua/Escritorio# python holamundo.py
Hello World!!

**Empaquetamos**
> root@insua-HP-Pavilion-g6-Notebook-PC:/home/insua/Escritorio# cde python holamundo.py
Hello World!!

**Ejecutando desde el directorio apropiado...**
>root@insua-HP-Pavilion-g6-Notebook-PC:/home/insua/Escritorio/cde-package# ./python.cde /home/insua/Escritorio/holamundo.py
Hello World!!

#### Ejercicio 4
 Comprobar si el procesador o procesadores instalados tienen estos flags. ¿Qué modelo de procesador es? ¿Qué aparece como salida de esa orden?

> cat /proc/cpuinfo

model name	: Intel(R) Core(TM) i5-2430M CPU @ 2.40GHz

root@insua-HP-Pavilion-g6-Notebook-PC:/home/insua/Escritorio# egrep '^flags.(vmx|svm)' /proc/cpuinfo
flags		: fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush dts acpi mmx fxsr sse sse2 ss ht tm pbe syscall nx rdtscp lm constant_tsc arch_perfmon pebs bts rep_good nopl xtopology nonstop_tsc aperfmperf eagerfpu pni pclmulqdq dtes64 monitor ds_cpl vmx est tm2 ssse3 cx16 xtpr pdcm pcid sse4_1 sse4_2 x2apic popcnt tsc_deadline_timer aes xsave avx lahf_lm epb tpr_shadow vnmi flexpriority ept vpid xsaveopt dtherm ida arat pln pts
flags		: fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush dts acpi mmx fxsr sse sse2 ss ht tm pbe syscall nx rdtscp lm constant_tsc arch_perfmon pebs bts rep_good nopl xtopology nonstop_tsc aperfmperf eagerfpu pni pclmulqdq dtes64 monitor ds_cpl vmx est tm2 ssse3 cx16 xtpr pdcm pcid sse4_1 sse4_2 x2apic popcnt tsc_deadline_timer aes xsave avx lahf_lm epb tpr_shadow vnmi flexpriority ept vpid xsaveopt dtherm ida arat pln pts
flags		: fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush dts acpi mmx fxsr sse sse2 ss ht tm pbe syscall nx rdtscp lm constant_tsc arch_perfmon pebs bts rep_good nopl xtopology nonstop_tsc aperfmperf eagerfpu pni pclmulqdq dtes64 monitor ds_cpl vmx est tm2 ssse3 cx16 xtpr pdcm pcid sse4_1 sse4_2 x2apic popcnt tsc_deadline_timer aes xsave avx lahf_lm epb tpr_shadow vnmi flexpriority ept vpid xsaveopt dtherm ida arat pln pts
flags		: fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush dts acpi mmx fxsr sse sse2 ss ht tm pbe syscall nx rdtscp lm constant_tsc arch_perfmon pebs bts rep_good nopl xtopology nonstop_tsc aperfmperf eagerfpu pni pclmulqdq dtes64 monitor ds_cpl vmx est tm2 ssse3 cx16 xtpr pdcm pcid sse4_1 sse4_2 x2apic popcnt tsc_deadline_timer aes xsave avx lahf_lm epb tpr_shadow vnmi flexpriority ept vpid xsaveopt dtherm ida arat pln pts


#### Ejercicio 5
a. Comprobar si el núcleo instalado en tu ordenador contiene este módulo del kernel usando la orden kvm-ok.
b. Instalar un hipervisor para gestionar máquinas virtuales, que más adelante se podrá usar en pruebas y ejercicios.

> apt-get install cpu-checker

> root@insua-HP-Pavilion-g6-Notebook-PC:/home/insua/Escritorio# kvm-ok

INFO: /dev/kvm exists
KVM acceleration can be used
