# La paradoja de la confianza: por qué el Sur Global le tiene más fe a la IA que las potencias tecnológicas

El Stanford AI Index Report 2026, la publicación de referencia mundial sobre el estado de la inteligencia artificial, trae todos los años una figura que pocas veces recibe la atención que merece: un gráfico comparando, país por país, qué porcentaje de la población usa IA en el trabajo y qué porcentaje confía en ella. La lectura rápida del dato ya es intrigante. India, Nigeria y Egipto encabezan ambas listas, con cifras de uso y confianza por encima del 80%. Japón, Alemania y los países nórdicos, las economías que durante décadas lideraron la innovación tecnológica mundial, aparecen en la parte baja de la tabla, con menos de la mitad de esa confianza.

¿Es casualidad? ¿Es que los países más desarrollados son simplemente más escépticos por naturaleza? Quise ir un poco más allá del dato crudo y cruzarlo con variables de contexto nacional para entender qué hay detrás de ese patrón. El resultado fue más interesante de lo que esperaba, y obliga a replantear una intuición bastante extendida sobre la relación entre desarrollo y adopción tecnológica.

![Uso y confianza en la IA en el trabajo, coloreado por IDH y dimensionado por GINI]({{ site.baseurl }}/Figures/ai_trust_use_hdi_gini.png)
Uso y confianza en la IA en el trabajo por país, coloreada por Índice de Desarrollo Humano y dimensionada por desigualdad (GINI). Fuente: Stanford AI Index 2026, PNUD, Banco Mundial.

**1. La primera sospecha: ¿es el desarrollo humano?**
La hipótesis más obvia es que el nivel de desarrollo de un país explica la diferencia. Es razonable pensar que las sociedades con sistemas educativos, sanitarios y económicos más consolidados —es decir, con un Índice de Desarrollo Humano (IDH) más alto— tendrían además más experiencia adoptando tecnología y, por tanto, más confianza en ella. Los datos confirman parcialmente esta intuición, pero en la dirección contraria: el IDH correlaciona negativamente tanto con el uso de IA en el trabajo (r = −0.65) como con la confianza (r = −0.66), ambas relaciones estadísticamente muy sólidas (p < 0.001). A mayor desarrollo humano, menor uso y menor confianza. Una pista, pero no toda la historia.

**2. ¿Y si es la desigualdad?**
La segunda hipótesis natural era la desigualdad económica. Las sociedades más desiguales, pensé, podrían mostrar actitudes distintas hacia una tecnología que muchos asocian con la automatización del empleo. Aquí los datos fueron más bien aburridos: el índice GINI correlaciona débilmente con el uso (r = 0.34, apenas significativo) y prácticamente nada con la confianza (r = 0.20, no significativo). De las cinco variables que terminé probando, la desigualdad resultó ser, con diferencia, la que menos explica.

**3. El factor demográfico que sí importa**
Una variable que no estaba en el radar inicial, pero que un colega sugirió como posible explicación alternativa, fue la edad mediana de la población. La idea es sencilla: los países con poblaciones más jóvenes —India, Nigeria, Egipto— podrían adoptar tecnología más rápido simplemente por estructura demográfica, sin que eso tenga que ver con su nivel de desarrollo. Y en efecto, la edad mediana resultó ser un predictor más fuerte que el propio IDH (r = −0.74 con confianza, r = −0.69 con uso), y se mantuvo significativa incluso controlando estadísticamente por las demás variables.

**4. La variable que cambió todo el panorama**
La pieza que más reorganizó mi interpretación del fenómeno fue la confianza institucional generalizada, medida por el Edelman Trust Barometer: qué tanto confía una sociedad en sus gobiernos, empresas, medios y ONGs, independientemente de la inteligencia artificial. La correlación con la confianza en la IA fue, por mucho, la más fuerte de todas las que probé: r = 0.85, equivalente a un 72% de la varianza explicada por sí sola. Para ponerlo en perspectiva: el IDH explica un 53%; la confianza institucional, un 72%.

Hice además una prueba más exigente, una regresión jerárquica para ver si la confianza institucional simplemente "reemplazaba" al desarrollo o si aportaba algo genuinamente nuevo. El resultado: añadir confianza institucional al modelo que ya tenía el IDH mejora el ajuste de un R² de 0.54 a 0.87 (un salto de 0.34 puntos, estadísticamente muy significativo), y ambas variables se mantienen como predictoras independientes. Es decir, no es que la confianza institucional sustituya al desarrollo —ambas aportan algo—, pero sí que es, de lejos, el factor más determinante de los dos.

