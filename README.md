# Leafsnap-Dataset
<!DOCTYPE html>
<html>
   <head>
      <title>Leafsnap Dataset | Leafsnap: An Electronic Field Guide</title>
      <meta charset="utf-8" />
      <meta name="description" content="Leafsnap is an electronic field guide for tree and plant species in New York City and Washington, DC." />
      <link rel="stylesheet" type="text/css" href="../main.css">
      <link rel="stylesheet" type="text/css" href="dataset.css" />
   </head>
   <body>
      <header>
         <nav>
            <h1 class="page-title">
               <a href="../index.html">
               <img src="../leafsnap_logo.png" style="width:197px;height:71px;border:0;">
               </a>
            </h1>
            <ul>
 	       <li><a class="active" href="../species.html">Species</a></li>
               <li><a class="active" href="../support.html">Support</a></li>
               <li><a href="https://itunes.apple.com/us/app/leafsnap/id430649829?mt=8">Download</a></li>
            </ul>
         </nav>
      </header>

  <div id="dataset" class="datacode">
    <h1>Leafsnap Dataset</h1>

    <p>To promote further research in leaf recognition, we are releasing the
    <b>Leafsnap dataset</b>, which consists of images of leaves taken from two different sources, as well as their automatically-generated segmentations: </p><ol>
        <li><b>23147 Lab</b> images, consisting of high-quality images taken of
        pressed leaves, from the Smithsonian collection. These images
        appear in controlled backlit and front-lit versions, with several
        samples per species.</li>
        <li><b>7719 Field</b> images, consisting of "typical" images taken by
        mobile devices (iPhones mostly) in outdoor environments. These
        images contain varying amounts of blur, noise, illumination
        patterns, shadows, etc.</li>
    </ol><p></p>
    <p>The dataset currently covers <a href="#specieslist">all <b>185</b> tree species</a> from the Northeastern United States.</p>
    <p>If you use this dataset, please cite the following paper:</p>
    <div class="publication" id="leafsnap_eccv2012">
        <div class="title">"Leafsnap: A Computer Vision System for Automatic Plant Species Identification,"</div>
        <div class="authors">Neeraj Kumar, Peter N. Belhumeur, Arijit Biswas, David W. Jacobs, W. John Kress, Ida C. Lopez, João V. B. Soares,</div>
        <div class="journal">Proceedings of the 12th European Conference on Computer Vision (ECCV),</div>
        <div class="date">October 2012</div>
        <div class="links">
            <span class="link">[<a href="http://neerajkumar.org/base/papers/nk_eccv2012_leafsnap.pdf">paper (pdf)</a>]</span>
            <span class="link">[<a href="http://neerajkumar.org/base/presentations/2012_leafsnap/leafsnap-eccv2012.pptx">slides (pptx)</a>]</span>
            <span class="link">[<a class="fakelink" onclick="$(this).parents('.links').find('.bibref').slideToggle()">bibtex</a>]</span>
            <div class="bibref">
                @InProceedings{leafsnap_eccv2012,<br>
                author = {Neeraj Kumar and Peter N. Belhumeur and Arijit Biswas and David W. Jacobs and W. John Kress and Ida Lopez and João V. B. Soares},<br>
                title = {Leafsnap: A Computer Vision System for Automatic Plant Species Identification},<br>
                booktitle = {The 12th European Conference on Computer Vision (ECCV)},<br>
                month = {October},<br>
                year = {2012}<br>
                }
            </div>
        </div>
    </div>
    <p><b>NOTE:</b> The dataset released here doesn't exactly match that used to compute results for the paper, nor the currently running version on our servers.</p>
    <p>For questions and comments, please contact contact@leafsnap.com.</p>
    

    <h2 id="downloads">Downloads</h2>
    <hr>
    <table class="downloads">
        <tbody><tr><th>Links</th><th>Description</th><th>Size</th><th>Version</th><th>Last updated</th></tr>
        <tr>
            <td><a href="../static/dataset/leafsnap-dataset.tar">Download</a></td>
            <td class="description">Full Leafsnap dataset with original images, segmented images, text index of images, and <a href="../static/dataset/leafsnap-dataset-readme.txt">readme</a></td><td>977MB</td>
            <td>1.0</td><td>July 11, 2014</td>
        </tr>
    </tbody></table>

    <h2 id="dataformat">Data format</h2>
    <hr>
    <p>The included <a href="../static/dataset/leafsnap-dataset-images.txt">leafsnap-dataset-images.txt</a> file contains a listing of all the images, in tab-separated format (tsv). The first line is the header row, which describes each column:</p>
    <pre>    file_id    image_path   segmented_path    species    source
    </pre>
    <p>Each line lists information about a single image. There are 5 fields, which are separated by tabs:</p>
    <p></p><ol>
        <li>A unique numerical id for each image. These are not guaranteed to be consecutive or in order. They will not change over future versions of the dataset.</li>
        <li>The path of the original image.</li>
        <li>The path of the segmented version of the image. Note that where segmentation fails, the images might be completely black. In our running system, we have an automated check to discard such images from inclusion in the dataset for recognition.</li>
        <li>The scientific name of the species of the image. Note that these can have spaces and hyphens, and are in mixed case.</li>
        <li>The source of the image. This is either <code>lab</code> or <code>field</code>.</li>
    </ol><p></p>


    <h2 id="examples">Example images and segmentations</h2>
    <hr>
    <p>This table shows example images and their segmentations for a few species. Click on any image to see the full-sized version in a new window.</p><p>
    </p><p></p><table id="examples">
        <thead>
            </thead><colgroup>
                <col class="speciesname">
                <col class="lab image-ex">
                <col class="lab seg-ex">
                <col class="field image-ex">
                <col class="field seg-ex">
            </colgroup>
        
        <tbody>
            <tr>
                <th>Species</th>
                <th>Example lab image</th>
                <th>Example lab segmentation</th>
                <th>Example field image</th>
                <th>Example field segmentation</th>
            </tr>
            <tr class="example">
                <td>Halesia tetraptera</td>
                <td>
                <a href="images/lab/halesiaTetraptera/ny1025-09-1.jpg" target="_blank"><img class="eximg" src="images/lab/halesiaTetraptera/ny1025-09-1-thumb.jpg"></a>
                </td>
                <td>
                <a href="images/lab/halesiaTetraptera/ny1025-09-1.png" target="_blank"><img class="exseg" src="images/lab/halesiaTetraptera/ny1025-09-1-thumb.png"></a>
                </td>
                <td>
                <a href="images/lab/halesiaTetraptera/13001949635157.jpg" target="_blank"><img class="eximg" src="images/lab/halesiaTetraptera/13001949635157-thumb.jpg"></a>
                </td>
                <td>
                <a href="images/lab/halesiaTetraptera/13001949635157.png" target="_blank"><img class="exseg" src="images/lab/halesiaTetraptera/13001949635157-thumb.png"></a>
                </td>
            </tr>
            <tr class="example">
                <td>Ostrya virginiana</td>
                <td>
                <a href="images/lab/ostryaVirginiana/pi2195-09-1.jpg" target="_blank"><img class="eximg" src="images/lab/ostryaVirginiana/pi2195-09-1-thumb.jpg"></a>
                </td>
                <td>
                <a href="images/lab/ostryaVirginiana/pi2195-09-1.png" target="_blank"><img class="exseg" src="images/lab/ostryaVirginiana/pi2195-09-1-thumb.png"></a>
                </td>
                <td>
                <a href="images/lab/ostryaVirginiana/13001985584752.jpg" target="_blank"><img class="eximg" src="images/lab/ostryaVirginiana/13001985584752-thumb.jpg"></a>
                </td>
                <td>
                <a href="images/lab/ostryaVirginiana/13001985584752.png" target="_blank"><img class="exseg" src="images/lab/ostryaVirginiana/13001985584752-thumb.png"></a>
                </td>
            </tr>
            <tr class="example">
                <td>Nyssa sylvatica</td>
                <td>
                <a href="images/lab/nyssaSylvatica/ny1130-03-1.jpg" target="_blank"><img class="eximg" src="images/lab/NyssaSylvatica/ny1130-03-1-thumb.jpg"></a>
                </td>
                <td>
                <a href="images/lab/nyssaSylvatica/ny1130-03-1.png" target="_blank"><img class="exseg" src="images/lab/NyssaSylvatica/ny1130-03-1-thumb.png"></a>
                </td>
                <td>
                <a href="images/lab/nyssaSylvatica/12992004640275.jpg" target="_blank"><img class="eximg" src="images/lab/NyssaSylvatica/12992004640275-thumb.jpg"></a>
                </td>
                <td>
                <a href="images/lab/nyssaSylvatica/12992004640275.png" target="_blank"><img class="exseg" src="images/lab/NyssaSylvatica/12992004640275-thumb.png"></a>
                </td>
            </tr>
        </tbody>
    </table><p></p>


    <h2 id="specieslist">List of Species and Image Counts</h2>
    <hr>
    <p>The following table shows the image counts for all species in the Leafsnap dataset:</p><p>
    </p><p></p><table id="specieslist">
        <thead>
            </thead><colgroup>
                <col class="index">
                <col class="speciesname">
                <col class="count">
                <col class="count">
                <col class="count">
            </colgroup>
        
        <tbody>
            <tr>
                <th>#</th>
                <th class="speciesname">Species</th>
                <th>Lab image count</th>
                <th>Field image count</th>
                <th>Total image count</th>
            </tr>
            <tr class="odd">
                <td>1</td>
                <td class="speciesname">Abies concolor</td>
                <td>200</td>
                <td>51</td>
                <td>251</td>
            </tr>
            <tr class="even">
                <td>2</td>
                <td class="speciesname">Abies nordmanniana</td>
                <td>124</td>
                <td>35</td>
                <td>159</td>
            </tr>
            <tr class="odd">
                <td>3</td>
                <td class="speciesname">Acer campestre</td>
                <td>108</td>
                <td>36</td>
                <td>144</td>
            </tr>
            <tr class="even">
                <td>4</td>
                <td class="speciesname">Acer ginnala</td>
                <td>120</td>
                <td>31</td>
                <td>151</td>
            </tr>
            <tr class="odd">
                <td>5</td>
                <td class="speciesname">Acer griseum</td>
                <td>80</td>
                <td>46</td>
                <td>126</td>
            </tr>
            <tr class="even">
                <td>6</td>
                <td class="speciesname">Acer negundo</td>
                <td>196</td>
                <td>33</td>
                <td>229</td>
            </tr>
            <tr class="odd">
                <td>7</td>
                <td class="speciesname">Acer palmatum</td>
                <td>120</td>
                <td>92</td>
                <td>212</td>
            </tr>
            <tr class="even">
                <td>8</td>
                <td class="speciesname">Acer pensylvanicum</td>
                <td>120</td>
                <td>35</td>
                <td>155</td>
            </tr>
            <tr class="odd">
                <td>9</td>
                <td class="speciesname">Acer platanoides</td>
                <td>120</td>
                <td>20</td>
                <td>140</td>
            </tr>
            <tr class="even">
                <td>10</td>
                <td class="speciesname">Acer pseudoplatanus</td>
                <td>120</td>
                <td>15</td>
                <td>135</td>
            </tr>
            <tr class="odd">
                <td>11</td>
                <td class="speciesname">Acer rubrum</td>
                <td>252</td>
                <td>45</td>
                <td>297</td>
            </tr>
            <tr class="even">
                <td>12</td>
                <td class="speciesname">Acer saccharinum</td>
                <td>148</td>
                <td>39</td>
                <td>187</td>
            </tr>
            <tr class="odd">
                <td>13</td>
                <td class="speciesname">Acer saccharum</td>
                <td>159</td>
                <td>24</td>
                <td>183</td>
            </tr>
            <tr class="even">
                <td>14</td>
                <td class="speciesname">Aesculus flava</td>
                <td>116</td>
                <td>15</td>
                <td>131</td>
            </tr>
            <tr class="odd">
                <td>15</td>
                <td class="speciesname">Aesculus glabra</td>
                <td>120</td>
                <td>44</td>
                <td>164</td>
            </tr>
            <tr class="even">
                <td>16</td>
                <td class="speciesname">Aesculus hippocastamon</td>
                <td>120</td>
                <td>19</td>
                <td>139</td>
            </tr>
            <tr class="odd">
                <td>17</td>
                <td class="speciesname">Aesculus pavi</td>
                <td>124</td>
                <td>101</td>
                <td>225</td>
            </tr>
            <tr class="even">
                <td>18</td>
                <td class="speciesname">Ailanthus altissima</td>
                <td>104</td>
                <td>16</td>
                <td>120</td>
            </tr>
            <tr class="odd">
                <td>19</td>
                <td class="speciesname">Albizia julibrissin</td>
                <td>116</td>
                <td>28</td>
                <td>144</td>
            </tr>
            <tr class="even">
                <td>20</td>
                <td class="speciesname">Amelanchier arborea</td>
                <td>88</td>
                <td>43</td>
                <td>131</td>
            </tr>
            <tr class="odd">
                <td>21</td>
                <td class="speciesname">Amelanchier canadensis</td>
                <td>120</td>
                <td>35</td>
                <td>155</td>
            </tr>
            <tr class="even">
                <td>22</td>
                <td class="speciesname">Amelanchier laevis</td>
                <td>120</td>
                <td>31</td>
                <td>151</td>
            </tr>
            <tr class="odd">
                <td>23</td>
                <td class="speciesname">Asimina triloba</td>
                <td>200</td>
                <td>49</td>
                <td>249</td>
            </tr>
            <tr class="even">
                <td>24</td>
                <td class="speciesname">Betula alleghaniensis</td>
                <td>120</td>
                <td>33</td>
                <td>153</td>
            </tr>
            <tr class="odd">
                <td>25</td>
                <td class="speciesname">Betula jacqemontii</td>
                <td>120</td>
                <td>22</td>
                <td>142</td>
            </tr>
            <tr class="even">
                <td>26</td>
                <td class="speciesname">Betula lenta</td>
                <td>120</td>
                <td>11</td>
                <td>131</td>
            </tr>
            <tr class="odd">
                <td>27</td>
                <td class="speciesname">Betula nigra</td>
                <td>120</td>
                <td>20</td>
                <td>140</td>
            </tr>
            <tr class="even">
                <td>28</td>
                <td class="speciesname">Betula populifolia</td>
                <td>120</td>
                <td>26</td>
                <td>146</td>
            </tr>
            <tr class="odd">
                <td>29</td>
                <td class="speciesname">Broussonettia papyrifera</td>
                <td>240</td>
                <td>54</td>
                <td>294</td>
            </tr>
            <tr class="even">
                <td>30</td>
                <td class="speciesname">Carpinus betulus</td>
                <td>120</td>
                <td>15</td>
                <td>135</td>
            </tr>
            <tr class="odd">
                <td>31</td>
                <td class="speciesname">Carpinus caroliniana</td>
                <td>148</td>
                <td>31</td>
                <td>179</td>
            </tr>
            <tr class="even">
                <td>32</td>
                <td class="speciesname">Carya cordiformis</td>
                <td>148</td>
                <td>52</td>
                <td>200</td>
            </tr>
            <tr class="odd">
                <td>33</td>
                <td class="speciesname">Carya glabra</td>
                <td>100</td>
                <td>77</td>
                <td>177</td>
            </tr>
            <tr class="even">
                <td>34</td>
                <td class="speciesname">Carya ovata</td>
                <td>120</td>
                <td>35</td>
                <td>155</td>
            </tr>
            <tr class="odd">
                <td>35</td>
                <td class="speciesname">Carya tomentosa</td>
                <td>120</td>
                <td>53</td>
                <td>173</td>
            </tr>
            <tr class="even">
                <td>36</td>
                <td class="speciesname">Castanea dentata</td>
                <td>120</td>
                <td>41</td>
                <td>161</td>
            </tr>
            <tr class="odd">
                <td>37</td>
                <td class="speciesname">Catalpa bignonioides</td>
                <td>172</td>
                <td>45</td>
                <td>217</td>
            </tr>
            <tr class="even">
                <td>38</td>
                <td class="speciesname">Catalpa speciosa</td>
                <td>120</td>
                <td>72</td>
                <td>192</td>
            </tr>
            <tr class="odd">
                <td>39</td>
                <td class="speciesname">Cedrus atlantica</td>
                <td>80</td>
                <td>79</td>
                <td>159</td>
            </tr>
            <tr class="even">
                <td>40</td>
                <td class="speciesname">Cedrus deodara</td>
                <td>80</td>
                <td>40</td>
                <td>120</td>
            </tr>
            <tr class="odd">
                <td>41</td>
                <td class="speciesname">Cedrus libani</td>
                <td>120</td>
                <td>47</td>
                <td>167</td>
            </tr>
            <tr class="even">
                <td>42</td>
                <td class="speciesname">Celtis occidentalis</td>
                <td>112</td>
                <td>21</td>
                <td>133</td>
            </tr>
            <tr class="odd">
                <td>43</td>
                <td class="speciesname">Celtis tenuifolia</td>
                <td>120</td>
                <td>27</td>
                <td>147</td>
            </tr>
            <tr class="even">
                <td>44</td>
                <td class="speciesname">Cercidiphyllum japonicum</td>
                <td>119</td>
                <td>23</td>
                <td>142</td>
            </tr>
            <tr class="odd">
                <td>45</td>
                <td class="speciesname">Cercis canadensis</td>
                <td>172</td>
                <td>44</td>
                <td>216</td>
            </tr>
            <tr class="even">
                <td>46</td>
                <td class="speciesname">Chamaecyparis pisifera</td>
                <td>120</td>
                <td>52</td>
                <td>172</td>
            </tr>
            <tr class="odd">
                <td>47</td>
                <td class="speciesname">Chamaecyparis thyoides</td>
                <td>120</td>
                <td>45</td>
                <td>165</td>
            </tr>
            <tr class="even">
                <td>48</td>
                <td class="speciesname">Chionanthus retusus</td>
                <td>120</td>
                <td>23</td>
                <td>143</td>
            </tr>
            <tr class="odd">
                <td>49</td>
                <td class="speciesname">Chionanthus virginicus</td>
                <td>172</td>
                <td>45</td>
                <td>217</td>
            </tr>
            <tr class="even">
                <td>50</td>
                <td class="speciesname">Cladrastis lutea</td>
                <td>119</td>
                <td>51</td>
                <td>170</td>
            </tr>
            <tr class="odd">
                <td>51</td>
                <td class="speciesname">Cornus florida</td>
                <td>124</td>
                <td>51</td>
                <td>175</td>
            </tr>
            <tr class="even">
                <td>52</td>
                <td class="speciesname">Cornus kousa</td>
                <td>120</td>
                <td>15</td>
                <td>135</td>
            </tr>
            <tr class="odd">
                <td>53</td>
                <td class="speciesname">Cornus mas</td>
                <td>120</td>
                <td>44</td>
                <td>164</td>
            </tr>
            <tr class="even">
                <td>54</td>
                <td class="speciesname">Corylus colurna</td>
                <td>48</td>
                <td>36</td>
                <td>84</td>
            </tr>
            <tr class="odd">
                <td>55</td>
                <td class="speciesname">Crataegus crus-galli</td>
                <td>103</td>
                <td>13</td>
                <td>116</td>
            </tr>
            <tr class="even">
                <td>56</td>
                <td class="speciesname">Crataegus laevigata</td>
                <td>120</td>
                <td>23</td>
                <td>143</td>
            </tr>
            <tr class="odd">
                <td>57</td>
                <td class="speciesname">Crataegus phaenopyrum</td>
                <td>120</td>
                <td>22</td>
                <td>142</td>
            </tr>
            <tr class="even">
                <td>58</td>
                <td class="speciesname">Crataegus pruinosa</td>
                <td>120</td>
                <td>34</td>
                <td>154</td>
            </tr>
            <tr class="odd">
                <td>59</td>
                <td class="speciesname">Crataegus viridis</td>
                <td>120</td>
                <td>45</td>
                <td>165</td>
            </tr>
            <tr class="even">
                <td>60</td>
                <td class="speciesname">Cryptomeria japonica</td>
                <td>80</td>
                <td>132</td>
                <td>212</td>
            </tr>
            <tr class="odd">
                <td>61</td>
                <td class="speciesname">Diospyros virginiana</td>
                <td>200</td>
                <td>48</td>
                <td>248</td>
            </tr>
            <tr class="even">
                <td>62</td>
                <td class="speciesname">Eucommia ulmoides</td>
                <td>120</td>
                <td>71</td>
                <td>191</td>
            </tr>
            <tr class="odd">
                <td>63</td>
                <td class="speciesname">Evodia daniellii</td>
                <td>80</td>
                <td>35</td>
                <td>115</td>
            </tr>
            <tr class="even">
                <td>64</td>
                <td class="speciesname">Fagus grandifolia</td>
                <td>116</td>
                <td>38</td>
                <td>154</td>
            </tr>
            <tr class="odd">
                <td>65</td>
                <td class="speciesname">Ficus carica</td>
                <td>120</td>
                <td>45</td>
                <td>165</td>
            </tr>
            <tr class="even">
                <td>66</td>
                <td class="speciesname">Fraxinus americana</td>
                <td>88</td>
                <td>15</td>
                <td>103</td>
            </tr>
            <tr class="odd">
                <td>67</td>
                <td class="speciesname">Fraxinus nigra</td>
                <td>120</td>
                <td>85</td>
                <td>205</td>
            </tr>
            <tr class="even">
                <td>68</td>
                <td class="speciesname">Fraxinus pennsylvanica</td>
                <td>120</td>
                <td>15</td>
                <td>135</td>
            </tr>
            <tr class="odd">
                <td>69</td>
                <td class="speciesname">Ginkgo biloba</td>
                <td>120</td>
                <td>21</td>
                <td>141</td>
            </tr>
            <tr class="even">
                <td>70</td>
                <td class="speciesname">Gleditsia triacanthos</td>
                <td>152</td>
                <td>46</td>
                <td>198</td>
            </tr>
            <tr class="odd">
                <td>71</td>
                <td class="speciesname">Gymnocladus dioicus</td>
                <td>120</td>
                <td>28</td>
                <td>148</td>
            </tr>
            <tr class="even">
                <td>72</td>
                <td class="speciesname">Halesia tetraptera</td>
                <td>120</td>
                <td>24</td>
                <td>144</td>
            </tr>
            <tr class="odd">
                <td>73</td>
                <td class="speciesname">Ilex opaca</td>
                <td>216</td>
                <td>28</td>
                <td>244</td>
            </tr>
            <tr class="even">
                <td>74</td>
                <td class="speciesname">Juglans cinerea</td>
                <td>120</td>
                <td>97</td>
                <td>217</td>
            </tr>
            <tr class="odd">
                <td>75</td>
                <td class="speciesname">Juglans nigra</td>
                <td>148</td>
                <td>15</td>
                <td>163</td>
            </tr>
            <tr class="even">
                <td>76</td>
                <td class="speciesname">Juniperus virginiana</td>
                <td>48</td>
                <td>65</td>
                <td>113</td>
            </tr>
            <tr class="odd">
                <td>77</td>
                <td class="speciesname">Koelreuteria paniculata</td>
                <td>120</td>
                <td>74</td>
                <td>194</td>
            </tr>
            <tr class="even">
                <td>78</td>
                <td class="speciesname">Larix decidua</td>
                <td>120</td>
                <td>30</td>
                <td>150</td>
            </tr>
            <tr class="odd">
                <td>79</td>
                <td class="speciesname">Liquidambar styraciflua</td>
                <td>120</td>
                <td>46</td>
                <td>166</td>
            </tr>
            <tr class="even">
                <td>80</td>
                <td class="speciesname">Liriodendron tulipifera</td>
                <td>184</td>
                <td>51</td>
                <td>235</td>
            </tr>
            <tr class="odd">
                <td>81</td>
                <td class="speciesname">Maclura pomifera</td>
                <td>424</td>
                <td>24</td>
                <td>448</td>
            </tr>
            <tr class="even">
                <td>82</td>
                <td class="speciesname">Magnolia acuminata</td>
                <td>120</td>
                <td>28</td>
                <td>148</td>
            </tr>
            <tr class="odd">
                <td>83</td>
                <td class="speciesname">Magnolia denudata</td>
                <td>120</td>
                <td>60</td>
                <td>180</td>
            </tr>
            <tr class="even">
                <td>84</td>
                <td class="speciesname">Magnolia grandiflora</td>
                <td>120</td>
                <td>15</td>
                <td>135</td>
            </tr>
            <tr class="odd">
                <td>85</td>
                <td class="speciesname">Magnolia macrophylla</td>
                <td>120</td>
                <td>24</td>
                <td>144</td>
            </tr>
            <tr class="even">
                <td>86</td>
                <td class="speciesname">Magnolia soulangiana</td>
                <td>40</td>
                <td>16</td>
                <td>56</td>
            </tr>
            <tr class="odd">
                <td>87</td>
                <td class="speciesname">Magnolia stellata</td>
                <td>120</td>
                <td>47</td>
                <td>167</td>
            </tr>
            <tr class="even">
                <td>88</td>
                <td class="speciesname">Magnolia tripetala</td>
                <td>120</td>
                <td>32</td>
                <td>152</td>
            </tr>
            <tr class="odd">
                <td>89</td>
                <td class="speciesname">Magnolia virginiana</td>
                <td>120</td>
                <td>58</td>
                <td>178</td>
            </tr>
            <tr class="even">
                <td>90</td>
                <td class="speciesname">Malus angustifolia</td>
                <td>56</td>
                <td>29</td>
                <td>85</td>
            </tr>
            <tr class="odd">
                <td>91</td>
                <td class="speciesname">Malus baccata</td>
                <td>120</td>
                <td>35</td>
                <td>155</td>
            </tr>
            <tr class="even">
                <td>92</td>
                <td class="speciesname">Malus coronaria</td>
                <td>120</td>
                <td>31</td>
                <td>151</td>
            </tr>
            <tr class="odd">
                <td>93</td>
                <td class="speciesname">Malus floribunda</td>
                <td>120</td>
                <td>31</td>
                <td>151</td>
            </tr>
            <tr class="even">
                <td>94</td>
                <td class="speciesname">Malus hupehensis</td>
                <td>120</td>
                <td>32</td>
                <td>152</td>
            </tr>
            <tr class="odd">
                <td>95</td>
                <td class="speciesname">Malus pumila</td>
                <td>120</td>
                <td>53</td>
                <td>173</td>
            </tr>
            <tr class="even">
                <td>96</td>
                <td class="speciesname">Metasequoia glyptostroboides</td>
                <td>120</td>
                <td>52</td>
                <td>172</td>
            </tr>
            <tr class="odd">
                <td>97</td>
                <td class="speciesname">Morus alba</td>
                <td>128</td>
                <td>14</td>
                <td>142</td>
            </tr>
            <tr class="even">
                <td>98</td>
                <td class="speciesname">Morus rubra</td>
                <td>124</td>
                <td>15</td>
                <td>139</td>
            </tr>
            <tr class="odd">
                <td>99</td>
                <td class="speciesname">Nyssa sylvatica</td>
                <td>120</td>
                <td>44</td>
                <td>164</td>
            </tr>
            <tr class="even">
                <td>100</td>
                <td class="speciesname">Ostrya virginiana</td>
                <td>184</td>
                <td>25</td>
                <td>209</td>
            </tr>
            <tr class="odd">
                <td>101</td>
                <td class="speciesname">Oxydendrum arboreum</td>
                <td>120</td>
                <td>47</td>
                <td>167</td>
            </tr>
            <tr class="even">
                <td>102</td>
                <td class="speciesname">Paulownia tomentosa</td>
                <td>120</td>
                <td>22</td>
                <td>142</td>
            </tr>
            <tr class="odd">
                <td>103</td>
                <td class="speciesname">Phellodendron amurense</td>
                <td>120</td>
                <td>27</td>
                <td>147</td>
            </tr>
            <tr class="even">
                <td>104</td>
                <td class="speciesname">Picea abies</td>
                <td>120</td>
                <td>48</td>
                <td>168</td>
            </tr>
            <tr class="odd">
                <td>105</td>
                <td class="speciesname">Picea orientalis</td>
                <td>120</td>
                <td>44</td>
                <td>164</td>
            </tr>
            <tr class="even">
                <td>106</td>
                <td class="speciesname">Picea pungens</td>
                <td>120</td>
                <td>49</td>
                <td>169</td>
            </tr>
            <tr class="odd">
                <td>107</td>
                <td class="speciesname">Pinus bungeana</td>
                <td>120</td>
                <td>54</td>
                <td>174</td>
            </tr>
            <tr class="even">
                <td>108</td>
                <td class="speciesname">Pinus cembra</td>
                <td>120</td>
                <td>59</td>
                <td>179</td>
            </tr>
            <tr class="odd">
                <td>109</td>
                <td class="speciesname">Pinus densiflora</td>
                <td>120</td>
                <td>44</td>
                <td>164</td>
            </tr>
            <tr class="even">
                <td>110</td>
                <td class="speciesname">Pinus echinata</td>
                <td>120</td>
                <td>42</td>
                <td>162</td>
            </tr>
            <tr class="odd">
                <td>111</td>
                <td class="speciesname">Pinus flexilis</td>
                <td>124</td>
                <td>46</td>
                <td>170</td>
            </tr>
            <tr class="even">
                <td>112</td>
                <td class="speciesname">Pinus koraiensis</td>
                <td>116</td>
                <td>45</td>
                <td>161</td>
            </tr>
            <tr class="odd">
                <td>113</td>
                <td class="speciesname">Pinus nigra</td>
                <td>120</td>
                <td>41</td>
                <td>161</td>
            </tr>
            <tr class="even">
                <td>114</td>
                <td class="speciesname">Pinus parviflora</td>
                <td>120</td>
                <td>51</td>
                <td>171</td>
            </tr>
            <tr class="odd">
                <td>115</td>
                <td class="speciesname">Pinus peucea</td>
                <td>124</td>
                <td>36</td>
                <td>160</td>
            </tr>
            <tr class="even">
                <td>116</td>
                <td class="speciesname">Pinus pungens</td>
                <td>120</td>
                <td>39</td>
                <td>159</td>
            </tr>
            <tr class="odd">
                <td>117</td>
                <td class="speciesname">Pinus resinosa</td>
                <td>120</td>
                <td>50</td>
                <td>170</td>
            </tr>
            <tr class="even">
                <td>118</td>
                <td class="speciesname">Pinus rigida</td>
                <td>120</td>
                <td>44</td>
                <td>164</td>
            </tr>
            <tr class="odd">
                <td>119</td>
                <td class="speciesname">Pinus strobus</td>
                <td>120</td>
                <td>20</td>
                <td>140</td>
            </tr>
            <tr class="even">
                <td>120</td>
                <td class="speciesname">Pinus sylvestris</td>
                <td>120</td>
                <td>33</td>
                <td>153</td>
            </tr>
            <tr class="odd">
                <td>121</td>
                <td class="speciesname">Pinus taeda</td>
                <td>120</td>
                <td>43</td>
                <td>163</td>
            </tr>
            <tr class="even">
                <td>122</td>
                <td class="speciesname">Pinus thunbergii</td>
                <td>120</td>
                <td>10</td>
                <td>130</td>
            </tr>
            <tr class="odd">
                <td>123</td>
                <td class="speciesname">Pinus virginiana</td>
                <td>120</td>
                <td>45</td>
                <td>165</td>
            </tr>
            <tr class="even">
                <td>124</td>
                <td class="speciesname">Pinus wallichiana</td>
                <td>120</td>
                <td>40</td>
                <td>160</td>
            </tr>
            <tr class="odd">
                <td>125</td>
                <td class="speciesname">Platanus acerifolia</td>
                <td>120</td>
                <td>20</td>
                <td>140</td>
            </tr>
            <tr class="even">
                <td>126</td>
                <td class="speciesname">Platanus occidentalis</td>
                <td>168</td>
                <td>20</td>
                <td>188</td>
            </tr>
            <tr class="odd">
                <td>127</td>
                <td class="speciesname">Populus deltoides</td>
                <td>120</td>
                <td>46</td>
                <td>166</td>
            </tr>
            <tr class="even">
                <td>128</td>
                <td class="speciesname">Populus grandidentata</td>
                <td>120</td>
                <td>42</td>
                <td>162</td>
            </tr>
            <tr class="odd">
                <td>129</td>
                <td class="speciesname">Populus tremuloides</td>
                <td>120</td>
                <td>41</td>
                <td>161</td>
            </tr>
            <tr class="even">
                <td>130</td>
                <td class="speciesname">Prunus pensylvanica</td>
                <td>120</td>
                <td>30</td>
                <td>150</td>
            </tr>
            <tr class="odd">
                <td>131</td>
                <td class="speciesname">Prunus sargentii</td>
                <td>120</td>
                <td>168</td>
                <td>288</td>
            </tr>
            <tr class="even">
                <td>132</td>
                <td class="speciesname">Prunus serotina</td>
                <td>128</td>
                <td>21</td>
                <td>149</td>
            </tr>
            <tr class="odd">
                <td>133</td>
                <td class="speciesname">Prunus serrulata</td>
                <td>120</td>
                <td>15</td>
                <td>135</td>
            </tr>
            <tr class="even">
                <td>134</td>
                <td class="speciesname">Prunus subhirtella</td>
                <td>120</td>
                <td>47</td>
                <td>167</td>
            </tr>
            <tr class="odd">
                <td>135</td>
                <td class="speciesname">Prunus virginiana</td>
                <td>120</td>
                <td>183</td>
                <td>303</td>
            </tr>
            <tr class="even">
                <td>136</td>
                <td class="speciesname">Prunus yedoensis</td>
                <td>120</td>
                <td>17</td>
                <td>137</td>
            </tr>
            <tr class="odd">
                <td>137</td>
                <td class="speciesname">Pseudolarix amabilis</td>
                <td>116</td>
                <td>37</td>
                <td>153</td>
            </tr>
            <tr class="even">
                <td>138</td>
                <td class="speciesname">Ptelea trifoliata</td>
                <td>220</td>
                <td>50</td>
                <td>270</td>
            </tr>
            <tr class="odd">
                <td>139</td>
                <td class="speciesname">Pyrus calleryana</td>
                <td>120</td>
                <td>52</td>
                <td>172</td>
            </tr>
            <tr class="even">
                <td>140</td>
                <td class="speciesname">Quercus acutissima</td>
                <td>120</td>
                <td>49</td>
                <td>169</td>
            </tr>
            <tr class="odd">
                <td>141</td>
                <td class="speciesname">Quercus alba</td>
                <td>160</td>
                <td>15</td>
                <td>175</td>
            </tr>
            <tr class="even">
                <td>142</td>
                <td class="speciesname">Quercus bicolor</td>
                <td>124</td>
                <td>21</td>
                <td>145</td>
            </tr>
            <tr class="odd">
                <td>143</td>
                <td class="speciesname">Quercus cerris</td>
                <td>120</td>
                <td>16</td>
                <td>136</td>
            </tr>
            <tr class="even">
                <td>144</td>
                <td class="speciesname">Quercus coccinea</td>
                <td>120</td>
                <td>22</td>
                <td>142</td>
            </tr>
            <tr class="odd">
                <td>145</td>
                <td class="speciesname">Quercus falcata</td>
                <td>7</td>
                <td>53</td>
                <td>60</td>
            </tr>
            <tr class="even">
                <td>146</td>
                <td class="speciesname">Quercus imbricaria</td>
                <td>116</td>
                <td>27</td>
                <td>143</td>
            </tr>
            <tr class="odd">
                <td>147</td>
                <td class="speciesname">Quercus macrocarpa</td>
                <td>120</td>
                <td>44</td>
                <td>164</td>
            </tr>
            <tr class="even">
                <td>148</td>
                <td class="speciesname">Quercus marilandica</td>
                <td>120</td>
                <td>57</td>
                <td>177</td>
            </tr>
            <tr class="odd">
                <td>149</td>
                <td class="speciesname">Quercus michauxii</td>
                <td>120</td>
                <td>48</td>
                <td>168</td>
            </tr>
            <tr class="even">
                <td>150</td>
                <td class="speciesname">Quercus montana</td>
                <td>188</td>
                <td>59</td>
                <td>247</td>
            </tr>
            <tr class="odd">
                <td>151</td>
                <td class="speciesname">Quercus muehlenbergii</td>
                <td>120</td>
                <td>106</td>
                <td>226</td>
            </tr>
            <tr class="even">
                <td>152</td>
                <td class="speciesname">Quercus nigra</td>
                <td>120</td>
                <td>44</td>
                <td>164</td>
            </tr>
            <tr class="odd">
                <td>153</td>
                <td class="speciesname">Quercus palustris</td>
                <td>120</td>
                <td>15</td>
                <td>135</td>
            </tr>
            <tr class="even">
                <td>154</td>
                <td class="speciesname">Quercus phellos</td>
                <td>120</td>
                <td>15</td>
                <td>135</td>
            </tr>
            <tr class="odd">
                <td>155</td>
                <td class="speciesname">Quercus robur</td>
                <td>116</td>
                <td>27</td>
                <td>143</td>
            </tr>
            <tr class="even">
                <td>156</td>
                <td class="speciesname">Quercus rubra</td>
                <td>40</td>
                <td>31</td>
                <td>71</td>
            </tr>
            <tr class="odd">
                <td>157</td>
                <td class="speciesname">Quercus shumardii</td>
                <td>120</td>
                <td>38</td>
                <td>158</td>
            </tr>
            <tr class="even">
                <td>158</td>
                <td class="speciesname">Quercus stellata</td>
                <td>120</td>
                <td>52</td>
                <td>172</td>
            </tr>
            <tr class="odd">
                <td>159</td>
                <td class="speciesname">Quercus velutina</td>
                <td>120</td>
                <td>52</td>
                <td>172</td>
            </tr>
            <tr class="even">
                <td>160</td>
                <td class="speciesname">Quercus virginiana</td>
                <td>120</td>
                <td>45</td>
                <td>165</td>
            </tr>
            <tr class="odd">
                <td>161</td>
                <td class="speciesname">Robinia pseudo-acacia</td>
                <td>124</td>
                <td>21</td>
                <td>145</td>
            </tr>
            <tr class="even">
                <td>162</td>
                <td class="speciesname">Salix babylonica</td>
                <td>120</td>
                <td>51</td>
                <td>171</td>
            </tr>
            <tr class="odd">
                <td>163</td>
                <td class="speciesname">Salix caroliniana</td>
                <td>128</td>
                <td>39</td>
                <td>167</td>
            </tr>
            <tr class="even">
                <td>164</td>
                <td class="speciesname">Salix matsudana</td>
                <td>116</td>
                <td>50</td>
                <td>166</td>
            </tr>
            <tr class="odd">
                <td>165</td>
                <td class="speciesname">Salix nigra</td>
                <td>120</td>
                <td>77</td>
                <td>197</td>
            </tr>
            <tr class="even">
                <td>166</td>
                <td class="speciesname">Sassafras albidum</td>
                <td>112</td>
                <td>20</td>
                <td>132</td>
            </tr>
            <tr class="odd">
                <td>167</td>
                <td class="speciesname">Staphylea trifolia</td>
                <td>168</td>
                <td>45</td>
                <td>213</td>
            </tr>
            <tr class="even">
                <td>168</td>
                <td class="speciesname">Stewartia pseudocamellia</td>
                <td>120</td>
                <td>45</td>
                <td>165</td>
            </tr>
            <tr class="odd">
                <td>169</td>
                <td class="speciesname">Styrax japonica</td>
                <td>120</td>
                <td>108</td>
                <td>228</td>
            </tr>
            <tr class="even">
                <td>170</td>
                <td class="speciesname">Styrax obassia</td>
                <td>40</td>
                <td>39</td>
                <td>79</td>
            </tr>
            <tr class="odd">
                <td>171</td>
                <td class="speciesname">Syringa reticulata</td>
                <td>60</td>
                <td>38</td>
                <td>98</td>
            </tr>
            <tr class="even">
                <td>172</td>
                <td class="speciesname">Taxodium distichum</td>
                <td>116</td>
                <td>60</td>
                <td>176</td>
            </tr>
            <tr class="odd">
                <td>173</td>
                <td class="speciesname">Tilia americana</td>
                <td>144</td>
                <td>15</td>
                <td>159</td>
            </tr>
            <tr class="even">
                <td>174</td>
                <td class="speciesname">Tilia cordata</td>
                <td>120</td>
                <td>77</td>
                <td>197</td>
            </tr>
            <tr class="odd">
                <td>175</td>
                <td class="speciesname">Tilia europaea</td>
                <td>120</td>
                <td>15</td>
                <td>135</td>
            </tr>
            <tr class="even">
                <td>176</td>
                <td class="speciesname">Tilia tomentosa</td>
                <td>120</td>
                <td>25</td>
                <td>145</td>
            </tr>
            <tr class="odd">
                <td>177</td>
                <td class="speciesname">Toona sinensis</td>
                <td>40</td>
                <td>24</td>
                <td>64</td>
            </tr>
            <tr class="even">
                <td>178</td>
                <td class="speciesname">Tsuga canadensis</td>
                <td>120</td>
                <td>69</td>
                <td>189</td>
            </tr>
            <tr class="odd">
                <td>179</td>
                <td class="speciesname">Ulmus americana</td>
                <td>200</td>
                <td>15</td>
                <td>215</td>
            </tr>
            <tr class="even">
                <td>180</td>
                <td class="speciesname">Ulmus glabra</td>
                <td>104</td>
                <td>56</td>
                <td>160</td>
            </tr>
            <tr class="odd">
                <td>181</td>
                <td class="speciesname">Ulmus parvifolia</td>
                <td>120</td>
                <td>45</td>
                <td>165</td>
            </tr>
            <tr class="even">
                <td>182</td>
                <td class="speciesname">Ulmus procera</td>
                <td>120</td>
                <td>0</td>
                <td>120</td>
            </tr>
            <tr class="odd">
                <td>183</td>
                <td class="speciesname">Ulmus pumila</td>
                <td>120</td>
                <td>145</td>
                <td>265</td>
            </tr>
            <tr class="even">
                <td>184</td>
                <td class="speciesname">Ulmus rubra</td>
                <td>268</td>
                <td>49</td>
                <td>317</td>
            </tr>
            <tr class="odd">
                <td>185</td>
                <td class="speciesname">Zelkova serrata</td>
                <td>120</td>
                <td>63</td>
                <td>183</td>
            </tr>
        </tbody>
    </table><p></p>

    <hr>
</div> 
      <section class="content-wrapper links">
          <div style="width:100px; padding-top:20px; margin:auto; display:flex;">
              <img src="../github icon.png" width="34px" height="34px" style="padding-right:10px;"></img>
              <img src="../twitter icon.png" width="34px" height="34px"></img>
          </div>
          <ul class="list-horizontal">
               <li>Contact</li>
               <li><a href="../team/team.html">Team</a></li>
               <li>Privacy</li>
               <li style="padding-right:0px;"><a href="support.html">Support</a></li>
           </ul>
      </section>
    </body>
</html>
Madelines-MacbookPro:public madelinezechar$ 
