---
description: How to make Histogram plots in MATLAB<sup>&reg;</sup> with Plotly.
name: Histograms
display_as: statistical
order: 3
permalink: matlab/histograms/
thumbnail: thumbnail/histogram.jpg
layout: base
language: matlab
page_type: u-guide
---

## Histogram of Vector

Generate 10,000 random numbers and create a histogram. The `histogram` function automatically chooses an appropriate number of bins to cover the range of values in `x` and show the shape of the underlying distribution.

<pre class="mcode">
x = randn(10000,1);
h = histogram(x)

fig2plotly()
</pre>

{% capture plot_0_0_histogram_of_vector_73 %}
  {% raw %}{"data":[{"name":"x","type":"bar","x":[-3.7,-3.5,-3.3,-3.1,-2.9,-2.7,-2.5,-2.3,-2.1,-1.9,-1.7,-1.5,-1.3,-1.1,-0.9,-0.7,-0.5,-0.3,-0.1,0.0999999999999999,0.3,0.5,0.7,0.9,1.1,1.3,1.5,1.7,1.9,2.1,2.3,2.5,2.7,2.9,3.1,3.3,3.5],"y":[2,2,1,6,7,17,29,57,86,133,193,271,331,421,540,613,730,748,776,806,824,721,623,503,446,326,234,191,132,78,65,33,26,11,8,5,5],"xaxis":"x1","yaxis":"y1","marker":{"line":{"color":"rgb(0,0,0)","width":0.5}},"opacity":0.75,"visible":true,"width":[0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.199999999999999,0.2,0.2,0.2,0.2,0.199999999999999,0.2,0.2,0.2,0.2,0.199999999999999,0.2,0.2],"showlegend":true}],"layout":{"title":"","width":840,"height":630,"margin":{"b":0,"l":0,"r":0,"t":80,"pad":0},"scene1":{"domain":{"x":[0.13,0.905],"y":[0.11,0.925]}},"xaxis1":{"side":"bottom","type":"linear","range":[-4.17,3.97],"ticks":"inside","anchor":"y1","domain":[0.13,0.905],"mirror":"ticks","nticks":9,"ticklen":6.51,"autotick":true,"showgrid":false,"showline":true,"tickfont":{"size":10,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"zeroline":false,"autorange":false,"gridcolor":"rgb(38.25,38.25,38.25)","gridwidth":1,"linecolor":"rgb(38.25,38.25,38.25)","linewidth":1,"tickcolor":"rgb(38.25,38.25,38.25)","tickwidth":1,"titlefont":{"size":11,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"exponentformat":"none"},"yaxis1":{"side":"left","type":"linear","range":[0,900],"ticks":"inside","anchor":"x1","domain":[0.11,0.925],"mirror":"ticks","nticks":11,"ticklen":6.51,"autotick":true,"showgrid":false,"showline":true,"tickfont":{"size":10,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"zeroline":false,"autorange":false,"gridcolor":"rgb(38.25,38.25,38.25)","gridwidth":1,"linecolor":"rgb(38.25,38.25,38.25)","linewidth":1,"tickcolor":"rgb(38.25,38.25,38.25)","tickwidth":1,"titlefont":{"size":11,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"exponentformat":"none"},"barmode":"group","autosize":false,"hovermode":"closest","titlefont":{"size":11,"color":"rgb(0,0,0)","family":"Arial,sans-serif"},"showlegend":false,"annotations":[],"paper_bgcolor":"rgb(255,255,255)"},"frames":[]}{% endraw %}
{% endcapture %}
{% include posts/ssim_frame.html 
  raw_json_file=plot_0_0_histogram_of_vector_73
  ssim="https://raw.githubusercontent.com/plotly/ssim_baselines/main/out_matlab/matlab/code-examples/data-distribution-plots/histogram/plot_0_0_histogram_of_vector_ssim_map.png" 
  compare="https://raw.githubusercontent.com/plotly/ssim_baselines/main/out_matlab/matlab/code-examples/data-distribution-plots/histogram/plot_0_0_histogram_of_vector_montage.png" 
  index=73
%}


<pre class="codeoutput">h = 
  Histogram with properties:

             Data: [10000x1 double]
           Values: [1x37 double]
          NumBins: 37
         BinEdges: [1x38 double]
         BinWidth: 0.2000
        BinLimits: [-3.8000 3.6000]
    Normalization: 'count'
        FaceColor: 'auto'
        EdgeColor: [0 0 0]

  Show all properties

</pre>


When you specify an output argument to the `histogram` function, it returns a histogram object. You can use this object to inspect the properties of the histogram, such as the number of bins or the width of the bins.

Find the number of histogram bins. 

<pre class="mcode">
nbins = h.NumBins

fig2plotly()
</pre>


<pre class="codeoutput">nbins = 37
</pre>




<!--------------------- EXAMPLE BREAK ------------------------->

## Specify Number of Histogram Bins

Plot a histogram of 1,000 random numbers sorted into 25 equally spaced bins.

<pre class="mcode">
x = randn(1000,1);
nbins = 25;
h = histogram(x,nbins)

fig2plotly()
</pre>

{% capture plot_1_0_specify_number_of_histogram_bins_75 %}
  {% raw %}{"data":[{"name":"x","type":"bar","x":[-3.06,-2.78,-2.5,-2.22,-1.94,-1.66,-1.38,-1.1,-0.82,-0.54,-0.26,0.02,0.3,0.58,0.86,1.14,1.42,1.7,1.98,2.26,2.54,2.82,3.1,3.38,3.66],"y":[2,5,5,9,17,34,39,61,85,93,112,97,101,90,74,57,39,41,15,9,8,4,2,0,1],"xaxis":"x1","yaxis":"y1","marker":{"line":{"color":"rgb(0,0,0)","width":0.5}},"opacity":0.75,"visible":true,"width":[0.28,0.28,0.28,0.28,0.28,0.28,0.28,0.28,0.28,0.28,0.28,0.28,0.28,0.28,0.28,0.28,0.28,0.28,0.279999999999999,0.28,0.28,0.279999999999999,0.28,0.28,0.28],"showlegend":true}],"layout":{"title":"","width":840,"height":630,"margin":{"b":0,"l":0,"r":0,"t":80,"pad":0},"scene1":{"domain":{"x":[0.13,0.905],"y":[0.11,0.925]}},"xaxis1":{"side":"bottom","type":"linear","range":[-3.55,4.15],"ticks":"inside","anchor":"y1","domain":[0.13,0.905],"mirror":"ticks","nticks":9,"ticklen":6.51,"autotick":true,"showgrid":false,"showline":true,"tickfont":{"size":10,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"zeroline":false,"autorange":false,"gridcolor":"rgb(38.25,38.25,38.25)","gridwidth":1,"linecolor":"rgb(38.25,38.25,38.25)","linewidth":1,"tickcolor":"rgb(38.25,38.25,38.25)","tickwidth":1,"titlefont":{"size":11,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"exponentformat":"none"},"yaxis1":{"side":"left","type":"linear","range":[0,120],"ticks":"inside","anchor":"x1","domain":[0.11,0.925],"mirror":"ticks","nticks":8,"ticklen":6.51,"autotick":true,"showgrid":false,"showline":true,"tickfont":{"size":10,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"zeroline":false,"autorange":false,"gridcolor":"rgb(38.25,38.25,38.25)","gridwidth":1,"linecolor":"rgb(38.25,38.25,38.25)","linewidth":1,"tickcolor":"rgb(38.25,38.25,38.25)","tickwidth":1,"titlefont":{"size":11,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"exponentformat":"none"},"barmode":"group","autosize":false,"hovermode":"closest","titlefont":{"size":11,"color":"rgb(0,0,0)","family":"Arial,sans-serif"},"showlegend":false,"annotations":[],"paper_bgcolor":"rgb(255,255,255)"},"frames":[]}{% endraw %}
{% endcapture %}
{% include posts/ssim_frame.html 
  raw_json_file=plot_1_0_specify_number_of_histogram_bins_75
  ssim="https://raw.githubusercontent.com/plotly/ssim_baselines/main/out_matlab/matlab/code-examples/data-distribution-plots/histogram/plot_1_0_specify_number_of_histogram_bins_ssim_map.png" 
  compare="https://raw.githubusercontent.com/plotly/ssim_baselines/main/out_matlab/matlab/code-examples/data-distribution-plots/histogram/plot_1_0_specify_number_of_histogram_bins_montage.png" 
  index=75
%}


<pre class="codeoutput">h = 
  Histogram with properties:

             Data: [1000x1 double]
           Values: [1x25 double]
          NumBins: 25
         BinEdges: [1x26 double]
         BinWidth: 0.2800
        BinLimits: [-3.4000 3.6000]
    Normalization: 'count'
        FaceColor: 'auto'
        EdgeColor: [0 0 0]

  Show all properties

</pre>


Find the bin counts.

<pre class="mcode">
counts = h.Values

fig2plotly()
</pre>


<pre class="codeoutput">counts = <span class="emphasis"><em>1×25</em></span>

     1     3     0     6    14    19    31    54    74    80    92   122   104   115    88    80    38    32    21     9     5     5     5     0     2

</pre>




<!--------------------- EXAMPLE BREAK ------------------------->

## Change Number of Histogram Bins

Generate 1,000 random numbers and create a histogram. 

<pre class="mcode">
X = randn(1000,1);
h = histogram(X)

fig2plotly()
</pre>

{% capture plot_2_0_change_number_of_histogram_bins_77 %}
  {% raw %}{"data":[{"name":"X","type":"bar","x":[-3.45,-3.15,-2.85,-2.55,-2.25,-1.95,-1.65,-1.35,-1.05,-0.75,-0.45,-0.15,0.15,0.45,0.75,1.05,1.35,1.65,1.95,2.25,2.55,2.85,3.15],"y":[1,2,0,5,12,18,28,51,75,89,117,114,122,114,74,66,47,26,19,14,3,2,1],"xaxis":"x1","yaxis":"y1","marker":{"line":{"color":"rgb(0,0,0)","width":0.5}},"opacity":0.75,"visible":true,"width":[0.3,0.3,0.3,0.3,0.3,0.3,0.3,0.3,0.3,0.3,0.3,0.3,0.3,0.300000000000001,0.3,0.3,0.3,0.3,0.300000000000001,0.3,0.3,0.300000000000001,0.3],"showlegend":true}],"layout":{"title":"","width":840,"height":630,"margin":{"b":0,"l":0,"r":0,"t":80,"pad":0},"scene1":{"domain":{"x":[0.13,0.905],"y":[0.11,0.925]}},"xaxis1":{"side":"bottom","type":"linear","range":[-3.945,3.645],"ticks":"inside","anchor":"y1","domain":[0.13,0.905],"mirror":"ticks","nticks":8,"ticklen":6.51,"autotick":true,"showgrid":false,"showline":true,"tickfont":{"size":10,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"zeroline":false,"autorange":false,"gridcolor":"rgb(38.25,38.25,38.25)","gridwidth":1,"linecolor":"rgb(38.25,38.25,38.25)","linewidth":1,"tickcolor":"rgb(38.25,38.25,38.25)","tickwidth":1,"titlefont":{"size":11,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"exponentformat":"none"},"yaxis1":{"side":"left","type":"linear","range":[0,140],"ticks":"inside","anchor":"x1","domain":[0.11,0.925],"mirror":"ticks","nticks":9,"ticklen":6.51,"autotick":true,"showgrid":false,"showline":true,"tickfont":{"size":10,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"zeroline":false,"autorange":false,"gridcolor":"rgb(38.25,38.25,38.25)","gridwidth":1,"linecolor":"rgb(38.25,38.25,38.25)","linewidth":1,"tickcolor":"rgb(38.25,38.25,38.25)","tickwidth":1,"titlefont":{"size":11,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"exponentformat":"none"},"barmode":"group","autosize":false,"hovermode":"closest","titlefont":{"size":11,"color":"rgb(0,0,0)","family":"Arial,sans-serif"},"showlegend":false,"annotations":[],"paper_bgcolor":"rgb(255,255,255)"},"frames":[]}{% endraw %}
{% endcapture %}
{% include posts/ssim_frame.html 
  raw_json_file=plot_2_0_change_number_of_histogram_bins_77
  ssim="https://raw.githubusercontent.com/plotly/ssim_baselines/main/out_matlab/matlab/code-examples/data-distribution-plots/histogram/plot_2_0_change_number_of_histogram_bins_ssim_map.png" 
  compare="https://raw.githubusercontent.com/plotly/ssim_baselines/main/out_matlab/matlab/code-examples/data-distribution-plots/histogram/plot_2_0_change_number_of_histogram_bins_montage.png" 
  index=77
%}


<pre class="codeoutput">h = 
  Histogram with properties:

             Data: [1000x1 double]
           Values: [1x23 double]
          NumBins: 23
         BinEdges: [1x24 double]
         BinWidth: 0.3000
        BinLimits: [-3.3000 3.6000]
    Normalization: 'count'
        FaceColor: 'auto'
        EdgeColor: [0 0 0]

  Show all properties

</pre>


Use the `morebins` function to coarsely adjust the number of bins.

<pre class="mcode">
Nbins = morebins(h);
Nbins = morebins(h)

fig2plotly()
</pre>

{% capture plot_2_1_change_number_of_histogram_bins_78 %}
  {% raw %}{"data":[{"name":"X","type":"bar","x":[-3.4805,-3.2415,-3.0025,-2.7635,-2.5245,-2.2855,-2.0465,-1.8075,-1.5685,-1.3295,-1.0905,-0.8515,-0.6125,-0.3735,-0.1345,0.1045,0.3435,0.5825,0.8215,1.0605,1.2995,1.5385,1.7775,2.0165,2.2555,2.4945,2.7335,2.9725,3.2115,3.4505,3.6895,3.9285],"y":[1,0,1,2,3,4,15,23,32,43,53,63,80,76,94,101,96,79,68,59,40,28,14,16,2,1,3,1,1,0,0,1],"xaxis":"x1","yaxis":"y1","marker":{"line":{"color":"rgb(0,0,0)","width":0.5}},"opacity":0.75,"visible":true,"width":[0.239,0.239,0.239,0.239,0.239,0.239,0.239,0.239,0.239,0.239,0.239,0.239,0.239,0.239,0.239,0.239,0.239,0.239,0.239,0.239,0.239,0.239,0.239000000000001,0.239,0.239,0.239,0.239,0.239,0.239000000000001,0.239,0.239,0.238999999999999],"showlegend":true}],"layout":{"title":"","width":840,"height":630,"margin":{"b":0,"l":0,"r":0,"t":80,"pad":0},"scene1":{"domain":{"x":[0.13,0.905],"y":[0.11,0.925]}},"xaxis1":{"side":"bottom","type":"linear","range":[-3.9824,4.4304],"ticks":"inside","anchor":"y1","domain":[0.13,0.905],"mirror":"ticks","nticks":9,"ticklen":6.51,"autotick":true,"showgrid":false,"showline":true,"tickfont":{"size":10,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"zeroline":false,"autorange":false,"gridcolor":"rgb(38.25,38.25,38.25)","gridwidth":1,"linecolor":"rgb(38.25,38.25,38.25)","linewidth":1,"tickcolor":"rgb(38.25,38.25,38.25)","tickwidth":1,"titlefont":{"size":11,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"exponentformat":"none"},"yaxis1":{"side":"left","type":"linear","range":[0,120],"ticks":"inside","anchor":"x1","domain":[0.11,0.925],"mirror":"ticks","nticks":8,"ticklen":6.51,"autotick":true,"showgrid":false,"showline":true,"tickfont":{"size":10,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"zeroline":false,"autorange":false,"gridcolor":"rgb(38.25,38.25,38.25)","gridwidth":1,"linecolor":"rgb(38.25,38.25,38.25)","linewidth":1,"tickcolor":"rgb(38.25,38.25,38.25)","tickwidth":1,"titlefont":{"size":11,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"exponentformat":"none"},"barmode":"group","autosize":false,"hovermode":"closest","titlefont":{"size":11,"color":"rgb(0,0,0)","family":"Arial,sans-serif"},"showlegend":false,"annotations":[],"paper_bgcolor":"rgb(255,255,255)"},"frames":[]}{% endraw %}
{% endcapture %}
{% include posts/ssim_frame.html 
  raw_json_file=plot_2_1_change_number_of_histogram_bins_78
  ssim="https://raw.githubusercontent.com/plotly/ssim_baselines/main/out_matlab/matlab/code-examples/data-distribution-plots/histogram/plot_2_1_change_number_of_histogram_bins_ssim_map.png" 
  compare="https://raw.githubusercontent.com/plotly/ssim_baselines/main/out_matlab/matlab/code-examples/data-distribution-plots/histogram/plot_2_1_change_number_of_histogram_bins_montage.png" 
  index=78
%}


<pre class="codeoutput">Nbins = 29
</pre>


Adjust the bins at a fine grain level by explicitly setting the number of bins.

<pre class="mcode">
h.NumBins = 31;

fig2plotly()
</pre>

{% capture plot_2_2_change_number_of_histogram_bins_79 %}
  {% raw %}{"data":[{"name":"X","type":"bar","x":[-3.095,-2.885,-2.675,-2.465,-2.255,-2.045,-1.835,-1.625,-1.415,-1.205,-0.995,-0.785,-0.575,-0.365,-0.155,0.0549999999999997,0.265,0.475,0.685,0.895,1.105,1.315,1.525,1.735,1.945,2.155,2.365,2.575,2.785,2.995,3.205],"y":[2,1,3,4,5,9,15,29,37,39,55,67,73,87,71,66,88,70,69,55,54,37,19,21,11,5,2,3,0,1,2],"xaxis":"x1","yaxis":"y1","marker":{"line":{"color":"rgb(0,0,0)","width":0.5}},"opacity":0.75,"visible":true,"width":[0.21,0.21,0.21,0.21,0.21,0.21,0.21,0.21,0.21,0.21,0.21,0.21,0.21,0.21,0.21,0.21,0.21,0.21,0.21,0.21,0.21,0.21,0.21,0.21,0.21,0.21,0.21,0.21,0.21,0.21,0.21],"showlegend":true}],"layout":{"title":"","width":840,"height":630,"margin":{"b":0,"l":0,"r":0,"t":80,"pad":0},"scene1":{"domain":{"x":[0.13,0.905],"y":[0.11,0.925]}},"xaxis1":{"side":"bottom","type":"linear","range":[-3.5255,3.6355],"ticks":"inside","anchor":"y1","domain":[0.13,0.905],"mirror":"ticks","nticks":8,"ticklen":6.51,"autotick":true,"showgrid":false,"showline":true,"tickfont":{"size":10,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"zeroline":false,"autorange":false,"gridcolor":"rgb(38.25,38.25,38.25)","gridwidth":1,"linecolor":"rgb(38.25,38.25,38.25)","linewidth":1,"tickcolor":"rgb(38.25,38.25,38.25)","tickwidth":1,"titlefont":{"size":11,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"exponentformat":"none"},"yaxis1":{"side":"left","type":"linear","range":[0,90],"ticks":"inside","anchor":"x1","domain":[0.11,0.925],"mirror":"ticks","nticks":11,"ticklen":6.51,"autotick":true,"showgrid":false,"showline":true,"tickfont":{"size":10,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"zeroline":false,"autorange":false,"gridcolor":"rgb(38.25,38.25,38.25)","gridwidth":1,"linecolor":"rgb(38.25,38.25,38.25)","linewidth":1,"tickcolor":"rgb(38.25,38.25,38.25)","tickwidth":1,"titlefont":{"size":11,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"exponentformat":"none"},"barmode":"group","autosize":false,"hovermode":"closest","titlefont":{"size":11,"color":"rgb(0,0,0)","family":"Arial,sans-serif"},"showlegend":false,"annotations":[],"paper_bgcolor":"rgb(255,255,255)"},"frames":[]}{% endraw %}
{% endcapture %}
{% include posts/ssim_frame.html 
  raw_json_file=plot_2_2_change_number_of_histogram_bins_79
  ssim="https://raw.githubusercontent.com/plotly/ssim_baselines/main/out_matlab/matlab/code-examples/data-distribution-plots/histogram/plot_2_2_change_number_of_histogram_bins_ssim_map.png" 
  compare="https://raw.githubusercontent.com/plotly/ssim_baselines/main/out_matlab/matlab/code-examples/data-distribution-plots/histogram/plot_2_2_change_number_of_histogram_bins_montage.png" 
  index=79
%}



<!--------------------- EXAMPLE BREAK ------------------------->

## Specify Bin Edges of Histogram

Generate 1,000 random numbers and create a histogram. Specify the bin edges as a vector with wide bins on the edges of the histogram to capture the outliers that do not satisfy |x|<2. The first vector element is the left edge of the first bin, and the last vector element is the right edge of the last bin.

<pre class="mcode">
x = randn(1000,1);
edges = [-10 -2:0.25:2 10];
h = histogram(x,edges);

fig2plotly()
</pre>

{% capture plot_3_0_specify_bin_edges_of_histogram_80 %}
  {% raw %}{"data":[{"name":"x","type":"bar","x":[-6,-1.875,-1.625,-1.375,-1.125,-0.875,-0.625,-0.375,-0.125,0.125,0.375,0.625,0.875,1.125,1.375,1.625,1.875,6],"y":[21,19,20,45,54,64,81,93,105,110,95,80,67,42,37,30,15,22],"xaxis":"x1","yaxis":"y1","marker":{"line":{"color":"rgb(0,0,0)","width":0.5}},"opacity":0.75,"visible":true,"width":[8,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,8],"showlegend":true}],"layout":{"title":"","width":840,"height":630,"margin":{"b":0,"l":0,"r":0,"t":80,"pad":0},"scene1":{"domain":{"x":[0.13,0.905],"y":[0.11,0.925]}},"xaxis1":{"side":"bottom","type":"linear","range":[-11,11],"ticks":"inside","anchor":"y1","domain":[0.13,0.905],"mirror":"ticks","nticks":12,"ticklen":6.51,"autotick":true,"showgrid":false,"showline":true,"tickfont":{"size":10,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"zeroline":false,"autorange":false,"gridcolor":"rgb(38.25,38.25,38.25)","gridwidth":1,"linecolor":"rgb(38.25,38.25,38.25)","linewidth":1,"tickcolor":"rgb(38.25,38.25,38.25)","tickwidth":1,"titlefont":{"size":11,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"exponentformat":"none"},"yaxis1":{"side":"left","type":"linear","range":[0,120],"ticks":"inside","anchor":"x1","domain":[0.11,0.925],"mirror":"ticks","nticks":8,"ticklen":6.51,"autotick":true,"showgrid":false,"showline":true,"tickfont":{"size":10,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"zeroline":false,"autorange":false,"gridcolor":"rgb(38.25,38.25,38.25)","gridwidth":1,"linecolor":"rgb(38.25,38.25,38.25)","linewidth":1,"tickcolor":"rgb(38.25,38.25,38.25)","tickwidth":1,"titlefont":{"size":11,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"exponentformat":"none"},"barmode":"group","autosize":false,"hovermode":"closest","titlefont":{"size":11,"color":"rgb(0,0,0)","family":"Arial,sans-serif"},"showlegend":false,"annotations":[],"paper_bgcolor":"rgb(255,255,255)"},"frames":[]}{% endraw %}
{% endcapture %}
{% include posts/ssim_frame.html 
  raw_json_file=plot_3_0_specify_bin_edges_of_histogram_80
  ssim="https://raw.githubusercontent.com/plotly/ssim_baselines/main/out_matlab/matlab/code-examples/data-distribution-plots/histogram/plot_3_0_specify_bin_edges_of_histogram_ssim_map.png" 
  compare="https://raw.githubusercontent.com/plotly/ssim_baselines/main/out_matlab/matlab/code-examples/data-distribution-plots/histogram/plot_3_0_specify_bin_edges_of_histogram_montage.png" 
  index=80
%}

Specify the `Normalization` property as `'countdensity'` to flatten out the bins containing the outliers. Now, the area of each bin (rather than the height) represents the frequency of observations in that interval.

<pre class="mcode">
h.Normalization = 'countdensity';

fig2plotly()
</pre>

{% capture plot_3_1_specify_bin_edges_of_histogram_81 %}
  {% raw %}{"data":[{"name":"x","type":"bar","x":[-6,-1.875,-1.625,-1.375,-1.125,-0.875,-0.625,-0.375,-0.125,0.125,0.375,0.625,0.875,1.125,1.375,1.625,1.875,6],"y":[2.625,60,124,124,204,296,376,388,348,344,360,384,300,232,132,120,64,1.875],"xaxis":"x1","yaxis":"y1","marker":{"line":{"color":"rgb(0,0,0)","width":0.5}},"opacity":0.75,"visible":true,"width":[8,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,8],"showlegend":true}],"layout":{"title":"","width":840,"height":630,"margin":{"b":0,"l":0,"r":0,"t":80,"pad":0},"scene1":{"domain":{"x":[0.13,0.905],"y":[0.11,0.925]}},"xaxis1":{"side":"bottom","type":"linear","range":[-11,11],"ticks":"inside","anchor":"y1","domain":[0.13,0.905],"mirror":"ticks","nticks":12,"ticklen":6.51,"autotick":true,"showgrid":false,"showline":true,"tickfont":{"size":10,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"zeroline":false,"autorange":false,"gridcolor":"rgb(38.25,38.25,38.25)","gridwidth":1,"linecolor":"rgb(38.25,38.25,38.25)","linewidth":1,"tickcolor":"rgb(38.25,38.25,38.25)","tickwidth":1,"titlefont":{"size":11,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"exponentformat":"none"},"yaxis1":{"side":"left","type":"linear","range":[0,400],"ticks":"inside","anchor":"x1","domain":[0.11,0.925],"mirror":"ticks","nticks":10,"ticklen":6.51,"autotick":true,"showgrid":false,"showline":true,"tickfont":{"size":10,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"zeroline":false,"autorange":false,"gridcolor":"rgb(38.25,38.25,38.25)","gridwidth":1,"linecolor":"rgb(38.25,38.25,38.25)","linewidth":1,"tickcolor":"rgb(38.25,38.25,38.25)","tickwidth":1,"titlefont":{"size":11,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"exponentformat":"none"},"barmode":"group","autosize":false,"hovermode":"closest","titlefont":{"size":11,"color":"rgb(0,0,0)","family":"Arial,sans-serif"},"showlegend":false,"annotations":[],"paper_bgcolor":"rgb(255,255,255)"},"frames":[]}{% endraw %}
{% endcapture %}
{% include posts/ssim_frame.html 
  raw_json_file=plot_3_1_specify_bin_edges_of_histogram_81
  ssim="https://raw.githubusercontent.com/plotly/ssim_baselines/main/out_matlab/matlab/code-examples/data-distribution-plots/histogram/plot_3_1_specify_bin_edges_of_histogram_ssim_map.png" 
  compare="https://raw.githubusercontent.com/plotly/ssim_baselines/main/out_matlab/matlab/code-examples/data-distribution-plots/histogram/plot_3_1_specify_bin_edges_of_histogram_montage.png" 
  index=81
%}



<!--------------------- EXAMPLE BREAK ------------------------->

## Plot Categorical Histogram

Create a categorical vector that represents votes. The categories in the vector are `'yes'`, `'no'`, or `'undecided'`.

<pre class="mcode">
A = [0 0 1 1 1 0 0 0 0 NaN NaN 1 0 0 0 1 0 1 0 1 0 0 0 1 1 1 1];
C = categorical(A,[1 0 NaN],{'yes','no','undecided'})
</pre>


<pre class="codeoutput">C = <span class="emphasis"><em>1x27 categorical</em></span>
  Columns 1 through 9

     no      no      yes      yes      yes      no      no      no      no 

  Columns 10 through 16

     undecided      undecided      yes      no      no      no      yes 

  Columns 17 through 25

     no      yes      no      yes      no      no      no      yes      yes 

  Columns 26 through 27

     yes      yes 

</pre>


Plot a categorical histogram of the votes, using a relative bar width of `0.5`.

<pre class="mcode">
h = histogram(C,'BarWidth',0.5)

fig2plotly()
</pre>

{% capture plot_4_0_plot_categorical_histogram_82 %}
  {% raw %}{"data":[{"name":"","type":"bar","x":["yes","no","undecided"],"y":[11,14,2],"width":0.5,"xaxis":"x1","yaxis":"y1","marker":{"line":{"color":"rgb(0,0,0)","width":0.5},"color":"rgb(0,113.985,188.955)"},"opacity":0.75,"visible":true,"showlegend":true}],"layout":{"title":"","width":840,"height":630,"margin":{"b":0,"l":0,"r":0,"t":80,"pad":0},"scene1":{"domain":{"x":[0.13,0.905],"y":[0.11,0.925]}},"xaxis1":{"side":"bottom","type":"category","range":[-0.5,2.5],"ticks":"inside","anchor":"y1","domain":[0.13,0.905],"mirror":"ticks","nticks":4,"ticklen":6.51,"autotick":true,"showgrid":false,"showline":true,"tickfont":{"size":10,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"zeroline":false,"autorange":false,"gridcolor":"rgb(38.25,38.25,38.25)","gridwidth":1,"linecolor":"rgb(38.25,38.25,38.25)","linewidth":1,"tickcolor":"rgb(38.25,38.25,38.25)","tickwidth":1,"titlefont":{"size":11,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"exponentformat":"none"},"yaxis1":{"side":"left","type":"linear","range":[0,14],"ticks":"inside","anchor":"x1","domain":[0.11,0.925],"mirror":"ticks","nticks":9,"ticklen":6.51,"autotick":true,"showgrid":false,"showline":true,"tickfont":{"size":10,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"zeroline":false,"autorange":false,"gridcolor":"rgb(38.25,38.25,38.25)","gridwidth":1,"linecolor":"rgb(38.25,38.25,38.25)","linewidth":1,"tickcolor":"rgb(38.25,38.25,38.25)","tickwidth":1,"titlefont":{"size":11,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"exponentformat":"none"},"barmode":"group","autosize":false,"hovermode":"closest","titlefont":{"size":11,"color":"rgb(0,0,0)","family":"Arial,sans-serif"},"showlegend":false,"annotations":[],"paper_bgcolor":"rgb(255,255,255)"},"frames":[]}{% endraw %}
{% endcapture %}
{% include posts/ssim_frame.html 
  raw_json_file=plot_4_0_plot_categorical_histogram_82
  ssim="https://raw.githubusercontent.com/plotly/ssim_baselines/main/out_matlab/matlab/code-examples/data-distribution-plots/histogram/plot_4_0_plot_categorical_histogram_ssim_map.png" 
  compare="https://raw.githubusercontent.com/plotly/ssim_baselines/main/out_matlab/matlab/code-examples/data-distribution-plots/histogram/plot_4_0_plot_categorical_histogram_montage.png" 
  index=82
%}


<pre class="codeoutput">h = 
  Histogram with properties:

              Data: [1x27 categorical]
            Values: [11 14 2]
    NumDisplayBins: 3
        Categories: {'yes'  'no'  'undecided'}
      DisplayOrder: 'data'
     Normalization: 'count'
      DisplayStyle: 'bar'
         FaceColor: 'auto'
         EdgeColor: [0 0 0]

  Show all properties

</pre>




<!--------------------- EXAMPLE BREAK ------------------------->

## Histogram with Specified Normalization

Generate 1,000 random numbers and create a histogram using the `'probability'` normalization.

<pre class="mcode">
x = randn(1000,1);
h = histogram(x,'Normalization','probability')

fig2plotly()
</pre>

{% capture plot_5_0_histogram_with_specified_normalization_83 %}
  {% raw %}{"data":[{"name":"x","type":"bar","x":[-3.15,-2.85,-2.55,-2.25,-1.95,-1.65,-1.35,-1.05,-0.75,-0.45,-0.15,0.15,0.45,0.75,1.05,1.35,1.65,1.95,2.25,2.55,2.85,3.15,3.45],"y":[0.001,0,0.003,0.012,0.025,0.024,0.056,0.075,0.091,0.116,0.115,0.105,0.116,0.085,0.064,0.045,0.034,0.017,0.008,0.003,0.003,0,0.002],"xaxis":"x1","yaxis":"y1","marker":{"line":{"color":"rgb(0,0,0)","width":0.5}},"opacity":0.75,"visible":true,"width":[0.3,0.3,0.3,0.3,0.3,0.3,0.3,0.3,0.3,0.3,0.3,0.3,0.3,0.300000000000001,0.3,0.3,0.3,0.3,0.300000000000001,0.3,0.3,0.300000000000001,0.3],"showlegend":true}],"layout":{"title":"","width":840,"height":630,"margin":{"b":0,"l":0,"r":0,"t":80,"pad":0},"scene1":{"domain":{"x":[0.13,0.905],"y":[0.11,0.925]}},"xaxis1":{"side":"bottom","type":"linear","range":[-3.645,3.945],"ticks":"inside","anchor":"y1","domain":[0.13,0.905],"mirror":"ticks","nticks":8,"ticklen":6.51,"autotick":true,"showgrid":false,"showline":true,"tickfont":{"size":10,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"zeroline":false,"autorange":false,"gridcolor":"rgb(38.25,38.25,38.25)","gridwidth":1,"linecolor":"rgb(38.25,38.25,38.25)","linewidth":1,"tickcolor":"rgb(38.25,38.25,38.25)","tickwidth":1,"titlefont":{"size":11,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"exponentformat":"none"},"yaxis1":{"side":"left","type":"linear","range":[0,0.12],"ticks":"inside","anchor":"x1","domain":[0.11,0.925],"mirror":"ticks","nticks":8,"ticklen":6.51,"autotick":true,"showgrid":false,"showline":true,"tickfont":{"size":10,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"zeroline":false,"autorange":false,"gridcolor":"rgb(38.25,38.25,38.25)","gridwidth":1,"linecolor":"rgb(38.25,38.25,38.25)","linewidth":1,"tickcolor":"rgb(38.25,38.25,38.25)","tickwidth":1,"titlefont":{"size":11,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"exponentformat":"none"},"barmode":"group","autosize":false,"hovermode":"closest","titlefont":{"size":11,"color":"rgb(0,0,0)","family":"Arial,sans-serif"},"showlegend":false,"annotations":[],"paper_bgcolor":"rgb(255,255,255)"},"frames":[]}{% endraw %}
{% endcapture %}
{% include posts/ssim_frame.html 
  raw_json_file=plot_5_0_histogram_with_specified_normalization_83
  ssim="https://raw.githubusercontent.com/plotly/ssim_baselines/main/out_matlab/matlab/code-examples/data-distribution-plots/histogram/plot_5_0_histogram_with_specified_normalization_ssim_map.png" 
  compare="https://raw.githubusercontent.com/plotly/ssim_baselines/main/out_matlab/matlab/code-examples/data-distribution-plots/histogram/plot_5_0_histogram_with_specified_normalization_montage.png" 
  index=83
%}


<pre class="codeoutput">h = 
  Histogram with properties:

             Data: [1000x1 double]
           Values: [1x23 double]
          NumBins: 23
         BinEdges: [1x24 double]
         BinWidth: 0.3000
        BinLimits: [-3.3000 3.6000]
    Normalization: 'probability'
        FaceColor: 'auto'
        EdgeColor: [0 0 0]

  Show all properties

</pre>


Compute the sum of the bar heights. With this normalization, the height of each bar is equal to the probability of selecting an observation within that bin interval, and the height of all of the bars sums to 1.

<pre class="mcode">
S = sum(h.Values)

fig2plotly()
</pre>


<pre class="codeoutput">S = 1
</pre>




<!--------------------- EXAMPLE BREAK ------------------------->

## Plot Multiple Histograms

Generate two vectors of random numbers and plot a histogram for each vector in the same figure. 

<pre class="mcode">
x = randn(2000,1);
y = 1 + randn(5000,1);
h1 = histogram(x);
hold on
h2 = histogram(y);

fig2plotly()
</pre>

{% capture plot_6_0_plot_multiple_histograms_85 %}
  {% raw %}{"data":[{"name":"x","type":"bar","x":[-3.15,-2.85,-2.55,-2.25,-1.95,-1.65,-1.35,-1.05,-0.75,-0.45,-0.15,0.15,0.45,0.75,1.05,1.35,1.65,1.95,2.25,2.55,2.85,3.15,3.45],"y":[1,4,9,21,28,54,99,116,184,204,231,261,214,199,143,94,64,42,20,6,2,1,3],"xaxis":"x1","yaxis":"y1","marker":{"line":{"color":"rgb(0,0,0)","width":0.5}},"opacity":0.75,"visible":true,"width":[0.3,0.3,0.3,0.3,0.3,0.3,0.3,0.3,0.3,0.3,0.3,0.3,0.3,0.300000000000001,0.3,0.3,0.3,0.3,0.300000000000001,0.3,0.3,0.300000000000001,0.3],"showlegend":true},{"name":"y","type":"bar","x":[-2.3,-2.1,-1.9,-1.7,-1.5,-1.3,-1.1,-0.9,-0.7,-0.5,-0.3,-0.1,0.0999999999999999,0.3,0.5,0.7,0.9,1.1,1.3,1.5,1.7,1.9,2.1,2.3,2.5,2.7,2.9,3.1,3.3,3.5,3.7,3.9,4.1,4.3],"y":[1,3,4,12,18,29,33,56,88,132,195,210,256,284,385,376,401,401,397,327,322,281,240,168,121,107,59,41,23,15,11,1,1,2],"xaxis":"x1","yaxis":"y1","marker":{"line":{"color":"rgb(0,0,0)","width":0.5}},"opacity":0.75,"visible":true,"width":[0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.199999999999999,0.2,0.2,0.2,0.2,0.199999999999999,0.2,0.2,0.2,0.2],"showlegend":true}],"layout":{"title":"","width":840,"height":630,"margin":{"b":0,"l":0,"r":0,"t":0,"pad":0},"scene1":{"domain":{"x":[0.13,0.905],"y":[0.11,0.925]}},"xaxis1":{"side":"bottom","type":"linear","range":[-3.685,4.785],"ticks":"inside","anchor":"y1","domain":[0.13,0.905],"mirror":"ticks","nticks":9,"ticklen":6.51,"autotick":true,"showgrid":false,"showline":true,"tickfont":{"size":10,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"zeroline":false,"autorange":false,"gridcolor":"rgb(38.25,38.25,38.25)","gridwidth":1,"linecolor":"rgb(38.25,38.25,38.25)","linewidth":1,"tickcolor":"rgb(38.25,38.25,38.25)","tickwidth":1,"titlefont":{"size":11,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"exponentformat":"none"},"yaxis1":{"side":"left","type":"linear","range":[0,450],"ticks":"inside","anchor":"x1","domain":[0.11,0.925],"mirror":"ticks","nticks":11,"ticklen":6.51,"autotick":true,"showgrid":false,"showline":true,"tickfont":{"size":10,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"zeroline":false,"autorange":false,"gridcolor":"rgb(38.25,38.25,38.25)","gridwidth":1,"linecolor":"rgb(38.25,38.25,38.25)","linewidth":1,"tickcolor":"rgb(38.25,38.25,38.25)","tickwidth":1,"titlefont":{"size":11,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"exponentformat":"none"},"barmode":"group","autosize":false,"hovermode":"closest","titlefont":{"color":"rgba(0,0,0,0)"},"showlegend":false,"annotations":[{"x":0.5175,"y":0.935,"font":{"size":11,"color":"rgb(0,0,0)","family":"Arial,sans-serif"},"text":"","xref":"paper","yref":"paper","align":"center","xanchor":"center","yanchor":"bottom","borderpad":3,"showarrow":false,"textangle":0,"bordercolor":"rgba(0,0,0,0)","borderwidth":0.5}],"paper_bgcolor":"rgb(255,255,255)"},"frames":[]}{% endraw %}
{% endcapture %}
{% include posts/ssim_frame.html 
  raw_json_file=plot_6_0_plot_multiple_histograms_85
  ssim="https://raw.githubusercontent.com/plotly/ssim_baselines/main/out_matlab/matlab/code-examples/data-distribution-plots/histogram/plot_6_0_plot_multiple_histograms_ssim_map.png" 
  compare="https://raw.githubusercontent.com/plotly/ssim_baselines/main/out_matlab/matlab/code-examples/data-distribution-plots/histogram/plot_6_0_plot_multiple_histograms_montage.png" 
  index=85
%}

Since the sample size and bin width of the histograms are different, it is difficult to compare them. Normalize the histograms so that all of the bar heights add to 1, and use a uniform bin width.

<pre class="mcode">
h1.Normalization = 'probability';
h1.BinWidth = 0.25;
h2.Normalization = 'probability';
h2.BinWidth = 0.25;

fig2plotly()
</pre>

{% capture plot_6_1_plot_multiple_histograms_86 %}
  {% raw %}{"data":[{"name":"x","type":"bar","x":[-3.125,-2.875,-2.625,-2.375,-2.125,-1.875,-1.625,-1.375,-1.125,-0.875,-0.625,-0.375,-0.125,0.125,0.375,0.625,0.875,1.125,1.375,1.625,1.875,2.125,2.375,2.625,2.875,3.125],"y":[0.0015,0.001,0.0045,0.007,0.007,0.016,0.034,0.0305,0.049,0.0575,0.0785,0.11,0.097,0.0945,0.094,0.092,0.075,0.049,0.0385,0.0275,0.017,0.011,0.003,0.0025,0.0005,0.002],"xaxis":"x1","yaxis":"y1","marker":{"line":{"color":"rgb(0,0,0)","width":0.5}},"opacity":0.75,"visible":true,"width":[0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25],"showlegend":true},{"name":"y","type":"bar","x":[-3.125,-2.875,-2.625,-2.375,-2.125,-1.875,-1.625,-1.375,-1.125,-0.875,-0.625,-0.375,-0.125,0.125,0.375,0.625,0.875,1.125,1.375,1.625,1.875,2.125,2.375,2.625,2.875,3.125,3.375,3.625,3.875,4.125,4.375,4.625,4.875,5.125,5.375],"y":[0.0002,0,0.0006,0.0004,0.0014,0.0014,0.0032,0.0044,0.0118,0.0178,0.0276,0.0376,0.0586,0.0756,0.0766,0.0954,0.096,0.1014,0.0876,0.0756,0.069,0.0566,0.0322,0.0268,0.0146,0.013,0.0074,0.0024,0.0026,0.0012,0.0006,0.0002,0,0,0.0002],"xaxis":"x1","yaxis":"y1","marker":{"line":{"color":"rgb(0,0,0)","width":0.5}},"opacity":0.75,"visible":true,"width":[0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25,0.25],"showlegend":true}],"layout":{"title":"","width":840,"height":630,"margin":{"b":0,"l":0,"r":0,"t":0,"pad":0},"scene1":{"domain":{"x":[0.13,0.905],"y":[0.11,0.925]}},"xaxis1":{"side":"bottom","type":"linear","range":[-3.6875,5.9375],"ticks":"inside","anchor":"y1","domain":[0.13,0.905],"mirror":"ticks","nticks":10,"ticklen":6.51,"autotick":true,"showgrid":false,"showline":true,"tickfont":{"size":10,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"zeroline":false,"autorange":false,"gridcolor":"rgb(38.25,38.25,38.25)","gridwidth":1,"linecolor":"rgb(38.25,38.25,38.25)","linewidth":1,"tickcolor":"rgb(38.25,38.25,38.25)","tickwidth":1,"titlefont":{"size":11,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"exponentformat":"none"},"yaxis1":{"side":"left","type":"linear","range":[0,0.12],"ticks":"inside","anchor":"x1","domain":[0.11,0.925],"mirror":"ticks","nticks":8,"ticklen":6.51,"autotick":true,"showgrid":false,"showline":true,"tickfont":{"size":10,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"zeroline":false,"autorange":false,"gridcolor":"rgb(38.25,38.25,38.25)","gridwidth":1,"linecolor":"rgb(38.25,38.25,38.25)","linewidth":1,"tickcolor":"rgb(38.25,38.25,38.25)","tickwidth":1,"titlefont":{"size":11,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"exponentformat":"none"},"barmode":"group","autosize":false,"hovermode":"closest","titlefont":{"color":"rgba(0,0,0,0)"},"showlegend":false,"annotations":[{"x":0.5175,"y":0.935,"font":{"size":11,"color":"rgb(0,0,0)","family":"Arial,sans-serif"},"text":"","xref":"paper","yref":"paper","align":"center","xanchor":"center","yanchor":"bottom","borderpad":3,"showarrow":false,"textangle":0,"bordercolor":"rgba(0,0,0,0)","borderwidth":0.5}],"paper_bgcolor":"rgb(255,255,255)"},"frames":[]}{% endraw %}
{% endcapture %}
{% include posts/ssim_frame.html 
  raw_json_file=plot_6_1_plot_multiple_histograms_86
  ssim="https://raw.githubusercontent.com/plotly/ssim_baselines/main/out_matlab/matlab/code-examples/data-distribution-plots/histogram/plot_6_1_plot_multiple_histograms_ssim_map.png" 
  compare="https://raw.githubusercontent.com/plotly/ssim_baselines/main/out_matlab/matlab/code-examples/data-distribution-plots/histogram/plot_6_1_plot_multiple_histograms_montage.png" 
  index=86
%}



<!--------------------- EXAMPLE BREAK ------------------------->

## Adjust Histogram Properties

Generate 1,000 random numbers and create a histogram. Return the histogram object to adjust the properties of the histogram without recreating the entire plot.

<pre class="mcode">
x = randn(1000,1);
h = histogram(x)

fig2plotly()
</pre>

{% capture plot_7_0_adjust_histogram_properties_87 %}
  {% raw %}{"data":[{"name":"x","type":"bar","x":[-3.15,-2.85,-2.55,-2.25,-1.95,-1.65,-1.35,-1.05,-0.75,-0.45,-0.15,0.15,0.45,0.75,1.05,1.35,1.65,1.95,2.25,2.55],"y":[1,1,8,15,23,45,49,68,71,104,120,123,110,89,59,50,27,18,16,3],"xaxis":"x1","yaxis":"y1","marker":{"line":{"color":"rgb(0,0,0)","width":0.5}},"opacity":0.75,"visible":true,"width":[0.3,0.3,0.3,0.3,0.3,0.3,0.3,0.3,0.3,0.3,0.3,0.3,0.3,0.300000000000001,0.3,0.3,0.3,0.3,0.300000000000001,0.3],"showlegend":true}],"layout":{"title":"","width":840,"height":630,"margin":{"b":0,"l":0,"r":0,"t":80,"pad":0},"scene1":{"domain":{"x":[0.13,0.905],"y":[0.11,0.925]}},"xaxis1":{"side":"bottom","type":"linear","range":[-3.6,3],"ticks":"inside","anchor":"y1","domain":[0.13,0.905],"mirror":"ticks","nticks":8,"ticklen":6.51,"autotick":true,"showgrid":false,"showline":true,"tickfont":{"size":10,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"zeroline":false,"autorange":false,"gridcolor":"rgb(38.25,38.25,38.25)","gridwidth":1,"linecolor":"rgb(38.25,38.25,38.25)","linewidth":1,"tickcolor":"rgb(38.25,38.25,38.25)","tickwidth":1,"titlefont":{"size":11,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"exponentformat":"none"},"yaxis1":{"side":"left","type":"linear","range":[0,140],"ticks":"inside","anchor":"x1","domain":[0.11,0.925],"mirror":"ticks","nticks":9,"ticklen":6.51,"autotick":true,"showgrid":false,"showline":true,"tickfont":{"size":10,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"zeroline":false,"autorange":false,"gridcolor":"rgb(38.25,38.25,38.25)","gridwidth":1,"linecolor":"rgb(38.25,38.25,38.25)","linewidth":1,"tickcolor":"rgb(38.25,38.25,38.25)","tickwidth":1,"titlefont":{"size":11,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"exponentformat":"none"},"barmode":"group","autosize":false,"hovermode":"closest","titlefont":{"size":11,"color":"rgb(0,0,0)","family":"Arial,sans-serif"},"showlegend":false,"annotations":[],"paper_bgcolor":"rgb(255,255,255)"},"frames":[]}{% endraw %}
{% endcapture %}
{% include posts/ssim_frame.html 
  raw_json_file=plot_7_0_adjust_histogram_properties_87
  ssim="https://raw.githubusercontent.com/plotly/ssim_baselines/main/out_matlab/matlab/code-examples/data-distribution-plots/histogram/plot_7_0_adjust_histogram_properties_ssim_map.png" 
  compare="https://raw.githubusercontent.com/plotly/ssim_baselines/main/out_matlab/matlab/code-examples/data-distribution-plots/histogram/plot_7_0_adjust_histogram_properties_montage.png" 
  index=87
%}


<pre class="codeoutput">h = 
  Histogram with properties:

             Data: [1000x1 double]
           Values: [1x23 double]
          NumBins: 23
         BinEdges: [1x24 double]
         BinWidth: 0.3000
        BinLimits: [-3.3000 3.6000]
    Normalization: 'count'
        FaceColor: 'auto'
        EdgeColor: [0 0 0]

  Show all properties

</pre>


Specify exactly how many bins to use.

<pre class="mcode">
h.NumBins = 15;

fig2plotly()
</pre>

{% capture plot_7_1_adjust_histogram_properties_88 %}
  {% raw %}{"data":[{"name":"x","type":"bar","x":[-2.985,-2.555,-2.125,-1.695,-1.265,-0.835,-0.405,0.0249999999999997,0.455,0.885,1.315,1.745,2.175,2.605,3.035],"y":[3,7,12,50,94,108,151,184,165,93,70,34,18,10,1],"xaxis":"x1","yaxis":"y1","marker":{"line":{"color":"rgb(0,0,0)","width":0.5}},"opacity":0.75,"visible":true,"width":[0.43,0.43,0.43,0.43,0.43,0.43,0.43,0.43,0.43,0.43,0.43,0.430000000000001,0.43,0.43,0.430000000000001],"showlegend":true}],"layout":{"title":"","width":840,"height":630,"margin":{"b":0,"l":0,"r":0,"t":80,"pad":0},"scene1":{"domain":{"x":[0.13,0.905],"y":[0.11,0.925]}},"xaxis1":{"side":"bottom","type":"linear","range":[-3.5225,3.5725],"ticks":"inside","anchor":"y1","domain":[0.13,0.905],"mirror":"ticks","nticks":8,"ticklen":6.51,"autotick":true,"showgrid":false,"showline":true,"tickfont":{"size":10,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"zeroline":false,"autorange":false,"gridcolor":"rgb(38.25,38.25,38.25)","gridwidth":1,"linecolor":"rgb(38.25,38.25,38.25)","linewidth":1,"tickcolor":"rgb(38.25,38.25,38.25)","tickwidth":1,"titlefont":{"size":11,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"exponentformat":"none"},"yaxis1":{"side":"left","type":"linear","range":[0,200],"ticks":"inside","anchor":"x1","domain":[0.11,0.925],"mirror":"ticks","nticks":12,"ticklen":6.51,"autotick":true,"showgrid":false,"showline":true,"tickfont":{"size":10,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"zeroline":false,"autorange":false,"gridcolor":"rgb(38.25,38.25,38.25)","gridwidth":1,"linecolor":"rgb(38.25,38.25,38.25)","linewidth":1,"tickcolor":"rgb(38.25,38.25,38.25)","tickwidth":1,"titlefont":{"size":11,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"exponentformat":"none"},"barmode":"group","autosize":false,"hovermode":"closest","titlefont":{"size":11,"color":"rgb(0,0,0)","family":"Arial,sans-serif"},"showlegend":false,"annotations":[],"paper_bgcolor":"rgb(255,255,255)"},"frames":[]}{% endraw %}
{% endcapture %}
{% include posts/ssim_frame.html 
  raw_json_file=plot_7_1_adjust_histogram_properties_88
  ssim="https://raw.githubusercontent.com/plotly/ssim_baselines/main/out_matlab/matlab/code-examples/data-distribution-plots/histogram/plot_7_1_adjust_histogram_properties_ssim_map.png" 
  compare="https://raw.githubusercontent.com/plotly/ssim_baselines/main/out_matlab/matlab/code-examples/data-distribution-plots/histogram/plot_7_1_adjust_histogram_properties_montage.png" 
  index=88
%}

Specify the edges of the bins with a vector. The first value in the vector is the left edge of the first bin. The last value is the right edge of the last bin.

<pre class="mcode">
h.BinEdges = [-3:3];

fig2plotly()
</pre>

{% capture plot_7_2_adjust_histogram_properties_89 %}
  {% raw %}{"data":[{"name":"x","type":"bar","x":[-2.5,-1.5,-0.5,0.5,1.5,2.5],"y":[22,134,324,357,137,23],"xaxis":"x1","yaxis":"y1","marker":{"line":{"color":"rgb(0,0,0)","width":0.5}},"opacity":0.75,"visible":true,"width":[1,1,1,1,1,1],"showlegend":true}],"layout":{"title":"","width":840,"height":630,"margin":{"b":0,"l":0,"r":0,"t":80,"pad":0},"scene1":{"domain":{"x":[0.13,0.905],"y":[0.11,0.925]}},"xaxis1":{"side":"bottom","type":"linear","range":[-3.3,3.3],"ticks":"inside","anchor":"y1","domain":[0.13,0.905],"mirror":"ticks","nticks":8,"ticklen":6.51,"autotick":true,"showgrid":false,"showline":true,"tickfont":{"size":10,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"zeroline":false,"autorange":false,"gridcolor":"rgb(38.25,38.25,38.25)","gridwidth":1,"linecolor":"rgb(38.25,38.25,38.25)","linewidth":1,"tickcolor":"rgb(38.25,38.25,38.25)","tickwidth":1,"titlefont":{"size":11,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"exponentformat":"none"},"yaxis1":{"side":"left","type":"linear","range":[0,400],"ticks":"inside","anchor":"x1","domain":[0.11,0.925],"mirror":"ticks","nticks":10,"ticklen":6.51,"autotick":true,"showgrid":false,"showline":true,"tickfont":{"size":10,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"zeroline":false,"autorange":false,"gridcolor":"rgb(38.25,38.25,38.25)","gridwidth":1,"linecolor":"rgb(38.25,38.25,38.25)","linewidth":1,"tickcolor":"rgb(38.25,38.25,38.25)","tickwidth":1,"titlefont":{"size":11,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"exponentformat":"none"},"barmode":"group","autosize":false,"hovermode":"closest","titlefont":{"size":11,"color":"rgb(0,0,0)","family":"Arial,sans-serif"},"showlegend":false,"annotations":[],"paper_bgcolor":"rgb(255,255,255)"},"frames":[]}{% endraw %}
{% endcapture %}
{% include posts/ssim_frame.html 
  raw_json_file=plot_7_2_adjust_histogram_properties_89
  ssim="https://raw.githubusercontent.com/plotly/ssim_baselines/main/out_matlab/matlab/code-examples/data-distribution-plots/histogram/plot_7_2_adjust_histogram_properties_ssim_map.png" 
  compare="https://raw.githubusercontent.com/plotly/ssim_baselines/main/out_matlab/matlab/code-examples/data-distribution-plots/histogram/plot_7_2_adjust_histogram_properties_montage.png" 
  index=89
%}

Change the color of the histogram bars.

<pre class="mcode">
h.FaceColor = [0 0.5 0.5];
h.EdgeColor = 'r';

fig2plotly()
</pre>

{% capture plot_7_3_adjust_histogram_properties_90 %}
  {% raw %}{"data":[{"name":"x","type":"bar","x":[-2.5,-1.5,-0.5,0.5,1.5,2.5],"y":[23,158,333,319,137,26],"xaxis":"x1","yaxis":"y1","marker":{"line":{"color":"rgb(255,0,0)","width":0.5}},"opacity":0.75,"visible":true,"width":[1,1,1,1,1,1],"showlegend":true}],"layout":{"title":"","width":840,"height":630,"margin":{"b":0,"l":0,"r":0,"t":80,"pad":0},"scene1":{"domain":{"x":[0.13,0.905],"y":[0.11,0.925]}},"xaxis1":{"side":"bottom","type":"linear","range":[-3.3,3.3],"ticks":"inside","anchor":"y1","domain":[0.13,0.905],"mirror":"ticks","nticks":8,"ticklen":6.51,"autotick":true,"showgrid":false,"showline":true,"tickfont":{"size":10,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"zeroline":false,"autorange":false,"gridcolor":"rgb(38.25,38.25,38.25)","gridwidth":1,"linecolor":"rgb(38.25,38.25,38.25)","linewidth":1,"tickcolor":"rgb(38.25,38.25,38.25)","tickwidth":1,"titlefont":{"size":11,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"exponentformat":"none"},"yaxis1":{"side":"left","type":"linear","range":[0,350],"ticks":"inside","anchor":"x1","domain":[0.11,0.925],"mirror":"ticks","nticks":9,"ticklen":6.51,"autotick":true,"showgrid":false,"showline":true,"tickfont":{"size":10,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"zeroline":false,"autorange":false,"gridcolor":"rgb(38.25,38.25,38.25)","gridwidth":1,"linecolor":"rgb(38.25,38.25,38.25)","linewidth":1,"tickcolor":"rgb(38.25,38.25,38.25)","tickwidth":1,"titlefont":{"size":11,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"exponentformat":"none"},"barmode":"group","autosize":false,"hovermode":"closest","titlefont":{"size":11,"color":"rgb(0,0,0)","family":"Arial,sans-serif"},"showlegend":false,"annotations":[],"paper_bgcolor":"rgb(255,255,255)"},"frames":[]}{% endraw %}
{% endcapture %}
{% include posts/ssim_frame.html 
  raw_json_file=plot_7_3_adjust_histogram_properties_90
  ssim="https://raw.githubusercontent.com/plotly/ssim_baselines/main/out_matlab/matlab/code-examples/data-distribution-plots/histogram/plot_7_3_adjust_histogram_properties_ssim_map.png" 
  compare="https://raw.githubusercontent.com/plotly/ssim_baselines/main/out_matlab/matlab/code-examples/data-distribution-plots/histogram/plot_7_3_adjust_histogram_properties_montage.png" 
  index=90
%}



<!--------------------- EXAMPLE BREAK ------------------------->

## Determine Underlying Probability Distribution

Generate 5,000 normally distributed random numbers with a mean of 5 and a standard deviation of 2. Plot a histogram with `Normalization` set to `'pdf'` to produce an estimation of the probability density function.

<pre class="mcode">
x = 2*randn(5000,1) + 5;
histogram(x,'Normalization','pdf')

fig2plotly()
</pre>

{% capture plot_8_0_determine_underlying_probability_distribution_91 %}
  {% raw %}{"data":[{"name":"x","type":"bar","x":[-1.75,-1.25,-0.75,-0.25,0.25,0.75,1.25,1.75,2.25,2.75,3.25,3.75,4.25,4.75,5.25,5.75,6.25,6.75,7.25,7.75,8.25,8.75,9.25,9.75,10.25,10.75,11.25,11.75,12.25,12.75],"y":[0.0008,0.0012,0.0024,0.0052,0.0132,0.0248,0.032,0.0544,0.0764,0.1088,0.1604,0.1556,0.1812,0.194,0.1928,0.1864,0.1644,0.1424,0.1012,0.07,0.0536,0.0376,0.0176,0.0116,0.0032,0.0044,0.0012,0.0024,0.0004,0.0004],"xaxis":"x1","yaxis":"y1","marker":{"line":{"color":"rgb(0,0,0)","width":0.5}},"opacity":0.75,"visible":true,"width":[0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5],"showlegend":true}],"layout":{"title":"","width":840,"height":630,"margin":{"b":0,"l":0,"r":0,"t":80,"pad":0},"scene1":{"domain":{"x":[0.13,0.905],"y":[0.11,0.925]}},"xaxis1":{"side":"bottom","type":"linear","range":[-2.75,13.75],"ticks":"inside","anchor":"y1","domain":[0.13,0.905],"mirror":"ticks","nticks":9,"ticklen":6.51,"autotick":true,"showgrid":false,"showline":true,"tickfont":{"size":10,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"zeroline":false,"autorange":false,"gridcolor":"rgb(38.25,38.25,38.25)","gridwidth":1,"linecolor":"rgb(38.25,38.25,38.25)","linewidth":1,"tickcolor":"rgb(38.25,38.25,38.25)","tickwidth":1,"titlefont":{"size":11,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"exponentformat":"none"},"yaxis1":{"side":"left","type":"linear","range":[0,0.2],"ticks":"inside","anchor":"x1","domain":[0.11,0.925],"mirror":"ticks","nticks":12,"ticklen":6.51,"autotick":true,"showgrid":false,"showline":true,"tickfont":{"size":10,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"zeroline":false,"autorange":false,"gridcolor":"rgb(38.25,38.25,38.25)","gridwidth":1,"linecolor":"rgb(38.25,38.25,38.25)","linewidth":1,"tickcolor":"rgb(38.25,38.25,38.25)","tickwidth":1,"titlefont":{"size":11,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"exponentformat":"none"},"barmode":"group","autosize":false,"hovermode":"closest","titlefont":{"size":11,"color":"rgb(0,0,0)","family":"Arial,sans-serif"},"showlegend":false,"annotations":[],"paper_bgcolor":"rgb(255,255,255)"},"frames":[]}{% endraw %}
{% endcapture %}
{% include posts/ssim_frame.html 
  raw_json_file=plot_8_0_determine_underlying_probability_distribution_91
  ssim="https://raw.githubusercontent.com/plotly/ssim_baselines/main/out_matlab/matlab/code-examples/data-distribution-plots/histogram/plot_8_0_determine_underlying_probability_distribution_ssim_map.png" 
  compare="https://raw.githubusercontent.com/plotly/ssim_baselines/main/out_matlab/matlab/code-examples/data-distribution-plots/histogram/plot_8_0_determine_underlying_probability_distribution_montage.png" 
  index=91
%}

In this example, the underlying distribution for the normally distributed data is known. You can, however, use the `'pdf'` histogram plot to determine the underlying probability distribution of the data by comparing it against a known probability density function.

The probability density function for a normal distribution with mean μ, standard deviation σ, and variance σ<sup>2</sup> is



<pre class="mcode">

</pre>



Overlay a plot of the probability density function for a normal distribution with a mean of 5 and a standard deviation of 2.

<pre class="mcode">
hold on
y = -5:0.1:15;
mu = 5;
sigma = 2;
f = exp(-(y-mu).^2./(2*sigma^2))./(sigma*sqrt(2*pi));
plot(y,f,'LineWidth',1.5)

fig2plotly()
</pre>

{% capture plot_8_1_determine_underlying_probability_distribution_92 %}
  {% raw %}{"data":[{"name":"x","type":"bar","x":[-2.75,-2.25,-1.75,-1.25,-0.75,-0.25,0.25,0.75,1.25,1.75,2.25,2.75,3.25,3.75,4.25,4.75,5.25,5.75,6.25,6.75,7.25,7.75,8.25,8.75,9.25,9.75,10.25,10.75,11.25,11.75],"y":[0.0004,0,0.0004,0.0016,0.004,0.0068,0.0136,0.0212,0.0364,0.0556,0.084,0.1052,0.1284,0.162,0.1808,0.2108,0.1852,0.1836,0.1604,0.1424,0.1028,0.0736,0.0564,0.036,0.0268,0.0108,0.004,0.0048,0.0008,0.0012],"xaxis":"x1","yaxis":"y1","marker":{"line":{"color":"rgb(0,0,0)","width":0.5}},"opacity":0.75,"visible":true,"width":[0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5],"showlegend":true},{"line":{"dash":"solid","color":"rgb(216.75,82.875,24.99)","width":1.5},"mode":"lines","name":"","type":"scatter","x":[-5,-4.9,-4.8,-4.7,-4.6,-4.5,-4.4,-4.3,-4.2,-4.1,-4,-3.9,-3.8,-3.7,-3.6,-3.5,-3.4,-3.3,-3.2,-3.1,-3,-2.9,-2.8,-2.7,-2.6,-2.5,-2.4,-2.3,-2.2,-2.1,-2,-1.9,-1.8,-1.7,-1.6,-1.5,-1.4,-1.3,-1.2,-1.1,-1,-0.899999999999999,-0.8,-0.7,-0.6,-0.5,-0.399999999999999,-0.3,-0.199999999999999,-0.0999999999999996,0,0.100000000000001,0.2,0.300000000000001,0.4,0.5,0.600000000000001,0.7,0.800000000000001,0.9,1,1.1,1.2,1.3,1.4,1.5,1.6,1.7,1.8,1.9,2,2.1,2.2,2.3,2.4,2.5,2.6,2.7,2.8,2.9,3,3.1,3.2,3.3,3.4,3.5,3.6,3.7,3.8,3.9,4,4.1,4.2,4.3,4.4,4.5,4.6,4.7,4.8,4.9,5,5.1,5.2,5.3,5.4,5.5,5.6,5.7,5.8,5.9,6,6.1,6.2,6.3,6.4,6.5,6.6,6.7,6.8,6.9,7,7.1,7.2,7.3,7.4,7.5,7.6,7.7,7.8,7.9,8,8.1,8.2,8.3,8.4,8.5,8.6,8.7,8.8,8.9,9,9.1,9.2,9.3,9.4,9.5,9.6,9.7,9.8,9.9,10,10.1,10.2,10.3,10.4,10.5,10.6,10.7,10.8,10.9,11,11.1,11.2,11.3,11.4,11.5,11.6,11.7,11.8,11.9,12,12.1,12.2,12.3,12.4,12.5,12.6,12.7,12.8,12.9,13,13.1,13.2,13.3,13.4,13.5,13.6,13.7,13.8,13.9,14,14.1,14.2,14.3,14.4,14.5,14.6,14.7,14.8,14.9,15],"y":[7.43359757367149e-07,9.53300451561405e-07,1.21948037294668e-06,1.55608778957447e-06,1.98064954551604e-06,2.51475364429622e-06,3.18491258943354e-06,4.02359122824615e-06,5.07042603274338e-06,6.37366619091673e-06,7.99187055345274e-06,9.9958983534614e-06,1.24712356450268e-05,1.55207035289251e-05,1.92675983710436e-05,2.38593182706025e-05,2.94715338782699e-05,3.63129651511262e-05,4.46308285885665e-05,5.47170217199003e-05,6.69151128824427e-05,8.1628204383121e-05,9.93277356963864e-05,0.000120563290112997,0.00014597346289573,0.000176297841183723,0.000212390135275376,0.000255232487172093,0.000305950965056887,0.000365832231415155,0.00043634134752288,0.000519140647830705,0.00061610958423651,0.000729365402333374,0.000861284469526841,0.00101452402864988,0.00119204410073242,0.00139712920743972,0.00163340952809996,0.00190488104911091,0.002215924205969,0.00257132046152697,0.00297626620988793,0.00343638334530699,0.00395772579148998,0.00454678125079553,0.0052104674072113,0.00595612180380259,0.00679148461684282,0.00772467356719759,0.00876415024678427,0.00991867719589767,0.0111972651474214,0.0126091099575972,0.0141635188708006,0.0158698259178337,0.0177372964231157,0.0197750207946851,0.0219917979902136,0.0243960092895914,0.026995483256594,0.0297973530344081,0.0328079073873383,0.036032437168109,0.0394750791504471,0.0431386594132558,0.0470245386884435,0.051132462281989,0.0554604173397278,0.0600045003484928,0.0647587978329459,0.0697152832226802,0.0748637328178724,0.0801916636709598,0.0856842960239037,0.091324542694511,0.0970930274916065,0.102968134359987,0.108926088516275,0.114941070342117,0.120985362259572,0.127029528234594,0.133042624949377,0.138992443065498,0.144845776380741,0.150568716077402,0.156126966683381,0.161486179833957,0.1666123014459,0.171471927509692,0.17603266338215,0.180263481230824,0.184135070151662,0.187620173458469,0.190693907730262,0.193334058401425,0.195521346987728,0.197239665453944,0.198476273738506,0.199221957047382,0.199471140200716,0.199221957047382,0.198476273738506,0.197239665453944,0.195521346987728,0.193334058401425,0.190693907730262,0.187620173458469,0.184135070151662,0.180263481230824,0.17603266338215,0.171471927509692,0.1666123014459,0.161486179833957,0.156126966683381,0.150568716077402,0.144845776380741,0.138992443065498,0.133042624949377,0.127029528234594,0.120985362259572,0.114941070342117,0.108926088516275,0.102968134359987,0.0970930274916065,0.091324542694511,0.0856842960239037,0.0801916636709598,0.0748637328178724,0.0697152832226802,0.0647587978329459,0.0600045003484928,0.0554604173397278,0.051132462281989,0.0470245386884435,0.0431386594132558,0.0394750791504471,0.036032437168109,0.0328079073873383,0.0297973530344081,0.026995483256594,0.0243960092895914,0.0219917979902136,0.0197750207946851,0.0177372964231157,0.0158698259178337,0.0141635188708006,0.0126091099575972,0.0111972651474214,0.00991867719589768,0.00876415024678427,0.00772467356719759,0.00679148461684282,0.00595612180380259,0.00521046740721131,0.00454678125079553,0.00395772579148998,0.00343638334530699,0.00297626620988792,0.00257132046152698,0.002215924205969,0.00190488104911091,0.00163340952809996,0.00139712920743972,0.00119204410073242,0.00101452402864988,0.000861284469526841,0.000729365402333374,0.000616109584236509,0.000519140647830705,0.00043634134752288,0.000365832231415155,0.000305950965056887,0.000255232487172092,0.000212390135275376,0.000176297841183723,0.00014597346289573,0.000120563290112997,9.93277356963862e-05,8.1628204383121e-05,6.69151128824427e-05,5.47170217199003e-05,4.46308285885665e-05,3.63129651511262e-05,2.94715338782699e-05,2.38593182706025e-05,1.92675983710436e-05,1.55207035289251e-05,1.24712356450268e-05,9.9958983534614e-06,7.99187055345274e-06,6.37366619091673e-06,5.07042603274338e-06,4.02359122824615e-06,3.18491258943354e-06,2.51475364429622e-06,1.98064954551604e-06,1.55608778957447e-06,1.21948037294668e-06,9.53300451561405e-07,7.43359757367149e-07],"xaxis":"x1","yaxis":"y1","marker":{"line":{"width":1.5},"size":6,"color":"rgb(216.75,82.875,24.99)"},"visible":true,"showlegend":true}],"layout":{"title":"","width":840,"height":630,"margin":{"b":0,"l":0,"r":0,"t":0,"pad":0},"scene1":{"domain":{"x":[0.13,0.905],"y":[0.11,0.925]}},"xaxis1":{"side":"bottom","type":"linear","range":[-5,15],"ticks":"inside","anchor":"y1","domain":[0.13,0.905],"mirror":"ticks","nticks":6,"ticklen":6.51,"autotick":true,"showgrid":false,"showline":true,"tickfont":{"size":10,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"zeroline":false,"autorange":false,"gridcolor":"rgb(38.25,38.25,38.25)","gridwidth":1,"linecolor":"rgb(38.25,38.25,38.25)","linewidth":1,"tickcolor":"rgb(38.25,38.25,38.25)","tickwidth":1,"titlefont":{"size":11,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"exponentformat":"none"},"yaxis1":{"side":"left","type":"linear","range":[0,0.25],"ticks":"inside","anchor":"x1","domain":[0.11,0.925],"mirror":"ticks","nticks":7,"ticklen":6.51,"autotick":true,"showgrid":false,"showline":true,"tickfont":{"size":10,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"zeroline":false,"autorange":false,"gridcolor":"rgb(38.25,38.25,38.25)","gridwidth":1,"linecolor":"rgb(38.25,38.25,38.25)","linewidth":1,"tickcolor":"rgb(38.25,38.25,38.25)","tickwidth":1,"titlefont":{"size":11,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"exponentformat":"none"},"barmode":"group","autosize":false,"hovermode":"closest","titlefont":{"color":"rgba(0,0,0,0)"},"showlegend":false,"annotations":[{"x":0.5175,"y":0.935,"font":{"size":11,"color":"rgb(0,0,0)","family":"Arial,sans-serif"},"text":"","xref":"paper","yref":"paper","align":"center","xanchor":"center","yanchor":"bottom","borderpad":3,"showarrow":false,"textangle":0,"bordercolor":"rgba(0,0,0,0)","borderwidth":0.5}],"paper_bgcolor":"rgb(255,255,255)"},"frames":[]}{% endraw %}
{% endcapture %}
{% include posts/ssim_frame.html 
  raw_json_file=plot_8_1_determine_underlying_probability_distribution_92
  ssim="https://raw.githubusercontent.com/plotly/ssim_baselines/main/out_matlab/matlab/code-examples/data-distribution-plots/histogram/plot_8_1_determine_underlying_probability_distribution_ssim_map.png" 
  compare="https://raw.githubusercontent.com/plotly/ssim_baselines/main/out_matlab/matlab/code-examples/data-distribution-plots/histogram/plot_8_1_determine_underlying_probability_distribution_montage.png" 
  index=92
%}



<!--------------------- EXAMPLE BREAK ------------------------->

## Saving and Loading Histogram Objects

Use the `savefig` function to save a `histogram` figure.

<pre class="mcode">
histogram(randn(10));
savefig('histogram.fig');
close gcf

fig2plotly()
</pre>

Use `openfig` to load the histogram figure back into MATLAB. `openfig` also returns a handle to the figure, `h`. 

<pre class="mcode">
h = openfig('histogram.fig');

fig2plotly()
</pre>

{% capture plot_9_0_saving_and_loading_histogram_objects_93 %}
  {% raw %}{"data":[{"name":"","type":"bar","x":[-2.75,-2.25,-1.75,-1.25,-0.75,-0.25,0.25,0.75,1.25,1.75],"y":[1,1,2,7,23,19,20,14,8,5],"xaxis":"x1","yaxis":"y1","marker":{"line":{"color":"rgb(0,0,0)","width":0.5}},"opacity":0.75,"visible":true,"width":[0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5],"showlegend":true}],"layout":{"title":"","width":840,"height":630,"margin":{"b":0,"l":0,"r":0,"t":80,"pad":0},"scene1":{"domain":{"x":[0.13,0.905],"y":[0.11,0.925]}},"xaxis1":{"side":"bottom","type":"linear","range":[-3.25,2.25],"ticks":"inside","anchor":"y1","domain":[0.13,0.905],"mirror":"ticks","nticks":12,"ticklen":6.51,"autotick":true,"showgrid":false,"showline":true,"tickfont":{"size":10,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"zeroline":false,"autorange":false,"gridcolor":"rgb(38.25,38.25,38.25)","gridwidth":1,"linecolor":"rgb(38.25,38.25,38.25)","linewidth":1,"tickcolor":"rgb(38.25,38.25,38.25)","tickwidth":1,"titlefont":{"size":11,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"exponentformat":"none"},"yaxis1":{"side":"left","type":"linear","range":[0,25],"ticks":"inside","anchor":"x1","domain":[0.11,0.925],"mirror":"ticks","nticks":7,"ticklen":6.51,"autotick":true,"showgrid":false,"showline":true,"tickfont":{"size":10,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"zeroline":false,"autorange":false,"gridcolor":"rgb(38.25,38.25,38.25)","gridwidth":1,"linecolor":"rgb(38.25,38.25,38.25)","linewidth":1,"tickcolor":"rgb(38.25,38.25,38.25)","tickwidth":1,"titlefont":{"size":11,"color":"rgb(38.25,38.25,38.25)","family":"Arial,sans-serif"},"exponentformat":"none"},"barmode":"group","autosize":false,"hovermode":"closest","titlefont":{"size":11,"color":"rgb(0,0,0)","family":"Arial,sans-serif"},"showlegend":false,"annotations":[],"paper_bgcolor":"rgb(255,255,255)"},"frames":[]}{% endraw %}
{% endcapture %}
{% include posts/ssim_frame.html 
  raw_json_file=plot_9_0_saving_and_loading_histogram_objects_93
  ssim="https://raw.githubusercontent.com/plotly/ssim_baselines/main/out_matlab/matlab/code-examples/data-distribution-plots/histogram/plot_9_0_saving_and_loading_histogram_objects_ssim_map.png" 
  compare="https://raw.githubusercontent.com/plotly/ssim_baselines/main/out_matlab/matlab/code-examples/data-distribution-plots/histogram/plot_9_0_saving_and_loading_histogram_objects_montage.png" 
  index=93
%}

Use the `findobj` function to locate the correct object handle from the figure handle. This allows you to continue manipulating the original histogram object used to generate the figure.

<pre class="mcode">
y = findobj(h,'type','histogram')

fig2plotly()
</pre>


<pre class="codeoutput">y = 
  Histogram with properties:

             Data: [10x10 double]
           Values: [2 17 28 32 16 3 2]
          NumBins: 7
         BinEdges: [-3 -2 -1 0 1 2 3 4]
         BinWidth: 1
        BinLimits: [-3 4]
    Normalization: 'count'
        FaceColor: 'auto'
        EdgeColor: [0 0 0]

  Show all properties

</pre>




<!--------------------- EXAMPLE BREAK ------------------------->

