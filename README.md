# Python GIS Pipeline: Spatial Buffer & Thematic Mapping Analysis

Repository ini berisi skrip otomatisasi *end-to-end* menggunakan Python untuk pengolahan data geospasial administratif di Provinsi Aceh. Proyek ini mendemonstrasikan bagaimana mengawinkan analisis statistik atribut dengan manipulasi geometri spasial secara terprogram.

## Workflow / Pipeline Analisis:
1. **Data Preparation & Filtering:** Membaca dataset spasial kabupaten Indonesia dan memfokuskan subset ke wilayah Provinsi Aceh.
2. **Geodetic Rigor (UTM Reprojection):** Melakukan reproyeksi sistem koordinat ke *Universal Transverse Mercator* (UTM) agar perhitungan jarak (meter) dan luas (km²) valid secara matematis.
3. **Spatial Statistics & Filtering:** Menghitung luas wilayah per kabupaten secara otomatis, mencari nilai rata-rata, dan memfilter wilayah kategori besar.
4. **Spatial Buffering:** Menerapkan fungsi buffer radius 10 km secara otomatis pada subset kabupaten terpilih menggunakan Shapely/GeoPandas.
5. **Advanced Cartography & Labeling:** Visualisasi multi-layer (*sandwich method*) menggunakan Matplotlib, dilengkapi *dynamic labeling* (`representative_point`) untuk mencegah tumpang tindih teks, serta *custom legend*.
6. **Data & Image Export:** Mengekspor hasil analisis secara permanen ke format `.geojson` dan visualisasi peta resolusi tinggi (`.png`).

## Tools:
* **Language:** Python
* **Libraries:** `geopandas`, `matplotlib`, `shapely`, `google.colab`
* **Environment:** Google Colab

## Hasil Output:
* `Proyek_mini_buffer_Aceh.geojson` (Data spasial hasil buffer)
* `peta_buffer_aceh.png` (Peta tematik resolusi tinggi 300 DPI)

## Note:
Berisikan beberapa hasil visual peta:
* Peta Negara Indonesia
* Peta Wilayah Aceh (Derajat)
* Peta Wilayah Aceh (Meter) dan legenda
* Luas wilayah per Kabupaten
