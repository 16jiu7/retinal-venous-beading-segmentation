# retinal-venous-beading-segmentation
This repo. uses real data from hospital to tackle the retinal venous beading segmentation problem
3 steps are taken to finally segment the area of venous beading in RGB retinal images.
Step 1 is retinal blood vessel segmentation, using a U-Net-like CNN, the model is trained on DRIVE datasets and finetuned to suit the new domain, where data suffer from greater illumination variance.
Step 2 we place N m*m box on the resultant vessel map, covering all the vessel pixels. The problem is thus transfered to a classification problem.
Step 3 we distinguish between venous beading patches and non-beading ones and get the final resulting beading area, after which we test the performance of our algorithm. 
