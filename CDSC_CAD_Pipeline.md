# Introduction #

The second medical imaging benchmark explores a novel approach towards lung nodule screening that utilizes an adaptive low-dose computed tomography (CT) method for image acquisition to:
  1. reduce the amount of radiation given to a patient during a potential image screening exam; and
  1. provide real-time characterization of suspicious nodules that warrant further examination and follow-up.

First, a “low dose” imaging study is performed and a real-time CT image reconstruction algorithm is employed to generate image data. Next, from the image data, a computer-aided detection (CAD) system automatically provides the user (e.g., technologists, radiologists) with immediate feedback about the presence of likely nodules, and suggests regions of interest (ROIs) to scan at a higher resolution. Lastly, for the different ROIs involving detected nodules, the user selects higher-resolution CT scan parameters, and only those areas are rescanned in the patient for diagnosis and clinical interpretation.

A description of the pipeline can be [found here](http://www.mii.ucla.edu/~willhsu/static/CDSC_AdaptivePipelineBenchmark.pdf).

# Algorithms #

<table cellpadding='4' border='1' cellspacing='2'>
<blockquote><tbody>
<blockquote><tr>
<blockquote><td></td>
<td>MATLAB</td>
<td>C</td>
<td>FPGA</td>
<td>Notes</td>
</blockquote></tr>
<tr>
<blockquote><td>EM+TV v2.0</td>
<td>--</td>
<td><a href='https://onedrive.live.com/download?cid=9CE3D2200742EE14&resid=9CE3D2200742EE14%215433&authkey=ABTKtsWOzbRvoHY'>Download</a></td>
<td>--</td>
<td>Use the provided sinogram dataset below, see readme.txt for instructions</td>
</blockquote></tr>
<tr>
<blockquote><td>Segmentation</td>
<td><a href='https://onedrive.live.com/download?cid=9CE3D2200742EE14&resid=9CE3D2200742EE14%215430&authkey=ADBk2EFstC0nkqE'>Download</a></td>
<td>--</td>
<td>--</td>
<td>Use the provided reconstructed dataset below</td>
</blockquote></tr>
<tr>
<blockquote><td>Detection</td>
<td><a href='https://onedrive.live.com/download?cid=9CE3D2200742EE14&resid=9CE3D2200742EE14%215429&authkey=AH998_6f2EhqqyY'>Download</a></td>
<td>--</td>
<td>--</td>
<td>Use the provided reconstructed dataset below</td>
</blockquote></tr>
</blockquote></tbody>
</table></blockquote>

# Datasets #
<table cellpadding='4' border='1' cellspacing='2'>
<blockquote><tbody>
<blockquote><tr>
<blockquote><td></td>
<td>Link</td>
<td>Notes</td>
</blockquote></tr>
<tr>
<blockquote><td>Low-dose CT Sinogram Data (Patient 1)</td>
<td><a href='https://onedrive.live.com/download?cid=9CE3D2200742EE14&resid=9CE3D2200742EE14%215434&authkey=ABgep3UHXi6as04'>Download</a></td>
<td>File is 2.8Gb uncompressed</td>
</blockquote></tr>
<tr>
<blockquote><td>Low-dose CT FBP Reconstructed (Patient 1)</td>
<td><a href='https://onedrive.live.com/download?cid=9CE3D2200742EE14&resid=9CE3D2200742EE14%215432&authkey=AE0fCHqbNoDsIBE'>Download</a></td>
<td></td>
</blockquote></tr>
</blockquote></tbody>
</table>