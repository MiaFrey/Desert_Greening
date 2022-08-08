# Desert Greening, a Silver Bullet?

You can find our publication at [this link](https://drive.google.com/file/d/1VO43SZR9wCzDPwtWC6fFqxyiQJ8-fuvS/view)



## Introduction
The question of greening deserts to mitigate climate change is important since recent endeavours are considering this path [[12]](#12). 
This paper focuses on the albedo change, water cycle effect and carbon sequestrated by planting desert areas combined with reaching net-zero by 2100. We aim at predicting a global estimate of the impact on temperature. 
We considered 107 GtC as global tree restoration potential as given by Table 1 of [[9]](#9). This value encompasses biome-corrected carbon gain including those areas with an albedo change.

<p align="center">
    <img src="https://drive.google.com/uc?id=1d2_Am8_3MPHF1Ae-7WglpjzbIitCFbzJ">
    <em>Figure 1. (a) Predicted effect on the global average temperature anomaly, (b) process adopted, (c) variables used.</em>
</p>

## Methods
We describe here our predictive approach to produce Figure 1a. Our model considers past CO2 concentration and stratospheric water vapor data retrieved from NOAA and NASA databases [[13]](#13). 
Those annual values are fitted into a polynomial ridge regression to predict temperature anomalies. We chose this model because the results were closest to the IPCC projections [[4]](#4) (worst-case scenario in Figure 1a).

### Reduce Gas emissions
Our baseline scenario is net-zero by 2100. The other scenarios are computed relatively to this baseline. We apply a linear reduction rate on the yearly growth of the worst-case scenario.

### Sequestrate carbon
The total amount of CO2 sequestration potential is 107 GtC, including areas with albedo change, since there are several factors to consider, such as tree typology, consequences on soil carbon and impact on the ecosystem (e.g., loss of biodiversity or increase of fire intensity) [[9]](#9). In our model, we linearly decrease the atmospheric CO2, reaching the full capacity at the end of the century(CO2 in Figure 1c).

### Albedo change
The albedo of desert areas is high because of its light surface color [[1]](#1). However, trees are darker bringing about a change in the albedo and thus the radiation budget [[10]](#10), leading to a warming.
We calculated the effect of albedo on the temperature using the Stefan-Boltzmann law [[5]](#5) by modeling the effect of changing all desert surfaces into vegetation (from 0.32 to 0.27, subpluvial Sahara albedo [[8]](#8)). 

**Water cycle:** Tree’s transpiration [[3]](#3) and a warmer temperature, which is currently the case [[6]](#6), lead to more water vapor in the atmosphere [[2]](#2). This eventually induces the formation of clouds, which are a critical climate feedback. High clouds warm the Earth since they absorb and re-emit long-wave radiation back to the surface, thus increasing the greenhouse effect. Such variable is embedded into stratospheric water vapor predictor. Whereas, low clouds in the troposphere have a cooling effect because they reflect shortwave radiation. Overall, clouds have a cooling effect [[2]](#2), [[7]](#7). Hence, the cloud type and coverage over a forest should be considered too. Figure 1a shows the predictions for low cloud coverage of 50% and 70% [[11]](#11). These proportions are aligned with similar surfaces, notably big forests present on Earth, keeping in mind the impossibility of their complete emulation starting from a desert land. The global average temperature substantially decreases as it is sensitive to cloud feedback.

## Summary of results
Since planting trees including desert areas would sequester 107GtC and considering albedo change with a cloud coverage of 50% and 70%, the predicted temperature would be lower than by solely reaching net-zero carbon, remaining respectively below 1.5°C and 1°C degrees of anomaly. The potential cooling effect of increasing vegetation if reaching a 70% cloud cover is estimated to 1.27°C ± 0.44 (RMSE).

## Conclusions
In conclusion, the results are positive but highly sensitive to the amount of cloud coverage, resulting from new vegetation. In subsequent steps, we will conduct a sensitivity analysis and present each step of the process in more detail. Furthermore, we plan to train a model to predict the albedo change and cloud coverage resulting from new vegetation in a given area. Desert greening helps in mitigating climate.

## Collaborators
- [Dario Scalabrin](https://www.linkedin.com/in/scalabrindario/)
- [Massimo Poretti](https://www.linkedin.com/in/poretti-massimo/)
- [Mia Frey](https://www.linkedin.com/in/mia-frey-28209a208/)
- [Cédric Mesnage](https://www.linkedin.com/in/cedricmesnage/)
- [Michalis Vlachos](https://www.linkedin.com/in/michalis-vlachos/)

## References
<a id="1">[1]</a> D. L. Hartmann. Global physical climatology, volume 103. Newnes, 2015. <br>
<a id="2">[2]</a> C. Heinze et al. Esd reviews: Climate feedbacks in the earth system and prospects for their evaluation. Earth System Dynamics, 10(3):379–452, 2019. <br>
<a id="3">[3]</a> V. Inglezakis, S. Poulopoulos, E. Arkhangelsky, A. Zorpas, and A. Menegaki. Aquatic environment. In Environment and Development, pages 137–212. Elsevier, 2016. <br>
<a id="4">[4]</a> IPCC. Global warming of 1.5c. an ipcc special report on the impacts of global warming of 1.5c above pre-industrial levels and related global greenhouse gas emission pathways, in the context of strengthening the global response to the threat of climate change, sustainable development, and efforts to eradicate poverty, 2018.<br>
<a id="5">[5]</a> M. C. LoPresto and N. Hagoort. Determining planetary temperatures with the stefan-boltzmann law. The Physics Teacher, 49(2):113–116, 2011. <br>
<a id="6">[6]</a> V. MassonDelmotte et al. Climate change 2021: The physical science basis: Summary for policymakers. Working Group I to the Sixth Assessment Report of the Intergovernmental Panel on Climate Change, 2021. <br>
<a id="7">[7]</a> M. M. Millán. Extreme hydrometeorological events and climate change predictions in europe. Journal of Hydrology, 2014. <br>
<a id="8">[8]</a> G. Tetzlaff. Albedo of the sahara. Satellite Meas. of Radiation Budget Parameters, pages 60–63, 1983. <br>
<a id="9">[9]</a> J. W. Veldman et al. Comment on “the global tree restoration potential”. Science, 366(6463), 2019. <br>
<a id="10">[10]</a> J. M. Wallace and P. V. Hobbs. Atmospheric science: an introductory survey, volume 92. Elsevier, 2006. <br>
<a id="11">[11]</a> S. G. Warren et al. Global distribution of total cloud cover and cloud type amounts over land. Technical report, Washington Univ., Seattle (USA). Dept. of Atmospheric Sciences; Colorado Univ., Boulder (USA), 1986. <br>
<a id="12">[12]</a> We note here the Saudi Arabia announcement of planting 10 billion trees (https://www.reuters.com/world/ middle-east/saudi-arabia-sees-fields-green-with-major-tree-planting-drive-2021-03-27/) and the Weather makers project (https: //theweathermakers.nl/) to green the Sinai.<br>
<a id="13">[13]</a> GAT (https://www.ncdc.noaa.gov/cag/global/time- series/globe/land_ocean/ytd/12/1880- 2020.csv), CO2 (https://data.giss. nasa.gov/modelforce/ghgases/Fig1A.ext.txt), recent CO2 (ftp://aftp.cmdl.noaa.gov/products/trends/co2/co2_annmean_mlo.txt), Water Vapor(https://gml.noaa.gov/ozwv/wvap/) <br>

## License 
[MIT](https://choosealicense.com/licenses/mit/)
