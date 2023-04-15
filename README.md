# InSAR land subsidence mapping in Mexico City

# Introduction
The subsidence of Mexico City, due to groundwater extraction, began in the 1840s. Significant structural damage to urban infrastructure caused by compaction of overexploited aquifers is a well-known event in central Mexico.Due to the fact that the city is partially built over the area of an ancient lake (Lake Texcoco), it rests on heavily saturated clay that is collapsing due to over-extraction of groundwater.  In this study, subsidence is investigated and mapped with InSAR analysis using Sentinel-1A imagery, and the subsidence deformation patterns of the eastern part of Mexico City during the period from June to September 2022 are analyzed.

# Workflow
For this research, data of location and Sentinel-1 scenes were obtained by the Copernicus Open Access Hub. The advantage of the Sentinel-1A satellite is that it provides C-band (5.6 cm wavelength) SAR data that are considerably enhanced in aspects of coverage, repeat cycle, etc. In addition, the Sentinel-1A satellite with a total swath width of 250 km (pixel size: 5 m × 20 m) has the potential to map the global landmasses once every 12 days according to the acquisition plan of various sites [1]. The images used for InSAR analysis in this study were collected in 11 June 2022 and 27 September 2022. In addition, the images were obtained in the Interferometric Wide swath (IW) scanning mode with VV polarization and along the descending orbit of 143.

