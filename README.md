<div align="center">

# <img src="https://media.tenor.com/3KTBgh3cYyAAAAAi/chart-graph.gif" width="40"> TradePink

</div align="center">

## ⚠️ Advertencia

- Este proyecto es sólo para fines educativos.
- Verifica siempre precios y datos antes de tomar decisiones financieras.
- **No me hago responsable del mal uso de la información o los datos ofrecidos por las APIs.**

</div>

---

## 📋 Descripción TradePink (Panel)

Panel local para ver cotizaciones de acciones en:

- USD (precio en tiempo casi real con Twelve Data)
- Dólar blue (DolarAPI)
- Pesos ARS (USD × Dólar blue)

---

## 🔢 Descripcion TradePink Calculator

Calculadora local y muy simple para calcular cuántas acciones tienes según tu inversión, funciona completamente en el navegador.

Cómo usarla:

1. Abre TradePink_Calculator.html.
2. Por cada fila:
   - Ingresa el Símbolo.
   - Ingresa Precio por acción (USD).
   - Ingresa Monto invertido (USD).
3. Para añadir filas usa el botón "+" en la cabecera; para eliminar usa "-" en cada fila.
4. Presiona "Calcular todo".
5. En el recuadro de resultados verás una línea por cada entrada con la cantidad de acciones calculadas (monto / precio), redondeada a 4 decimales.

Notas:
- Valida que el precio sea > 0. Si los campos están incompletos o inválidos, esa fila se ignora en el cálculo.

---

## ✅ Requisitos TradePink (Panel)

- Navegador web.
- Editor de texto (Visual Studio Code, Sublime, Bloc de notas, etc)
- Cuenta gratuita en https://twelvedata.com para obtener tu API key (hasta 800 requests diarias en el plan free)
- Conexión a internet (para llamadas a APIs y recursos CDN como Bootstrap / Google Fonts)

---

## ⬇️ Descarga

Te llevara a la vista del archivo en GitHub, luego das click a descargar:

- TradePink:
[Download HTML](https://github.com/lil-mati/TradePink/blob/main/TradePink.html)
- TradePink Calculator:
[Download HTML](https://github.com/lil-mati/TradePink/blob/main/TradePink_Calculator.html)

--- 

## 🚀 Configuración TradePink (Panel)

1. Ingresa a https://twelvedata.com, crea una cuenta y obten tu API key (NO compartas esta key)

2. Abre el archivo:
   - TradePink.html

3. Dentro del archivo, busca la sección de configuración en el `<script>`:

```js
const API_KEY = "";
```

4. Pega tu API key de Twelve Data entre las comillas:

```js
const API_KEY = "TU_API_KEY_DE_TWELVEDATA";
```

5. Edita la lista de símbolos que se consultarán (por defecto):

```js
let symbols = [
    "AAPL",
    "MSFT",
    "TSLA",
    "AMZN",
    "NVDA",
];
```

Cada símbolo representa 1 consulta por actualización. Ajusta la lista según tus necesidades para no exceder el límite de tu plan.

---

## 🛠️ Ejecución TradePink (local)

No necesita backend. Se ejecuta directamente en el navegador.

1. Siguiendo las instrucciones previas, edita `API_KEY` & `symbols` del archivo `TradePink.html` con un editor de texto.
2. Abre el archivo `TradePink.html`.
3. Al cargar la página:
   - Se hace una petición a `https://dolarapi.com/v1/dolares/blue` para obtener el dólar blue.
   - Se consultan los precios de las acciones en `https://api.twelvedata.com`.
   - Se calculan los precios en pesos (USD × blue) y se muestran en la tabla.
4. Si las APIs responden con error o tu API key es inválida, verás valores `N/D` en la tabla y errores en la consola del navegador.

> Nota: controla la frecuencia de actualización y la cantidad de símbolos para no superar las cuotas de la API gratuita.

---

## 🧰 Herramientas

- HTML + CSS + JavaScript
- Bootstrap 5
- Google Fonts – DynaPuff
- APIs externas:
  - Twelve Data — precios en USD (https://twelvedata.com)
  - DolarAPI — dólar blue (https://dolarapi.com/)

---

<div align="center">

### ⭐ Si este proyecto te fue útil, considera darle una estrella

**Made with ❤️ for learning**

<img src="https://media.tenor.com/amZ5wxLGUEoAAAAi/hugging-heart-snoopy.gif" width="100">

</div>
