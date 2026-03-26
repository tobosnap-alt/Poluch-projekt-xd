# Poluch-projekt-xd

## WinNC Sústruh - Príklad programu

### Kus: Stupňovitý hriadeľ

```
|<-- 30mm -->|<---- 50mm ---->|<-- 20mm -->|
|            |                |            |
+---fi30-----+-----fi45-------+----fi50----+
  (schod)                          (surový)
```

### Polotovar
- Tyč fi50 × 120 mm, oceľ C45

### Nástroje
| T | Popis | Použitie |
|---|-------|----------|
| T1 | Hrubá platničká CNMG 120408 | Hrubé sústruženie |
| T2 | Dokončovacia VBMT 110304 | Čistenie kontúry |
| T3 | Zápichovací nôž 3mm | Zárezy / zápichy |

### Postup
1. **Hrubovanie** — odsustrúžiť na fi46 a fi34 (prídavok 0.5mm)
2. **CYCLE95** — dokončovací cyklus podľa kontúry `_KONTURA`
3. **Zazraznenie** — chamfer 1×45° na všetkých hranách
4. **Zárez** — zárezy pre poistný prstenec

### Spustenie vo WinNC
1. Otvor **WinNC** → Sinumerik 840D Sústruženie
2. Nahraj súbor `sustruh_hriadel.mpf`
3. Nastav nulový bod obrobku na čele kusu (G54)
4. Simul → ▶ Spusti

### Rezné podmienky
| Operácia | Otáčky | Posuv |
|----------|--------|-------|
| Hrubovanie | 600 ot/min | 0.3 mm/ot |
| Dokončovanie | 1200 ot/min | 0.1 mm/ot |
| Zápichy | 500 ot/min | 0.05 mm/ot |
