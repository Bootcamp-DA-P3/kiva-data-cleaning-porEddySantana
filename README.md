# Procesamiento y limpieza de datos con Python
## Mi proceso de trabajo

---

Este proyecto consiste en explorar, limpiar, transformar y validar un dataset de Kiva Crowdfunding utilizando Python y pandas.

---

La parte que más me costó al principio fue preparar el entorno de trabajo. Tuve que familiarizarme con Python, pandas, VS Code y GitHub, además de solucionar algunos problemas de actualizaciones, instalación de pandas y sincronización. También llegué a crear la carpeta del proyecto varias veces por error y, en un momento, VS Code se bloqueó y tuve que reiniciarlo.

Una vez solucionada esta parte, el trabajo comenzó a ser mucho más fluido. También aprendí mejor la interfaz de VS Code, sus menús, la organización de los archivos y algunos atajos de teclado.

---

Al comenzar con el ejercicio fui escribiendo el código paso a paso para entender qué hacía cada instrucción. Utilicé la IA de forma moderada y educativa, principalmente para resolver dudas, entender errores y recibir explicaciones cortas, sin saltarme pasos ni sustituir mi propio proceso de aprendizaje. Al principio trabajaba con líneas y bloques pequeños. Después de repetir y practicar muchas veces, fui comprendiendo mejor las instrucciones y pude trabajar progresivamente.

*Entiendo que, como recomendación y buena práctica, el código debería quedar limpio y simple. En ese sentido, sí limpié 75 códigos que podían interrumpir el buen funcionamiento. Sin embargo, el resto de las pruebas y errores los he dejado como rastro visible del proceso de aprendizaje.*

---

### 🔎 Exploración inicial de los datos

Primero comprobé la estructura y el contenido del dataset utilizando instrucciones como:

```python
df.shape
df.head()
df.info()
df.describe()
df.columns.tolist()

El dataset tenía 42.308 registros y 20 columnas.

🧹 Comprobación y limpieza

Después comprobé los valores nulos y los duplicados mediante:

df.isnull().sum()
df.duplicated().sum()
df["id"].duplicated().sum()

No encontré valores nulos ni duplicados, por lo que no fue necesario sustituir ni eliminar registros por estos motivos.

Mi criterio durante la limpieza fue no modificar los datos simplemente porque parecieran diferentes. Primero comprobé si existía realmente un problema y después decidí qué transformación era necesaria.

##🔧 Transformaciones realizadas

Sí realicé diferentes modificaciones: limpié espacios innecesarios, normalicé determinados textos, convertí las fechas al formato datetime, ajusté algunos tipos de datos y creé nuevas variables para facilitar posteriores análisis.

Para ello utilicé instrucciones como:

df_clean[col] = df_clean[col].str.strip()

df_clean[col] = df_clean[col].str.lower()

df_clean[col] = pd.to_datetime(df_clean[col])
📊 Nuevas variables

También creé variables como el año y mes de publicación y el porcentaje de financiación mediante:

posted_year
posted_month
funding_ratio

Después volví a comprobar los datos para validar que las transformaciones se habían aplicado correctamente.

```🧠 Lo que aprendí

Este proyecto me ayudó a comprender mejor que la limpieza de datos no consiste simplemente en borrar o sustituir información. Aprendí a comprobar primero, decidir después y validar al final.

También mejoré mi manejo de Python y pandas y comprendí mejor el funcionamiento de VS Code, su interfaz, menús, archivos y atajos de teclado. Al principio necesitaba mucha explicación para cada paso. Con la práctica fui necesitando menos ayuda y pude trabajar con bloques de código más largos y entender mejor lo que estaba haciendo.

🚀 GitHub y resultado final

La parte de guardar y subir el proyecto a GitHub fue mucho más sencilla porque ya la habíamos practicado anteriormente. Una vez subido el proyecto, modifiqué también el README para reflejar de una forma más natural el trabajo que realmente había realizado y mi proceso de aprendizaje.

🎨 Una última parte del aprendizaje

Al final también terminé divirtiéndome *“cacharreando”* con Markdown, probando diferentes formas de estructurar y decorar el texto.

*Lo más importante de este proyecto no fue solamente trabajar con la base de datos, sino ir ganando poco a poco comprensión, práctica y autonomía en el trabajo con Python y las herramientas del proyecto.*
