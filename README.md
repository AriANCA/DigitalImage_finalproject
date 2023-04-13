# InSAR land subsidence mapping in Mexico City

# Introduction
The subsidence of Mexico City, due to groundwater extraction, began in the 1840s. Significant structural damage to urban infrastructure caused by compaction of overexploited aquifers is a well-known event in central Mexico.Due to the fact that the city is partially built over the area of an ancient lake (Lake Texcoco), it rests on heavily saturated clay that is collapsing due to over-extraction of groundwater.  In this study, subsidence is investigated and mapped with InSAR analysis using Sentinel-1A imagery, and the subsidence deformation patterns of the eastern part of Mexico City during the period from June to September 2022 are analyzed.

# Workflow
For this research, data of location and Sentinel-1 scenes were obtained by the Copernicus Open Access Hub. The advantage of the Sentinel-1A satellite is that it provides C-band (5.6 cm wavelength) SAR data that are considerably enhanced in aspects of coverage, repeat cycle, etc. In addition, the Sentinel-1A satellite with a total swath width of 250 km (pixel size: 5 m × 20 m) has the potential to map the global landmasses once every 12 days according to the acquisition plan of various sites [1]. The images used for InSAR analysis in this study were collected in 11 June 2022 and 27 September 2022. In addition, the images were obtained in the Interferometric Wide swath (IW) scanning mode with VV polarization and along the descending orbit of 143.

![data](https://user-images.githubusercontent.com/118282872/231750806-f9b651f6-1701-4f8b-a264-f3a38e5ba83d.png)

In this study, InSAR processing was performed with the support of SNAP (Sentinel Application Platform) software. Forming interferograms from single-look complex (SLC) images is the preprocessing target of SNAP [2]. It does this by applying precise orbit correction to co-register the stack, choosing the master image, generating interferograms and removing the topographic phase. Moreover, the Goldstein adaptative filter (window size: 3; value of α: 0.2) was applied during the phase unwrapping process to reduce the noise phase.

![Workflow](https://user-images.githubusercontent.com/118282872/231753042-4a5adbee-c45d-454a-b720-6af29c7ced78.png)

The image above shows the workflow represented with the graphics builder of the used program. InSAR can derive information from the interferograms that are formed by phase differences between two high resolution SAR images for the same area [3]. In this method, the DEM (Digital Elevation Model) with 30 m spatial resolution was used to remove topography phase, Goldstein filter was also used to remove noises and to strengthen radar signal and Minimum Cost Flow (MCF) was used in unwrapping phase.

# Results and Discussion
Two Sentinel-1A radar scans acquired between 11 June and 27 September 2022 were combined to create the following image of ground deformation in Mexico City. The defor-mation is caused by ground water extraction, with some areas of the city subsiding at up to 0.05 m/yr. By means of an appropriate post-processing of the displacement product, in this case the masking of the incoherent values, (Figure 1b) was obtained.


# Conclusion


# References
1. Geudtner, D.; Prats, P.; Yague, N.; Navas-Traver, I.; Barat, I.; Torres, R. Sentinel-1 SAR interferometry performance verifica-tion. In Proceedings of the EUSAR 2016: 11th European Conference on Synthetic Aperture Radar, Hamburg, Germany, 6–9 June 2016; pp. 1–4.
2. Hooper, A.; Pa, S.; Howard, Z.A. Persistent scatterer interferometric synthetic aperture radar for crustal deformation analy-sis, with application to Volcán Alcedo, Galápagos. J. Geophys. Res. Solid Earth 2007, 112, B7.
3. Saracin A, Cosarca C, Didulescu C, et al. 2014. Using InSAR technology for monitoring vertical deformation of the earth surface. Advances in environmental development, geomatics engineering and tourism. In: Proceedings of the 2nd European Conference of Geodesy and Geomatics Engineering (GENG 14). Brasov, Romania: GENG, 41–48.
4. 
