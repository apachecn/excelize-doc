# Rendimiento

Las siguientes cifras de rendimiento muestran el tiempo de ejecución y el uso de memoria para hojas de trabajo de tamaño `N` filas x `50` columnas con una mezcla 50/50 de cadenas y números. Las cifras se han tomado de una máquina arbitraria de rango medio (SO: macOS Catalina versión 10.15.7, CPU: Intel Core i5 a 3.4 GHz, RAM: 16 GB 2400 MHz DDR4, HDD: 1 TB, Versión Go: `go1.15.7 darwin/amd64`, Confirmar: [`23c73ab`](https://github.com/360EntSecGroup-Skylar/excelize/tree/23c73ab527731f9d414e81f7ea15e2ae1a72a290)). Specific figures will vary from machine to machine but the trends should be the same.

<table>
    <tr>
        <th>Tipo</th>
        <th>Filas</th>
        <th>Columnas</th>
        <th>Hora (s)</th>
        <th>Memoria (MB)</th>
    </tr>
    <tr>
        <td rowspan="10">SetSheetRow</td>
        <td>200</td>
        <td>50</td>
        <td>0.006</td>
        <td>16</td>
    </tr>
    <tr>
        <td>400</td>
        <td>50</td>
        <td>0.106</td>
        <td>25</td>
    </tr>
    <tr>
        <td>800</td>
        <td>50</td>
        <td>0.207</td>
        <td>44</td>
    </tr>
    <tr>
        <td>1600</td>
        <td>50</td>
        <td>0.410</td>
        <td>75</td>
    </tr>
    <tr>
        <td>3200</td>
        <td>50</td>
        <td>0.810</td>
        <td>167</td>
    </tr>
    <tr>
        <td>6400</td>
        <td>50</td>
        <td>1.651</td>
        <td>298</td>
    </tr>
    <tr>
        <td>12800</td>
        <td>50</td>
        <td>3.278</td>
        <td>585</td>
    </tr>
    <tr>
        <td>25600</td>
        <td>50</td>
        <td>6.632</td>
        <td>1291</td>
    </tr>
    <tr>
        <td>52100</td>
        <td>50</td>
        <td>13.718</td>
        <td>2658</td>
    </tr>
    <tr>
        <td>102400</td>
        <td>50</td>
        <td>27.491</td>
        <td>5049</td>
    </tr>
    <tr>
        <td rowspan="10">StreamWriter</td>
        <td>200</td>
        <td>50</td>
        <td>0.017</td>
        <td>9</td>
    </tr>
    <tr>
        <td>400</td>
        <td>50</td>
        <td>0.031</td>
        <td>11</td>
    </tr>
    <tr>
        <td>800</td>
        <td>50</td>
        <td>0.059</td>
        <td>13</td>
    </tr>
    <tr>
        <td>1600</td>
        <td>50</td>
        <td>0.113</td>
        <td>17</td>
    </tr>
    <tr>
        <td>3200</td>
        <td>50</td>
        <td>0.230</td>
        <td>29</td>
    </tr>
    <tr>
        <td>6400</td>
        <td>50</td>
        <td>0.435</td>
        <td>50</td>
    </tr>
    <tr>
        <td>12800</td>
        <td>50</td>
        <td>0.893</td>
        <td>65</td>
    </tr>
    <tr>
        <td>25600</td>
        <td>50</td>
        <td>1.813</td>
        <td>82</td>
    </tr>
    <tr>
        <td>52100</td>
        <td>50</td>
        <td>3.939</td>
        <td>106</td>
    </tr>
    <tr>
        <td>102400</td>
        <td>50</td>
        <td>8.043</td>
        <td>154</td>
    </tr>
    <tr>
        <td rowspan="10">RowIterator</td>
        <td>200</td>
        <td>50</td>
        <td>0.051</td>
        <td>10</td>
    </tr>
    <tr>
        <td>400</td>
        <td>50</td>
        <td>0.010</td>
        <td>10</td>
    </tr>
    <tr>
        <td>800</td>
        <td>50</td>
        <td>0.197</td>
        <td>12</td>
    </tr>
    <tr>
        <td>1600</td>
        <td>50</td>
        <td>0.395</td>
        <td>15</td>
    </tr>
    <tr>
        <td>3200</td>
        <td>50</td>
        <td>0.784</td>
        <td>24</td>
    </tr>
    <tr>
        <td>6400</td>
        <td>50</td>
        <td>1.530</td>
        <td>40</td>
    </tr>
    <tr>
        <td>12800</td>
        <td>50</td>
        <td>3.029</td>
        <td>73</td>
    </tr>
    <tr>
        <td>25600</td>
        <td>50</td>
        <td>6.054</td>
        <td>140</td>
    </tr>
    <tr>
        <td>52100</td>
        <td>50</td>
        <td>12.317</td>
        <td>271</td>
    </tr>
    <tr>
        <td>102400</td>
        <td>50</td>
        <td>24.175</td>
        <td>534</td>
    </tr>
    <tr>
        <td rowspan="1">AddChart</td>
        <td>200</td>
        <td>50</td>
        <td>8.693</td>
        <td>210</td>
    </tr>
    <tr>
        <td rowspan="3">SetHyperLink</td>
        <td>200</td>
        <td>50</td>
        <td>1.034</td>
        <td>16</td>
    </tr>
    <tr>
        <td>400</td>
        <td>50</td>
        <td>3.937</td>
        <td>24</td>
    </tr>
    <tr>
        <td>800</td>
        <td>50</td>
        <td>15.744</td>
        <td>46</td>
    </tr>
    <tr>
        <td rowspan="4">AddPicture</td>
        <td>200</td>
        <td>50</td>
        <td>1.471</td>
        <td>51</td>
    </tr>
    <tr>
        <td>400</td>
        <td>50</td>
        <td>4.925</td>
        <td>95</td>
    </tr>
    <tr>
        <td>800</td>
        <td>50</td>
        <td>18.586</td>
        <td>184</td>
    </tr>
    <tr>
        <td>1600</td>
        <td>50</td>
        <td>79.356</td>
        <td>360</td>
    </tr>
</table>

Los datos de rendimiento son generados por [esta secuencia de comandos de prueba comparativa](https://gist.github.com/xuri/6a5733d7c68fb212792a94b29280234b).

## Comparación de rendimiento de bibliotecas similares

El siguiente gráfico muestra una comparación de rendimiento de la matriz de texto plano de generación `102400*50` de las principales bibliotecas de Excel de código abierto en una computadora personal (SO: macOS Catalina versión 10.15.7, CPU: 3.4 GHz Intel Core i5, RAM: 16 GB 2400 MHz DDR4, HDD: 1 TB), incluidos Go, Python, Java, PHP y NodeJS.

<p align="center"><img width="688" src="https://xuri.me/wp-content/uploads/2016/08/excelize-golang-library-for-reading-and-writing-xlsx-files-3.png" alt="Comparación de rendimiento de bibliotecas similares"></p>