<div align="center">

# <img src="https://media.tenor.com/3KTBgh3cYyAAAAAi/chart-graph.gif" width="40"> TradePink

</div align="center">

## ⚠️ Advertencia

- Este proyecto es sólo para fines educativos.
- Verifica siempre precios y datos antes de tomar decisiones financieras.
- **No me hago responsable del mal uso de la información o los datos ofrecidos por las APIs.**

</div>

---

📋 Panel local para ver cotizaciones de acciones en:

- USD (precio en tiempo casi real con Twelve Data)
- Dólar blue (DolarAPI)
- Pesos ARS (USD × Dólar blue)

---

## ✅ Requisitos

- Navegador web.
- Editor de texto (Visual Studio Code, Sublime, Bloc de notas, etc)
- Cuenta gratuita en https://twelvedata.com para obtener tu API key (hasta 800 requests diarias en el plan free)
- Conexión a internet (para llamadas a APIs y recursos CDN como Bootstrap / Google Fonts)

---

## 🚀 Configuración

1. Abre el archivo:
   - Cotizaciones automaticas.html

2. Dentro del archivo, busca la sección de configuración en el `<script>`:

```js
const API_KEY = "";
```

3. Pega tu API key de Twelve Data entre las comillas:

```js
const API_KEY = "TU_API_KEY_DE_TWELVEDATA";
```

4. Edita la lista de símbolos que se consultarán (por defecto):

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

## 🛠️ Ejecución (local)

No necesita backend. Se ejecuta directamente en el navegador.

1. Siguiendo las instrucciones previas, edita API_KEY & symbols del archivo `Cotizaciones automaticas.html` con un editor de texto.
2. Abre el archivo `Cotizaciones automaticas.html`.
3. Al cargar la página:
   - Se hace una petición a `https://dolarapi.com/v1/dolares/blue` para obtener el dólar blue.
   - Se consultan los precios de las acciones en `https://api.twelvedata.com`.
   - Se calculan los precios en pesos (USD × blue) y se muestran en la tabla.
4. Si las APIs responden con error o tu API key es inválida, verás valores `N/D` en la tabla y errores en la consola del navegador.

> Nota: controla la frecuencia de actualización y la cantidad de símbolos para no superar las cuotas de la API gratuita.

---

## 🧰 Herramientas

- HTML + CSS + JavaScript puro
- Bootstrap 5 (layout y tablas)
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
