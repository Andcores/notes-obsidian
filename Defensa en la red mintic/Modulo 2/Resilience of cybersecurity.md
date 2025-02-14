# High availability
Alta disponibilidad describe  los sistemas hechos para no perder tiempo.
Esta se a vuelto imprescindible ya que los sistemas de información actualmente los usamos  en todo momento, para la vida moderna.
Estos se basan en 3 principios de diseño 

1. Eliminar puntos únicos de falla: Se busca identificar aquello que haga que falle el sistema completamente. Parte de la solución reemplazar y/o eliminar dispositivos  de reserva activos, componentes redundantes y multiples conexiones o rutas.
2. Proporcionando un crossover confiable : Tener un respaldo de energia y comunicacion brindan un crossover confiable
3. Detectar fallas a medida que se producen: Monitoreo activo de los dispositivos , esto se hace para detectar fallas  o eventos. Esto podria activar el sistema de respaldo en caso de falla 

# The fine nines 

De las practicas mas  populares es lograr una tasa de disponibilidad del 99.999, en la  practica significa 5.26 al año de inactividad 

Pasos para alcanzar los 5 nueves 
1. Sistemas estandarizados: Esto básicamente estandariza los componentes de sistemas, así sis e tiene que reemplazar algo es mas fácil de hacerlo  durante un emergencia .Algunas instalaciones usan guardias de seguridad para  las instalaciones de mayor seguridad, esto pude hacer que los guardias descubran y diferencien varias condiciones y situaciones, y tomar decisiones en su lugar 
2. Agrupaciones: Se agrupan varios dispositivos, que para el usuario podría ser solo 1. Si uno de estos falla en su lugar están los otros.
3. Sistemas de componentes compartidos : Estos sistemas se construyen para que un sistema completo pueda sustituir a otro que haya fallado 


# Unique points of failure

Los puntos únicos de falla, se podría definir como es eslabón mas débil de una cadena , en este caso supondría una falla en todo el sistema.
Este podría ser un daño en la parte de hardware especifico , una pieza de datos una utilidad un proceso .
Usualmente su solución  es modificar la operación critica para que no dependa de solo 1  elemento 