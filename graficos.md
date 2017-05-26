##Inserción de gráficos.

Lo primero que tenemos que hacer es añadir lo siguiente en el instrucción en el preámbulo (antes de \begin{document} de nuestro documento para poder trabajar con gráficos.
  
Si compilamos el documento con pdflatex tenemos que usar figuras en formato .png o .jpg e incluir el siguiente paquete:\usepackage[pdftex]{graphicx}
Si usamos LaTeX para compilar el documento tenemos que usar figuras en formato .eps (encapsulated postscript) o en formato .ps (postscript). Hay que usar el paquete:\usepackage[dvips]{graphicx}
  
Con esta linea ya podemos añadir nuestros gráficos, imágenes en nuestro documento, en la parte que corresponda.
  
La estructura típica seria esta:
   
\begin{figure}  
\includegraphics{foto}  
\caption{Foto}  
\label{fig:XXXX}  
\end{figure}
  
Vamos a analizar cada uno de ellos.
  
\begin{figure}[]
  
Parámetros que podemos usar:
  
Especifico Efecto
  
h Coloca la imagen aquí, es decir, aproximadamente en el mismo punto que se produce en el texto original (sin embargo, no exactamente en el lugar) t Coloca la imagen en la parte superior de la página b Coloca la imagen en la parte inferior de la página. ! Coloca en el lugar exacto que queremos. H Lo coloca en el lugar preciso en el código LaTeX. Requiere el paquete flot, por ejemplo, \usepackage {float}; Es algo equivalente a h!
  
\includegraphics{foto}
  
Parámetros que podemos usar:
  
Especifico Efecto Ejemplo width Definimos el ancho de nuestro gráfico
  
\includegraphics[width=60mm]{foto.png} height 
  
Definimos el alto de nuestro gráfico \includegraphics[heigt=60mm]{foto.png} scale Definimos la escala de nuestro gráfico \includegraphics[scale=.75]{foto.png} angle Definimos la rotación de nuestro gráfico \includegraphics[angle=45,width=39mm]{foto.png}
  
\caption{Foto}

Define un "pie de foto" para la imagen. LaTeX añadirá un número correlativo.

Si usamos \listoffigures, nos genera un índice de imágenes, en el punto que lo situemos.

\label{fig:XXXX}

Con \label y \ref, puede crear una referencia al flotante dentro del texto.

\end{figure}

Cerramos el entorno de imágenes.

Un ejemplo con casi todos los parámetros.

La figura \ref{blanco} es un ejemplo de blanco liso. \begin{figure}[!hbp] \includegraphics[angle=37,width=25mm]{blanco.png} \caption{Imagen en blanco, rotada 37 grados.} \label{blanco} \end{figure}
