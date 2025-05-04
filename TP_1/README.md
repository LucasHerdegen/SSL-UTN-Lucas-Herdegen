# 1. Preprocesador

Para solo preprocesar se usa: gcc -E archivo.c -o archivo.i

Conclusiones de hello2: el .i a diferencia del .c remueve comentarios y los reemplaza por un espacio, y hace un copia
y pega de la biblioteca que incluimos

La semantica de 'int printf(const char * restrict s, ...);', es que es el prototipo de una funcion llamada printf,
que recibe minimoun parametro de tipo cadena, y que retorna un entero

Diferencias entre hello3.c y hello3.i: es igual solo que arriba del .i se agregan
#0 "hello3.c"0 "built-in"0 "command-line"1 "hello3.c

# 2. Compilacion

Para parar despues de la compilacion se usa: gcc -S archivo.c -o archivo.s

En el codigo assembler, primero se hacen los preparativos antes de llamar a la funcion principal,
y una vez realizado se llama a 'main'. Se ejecuta 'main', llamando a printf, y al final retorna

Para parar despues de ensamblar se usa: gcc -c archivo.c -o archivo.o

# 3. Vinculacion

Para parar despues de vincular se usa: gcc archivo.o -o ejecutable

Cuando genero el ejecutable de hello4, el programa me imprime un valor inconsistente.
Aunque no incluya la libreria, el compilador reconoce 'printf'

# 4. Correccion del bug

Una vez generado el ejecutable, con poner './ejecutable', se ejecutara normalmente

Una vez añadimos lo que queremos imprimir, ya no imprimirá valores inconsistentes por pantalla