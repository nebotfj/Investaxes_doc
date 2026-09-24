# Gestión de errores y alertas

## Tipos de alertas en Investaxes

### Precio faltante

**Síntoma:** Alerta roja que dice "Missing price"

**Causa:** Investaxes no encontró el precio histórico de esa operación

**Soluciones:**
1. Usa CoinGecko.com: Busca la moneda → Historical data
2. Edita la transacción
3. Introduce el precio manualmente
4. Guarda

**¿Por qué pasa?**
- Monedas muy pequeñas (microcaps)
- Fecha incorrecta
- Moneda descontinuada

### Transacción duplicada

**Síntoma:** Dos transacciones idénticas (misma fecha, monto, tipo)

**Causa común:** Transferencia entre exchanges aparece en ambos
- Ejemplo: Transfer de Binance a Kraken se ve como:
  - Binance: -1 BTC
  - Kraken: +1 BTC
  - Se ve como transacción doble si se importaron por separado

**Solución:**
1. Ve a **Error Management** → **Duplicates**
2. Identifica cuál es la duplicada
3. Marca como "Duplicate" y elimina una
4. Guarda

### Movimiento interno no coincide exactamente

**Síntoma:** Envías 1 BTC pero recibes 0.99 BTC

**Causa:** Comisión de red de blockchain

**Solución:**
1. Es normal (comisión de minería)
2. Investaxes te lo señala para que lo verifiques
3. Marca como "Confirmed"
4. O edita el monto si fue mayor la comisión de lo esperado

### Precio muy alto/bajo

**Síntoma:** Alerta sobre un precio que parece incorrecto

**Ejemplo:** BTC a €100,000 en 2023 (cuando debería haber estado en €30,000)

**Solución:**
1. Revisa manualmente en CoinGecko
2. Si efectivamente es incorrecto, edita la transacción
3. Introduce el precio correcto

## Errores fiscales comunes

### Error: Ganancia/pérdida incorrecta

**Síntoma:** Reporte muestra €50,000 pero esperas €30,000

**Causas y soluciones:**

1. **Precio de compra incorrecto**
   - Solución: Revisa cada transacción en CoinGecko
   - Si es incorrecto, edita y corrigue
   - Regenera reporte

2. **Falta el precio de compra**
   - Solución: Si compraste pero no aparece, agrégalo manualmente
   - Ve a Transactions → Add Manual Transaction

3. **Operación mal clasificada**
   - Síntoma: Una venta aparece como "Transfer"
   - Solución: Edita la transacción, cambia el tipo
   - Regenera reporte

4. **Comisiones no contabilizadas**
   - Solución: Verifica que las comisiones se hayan restado del precio
   - Investaxes debería hacerlo automáticamente

### Error: Modelo 721 dice SÍ pero tengo en exchange español

**Causa:** Investaxes clasifica mal qué es "extranjero"

**Solución:**
1. Ve a **Accounts**
2. Selecciona cada exchange
3. Edita la configuración
4. Marca exchanges españoles como "National"
5. Regenera reporte

### Error: Staking rewards no aparecen

**Causa:** Wallet blockchain no está sincronizada

**Solución:**
1. Ve a **Accounts** → **Blockchains**
2. Verifica que tu dirección esté conectada
3. Puede tomar 30 minutos sincronizarse
4. Regenera reporte

### Error: Swap no se calcula correctamente

**Causa común:** Swap de moneda muy pequeña que Investaxes no reconoce

**Solución:**
1. Ve a Transactions
2. Edita el swap manualmente
3. Introduce precios correctos en ambos lados
4. Guarda

## Validación previa a presentar

**ANTES de presentar a Hacienda, verifica:**

Checklist fiscal:
- [ ] ¿Todas las transacciones tienen fecha?
- [ ] ¿Todos los precios están completos?
- [ ] ¿No hay errores obvios en cantidades?
- [ ] ¿El total de ganancias/pérdidas suma correctamente?
- [ ] ¿El total de staking está presente?
- [ ] Si tengo > €50k en exchange extranjero: ¿Necesito Modelo 721?
- [ ] Si tengo > €700k en total: ¿Necesito Impuesto Patrimonio?
- [ ] ¿Tengo guardados registros de 6 años?

Si todo está ✅: Procede a presentar.

Si hay dudas ❓: Contacta con soporte o un asesor.

