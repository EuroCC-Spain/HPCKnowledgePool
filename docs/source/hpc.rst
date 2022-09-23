Computación de alto rendimiento (HPC en inglés)
===============================================

El término *computación de alto rendimiento* hace referencia a cualquier sistema informático que su capacidad de computo es mayor que pueden manejar los ordenadores de sobremesa normales. En otras palabras, la computación de alto rendimiento es un conjunto de tecnologías hardware y software que es capaz de tratar información en el menor tiempo posible es decir a gran velocidad. El término *supercomputación* se usa como sinómino a computación de alto rendimiento. 

* Supercomputación en la empresa, rompiendo barreras

  * https://www.youtube.com/watch?v=TtGpnoRmQLc

* Supercomputación e Industria - Salud y Medio Ambiente

  * https://www.youtube.com/watch?v=vX3bMgx7ssw

* Supercomputación e Industria - Manufactura
  
  * https://www.youtube.com/watch?v=T2qQZ_SCUZY
  
* Introducción en computación de alto rendimiento
  
  * https://www.youtube.com/watch?v=7zJUceJiYxQ
  
* Entrevista con Mateo Valero, ¿Para qué se necesita realmente la supercomputación?
  
  * https://www.innovaspain.com/bsc-para-que-sirve-supercomputacion/

Los ordenadores de alto rendimiento contienen todos los componentes habituales de un ordenador de sobremesa - procesador (CPU), memoria principal (RAM), almacenamiento (storage), refrigeración, etc.

En la taxomonía de los ordenadores de alto rendimiento, los *superordenadores* o *supercomputadores* son los más potentes en computación. 

Los superordenadores es una agrupación (cluster en inglés) de ordenadores que están interconectado por una red de alto rendimiento y conectado a un sistema de almacenamiento de alto rendimiento.

* Superordenador

  * https://www.youtube.com/watch?v=nctTZplQY-o

A cada ordenador en un superordenador es conocido como nodo. Cada nodo puede se construido con un o más procesadores, una cantidad de memoria principal y una capacidad de disco duro local limitada. Además, puede contener distintos tipos de aceleradores:

* La unidad de procesamiento gráfica (GPU en inglés): Este tipo de hardware es usado generalmente para el procesamiento gráfico. A su vez, es capaz de proporcionar una cantidad elevada de capacidad de cómputo, es decir, cientos de procesos ejecutándose paralelamente. Este tipo de hardware es adecuado para el cálculo algebraico lineal.

* Una matriz de puertas lógicas programable en campo (FPGA es ingés): Es una hardware programable que puede ser utilizado para acelerar algunos procesos específicos que normalmente se llevan a cabo con los procesadores.


Generalmente, los ordenadores de alto rendimiento son gestionados por el sistema operativo Linux.

* ¿Qué es Linux?
  
  * https://www.youtube.com/watch?v=UUJ0dFpj1-M
  
  * https://www.youtube.com/watch?v=NDhJfHhe3e4
   
  * https://www.youtube.com/watch?v=OR3tWKKmhEM&t=5s (en inglés)

Típicamente, la interacción con los ordenadores de alto rendimiento se realiza con la consola o shell.

  * Introducción a shell

    * https://gitlab.com/makhlaghi/smack-talks-iac/-/blob/master/smack-2-shell.md
    * https://www.youtube.com/watch?v=48r76WVkQUI

A su vez, popularmente, las aplicaciones software son gestionadas por el sistema *module*.

* Introducción

  * https://gitlab.com/makhlaghi/smack-talks-iac/-/blob/master/smack-18-module-py-virtual-env.rst

* Se distribuyen en dos versiones:

  * TCL: Distribución más expendida en los ordenadores de alto rendimiento actualmente
    
    * https://modules.readthedocs.io/en/latest/index.html
    
  * LMOD: Distribución en expansión y ofrece una gran versatilidad.
    
    * https://lmod.readthedocs.io/en/latest/

Gestor de colas/trabajos
------------------------

Tradicionalmente, los ordenadores de alto rendimiento emplean algún sistema para la gestión de los recursos del ordenador entre los usuarios.  Por lo general, a estos sistemas se conoce con el nombre de *gestor de colas* o *gestor de trabajos*. En un gestor de cola, un *trabajo* o *job* (en inglés) se refiere a una aplicación con los datos de entrada para su ejecución.

Los gestores de colas principales son:

* *SLURM* (Simple Linux Utility for Resources Management)
* *PBS* (Portable Batch System) o TORQUE (Terascale Open-source Resource and QUEue Manager) que se distribuye en el estándad abierto, OpenPBS (https://www.openpbs.org/)

Hoy en día, el gestor de cola SLURM es el más popular en los ordenadores de alto rendimiento:

* Página oficial:
 
  * https://slurm.schedmd.com/

* Resumen de los comandos:

  * https://slurm.schedmd.com/pdfs/summary.pdf
  * https://www.scayle.es/manual/es/hpc/gestor-de-trabajos
  * https://research.iac.es/sieinvens/siepedia/pmwiki.php?n=HOWTOs.LaPalma3UsefulCommands2 (en inglés)

