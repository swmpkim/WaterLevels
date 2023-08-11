# Water Levels

Download de-seasonalized water level data from an NWLON station and calculate trends on water level change

This process was originally created so [National Estuarine Research Reserves](https://coast.noaa.gov/nerrs/ "NOAA webpage about NERR System") involved in the [SETr project](https://nerrssciencecollaborative.org/index.php/project/Cressman18 "SETr official webpage") would be able to easily re-calculate 19-year water level change, based on the same data and statistical process used by NOAA COOPS to calculate long-term sea level rise. Note that 19 years is not long enough to call the resulting trend "sea level rise", so in SETr we referred to it as 19-year water level change.

# To use:

1.  Download this repository, by clicking on the big green "Code" button at the top and selecting "Download ZIP". Note - if you're familiar with git and github, go ahead and use your favorite process to get everything. I'm assuming most people using this are *not* github pros.\
2.  Unzip the downloaded repo to live someplace logical on your computer.\
3.  Open it up, and open the .Rproj file: WaterLevels.RProj.\
4.  That should open up an instance of RStudio. From the files pane (bottom right pane in RStudio), open up the file water_level_parameterized_reporting.Rmd (you can change its name first if you want to).\
5.  Up at the very top, set the parameters in lines 8-11:
    a.  what's your NWLON station\
    b.  when do the records start for SLR\
    c.  when did your SET stations get installed, and
    d.  what year should the rates be calculated through. (you will probably need to update through the end of the previous year).\
6.  At the top of the pane in RStudio that contains this code, hit the "Knit" button.

The script will download data from your NWLON station and store it in the 'data' subfolder. It will also save the rates into a csv file, in the 'csvs_for_SETr' subfolder. Finally, an html file will pop up that shows you what all those rates are, which years they encompass, and where things are saved. If you want to see that html file again in the future, it lives in the same directory as the .Rproj file you opened in step 3, and is named the same as the .Rmd file you are using (but ends with .html).
