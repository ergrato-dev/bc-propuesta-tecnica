# Taller 01 — Construye el Presupuesto de FerreMax

## 🎯 Objetivo del taller

En este taller construirás el presupuesto completo del proyecto FerreMax paso a paso, usando los datos de estimación de la Semana 4 y el cronograma de la Semana 5. Al terminar tendrás una tabla lista para incluir en la propuesta técnica.

**Duración estimada:** 2.5 horas

---

## 📋 Contexto rápido

**Proyecto:** FerreMax S.A.S. — Sistema de gestión de inventario, clientes y ventas  
**Equipo:** Dev A (semi-senior) + Dev B (junior)  
**Total de esfuerzo (S04):** 194 días-persona  
**Duración del proyecto (S05):** 15 semanas  
**Moneda:** Pesos colombianos (COP)

---

## Paso 1: Define la distribución del trabajo entre el equipo

**Contexto:** Con los módulos y el cronograma de S05, el trabajo quedó distribuido así entre los dos desarrolladores.  

**Ejemplo resuelto:**

| Dev | Módulos asignados | Esfuerzo (días-persona) |
|-----|------------------|------------------------|
| Dev A | M0(5) + M1(31) + M3(12) + M4(24) + M5(20) | 92 días |

**Tu turno:** Calcula los días de Dev B sumando los módulos que le correspondieron:

| Dev | Módulos asignados | Esfuerzo (días-persona) |
|-----|------------------|------------------------|
| Dev B | M0(5) + M2(67) + M4(24) + M6(16) | <!-- Completar: suma los días de Dev B --> |
| **Total** | | <!-- Suma Dev A + Dev B --> |

> 💡 **Pista**: El total de Dev A + Dev B da más de 194 porque en M0 y M4 trabajan juntos — cada uno aporta días que se cuentan individualmente.

---

## Paso 2: Calcula el costo de Recurso Humano

**Instrucción:** Usa la fórmula de la Teoría 02 para calcular el costo de cada desarrollador.

$$\text{Costo RH} = \text{Días} \times 8 \text{ horas/ d\'{i}a} \times \text{Tarifa por hora}$$

**Tarifas de referencia para este taller:**
- Dev A (semi-senior): $55,000/hora
- Dev B (junior): $38,000/hora

**Ejemplo resuelto:**
```
Dev A = 92 días × 8 horas × $55,000/hora = $40,480,000
```

**Tu turno:**
```
Dev B = _______ días × 8 horas × $38,000/hora = _______________
```

Completa la tabla:

| Rol | Días-persona | Horas/día | Tarifa/hora (COP) | Subtotal (COP) |
|-----|-------------|-----------|------------------|----------------|
| Dev A — Semi-senior | 92 | 8 | $55,000 | $40,480,000 |
| Dev B — Junior | <!-- Completar --> | 8 | $38,000 | <!-- Completar --> |
| **Subtotal RH** | | | | <!-- Suma de los dos --> |

---

## Paso 3: Calcula el costo de Infraestructura

**Instrucción:** Usando la información del caso FerreMax, completa la tabla de infraestructura. Los ítems gratuitos ya están identificados.

**Ejemplo resuelto:**
```
AWS EC2 t3.micro (staging) = $90,000/mes × 4 meses = $360,000
```

**Tu turno:** Completa la tabla:

| Ítem | Especificación | Cantidad | Costo unitario (COP) | Subtotal (COP) |
|------|---------------|----------|-----------------|----------------|
| Servidor staging | AWS EC2 t3.micro | 4 meses | $90,000/mes | $360,000 |
| Servidor producción | AWS EC2 t3.small | 1 mes | $160,000/mes | <!-- Completar --> |
| Backups en S3 | 20 GB | 4 meses | $8,000/mes | <!-- Completar --> |
| Dominio .com.co | ferremax-sistema.com.co | 1 año | $45,000 | $45,000 |
| Certificado SSL | Let's Encrypt | — | $0 | $0 |
| **Subtotal Infraestructura** | | | | <!-- Suma total --> |

---

## Paso 4: Licencias y Software

**Instrucción:** FerreMax usa stack open source. Verifica que todos los ítems son gratuitos y completa el subtotal.

| Herramienta | Licencia | Costo |
|-------------|---------|-------|
| Python 3.12 | Open Source | $0 |
| Django o FastAPI | Open Source | $0 |
| PostgreSQL | Open Source | $0 |
| React o Vue.js | Open Source | $0 |
| Git + GitHub | Gratuito | $0 |
| **Subtotal Licencias** | | <!-- Completar --> |

---

## Paso 5: Calcula la Contingencia

**Instrucción:** La contingencia es el 10% sobre el subtotal de costros directos (A + B + C). Completa el cálculo.

```
Subtotal A (RH)             = _______________
Subtotal B (Infraestructura) = _______________
Subtotal C (Licencias)       = $0
─────────────────────────────
Total costos directos        = _______________

Contingencia (10%)           = _______________ × 0.10 = _______________
```

| Concepto | Base | % | Valor (COP) |
|----------|------|---|-------------|
| Contingencia | <!-- Total A + B + C --> | 10% | <!-- Completar --> |

---

## Paso 6: Consolida el presupuesto total

**Instrucción:** Suma todas las secciones para obtener el costo total del proyecto.

```
A. Recurso Humano            = _______________
B. Infraestructura           = _______________
C. Licencias                 = $0
D. Contingencia              = _______________
─────────────────────────────────────────────
SUBTOTAL COSTOS DEL PROYECTO = _______________
```

Completa la tabla de resumen:

| Sección | Concepto | Subtotal (COP) |
|---------|---------|----------------|
| A | Recurso Humano | <!-- Completar --> |
| B | Infraestructura | <!-- Completar --> |
| C | Licencias | $0 |
| D | Contingencia | <!-- Completar --> |
| **SUBTOTAL TOTAL** | | <!-- Suma de A+B+C+D --> |

---

## Paso 7: Agrega el margen de ganancia y calcula la cotización

**Instrucción:** La consultora aplica un margen del 20% sobre el subtotal de costos para generar la cotización al cliente.

```
Subtotal costos del proyecto = _______________
Margen de ganancia (20%)     = _______________ × 0.20 = _______________
TOTAL COTIZACIÓN AL CLIENTE  = _______________
```

Completa la tabla final para la propuesta:

| Concepto | Descripción | Valor (COP) |
|----------|-------------|-------------|
| Desarrollo del sistema | 2 devs, 15 semanas, 6 módulos | <!-- Completar --> |
| Infraestructura | Servidores, dominio, backups | <!-- Completar --> |
| Gestión y contingencia | Reserva 10% | <!-- Completar --> |
| **Subtotal** | | <!-- Completar --> |
| Servicios profesionales | Margen 20% | <!-- Completar --> |
| **TOTAL DE LA PROPUESTA** | | <!-- TOTAL FINAL --> |

---

## 🏁 Revisión final

Al terminar verifica que:

- [ ] El subtotal de RH está correcto (Dev A + Dev B)
- [ ] La contingencia se calculó sobre el total A+B+C, no solo sobre RH
- [ ] El margen se calculó sobre el subtotal con contingencia incluida
- [ ] Todos los valores están en COP
- [ ] El total final es razonable (debería estar entre $85M y $110M para este caso)

> 📄 Continúa con **`plantilla-presupuesto-ferremax.md`** para consolidar el presupuesto en el formato final de propuesta técnica.