![data](https://user-images.githubusercontent.com/118282872/231750806-f9b651f6-1701-4f8b-a264-f3a38e5ba83d.png)

In this study, InSAR processing was performed with the support of SNAP (Sentinel Application Platform) software. Forming interferograms from single-look complex (SLC) images is the preprocessing target of SNAP [2]. It does this by applying precise orbit correction to co-register the stack, choosing the master image, generating interferograms and removing the topographic phase. Moreover, the Goldstein adaptative filter (window size: 3; value of α: 0.2) was applied during the phase unwrapping process to reduce the noise phase.

![Workflow](https://user-images.githubusercontent.com/118282872/231753042-4a5adbee-c45d-454a-b720-6af29c7ced78.png)

The figure above shows the workflow represented with the graphics builder of the used program. InSAR can derive information from the interferograms that are formed by phase differences between two high resolution SAR images for the same area [3]. In this method, the DEM (Digital Elevation Model) with 30 m spatial resolution was used to remove topography phase, Goldstein filter was also used to remove noises and to strengthen radar signal and Minimum Cost Flow (MCF) was used in unwrapping phase.

# Results and Discussion
Two Sentinel-1A radar scans acquired between 11 June and 27 September 2022 were combined to create the following figure of ground deformation in Mexico City. The deformation is caused by ground water extraction, with some areas of the city subsiding at up to 0.05 m/yr. By means of an appropriate post-processing of the displacement product, in this case the masking of the incoherent values, (Figure 1b) was obtained.

![ImagenVV](https://user-images.githubusercontent.com/118282872/231756659-7287292d-4aa7-499b-869c-f404da913755.png)

The figure above is the result of Range Doppler orthorectification method: (a) Displacement product; (b) Masking of the incoherent values in the displacement product.

https://user-images.githubusercontent.com/118282872/231763631-d7b79707-2307-4e3f-b904-d8d2b3e344fe.mp4

The Guadiana valley of Ecatepec de Morelos falls within the wide-area analysis based on Sentinel 1A imagery acquired in 2016 [4], which showed peak vertical rates of about -4-5 cm/yr, these are consistent with the rates estimated based on the analysis presented in this paper. The InSAR results reveal high subsidence rates detected in the Guadiana valley with peaks of ~-4 cm/yr and are concentrated within the Aragon forests.

![Northzone](https://user-images.githubusercontent.com/118282872/231768206-02fc7ae3-f094-4303-9ff4-60595ba44a35.png)

As also observed in the north zone of the figure above, higher subsidence rates spatially correlated with industrial land use, especially in the areas of Rio de Luz, Sagitario X, Miguel Hidalgo and Del Bosque where more than 20 groundwater wells operate [5]. This corroborates the conclusion that groundwater pumping for industrial activities in those sectors acts as the lead factor that determines ground deformation.
To better understand the InSAR results, it is necessary to consider the geological setting and the characteristics of the Zacatepec aquifer.It is located in the central part of the country, in the southwestern portion of the State of Morelos, between the parallels 18° 20' and 18° 45' North latitude and the meridians 99° 30' and 99° 9' West longitude, covering an approximate area of 1,279 km2 [6].
The oldest stratigraphic units in this zone are volcanoclastic products of the Tertiary and Quaternary [5]. The alluvial and fluvial deposits within the channels and valleys host the unconfined aquifer, the main source to address water needs of the region. The deeper portion of the aquifer sits within a sequence of highly fractured extrusive igneous rocks, composed primarily of basalts, tuffs, and andesites. The barriers to horizontal and vertical flow are mainly the same volcanic rocks, where the fracturing disappears at depths [6].

![Southzone](https://user-images.githubusercontent.com/118282872/231768300-53228323-4e5e-4e89-9e8e-724fa2c71fa3.png)

A similar situation occurs in the southern zone of the figure above in the Chalco Valley. Groundwater extraction in the Chalco-Amecameca aquifer, which belongs to the Transmexican Volcanic Belt, receives its recharge from rainfall, mainly in the topographically elevated portions [7]. In addition, there is another source of recharge that feeds the aquifer, which is the incidental recharge caused by leaks from the supply systems. The main discharge of the aquifer is mainly through deep wells and some springs. The large number of wells has caused overexploitation, which is manifested in a continuous decline in groundwater levels [8].
The land subsidence map generated in this study indicates a relatively strong correlation between land subsidence and urban development, probably due to excessive groundwater extraction in urban areas [9]. This map could be used by local environmental authorities and urban developers to identify areas at high risk of subsidence. In addition, the InSAR method for mapping ground deformation using radar images of the Earth's surface obtained from orbiting satellites could be applied to other regions of the planet.

# Conclusion
This study compared two radar images of the eastern part of Mexico City taken during the period from June to September 2022 from similar strategic points in space to measure subsidence of the area due to groundwater extraction and related risk assessments. The InSAR results reveal high rates of subsidence detected with peaks of ~-4 cm/year. It can then be concluded that this phenomenon was caused by the increased number of deep wells in the area, intense water extraction and decreased groundwater height. 
The findings of this study with the help of continuous radar satellite monitoring will help aquifer managers make informed decisions about their valuable water resources.

# References
1. Geudtner, D.; Prats, P.; Yague, N.; Navas-Traver, I.; Barat, I.; Torres, R. Sentinel-1 SAR interferometry performance verification. In Proceedings of the EUSAR 2016: 11th European Conference on Synthetic Aperture Radar, Hamburg, Germany, 6–9 June 2016; pp. 1–4.
2. Hooper, A.; Pa, S.; Howard, Z.A. Persistent scatterer interferometric synthetic aperture radar for crustal deformation analysis, with application to Volcán Alcedo, Galápagos. J. Geophys. Res. Solid Earth 2007, 112, B7.
3. Saracin A, Cosarca C, Didulescu C, et al. 2014. Using InSAR technology for monitoring vertical deformation of the earth surface. Advances in environmental development, geomatics engineering and tourism. In: Proceedings of the 2nd European Conference of Geodesy and Geomatics Engineering (GENG 14). Brasov, Romania: GENG, 41–48.
4. Castellazzi P, Domínguez N, Martel R, Calderhead A, Normand J, Gárfias J, Rivera A. Land subsidence in major cities of Central Mexico: Interpreting InSAR-derived land subsidence mapping with hydrogeological data. International Journal of Applied Earth Observation and Geoinformation, volume 47, 2016,102-111.
5. CONAGUA. Actualización de la Disponibilidad Media Anual de Agua en el Acuífero Texcoco (1507), Estado de México. Diario Diario Oficial de la Federación. 10 December 2020. Available online: https://sigagis.conagua.gob.mx/gas1/Edos_Acuiferos_18/edomex/DR_1507.pdf (accessed on 15 march 2022).
6. CONAGUA. Actualización de la Disponibilidad Media Anual de Agua en el Acuífero Zacatepec (1703), Estado de Morelos. Diario Oficial de la Federación. 10 December 2020. Available online: https://sigagis.conagua.gob.mx/gas1/Edos_Acuiferos_18/morelos/DR_1701.pdf (accessed on 15 march 2022).
7. CONAGUA. Actualización de la Disponibilidad Media Anual de Agua en el Acuífero Chalco-Amecameca (1506), Estado de Mexico. Diario Oficial de la Federación. 10 December 2020. Available online: https://sigagis.conagua.gob.mx/gas1/Edos_Acuiferos_18/edomex/DR_1506.pdf (accessed on 15 march 2022). 
8. Sowter, A.; Che Amat, M.; Cigna, F.; Marsh, S.; Athab, A.; Alshammari, L. Mexico City land subsidence in 2014–2015 with Sentinel-1 IW TOPS: First results using the Intermittent SBAS (ISBAS) technique. Int. J. Appl. Earth Obs. Geoinf. 2016, 52, 230–242.
9. Chaussard, E.; Wdowinski, S.; Cabral-Cano, E.; Amelung, F. Land subsidence in central Mexico detected by ALOS InSAR time-series. Remote Sens. Environ. 2014, 140, 94–106.
