Programación paralela
---------------------

Esta sección, se expone la programación aplicada generalmente en ordenadores de computación de alto rendimiento. El concepto de rendimiento es vago y puede significar varias cosas. Nosotros usaremos el concepto de rendimiento significado la resolución de un problema en el menor tiempo posible. En cambio, la productividad es cuánto trabajo se puede realizar por unidad de tiempo. 

En el entorno de computación de alto rendimiento, el rendimiento es la métrica principal que se quiere conseguir optimizar, es decir, la resolución de un problema se complete en el menor tiempo posible. 

Tradicionalmente, la *computación en serie* se ha empleado para el desarrollos de las aplicaciones software y consiste en la ejecución o división del trabajo una tras otra. En cambio, a mediado de la década de 2000, se democratizó los ordenadores paralelos motivando el uso de la computación en paralelo. 

La *computación en paralelo* aplica el concepto de *paralelismo* que consiste en la realización de múltiples cosas al mismo tiempo. En concreto, se puede definir como la utilización de varios recursos de computación para la resolución de un problema. Este paradigma de computación permite:

* La división de un problema en partes discretas para su ejecución simultáneamente, es decir, en múltiples recursos de computación como los procesadores.

En la computación en paralelo se emplean varios/as modelos/paradigmas de programación, conocido también como programación paralela, de las cuales se resaltan:

* Memoria compartida, OpenMP
* Hilos, (OpenMP o POSIX threads en linux)
* Pasos de mensajes, MPI

Estos paradigmas de programación son abstracciones sobre de arquitecturas del ordenador, y se pueden emplear en cualquier de las mismas. 

Paradigmas de programación
^^^^^^^^^^^^^^^^^^^^^^^^^^

* OpenMP

Un modelo de programación portable y escalable que proporciona a los programadores una interfaz simple y flexible para el desarrollo de aplicaciones paralelas. En otras palabras, es una interfaz de programación de aplicaciones (API) para la programación paralela de memoria compartida.

* Página web oficial
    
    * https://www.openmp.org/

  * Introducción a openMP
   
    * https://www.youtube.com/watch?v=nE-xN4Bf8XI&list=PLLX-Q6B8xqZ8n8bwjGdzBJ25X2utwnoEG
   
  * Resumen de las directivas:
   
    * https://www.openmp.org/wp-content/uploads/OpenMP-4.0-C.pdf

* MPI

MPI (Message Passing Interface) es un estándar que define la sintaxis y la semántica de las funciones contenidas en una biblioteca de paso de mensajes 
   
  * Introducción de MPI (inglés)
    
    * https://mpitutorial.com/tutorials/mpi-introduction/
    * https://www.youtube.com/watch?v=D0-xSWBGNAw (What is Open MPI)
  
  * Resumen del lenguaje
    
    * http://www.netlib.org/utk/people/JackDongarra/WEB-PAGES/SPRING-2006/mpi-quick-ref.pdf

* GPGPU

La computación de propósito general en la unidad de procesamiento gráfica (GPU) consiste en aprovechar las capacidades de cómputo de las GPUs. La GPU es una aceleradora de computación para la álgebra lineal, como el aprendizaje profundo.  Principalmente, los grandes fabricantes de GPUs son Nvidia y AMD. 

  * Introducción GPU
    * https://www.youtube.com/watch?v=9zfojkQXNoQ

Varios modelos de programación que son empleados
  
  * Nvidia CUDA (lenguaje de programación para las tarjetas gráficas de Nvidia)
    
    * https://developer.nvidia.com/cuda-toolkit
    
    * https://www.youtube.com/watch?v=iwEoVufzqhg
    
    * Parallel computing on GPUs with CUDA (curso en inglés)
    
     * https://www.youtube.com/playlist?list=PL6lZw8yhOjVh9Hq89p1ECl9hpzjk3ivoq
  
  * OpenACC (programación se realiza con  directivas (pragmas) y biblioteca e independiente del fabricante de la tarjeta gráfica)
    
    * https://www.openacc.org/

  * AMD HIP, lenguaje de programación para las tarjetas gráficas de AMD. Este lenguaje también puede ser empleado con las tarjetas gráficas de Nvidia.   
    
    * Introducción: 
      
      * https://www.youtube.com/watch?v=3ZXbRJVvgJs

    * Guía de programación
      
      * https://docs.amd.com/
      
      * https://rocmdocs.amd.com/en/latest/Programming_Guides/HIP-GUIDE.html
      
      * https://github.com/RadeonOpenCompute/ROCm/blob/rocm-4.5.2/AMD_HIP_Programming_Guide.pdf

Compiladores
------------

La creación de una aplicación software desde el código fuente se consigue a través de los *compiladores*. Este proceso es conocido como *compilación*. Los compiladores principales son:

* *GNU GCC*: es un conjunto de compiladores y librerías de los lenguajes  C, C++, Objective-C, Fortran, Ada, Go, and D.
  
  * Página oficial
  
    * https://gcc.gnu.org/

* *Intel oneAPI*: conjunto de herramientas y librerías para el desarrollo de aplicaciones a través de diferentes arquitectura de computadores. 

  * Página oficial

    * https://www.intel.com/content/www/us/en/developer/tools/oneapi/overview.html#gs.a5u5dz

    * https://www.intel.com/content/www/us/en/developer/tools/oneapi/toolkits.html#gs.a5xmdj

    * Introducción 
    
      * https://www.youtube.com/watch?v=NsFGFbdPsh0 (en inglés)
      
      * https://www.youtube.com/watch?v=ynkDh4yYybs

* *Nvidia HPC SDK*: conjunto de software, librerías y compiladores para los lenguajes C, C++, Fortran, directivas OpenACC y CUDA
  
  * Página oficial

    * https://developer.nvidia.com/hpc-sdk

En la siguinte tabla se muestra la relación de los compiladores y los lenguajes:

.. list-table::
   :header-rows: 1

   * - Lenguaje
     - GNU GCC
     - Intel oneAPI
     - Nvidia HPC SDK
   * - C
     - gcc
     - Actual: icx; Clásico: icc
     - nvc
   * - C++
     - g++
     - Actual: icpx; Clásico: icpc
     - nvc++
   * - Fortan
     - gfortran
     - Actual: ifx;  Clásico: ifort
     - nvfortran
   * - Aceleradores
     - --
     - dpc++ (C++ basado en SYCL)
     - nvcc (CUDA)

Buenas prácticas
----------------

Control de versiones
^^^^^^^^^^^^^^^^^^^^

El control de versiones se define como la gestión de la historia de cambio de un proyecto. Una versión, revisión o edición de un proyecto, es el estado en el que se encuentra el mismo en un momento dado de su desarrollo o modificación. Esta gestión permite el trabajo en equipo en el mismo proyecto sincronizado las contribuciones de cada miembro del equipo.

Generalmente, el control de versiones se realiza a través de un sistema de control de versiones (en inglés Version Control System, VCS). De estos sistemas hay una gran abánico y nosotros resaltaremos el *git*:

* Página oficial de git

  * https://git-scm.com/

* Videos de git (en inglés):

  * Principiante: http://iactalks.iac.es/talks/view/1426
  * Medio: http://iactalks.iac.es/talks/view/1428
  * Advanzado: http://iactalks.iac.es/talks/view/1438

Para mayor información de buenas prácticas puedes leer `la página web <https://deic-hpc.github.io/EuroCC-knowledgepool/best/>`_ (best practices del EuroCC danés).