![Cinco predictores de la confianza en la IA en el trabajo]({{ site.baseurl }}/Figures/panel_predictores_confianza.png)
Confianza en la IA en el trabajo frente a IDH, edad mediana, PIB per cápita, GINI y confianza institucional (Edelman Trust Barometer).

**5. Lo que esto sugiere**
La lectura que me convence más, después de ver estos números, es que "confiar en la IA en el trabajo" no es tanto una actitud específica hacia la tecnología como un reflejo de algo más amplio: cuánta confianza tiene una sociedad en sus instituciones en general. Dicho de otro modo, no es que India confíe particularmente en los modelos de lenguaje; es que India, como sociedad, tiende a confiar más en sus instituciones que Japón o Alemania, y eso se traslada también a la IA. Esta interpretación tiene sentido con un hallazgo bien documentado en la literatura de adopción tecnológica: la confianza generalizada predice consistentemente la confianza en tecnologías específicas, mucho antes de que la gente tenga experiencia directa con ellas.

![Coeficientes estandarizados de los modelos de regresión]({{ site.baseurl }}/Figures/coeficientes_regresion.png)
Coeficientes estandarizados: modelo con IDH, GINI, edad mediana y PIB per cápita (izquierda) frente al modelo reducido IDH + confianza institucional (derecha).

**6. Lo que estos datos no permiten decir**
Como en cualquier análisis correlacional, hay que ser honesto sobre los límites. Primero, esto es un corte transversal: no podemos afirmar causalidad, solo asociación. Segundo, el Edelman Trust Barometer cubre apenas 24 de los 47 países de la muestra original —faltan, sobre todo, economías pequeñas europeas—, así que el modelo con confianza institucional corre sobre una submuestra sesgada hacia economías grandes. Tercero, el IDH y el PIB per cápita están tan correlacionados entre sí (r = 0.95) que sus efectos individuales en un modelo conjunto son difíciles de separar limpiamente; no es un defecto del análisis, sino una propiedad conocida de estas dos variables, que en gran medida miden la misma dimensión subyacente de desarrollo económico.

## Conclusión
Lo que empezó como una curiosidad ante un gráfico del AI Index terminó siendo un buen recordatorio de un principio que aplica mucho más allá de la inteligencia artificial: las primeras explicaciones que se nos ocurren —en este caso, "los países ricos son más escépticos"— rara vez son las correctas, o al menos rara vez son las completas. El nivel de desarrollo de un país sí importa, pero pesa menos que algo más fundamental y menos visible: la confianza que esa sociedad ya tenía, de antemano, en sus propias instituciones. Para cualquiera que trabaje diseñando, regulando o desplegando sistemas de IA, la implicación práctica es directa: construir confianza en la tecnología probablemente dependa menos de mejorar el producto y más de operar dentro de —o reconstruir— un ecosistema institucional confiable.

Si algo deja claro este ejercicio es que los datos abiertos, bien cruzados, pueden desafiar intuiciones que parecían razonables a primera vista. Y esa, más que cualquier hallazgo puntual, es la mejor razón para seguir mirando los números con calma antes de sacar conclusiones.

## Algunas referencias:
- AI Index Report 2026. Stanford HAI (2026). [https://hai.stanford.edu/ai-index/2026-ai-index-report](https://hai.stanford.edu/ai-index/2026-ai-index-report)
- Human Development Report 2025. PNUD (2025). [https://hdr.undp.org/data-center/country-insights](https://hdr.undp.org/data-center/country-insights)
- Gini index (World Bank estimate). Banco Mundial (2026). [https://data.worldbank.org/indicator/SI.POV.GINI](https://data.worldbank.org/indicator/SI.POV.GINI)
- Median Age by Country 2026. World Population Review (2026). [https://worldpopulationreview.com/country-rankings/median-age](https://worldpopulationreview.com/country-rankings/median-age)
- 2026 Edelman Trust Barometer Global Report. Edelman (2026). [https://www.edelman.com/trust/2026/trust-barometer](https://www.edelman.com/trust/2026/trust-barometer)
