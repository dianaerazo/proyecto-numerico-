# Procesamiento de Imágenes con FFT 2D
**Universidad Centroamericana "José Simeón Cañas"**  
Análisis Numérico | Ciclo 01-2026 | Sección 01

## Integrantes
- Maria Auxiliadora Chinchilla Flores
- Darlyn Maricela Donis Palma
- Diana Alejandra Erazo Pérez
- Luis Eduardo Martinez Linares
- Rebeca Elizabeth Torres Angel

---

## Descripción

Este proyecto explora la aplicación de la **Transformada Rápida de Fourier en 2 dimensiones (FFT 2D)** al procesamiento digital de imágenes. Se implementan y analizan distintos filtros en el dominio de frecuencias: pasa bajas, pasa altas, notch y gaussiano, evaluando su efecto tanto visualmente como con métricas de calidad (MSE, PSNR, SSIM).

---

## Estructura del repositorio

```
Proyecto-numerico/
│
├── proyecto_fft_imagenes.ipynb
│
├── images/
│   ├── originales/                  ← imágenes de entrada
│   ├── espectros/                   ← análisis espectral FFT 2D
│   ├── filtro_pasa_bajas/           ← suavizado (r = 10, 30, 80)
│   ├── filtro_pasa_altas/           ← detección de bordes (r = 10, 30, 60)
│   ├── ruido_periodico/             ← generación de ruido sinusoidal
│   ├── filtro_notch/                ← eliminación de ruido periódico
│   ├── ruido_gaussiano/             ← reducción de ruido + Gaussian Smoothing
│   └── panel_comparativo/           ← comparación de todos los filtros
│
└── README.md
```

Cada carpeta de resultados contiene subcarpetas por imagen procesada, por lo que correr el notebook con distintas imágenes no sobreescribe resultados anteriores.

---

## Experimentos

| Sección | Experimento |
|---|---|
| 3 | Análisis espectral con FFT 2D |
| 5.1 | Filtro Pasa Bajas |
| 5.2 | Filtro Pasa Altas — detección de bordes |
| 5.3 | Ruido periódico y filtro Notch |
| 6 | Reducción de ruido gaussiano y Gaussian Smoothing |
| 7 | Métricas de calidad: MSE, PSNR, SSIM |
| 8 | Panel comparativo final |

---

## Cómo ejecutar

1. Clona el repositorio e instala las dependencias:
   ```bash
   pip install numpy matplotlib Pillow scikit-image
   ```

2. Coloca tu imagen en `images/originales/`.

3. Abre el notebook y cambia `NOMBRE_IMAGEN` en la **Sección 2** al nombre de tu archivo.

4. Ejecuta todas las celdas con `Kernel → Restart & Run All`.

5. Los resultados se guardan automáticamente en la subcarpeta correspondiente a tu imagen.

---

## Dependencias

| Librería | Uso |
|---|---|
| `numpy` | Cálculo de la FFT 2D y operaciones matriciales |
| `matplotlib` | Visualización de imágenes y espectros |
| `Pillow` | Carga y conversión de imágenes |
| `scikit-image` | Métricas de calidad (MSE, PSNR, SSIM) |
