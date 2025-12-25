# 📊 Análisis de Churn – Telecom X

## 🧾 Introducción
El propósito de este análisis es ayudar a la empresa **Telecom X** a identificar posibles causas del abandono del servicio (*churn*) por parte de un porcentaje de sus clientes.  
Para ello, se utilizaron métodos de **depuración y preparación de datos** mediante la librería **Pandas de Python**, con el objetivo de obtener un *DataFrame* limpio y estructurado que sirva como base para un análisis más profundo por parte del equipo de ciencia de datos.

Este proyecto busca comprender algunos de los factores que han llevado a los clientes a cancelar el servicio de Telecom X, apoyándose en un análisis exploratorio inicial.

---

## 🧹 Limpieza de los datos
Para facilitar el acceso continuo a los datos, el archivo en formato **JSON** fue cargado en una carpeta de **Google Drive**, desde donde se obtuvo la ruta necesaria para acceder rápidamente al *DataFrame*.

Una vez validado el acceso correcto al conjunto de datos, se realizó un análisis de las columnas, identificando que varias de ellas contenían **diccionarios anidados** con información relevante, tales como:
- Datos de la cuenta
- Información del cliente
- Características del tipo de servicio contratado

Esta información fue extraída y posteriormente **concatenada al DataFrame principal (`df`)**, permitiendo iniciar el análisis de manera estructurada.

Posteriormente, se llevó a cabo el tratamiento de los datos, que incluyó:
- Conversión de columnas con valores numéricos almacenados como texto a tipos numéricos usando `astype(np.int64)`.
- Transformación de variables categóricas binarias (Sí / No) a valores booleanos:
  - `0` para **No**
  - `1` para **Sí**

Este proceso permitió mejorar la consistencia y calidad del conjunto de datos.

---

## 🔍 Análisis exploratorio de los datos
En esta etapa, los datos fueron agrupados según las siguientes variables:
- **Género**
- **Método de pago**
- **Tipo de contrato**

Apoyándose en la **moda**, se calculó la proporción de clientes que abandonan el servicio, obteniendo como resultado una tasa aproximada de **27% de cancelaciones**.

### 📈 Visualizaciones
El siguiente gráfico muestra la probabilidad de *churn* según género, tipo de contrato y método de pago:

<img width="1394" height="467" alt="image" src="https://github.com/user-attachments/assets/7049e6db-0006-4789-b572-8be828825658" />


---

## 📌 Resultados
1. Los clientes de **género masculino** presentan una menor tasa de cancelación.  
   Esto sugiere la necesidad de estudiar la raíz de la insatisfacción en la clientela femenina para reducir el porcentaje de abandono.

2. El **contrato mensual** es el que presenta la mayor tasa de cancelaciones.  
   Esto podría indicar que dicho plan es utilizado como un periodo de prueba para evaluar la calidad del servicio antes de decidir una permanencia a largo plazo.

3. En cuanto al **método de pago**, el **cheque electrónico** muestra la mayor proporción de cancelaciones.  
   Esto podría estar relacionado con preferencias del cliente o limitaciones impuestas por sus instituciones bancarias.

---

## 🧠 Conclusiones y sugerencias

### Conclusiones
Aunque la tasa general de cancelación no es extremadamente alta, sí refleja **problemas en la retención de clientes**.  
Bajo el supuesto de que los planes mensuales y anuales funcionan como periodos de prueba, se observa que al término de estos la retención disminuye considerablemente.

### Sugerencias
- Implementar **estrategias de retención** al momento en que el cliente solicita la cancelación del servicio.
- Ofrecer **promociones temporales o incentivos personalizados**, lo cual podría incrementar la permanencia de los clientes en planes mensuales y anuales.
- Profundizar el análisis con variables adicionales (antigüedad del cliente, cargos mensuales, servicios contratados) para fortalecer la toma de decisiones.

---

## 🛠️ Tecnologías utilizadas
- Python
- Pandas
- NumPy
- Matplotlib / Seaborn
- Google Drive (almacenamiento de datos)

---

## 👤 Autor
**Aaron Sotelo**  
Proyecto académico / Análisis exploratorio de datos
