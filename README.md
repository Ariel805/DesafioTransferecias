Simuladores Interactivos
Desafío Técnico de Programación Web

Descripción

Plataforma web interactiva con dos simuladores matemáticos desarrollados en **HTML, CSS y JavaScript**. Incluye una página de inicio con navegación hacia cada simulador.

Estructura de Archivos

simuladores/
├── index.html          → Página principal con acceso a los dos simuladores
├── estilos/
│   └── styles.css      → Estilos compartidos (tema, variables, componentes)
├── javascript/
│   ├── calor.js        → Lógica del Ejercicio 1
│   └── combinaciones.js → Lógica del Ejercicio 2 (con función factorial propia)
│
├── calor.html          → Simulador de Transferencia de Calor (Ejercicio 1)
├── combinaciones.html  → Calculador de Combinaciones Complejas (Ejercicio 2)
│
└── README.md           → Este archivo
Ejercicio 1 — Simulador de Transferencia de Calor

Calcula la temperatura final de un objeto usando la **Ley de Enfriamiento de Newton**.

Fórmula

T = Ts + (T0 - Ts) * e^(-k * t)


| Variable | Descripción |
|----------|-------------|
| `T`  | Temperatura final (°C) |
| `T0` | Temperatura inicial (°C) |
| `Ts` | Temperatura del entorno (°C) |
| `k`  | Constante de enfriamiento (positiva) |
| `t`  | Tiempo transcurrido (horas) |

### Ejemplo de Prueba

| Campo | Valor |
|-------|-------|
| T0    | 120 °C |
| Ts    | 38 °C |
| k     | 0.45 |
| t     | 3 horas |

**Resultado esperado: `59 °C`**

### Implementación JS
- Captura con `document.getElementById().value`
- Cálculo exponencial con `Math.exp()`
- Redondeo con `Math.round()`
- Validaciones: campos vacíos, `k > 0`, `t ≥ 0`

---

## 🎰 Ejercicio 2 — Calculador de Combinaciones Complejas

Calcula el total de combinaciones posibles para un sorteo con **dos grupos independientes**, multiplicando sus resultados.

### Fórmula
```
C(n, r) = n! / (r! * (n - r)!)
Total   = C(n1, r1) × C(n2, r2)
```

### Valores Preconfigurados

| Grupo | n | r |
|-------|---|---|
| Grupo 1 | 59 | 5 |
| Grupo 2 | 35 | 1 |

**Resultado esperado: `5.006.386 × 35 = 175.223.510`**

### Implementación JS
- **Función `factorial(num)`** propia e iterativa (sin librerías externas)
- **Función `combinacion(n, r)`** que aplica la fórmula estándar
- Validaciones: `r > n`, valores negativos, campos vacíos
- Resultado formateado con `toLocaleString()` para legibilidad

---

## 🛠️ Tecnologías Utilizadas

| Tecnología | Uso |
|------------|-----|
| HTML5 semántico | Estructura con `<form>`, `<input>`, `<label>`, `<button>` |
| CSS3 + Variables | Box Model, Flexbox, tema oscuro, animaciones |
| JavaScript Vanilla | Lógica matemática, DOM, validaciones |
| Google Fonts | Tipografías Syne + Space Mono |


## 👤 Autor

-Ariel Orlando Bustillos Cadena-
Carrera de Informática - Universidad Mayor de San Andrés (UMSA) 
Desafío Técnico de Programación Web
