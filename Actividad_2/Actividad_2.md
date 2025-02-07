## 📤 Para la bitácora

1. Escribe un párrafo explicando, en tus propias palabras, cómo se representan los datos en una computadora. Por ejemplo, ¿cómo se ingresan números, letras, imágenes a una computadora?

    
    - Los datos en loc computadores se codifican binariamente, con 0 y 1, ya que los circuitos solo pueden estar encendidos o apagados, 0 apagado 1 encendido.

        - Números: Se pasan de sistema decimal a binario

        - Letras: con estandares ACII o Unicode se le asigna un valor numérico a la letra, luego este se pasa a binario y se almacena.

        - Imágenes: Cáda pixel tiene un color dado por RGB (RED GREEN BLUE, el más usado para pantallas) ó CMYK, estos se representan por códigos de números asociados a cada color, es decir en RGB, un valor de rojo, uno de verde, y uno de azul, estos números se pasan a binario y se almacenan.
            - Dato curioso (teoría fotográfica del color): El sistema RGB viene derivado de los colores de los leds, y los tonos se basan en la iluminación. EL sistema CMYK se utiliza principalmente para tintas, dado que el objetivo es cubrir un fondo blanco con otros colores. Originalmente el proposito de RGB y CMYK era opuesto. En la intersección se ve como RGB es blanco porque busca iluminar, y CYMK busca oscurecer:

                ![colores](./images/img1.jpg)
    
    - 
         - Sonido: se almacenn valores numéticos querepresentan la amplitud de onda en intervalos temporales. Estos valores se pasan a binario y se amacenan.

        -  Videos: Se codifican las imágenes y el sonido y se comprimen usando distintos formatos. Los valores númericos comprimidos se pasan a binario y se almacenan.


2. Luego de realizar el ejercicio 1, escribe tus conclusiones acerca de la pregunta planteada en la Figura 2. ¿Cuántos estados diferentes pueden ser representados por N variables binarias?


    ```
    2**N ó 2^N
    ```

3. ¿Cuáles son las unidades de almacenamiento de datos que se utilizan en computación? Crea una tabla donde muestres estas unidades con sus prefijos. En este caso me refiero a KiloByte, MegaByte, etc. 

    ![Tabla](./images/img2.png)


4. Incluye un pequeño resumen, de un par de renglones, donde menciones la importancia del trabajo de George Bool en este tópico.

-  El trabajo de Boole permite que los computadores puedan funcionar, ya que con una lógica binaria se puede representar la energización o ausencia de energía en los circuitos, es decir estado encendido y apagado. Sin embargo no se reduce solo a eso, dado que con una lógica binaria, se puede tener un valor de verdad, haciendo así posibles los loops. Si la lógica Booleana binara no existiese, no tendríamos sistemas de cómputo como los conocemos-