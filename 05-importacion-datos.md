# Importación de datos: El paso más crítico

Esta es la sección MÁS IMPORTANTE. Si importas datos incorrectamente, toda tu declaración será incorrecta.

## Estrategia general de importación

**IMPORTANTE:** Importa **TODOS** tus exchanges y wallets, **incluso** si tienes pocos o si crees que no son importantes. La falta de una transacción puede afectar el cálculo FIFO de todas las demás.

## Exportar datos de Exchanges

### Desde Binance

1. Accede a **Account** → **Binance Rewards** (en billetera) → **Download Statement**
2. Selecciona el período (enero a diciembre del año fiscal)
3. Descarga el archivo CSV (puede ser grande)
4. En Investaxes, ve a **Accounts** → **Add Account** → **Binance**
5. Carga el archivo CSV
6. Investaxes procesa automáticamente

**Nota:** Si tienes demasiadas transacciones, Binance puede generar múltiples archivos. Cárgalos todos.

### Desde Coinbase

1. Ve a **Settings** → **Reports**
2. Haz clic en **Generate Report** para el año fiscal completo
3. Descarga el CSV
4. En Investaxes, carga como cuenta Coinbase

### Desde Kraken

1. Ve a **Settings** → **API**
2. Crea una API Key con permisos de **lectura solamente**
3. En Investaxes, conecta directamente con la API
4. O descarga manualmente: **History** → **Export** → **CSV**

### Desde Bit2Me (Exchange español)

1. Accede a tu cuenta en **Bit2Me.com**
2. Ve a **Historial**
3. Descarga el CSV
4. En Investaxes, sube como **Importación genérica**

### Otros exchanges

Para exchanges no listados:
1. Ve a **Importación Genérica - Excel**
2. Descarga la plantilla
3. Exporta datos manualmente o desde tu exchange
4. Completa la plantilla
5. Importa en Investaxes

## Importar direcciones Blockchain (CRÍTICO para DeFi)

Este paso es **imprescindible** si usas MetaMask, Ledger, TrustWallet, o cualquier wallet descentralizada.

1. Ve a **Accounts** → **Add Account** → **Blockchain**
2. Selecciona la blockchain (Ethereum, Solana, Polygon, etc.)
3. Pega tu dirección pública (NO tu clave privada)
4. Investaxes escanea automáticamente toda tu actividad
5. Detecta: Swaps, Transfers, Staking, Lending, Airdrops, etc.

**Seguridad:** Solo necesitas tu dirección pública. Nunca compartas tu clave privada con nadie.

## Sincronización y verificación

Después de importar:

1. **Espera a que sincronice** (puede tomar 5-30 minutos según volumen)
2. Ve a **Transactions** para ver todos tus movimientos
3. Investaxes debe mostrar el total de transacciones importadas
4. Verifica que **fechas** y **montos** sean correctos
5. Si hay errores obvios, Investaxes los señala en **Error Management**

