# Laboratorio de Concurrencia en Java

Autor:
Jose Luis Leudo Mosquera  
Universidad Distrital Francisco José de Caldas  
Programación Avanzada  
Grupo: 020-85  
Docente: Nancy Gelvéz García  
Febrero 2026  

# Descripción
Este repositorio contiene la solución a 10 ejercicios prácticos sobre concurrencia en Java, abordando problemas clásicos de sincronización, exclusión mutua, interbloqueo (deadlock) y control de acceso a recursos compartidos.

Se aplican mecanismos fundamentales de programación concurrente como:

- synchronized
- wait() / notify() / notifyAll()
- Semaphore
- CyclicBarrier
- BlockingQueue
- ReentrantLock

# Ejercicios

# 1. Contador Compartido

**Problema:**  
Cinco hilos incrementan un contador inicializado en 0. Cada hilo suma 1000, pero sin sincronización se pierde información debido a condiciones de carrera.

**Solución:**  
Uso de synchronized en el método incrementar() para garantizar exclusión mutua.

**Resultado esperado:**  
5000

# 2. Simulación de Cajero Automático

**Problema:**  
Tres cajeros retiran dinero de una cuenta con saldo inicial de $1000 sin permitir saldo negativo.

**Solución:**  
El método retirar() se implementa como synchronized para asegurar que cada hilo acceda al estado actualizado de la cuenta y evitar inconsistencias.

# 3. Productor–Consumidor con Buffer Limitado

**Problema:**  
Dos productores y dos consumidores comparten un buffer de tamaño 5. Sin sincronización se produce pérdida de información.

**Solución:**  
Se implementa sincronización mediante:
- synchronized
- wait()
- notifyAll()

El productor espera cuando el buffer está lleno y el consumidor espera cuando está vacío.

# 4️. Lectores y Escritores

**Problema:**  
Permitir que múltiples lectores accedan simultáneamente a un recurso, manteniendo acceso exclusivo para el escritor.

**Solución:**  
Se utilizan métodos sincronizados junto con wait() y notify() / notifyAll() para coordinar el acceso concurrente correctamente.

# 5️. Barrera de Sincronización

**Problema:**  
Cinco hilos ejecutan tres fases y ninguno puede avanzar hasta que todos terminen la fase actual.

**Solución:**  
Uso de CyclicBarrier.  
Cada hilo ejecuta su tarea y luego llama a await() hasta que todos alcanzan la barrera.

# 6️. Deadlock Intencional

**Problema:**  
Dos hilos intentan acceder a dos recursos en distinto orden, generando un posible interbloqueo.

**Solución:**  
Se demuestra el problema utilizando bloques synchronized para evidenciar cómo ocurre el deadlock cuando no se respeta un orden consistente en la adquisición de recursos.

# 7️. Filósofos Comensales

**Problema:**  
Cinco filósofos comparten cinco tenedores y deben alternar entre pensar y comer evitando bloqueos.

**Solución:**  
Se utilizan semáforos (Semaphore) para representar los tenedores.  
Se rompe la simetría haciendo que uno de los filósofos tome los recursos en orden inverso para evitar deadlock.

# 8️. Control de Acceso a un Recurso Limitado

**Problema:**  
Cuatro usuarios intentan utilizar una impresora que solo permite dos accesos simultáneos.

**Solución:**  
Uso de Semaphore con capacidad 2.  
Cada hilo utiliza acquire() antes de imprimir y release() al finalizar.

# 9. Cola de Tareas Concurrentes

**Problema:**  
Cinco hilos procesan tareas simultáneamente y pueden perder recursos sin control adecuado.

**Solución:**  
Uso de BlockingQueue para gestionar tareas de forma segura, evitando condiciones de carrera y optimizando la espera de los hilos.

# 10. Simulación de Tráfico

**Problema:**  
Varios autos intentan cruzar un recurso compartido (cruce) al mismo tiempo.

**Solución:**  
Uso de ReentrantLock para garantizar exclusión mutua y liberar el lock correctamente en un bloque finally.

# Conceptos Aplicados
- Programación concurrente
- Exclusión mutua
- Condiciones de carrera
- Deadlock
- Inanición
- Sincronización de hilos
- Semáforos
- Barreras
- Locks explícitos


# Lenguaje Utilizado
Java
