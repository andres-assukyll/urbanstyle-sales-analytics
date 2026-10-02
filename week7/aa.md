# Nädal 7: Python Pandas

**Nimi:** Andres Assuküll   
**Meeskond:** Sales Analytics    
**Roll:** A – Data loading and cleaning  
**Andmeallikad:** Nädal 1 CSV failid (sales.csv + customers.csv)
<br>

### A: Andmete laadimine

```python
import pandas as pd

# Müügi- ja klienditabeli laadimine

df_sales = pd.read_csv('sales.csv')

print(' === Esimesed 5 müügitabeli rida === \n')
print(df_sales.head())
print('\n === Ridade ja veergude arv sales tabelis === \n')
print(df_sales.shape)

df_customers = pd.read_csv('customers.csv')

print('\n === Esimesed 5 klienditabeli rida === \n')
print(df_customers.head())
print('\n === Ridade ja veergude arv customers tabelis === \n')
print(df_customers.shape)

# Tabelite JOIN by customer_id

df = pd.merge(df_sales, df_customers, on='customer_id', how='left')

print('\n === Esimesed 5 ühendatud tabeli rida === \n')
print(df.head())
print('\n === Ridade ja veergude arv ühendatud tabelis === \n')
print(df.shape)
print('\n === Andmetüübid ühendatud tabelis === \n')
print(df.dtypes)
```

### B: Andmete puhastamine

```python
# Algne DF

print(' === Ühendatud tabeli read ja veerud enne puhastamist === \n')
print(df.shape)

# Duplikaatide leidmine 

print('\n === Duplikaatide arv === \n')
print('Duplikaadid:', df.duplicated(subset=['invoice_id']).sum())

# Duplikaatide eemaldamine

df = df.drop_duplicates(subset=['invoice_id'], keep='first')

# NULL väärtused

print('\n === NULL-väärtuste arv === \n')
print("NULL-id:\n", df.isnull().sum())

# NULL-ide eemaldamine veergudes: customer_id, sale_date, total_price

df = df.dropna(subset=['customer_id', 'sale_date', 'total_price'])

# Kuupäeva teisendamine

df['sale_date'] = df['sale_date'].apply(lambda x: pd.to_datetime(x, format='%d/%m/%Y')
                                        if '/' in x else pd.to_datetime(x)
                                        )

# 26 kuud alates 01/2023

before = len(df) # Enne kuupäevavahemiku filtreerimist

df = df[(df['sale_date'] >= '2023-01-01') & (df['sale_date'] < '2025-03-01')]

print('\n === Kuupäevavahemiku tõttu eemaldatud read === \n') 
print(before - len(df))

# Äärmuslikud väärtused total_price veerus

print('\n === Negatiivsete total_price väärtuste arv === \n')
print((df['total_price'] < 0).sum())

# # Negatiivsete total_price väärtuste eemaldamine  

df = df[df['total_price'] > 0]

# PUHASTUSRAPORT

print('\n === Puhastamisraport === \n')
print(f'Puhastatud tabel: {df.shape[0]} rida, {df['customer_id'].nunique()} klienti')
print(f'Kuupäevavahemik: {df['sale_date'].min().date()} - {df['sale_date'].max().date()}')
```
