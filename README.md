# satellite-clustering

`read_multispectral.py`

Makes a satellite image into a jpg.
* Must be run using Python 2. 
* To run: `python read_multispectral.py /path/to/bin/file` where the path to the bin file is the path to the multispectral image (BSQ format), that also has a `.hdr` file.

    e.g. to view Sentinel-2 image: `python read_multispectral.py mS2.bin`
    
    e.g. to view Landsat-8 image: `python read_multispectral.py mL8.bin`
    
   
`cluster.py`

Runs k-means and elbow method on given satellite image.
* Provides functions to run k-means clustering and plot elbow method. 
* Created for Python 3.
* First run `read_multispectral.py` to get the satellite image as a jpg
* To run: `python3 cluster.py /path/to/jpg/satellite/image`

    e.g. to cluster Sentinel-2 image: `python cluster.py mS2.bin`
    
    e.g. to cluster Landsat-8 image: `python cluster.py mL8.bin`

    e.g. to cluster fused Sentinel-2 and Landsat-8 images: `python cluster.py mS2_L8.bin`
    
`small data test chips:`
*Sentinel-2 scene (12 bands)
mS2.bin  	
mS2.hdr 	

*Landsat-8 scene (11 bands)
mL8.bin
mL8.hdr 	

*Fused Sentinel-2 and Landsat-8 scene (23 bands)
mS2_L8.bin
mS2_L8.hdr
