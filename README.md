# -QMP2-Qu-Me-Pongo---Segunda-iteraci-n---Lovelli
## Resolución:
•	Para la trama de la tela se me ocurrió que sea directamente un Enum ya que conozco las opciones de trama a manejar (lisa, rayada, con lunares, a cuadros o un estampado). En cuanto a como lo relaciono con la prenda pensé 2 posibilidades:
1.	Que la Prenda tenga una Tela y una Trama que se relaciones de manera indirecta a través de la prenda, lo cual posterior mente descarte al leer que [“…no indicar ninguna trama para una tela, y que por defecto ésta sea lisa.”] por lo que me genera que la tela y la trama están relacionadas directamente
2.	Que la Tela posea el Material y la Trama, que el material siga proviniendo del enum pero cambiando el nombre de Tela a Material y que dicho material posea la Trama la cual también es un enum, facilitando que por defecto tenga una trama lisa.
 ![image](https://user-images.githubusercontent.com/40477288/165193160-48a3276f-f3c7-4373-a10b-8a99f388521a.png)

•	Para que el tipo de prenda condicione al material me encontré con una mayor dificultad ya que en mi modelo no se relacionaban directamente, sino que lo hacían a través de la prenda y el nombre del TipoDePrenda podía ingresarse con un string libremente, para esto creo un enum con los posibles nombres del TipoDePrenda. Ya que ahora tiene que cumplir con la condición de que el TipoDePrenda condicione al Material para que no ocurran inconsistencias (lentes de cuero, remera de madera, etc.).
La forma de solucionar esto que se me ocurrió es tener una configuración en donde el TipoDePrenda tiene una lista de posibles telas (las cuales poseen los materiales y tramas).
 ![image](https://user-images.githubusercontent.com/40477288/165193172-0787edc0-a03d-4c3d-916c-e142e108c14d.png)

•	Para el borrador de la prenda me di cuente que me faltaba algo fundamental del sistema, el Usuario, el cual posee al Armario el cual es el encargado de poseer las prendas creadas por le Usuario y de validar si la Prenda cumple con las condiciones para poder generarse correctamente; y también posee a la Prenda que estaba creando para poder continuarla luego.
 ![image](https://user-images.githubusercontent.com/40477288/165193178-3847295d-593d-4e0d-9c8c-6fdc33fb8c23.png)

•	Para esto la Tela posee un constructor donde si no recibe una trama la crea lisa.

## Bonus:
•	Para manejar la incorporación de instituciones relaciono al usuario del sistema con una institución para así poder pedirle a este que genere el uniforme para esta institución, esto me permite que cada usuarie lo genere con las prendas propias que posee y en caso de querer puedo incorporar roles de usuario creando un usuario administrador de la institución. 
•	La lógica de que el uniforme siempre posea la parte superior, inferior y el calzado la manejaría en el generarUniforme(), fijándome que si la institución posee un criterio entonces necesita una prenda que cumpla con ese criterio, sino no lo generaría, el criterio del accesorio lo agrego por si se necesita una corbata, por ejemplo.
•	El poder confeccionar un uniforme específico para la institución lo aplico con el criterio por institución.
 ![image](https://user-images.githubusercontent.com/40477288/165193184-481fd26f-1d9f-4cbd-85f1-0025c45659bd.png)
## Modelo Final
![image](https://user-images.githubusercontent.com/40477288/165193232-b84b1b4e-1e86-4546-998e-5360277c47bf.png)
