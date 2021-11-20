[![DOI](https://zenodo.org/badge/430140035.svg)](https://zenodo.org/badge/latestdoi/430140035)

# Data & code repository for *A re-appraisal of the ENSO response to volcanism with paleoclimate data assimilation*

This repository includes the data and code that can be used to reproduce the figures for the paper entitled *A re-appraisal of the ENSO response to volcanism with paleoclimate data assimilation*.

The code is tested with Python v3.8, and the package [LMRt](https://github.com/fzhu2e/LMRt) (Zhu et. al., 2021) is required to perform essential analysis (e.g. Superposed Epoch Analysis) and the corresponding visualization.

## Repository Structure

+ `recons`: the folder that includes our reconstructions of (i) the NINO3.4 series with 0.05, 0.25, 0.5, 0.75, 0.95 quantiles and (ii) the ensemble median surface temperature field
  + `recon_Ocn2kCorals_Li13b6.nc`: the reconstruction that assimilates all the available Ocean2k corals (Tierney et al., 2015; PAGES2k Consortium, 2017) and the six best ENSO predictors in Li et al. (2013).
  + `recon_Corals_Li13b6.nc`: the reconstruction that assimilates the corals reaching back before 1750 CE and the six best ENSO predictors in Li et al. (2013).
  + `recon_Corals.nc`: the reconstruction that assimilates the corals reaching back before 1750 CE.
  + `recon_Li13b6.nc`: the reconstruction that assimilates the six best ENSO predictors in Li et al. (2013).

+ `notebooks`: the folder that includes Jupyter notebooks
  + `Fig-1.ipynb`: the notebook that performs analysis and generates Fig. 1 in the main text
  + `Fig-2.ipynb`: the notebook that performs analysis and generates Fig. 2 in the main text
  + `Fig-3.ipynb`: the notebook that performs analysis and generates Fig. 3 in the main text
  + `Fig-4.ipynb`: the notebook that performs analysis and generates Fig. 4 in the main text

+ `data`: the folder that includes auxiliary data for the analysis and visualization
  + `proxy_locs.pkl`: the pickle file that includes the location information of the assimilated proxies
  + `eVolv2k_v3_ds_1.nc`: the eVolv2k v3 volcanic forcing data (Toohey & Sigl, 2017), which is publicly available and can be downloaded [here](https://doi.org/10.26050/WDCC/eVolv2k_v3)
  + `palmyra2013.txt`: the Palmyra coral d18O data (Emile-Geay et al., 2013), which is publicly available and can be downloaded [here](https://www.ncdc.noaa.gov/cdo/f?p=519:1:::::P1_STUDY_ID:1875)
  + `Li13b6.txt`: the six best ENSO predictors in Li et al. (2013), including the first two principle components (PCs) of the North American Drought Atlas (NADA; Cook et al., 2004) and Monsoon Asia Drought Atlas (MADA; Cook et al., 2010) networks, the Kauri tree-ring composite (Fowler et al., 2012), and the South America Altiplano (SA Altiplano) tree-ring composite (Morales et al., 2012)
  + `enso-li2013.txt`: the Li et al. (2013) NINO3.4 reconstruction, which is publicly available and can be downloaded with the link: `ftp://ftp.ncdc.noaa.gov/pub/data/paleo/treering/reconstructions/enso-li2013.txt`
  + `ERSSTv5_sst_DJF.nc`: the ERSSTv5 boreal winter (December-February) SST field data (Huang et al., 2017)

+ `figs`: the folder that includes figures
  + `Fig-1.pdf`: Fig. 1 in the main text
  + `Fig-2.pdf`: Fig. 2 in the main text
  + `Fig-3.pdf`: Fig. 3 in the main text
  + `Fig-4.pdf`: Fig. 4 in the main text

## References
+ Cook, E. R., Woodhouse, C. A., Eakin, C. M., Meko, D. M., & Stahle, D. W. (2004). Long-Term Aridity Changes in the Western United States. Science, 306(5698), 1015–1018. https://doi.org/10.1126/science.1102586
+ Cook, E. R., Anchukaitis, K. J., Buckley, B. M., D’Arrigo, R. D., Jacoby, G. C., & Wright, W. E. (2010). Asian Monsoon Failure and Megadrought During the Last Millennium. Science, 328(5977), 486–489. https://doi.org/10.1126/science.1185188
+ Emile-Geay, J., Cobb, K. M., Mann, M. E., & Wittenberg, A. T. (2013). Estimating Central Equatorial Pacific SST Variability over the Past Millennium. Part II: Reconstructions and Implications. Journal of Climate, 26(7), 2329–2352. https://doi.org/10.1175/JCLI-D-11-00511.1
+ Fowler, A. M., Boswijk, G., Lorrey, A. M., Gergis, J., Pirie, M., McCloskey, S. P. J., et al. (2012). Multi-centennial tree-ring record of ENSO-related activity in New Zealand. Nature Climate Change, 2(3), 172–176. https://doi.org/10.1038/nclimate1374
+ Huang, B., Thorne, P. W., Banzon, V. F., Boyer, T., Chepurin, G., Lawrimore, J. H., et al. (2017). Extended Reconstructed Sea Surface Temperature, Version 5 (ERSSTv5): Upgrades, Validations, and Intercomparisons. Journal of Climate, 30(20), 8179–8205. https://doi.org/10.1175/JCLI-D-16-0836.1
+ Li, J., Xie, S.-P., Cook, E. R., Morales, M. S., Christie, D. A., Johnson, N. C., et al. (2013). El Niño modulations over the past seven centuries. Nature Climate Change, 3(9), 822–826. https://doi.org/10.1038/nclimate1936
+ Morales, M. S., Christie, D. A., Villalba, R., Argollo, J., Pacajes, J., Silva, J. S., et al. (2012). Precipitation changes in the South American Altiplano since 1300 AD reconstructed by tree-rings. Climate of the Past, 8(2), 653–666. https://doi.org/10.5194/cp-8-653-2012
+ PAGES2k Consortium (2017). A global multiproxy database for temperature reconstructions of the Common Era. Scientific Data, 4, 170088. https://doi.org/10.1038/sdata.2017.88
+ Tierney, J. E., Abram, N. J., Anchukaitis, K. J., Evans, M. N., Giry, C., Kilbourne, K. H., et al. (2015). Tropical sea surface temperatures for the past four centuries reconstructed from coral archives. Paleoceanography, 30(3), 2014PA002717. https://doi.org/10.1002/2014PA002717
+ Toohey, M., & Sigl, M. (2017). Volcanic stratospheric sulfur injections and aerosol optical depth from 500 BCE to 1900 CE. Earth System Science Data, 9(2), 809–831. https://doi.org/10.5194/essd-9-809-2017
+ Zhu, F., Emile-Geay, J. Hakim, G. J., Tardif, R., and Perkins., A., (2021). LMR Turbo (LMRt): a lightweight implementation of the LMR framework (0.8.0). Zenodo. http://doi.org/10.5281/zenodo.5205223

## How to cite this repo
This repo can be cited with [DOI: 10.5281/zenodo.5716165](https://doi.org/10.5281/zenodo.5716165).
