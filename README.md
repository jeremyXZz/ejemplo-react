# ejemplo-react
demo de react, esto tendra el contenido 

La función Square renderiza un botón que se utiliza para representar cada uno de los cuadrados del tablero de juego. Recibe dos propiedades: value, que representa el contenido del cuadrado (puede ser "X", "O" o nulo), y onSquareClick, que es una función que se ejecuta cuando se hace clic en el botón.

La función Board renderiza el tablero de juego completo y se encarga de manejar el estado de los cuadrados y del juego en general. Recibe tres propiedades: xIsNext, que indica si el próximo jugador es "X" o "O"; squares, que es un arreglo de nueve elementos que representa el estado actual del tablero; y onPlay, que es una función que se ejecuta cada vez que se realiza un movimiento.

La función handleClick se llama cuando el jugador hace clic en uno de los cuadrados del tablero. Primero comprueba si ya hay un ganador o si el cuadrado ya ha sido seleccionado, en cuyo caso no hace nada. Si el movimiento es válido, actualiza el arreglo squares con la nueva jugada y llama a la función onPlay con el nuevo arreglo.

La función calculateWinner determina si hay un ganador en el juego. Comprueba todas las posibles combinaciones de líneas en el tablero para ver si todas las casillas en la línea tienen el mismo valor (ya sea "X" o "O"). Si encuentra una línea ganadora, devuelve el valor del ganador ("X" o "O"); de lo contrario, devuelve nulo.

La función Game es la función principal que renderiza el juego completo y maneja el estado del historial de movimientos. Utiliza los hooks useState para mantener el historial de movimientos y el índice del movimiento actual. También define dos funciones, handlePlay y jumpTo, que se utilizan para actualizar el estado del historial de movimientos y del movimiento actual. Finalmente, renderiza el tablero de juego y el historial de movimientos, utilizando la función Board y una lista ordenada de botones que representan cada movimiento en el historial.