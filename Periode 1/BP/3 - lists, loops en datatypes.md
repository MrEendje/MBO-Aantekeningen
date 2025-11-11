## Data types

Data is informatie die een computer kan verwerken. Achter de schermen is alles binair (1 en 0), maar programmeurs hoeven dat meestal niet direct te gebruiken.

### Belang van data types

- Computers hebben duidelijke instructies nodig.
    
- Je moet het juiste type data geven aan de computer.
    
- Fouten voorkomen door juiste data types te gebruiken.
    

### Veelvoorkomende data types

- **Integer**: Hele getallen, maximaal 2,147,483,647.
    
- **String**: Tekst, kan letters, cijfers, symbolen bevatten.
    
- **Boolean**: Waar of niet waar (`True`/`False`).
    
- **Double**: Komma-getallen of zeer grote getallen (64-bit).
    
- **Float**: Komma-getallen, minder groot of minder precies dan double (32-bit).
    
- **Number (JavaScript)**: Alle getallen, vaak hetzelfde als double.
    

### Voordelen van data types

- Helpt computer de juiste instructies te geven.
    
- Beter geheugen- en rekenkrachtgebruik.
    
- Voorkomt fouten bij berekeningen of bewerkingen.
    

---

## Lijsten

Een lijst is een variabele die meerdere waarden kan opslaan.

```python
namen = ["Ali", "Sophie", "Eva"]
print(namen)
# Output: ['Ali', 'Sophie', 'Eva']
```

- Elementen ophalen:
    

```python
print(namen[0])  # Ali
print(namen[2])  # Eva
```

- Let op: Python telt vanaf 0.
    

### For-loop

Gebruik een for-loop om iets voor elk element uit te voeren:

```python
for naam in namen:
    print("Hallo", naam)
```

Output:

```
Hallo Ali
Hallo Sophie
Hallo Eva
```

### Range in for-loop

Met `range()` maak je een reeks getallen:

```python
for i in range(1, 6):
    print(i)
```

Output:

```
1
2
3
4
5
```

### While-loop

Herhaalt iets zolang een conditie waar is:

```python
x = 5
while x > 0:
    print(x)
    x -= 1
```

Output:

```
5
4
3
2
1
```

- Let op: Als de waarde niet verandert, wordt de loop oneindig.
    

### Voordelen van lijsten en loops

- Minder code schrijven voor meerdere waarden.
    
- Automatische herhaling van taken.
    
- Gemakkelijk meerdere items tegelijk verwerken.