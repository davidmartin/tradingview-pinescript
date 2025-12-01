---
agent: speckit.constitution
---

# Constitución del Proyecto: TradingView Pine Script Strategies

## 🎯 Propósito del Proyecto

Este repositorio contiene estrategias de trading desarrolladas en Pine Script para TradingView,
siguiendo estándares profesionales de desarrollo, testing y documentación.

## 📐 Convenciones Obligatorias

### 1. Nomenclatura de Scripts Pine

**Formato estándar:** `tv_<mercado>_<setup>_<timeframe>.pine`

**Componentes:**

- `tv_` - Prefijo obligatorio para TradingView
- `<mercado>` - crypto | forex | stocks | indices | commodities
- `<setup>` - Descripción breve (ej: breakout, scalping, ema_crossover)
- `<timeframe>` - 1m | 5m | 15m | 30m | 1h | 4h | daily | weekly

**Ejemplos válidos:**

- ✅ `tv_crypto_ema_crossover_15m.pine`
- ✅ `tv_forex_breakout_1h.pine`
- ✅ `tv_stocks_mean_reversion_daily.pine`

### 2. Estándar de Comentarios en Pine Script

Toda estrategia DEBE incluir encabezado completo con:

- Nombre, mercado, timeframe, autor, fecha
- Descripción detallada
- Condiciones de entrada (Long y Short)
- Condiciones de salida (TP, SL, etc.)
- Notas importantes

### 3. Estilo de Backtesting

**Configuración estándar obligatoria:**

- initial_capital: 10000
- commission_value: 0.1%
- slippage: 2
- Gestión de riesgo con TP/SL configurables

### 4. Criterios Mínimos

Toda estrategia DEBE tener:

#### A. Backtest Básico

- Capital inicial, comisiones y slippage configurados
- Timeframe recomendado especificado

#### B. Parámetros Configurables

- Sin valores hardcoded
- Uso de `input.*` con tooltips
- Agrupación lógica con `group=`

#### C. Descripción de Condiciones

- Entrada: Condiciones Long y Short documentadas
- Salida: TP/SL claramente definidos

#### D. Métricas Mínimas Aceptables

- Profit Factor: > 1.5
- Win Rate: > 45%
- Max Drawdown: < 25%
- Total Trades: > 30

## ✅ Checklist de Calidad

- [ ] Nombre sigue convención: `tv_<mercado>_<setup>_<timeframe>.pine`
- [ ] Encabezado completo
- [ ] Parámetros configurables
- [ ] Gestión de riesgo (TP/SL)
- [ ] Backtest > 30 trades
- [ ] Profit Factor > 1.5
- [ ] Resultados documentados
- [ ] Sin repainting

Ver documentación completa en:

- `README.md` - Visión general
- `docs/STYLE_GUIDE.md` - Guía de estilo
- `docs/QUICK_START.md` - Inicio rápido
- `docs/STRATEGY_CHECKLIST.md` - Checklist completo
