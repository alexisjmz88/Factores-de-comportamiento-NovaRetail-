# NovaRetail+ Analysis – Sprint 8

Este repositorio contiene el análisis realizado durante el Sprint 8 del caso NovaRetail+.

El objetivo de este proyecto fue explorar los factores del comportamiento del cliente en la plataforma de comercio electrónico NovaRetail+ para responder a la pregunta del equipo de Crecimiento y Retención: **¿qué factores del comportamiento del cliente están más fuertemente asociados con el ingreso anual generado?**

Se utilizó un dataset de **usuarios** con **15,000 registros** y **12 columnas** (`id_cliente`, `edad`, `nivel_ingreso`, `visitas_mes`, `compras_mes`, `gasto_publicidad_dirigida`, `satisfaccion`, `miembro_premium`, `abandono`, `tipo_dispositivo`, `region`, `ingreso_anual`), sin valores nulos.

> ⚠️ Este es un análisis **correlacional** (exploratorio). **Correlación ≠ causalidad.**

## ▶ Cómo abrir el notebook en Google Colab

1. Abre el archivo `.ipynb` en GitHub
2. Haz clic en **Open in Colab**

## 📘 Cómo reproducir el análisis

1. Abre `notebooks/S8_Student_Version-Project-NovaRetail.ipynb`
2. Ejecuta las celdas en orden
3. El notebook carga automáticamente el dataset desde `/data/` o desde un enlace público (según corresponda)

## 🧠 Objetivo del análisis

- Cargar y explorar el dataset de usuarios de NovaRetail+
- Documentar los supuestos utilizados para el análisis de correlación
- Visualizar relaciones entre variables numéricas, binarias y categóricas
- Calcular coeficientes de correlación (Pearson, Spearman, punto-biserial y V de Cramér) según el tipo de variable
- Interpretar los hallazgos en términos de negocio, sin inferir causalidad
- Identificar limitaciones del análisis y próximos pasos

## 🔎 Principales hallazgos

- Existe una correlación positiva moderada entre `gasto_publicidad_dirigida` y `visitas_mes` (Pearson: 0.58, Spearman: 0.56).
- Existe una correlación positiva débil entre `visitas_mes` e `ingreso_anual` (Pearson: 0.34, Spearman: 0.32).
- `compras_mes` e `ingreso_anual` muestran una correlación positiva alta, pero se descarta como hallazgo principal por posible colinealidad (compras × precio promedio ≈ ingreso).
- Las variables binarias (`miembro_premium`, `abandono`) y categóricas (`tipo_dispositivo`, `region`) muestran relaciones débiles con `ingreso_anual`.

## ⚠️ Limitaciones

- Correlación ≠ causalidad: los resultados no permiten afirmar relaciones causales entre variables.

## 🚀 Próximos pasos

- Probar segmentación adicional por nivel de ingreso y por edad.
- Realizar análisis por cohortes para identificar oportunidades de mejora en el funnel de experiencia del usuario.
