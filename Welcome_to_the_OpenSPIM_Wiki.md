---
---
<table>
<tbody>
<tr class="odd">
<td><div cellspacing="5" style="width: 31em; font-size: 90%; text-align:left; float:right; position:relative; border:2px; border-style:solid;">
<p><b>News</b><br />
<listnews/></p>
</div>
<p><b>The Idea</b><br />
OpenSPIM is an <i>Open Access</i> platform for applying and enhancing <strong>Selective Plane Illumination Microscopy</strong> (<em>SPIM</em>).</p>
<blockquote>
<p>We hope that OpenSPIM in its radical openness will demonstrate that the benefits brought to science by the Open Source approach apply equally well to hardware.</p>
</blockquote></td>
<td><p> </p></td>
</tr>
<tr class="even">
<td><p> </p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><b>SPIM principle</b></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><img src="SPIM_logo.jpg" title="fig:SPIM schematic" width="200" alt="SPIM schematic" /> The SPIM technology offers fast, optically-sectioning, minimally-invasive 3D acquisition of fluorescing specimen over time. It achieves that by focusing a thin laser light-sheet into the specimen, taking two-dimensional images of the illuminated slice with a perpendicularly positioned detector (CCD camera). Three-dimensional stacks are obtained by moving the specimen orthogonal to the light-sheet between consecutive images. By mounting the sample in a rigid medium, e.g. agarose, and hanging it into the sample chamber in front of the detection lens, it is possible to rotate the sample and collect 3d stacks from multiple angles (views).</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p> </p></td>
<td></td>
</tr>
<tr class="even">
<td><p><b>OpenSPIM</b></p></td>
<td></td>
</tr>
<tr class="odd">
<td><figure>
<img src="Combined_solidworks_real_registered_small_faster.gif" title="OpenSPIM buildup" alt="" /><figcaption>OpenSPIM buildup</figcaption>
</figure>
<p>OpenSPIM is a platform to build, adapt and enhance SPIM technology. It is designed to be as accessible as possible:</p>
<ul>
<li><a href="Step_by_step_assembly" title="wikilink">detailed, easy-to-follow build instructions</a></li>
<li><a href="Table_of_parts" title="wikilink">off-the-shelf components and 3D-printed parts</a></li>
<li><a href=":File:Combined_OpenSPIM_buildup_looped.gif" title="wikilink">Modular</a> and <a href="Configurations" title="wikilink">extensible</a> design</li>
<li><a href=":Category:Hardware" title="wikilink">completely open blueprints</a></li>
<li><a href=":Category:Software" title="wikilink">completely Open Source</a></li>
</ul>
<p>The build instructions are intended to allow scientists without prior knowledge in building optical systems to make their own OpenSPIM set-up. If a 3D printer is not readily available, the parts are designed to be easily machined by any competent work shop. The set-up is small enough to fit inside a <a href="Media:SPIM_in_a_suitcase.jpg" title="wikilink">suitcase</a>. The software is built on top of the Open Source projects <a href="http://micro-manager.org">µManager</a> and <a href="http://fiji.sc/">Fiji</a>.</p>
<p>OpenSPIM is designed to be maximally cost-effective allowing anyone to build an entry level system and further tweak it for the specific imaging needs. Parallel set-ups (<a href=":File:2I_1D_OpenSPIM_farm_02.jpg" title="wikilink">SPIM farms</a>) can be realized to enable medium throughput, long-term, time-lapse imaging.</p>
<p>OpenSPIM aims to creates a powerful synergy between Open Software and Open Hardware that can serve as a nucleus for further development of the SPIM technology.</p></td>
<td></td>
</tr>
<tr class="even">
<td><p> </p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><b>SPIM application</b></p></td>
<td></td>
</tr>
<tr class="even">
<td><figure>
<img src="HisYFP_front_page.gif" title="OpenSPIM recording of Drosophila embryogenesis" width="200" alt="" /><figcaption>OpenSPIM recording of Drosophila embryogenesis</figcaption>
</figure>
<p>SPIM promises to revolutionize several fields of biological research, in particular developmental and cell biology, by allowing imaging of large samples with high resolution over extended periods of time. SPIM has been used in a spectacular fashion to record the development of embryos of model organisms such as <i>Drosophila</i> and zebra fish with cellular resolution throughout the developing specimen (the so-called <i>in toto</i> imaging). The ability of SPIM to deliver high signal-to-noise 3D images of large specimen from different angles in an extended time-lapse is currently hard to achieve with any other microscopy technology. Since monitoring biological systems with high resolution over time is the goal of essentially all fields of biological inquiry, SPIM technology is imminently useful to biologists.</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p> </p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Partners and funding: <img src="Mpi-cbg-logo.gif" title="fig:Mpi-cbg-logo.gif" width="150" alt="Mpi-cbg-logo.gif" /> <img src="LOCI_logo.jpg" title="fig:LOCI_logo.jpg" width="150" alt="LOCI_logo.jpg" /> <img src="LMF_logo.jpg" title="fig:LMF_logo.jpg" width="80" alt="LMF_logo.jpg" /> <img src="ERC_acronym.jpg" title="fig:ERC_acronym.jpg" width="100" alt="ERC_acronym.jpg" /> <img src="RMS_logo.jpg" title="fig:RMS_logo.jpg" width="150" alt="RMS_logo.jpg" /></p></td>
<td></td>
</tr>
</tbody>
</table>

\_\_NOTOC\_\_

# Building your own OpenSPIM

  - [Table of Parts](Table_of_parts "wikilink")
  - [Step by step assembly](Step_by_step_assembly "wikilink")
  - [How to install](How_to_install "wikilink") the Micro-Manager
    software with SPIM support.
  - [How to operate](Operation "wikilink") OpenSPIM including sample
    preparation, calibration and data processing.

Please feel free to put information about your system on [this
page](Who_has_an_OpenSPIM? "wikilink")\!

# OpenSPIM data

Check the [gallery](Gallery#OpenSPIM_data "wikilink") to see more\!

## MAMED EMBO course

<File:Platynereis> fused deconvolved labeled.ogv|Marine annelid
*Platynereis dumerilii* stained with Sytox-green imaged with OpenSPIM
from 7 angles. Walk through fused and deconvolved data (15 iterations on
default settings). Staining, OpenSPIM assembly and imaging done by Mette
Handberg-Thorsager, processing by Pavel Tomancak.

## Fruit fly

<File:Supplementary> Video 5.ogv|Histone-YFP from gastrulation to
beginning of muscle contraction from ventral, lateral and dorsal view
<File:Supplementary> Video 6.ogv|Expression pattern of Csp-sGFP recorded
with OpenSPIM

## Zebrafish

<File:Zebrafish> fused max gamma0.8.png | Multi-position z-stack of a
living 48 hpf Tg(Bactin:H2A-EGFP) zebrafish, stitched using the
Grid/Collection Plugin in Fiji. Maximum intensity projection, gamma 0.8.
<File:Supplementary> Video 2.ogv|Beating heart of a 48 hpf
Tg(cmlc2:EGFP) zebrafish. Left: overlay of transmitted light and
fluorescence signal. Right: fluorescence signal.

## Twitter

Follow OpenSPIM on Twitter for news on light sheet microscopy:
[@OpenSPIM](https://twitter.com/openspim)
