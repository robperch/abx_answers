# Roberto Pérez Technical Interview Answers

## Objective
Forecast demand of a product for a given week, at a particular store.

## Project details
- Weekly delivery trucks
- Transaction:
    - Sales: Delivered product 
    - Returns: Unsold and expired products
- Demand: sales (current week) - returns (next week)

## Answers
1. Algorithm used
2. Time-series of determined product-client-agency combination
3. Metrics to support algorithm
4. Sample of clients that represent agency
5. Week 9 prediction of top 3 selled productsin client sample
6. Flowchart of algorithm steps
    1. Find top 3 products 

## Files used
- cliente_tabla.csv (ID feature: Cliente_ID)
- producto_tabla.csv (ID feature: Producto_ID)
- town_state.csv (ID feature: Agencia_ID)

## EDA Observations
- cliente_tabla.csv
    - There are 4,862 Client_ID entries that appear 2 times
    - Decided to drop the 4,862 duplicated entries assuming there is no loss of relevant information 

## Data features
Semana — Week number (From Thursday to Wednesday)
Agencia_ID — Sales Depot ID
Canal_ID — Sales Channel ID
Ruta_SAK — Route ID (Several routes = Sales Depot)
Cliente_ID — Client ID
NombreCliente — Client name
Producto_ID — Product ID
NombreProducto — Product Name
Venta_uni_hoy — Sales unit this week (integer)
Venta_hoy — Sales this week (unit: pesos)
Dev_uni_proxima — Returns unit next week (integer)
Dev_proxima — Returns next week (unit: pesos)
Demanda_uni_equil — Adjusted Demand (integer) (This is the target you will predict)