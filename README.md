# Laboratorio de Concurrencia en Java

Autor:
Jose Luis Leudo Mosquera  
Universidad Distrital Francisco José de Caldas  
Programación Avanzada  
Grupo: 020-85  
Docente: Nancy Gelvéz García  
Febrero 2026  

## Índice

- [Descripción](#descripción)
- [Ejercicios](#ejercicios)
- [Aplicación de los conceptos](#aplicación-de-los-conceptos)
- [Problemas abordados](#problemas-abordados)
- [Recursos necesarios para su ejecución](#recursos-necesarios-para-su-ejecución)
- [Uso](#uso)
- [Licencia](#licencia)
- [Contribuciones](#contribuciones)


## Descripción

Este repositorio contiene metodos de como se implementan 10 ejercicios prácticos sobre **concurrencia en Java**, abordando problemas de sincronización, exclusión mutua, interbloqueo (deadlock) y control de acceso a recursos compartidos. Como objetivo comprender cual mecanismo tendremos que aplicar a cada uno de los problemas para que la sincronización funcione correctamente.

## Ejercicios

1. Contador compartido
2. Simulación de cajeros automáticos
3. Productor – Consumidor con buffer limitado
4. Lectores y escritores
5. Barrera de sincronización
6. Deadlock intencional
7. Filósofos comensales
8. Control de acceso a un recurso limitado
9. Cola de tareas concurrente
10. Simulación de tráfico

## Aplicación de los conceptos

-  **Sincronización Básica:**
- Uso de `synchronized` para garantizar la exclusión mutua.
- Coordinación con `wait()`, `notify()` y `notifyAll()`.
  
- **Sincronización Avanzada (java.util.concurrent):**
  
- Control de acceso con **Semáforos** (`Semaphore`).
- Puntos de encuentro entre hilos usando **Barreras** (`CyclicBarrier`).
- Comunicación segura entre hilos con **Colas Bloqueantes** (`BlockingQueue`).
- Uso de **Locks explícitos** (`ReentrantLock`) para un control más fino.
      
## Problemas abordados:

- **Exclusión Mutua**= synchronized, ReentrantLock.
- **Deadlock (Interbloqueo)**= Lock, ReentrantLock, tryLock().
- **Programación Concurrente**= Thread, Runnable.
- **Semáforos**= Semaphore.
- **Barreras**= CyclicBarrier.
      
## Recursos necesarios para su ejecución

Para la ejecución de estos ejercicios practicos de concurrencia es necesario, lo siguiente: 

1. Sistema operativo (Windows, Linux o macOs)
   
2. Java Oracle para el **IDE Netbeans** (versión 21): https://download.oracle.com/java/21/latest/jdk-21_windows-x64_bin.exe (sha256)
   
3. Tener instalado un entorno o **IDE** para su ejecución, como:
   
- **Visual Studio Code:** https://code.visualstudio.com/download
   
- **NetBeans:** https://netbeans.apache.org/front/main/download/nb28/

- **IntelliJ IDEA:** https://www.jetbrains.com/idea/download/
   
4. Abrir la carpeta con los ejercicios practicos llamada (laboratorio_concurrencia) y ejecutar cada uno de los programas en el IDE.
   
5. Darle correr según el IDE para visualizar el resultado.

## Uso

Estos programas están creados con fines educativos y demostrativos para comprender los principios fundamentales de la concurrencia en Java. Cada ejercicio aborda un problema específico de sincronización y muestra cómo diferentes mecanismos (synchronized, semáforos, barreras, etc.) pueden aplicarse para resolverlo.

## Licencia
Este proyecto está bajo la licencia MIT. Consulta el archivo [LICENSE](LICENSE) para más detalles.

## Contribuciones

Este es un proyecto de carácter académico, por lo que no se esperan contribuciones externas. Sin embargo, si encuentras algún error o tienes una sugerencia, no dudes en preguntarme para discutirlo.
