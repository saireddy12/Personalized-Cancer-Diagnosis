---------------------------------More About cancer---------------------------

Causes
Cancer is caused by changes (mutations) to the DNA within cells. The DNA inside a cell is packaged into a large number of individual genes, each of which contains a set of instructions telling the cell what functions to perform, as well as how to grow and divide. Errors in the instructions can cause the cell to stop its normal function and may allow a cell to become cancerous.

What do gene mutations do?
A gene mutation can instruct a healthy cell to:

Allow rapid growth. A gene mutation can tell a cell to grow and divide more rapidly. This creates many new cells that all have that same mutation.
Fail to stop uncontrolled cell growth. Normal cells know when to stop growing so that you have just the right number of each type of cell. Cancer cells lose the controls (tumor suppressor genes) that tell them when to stop growing. A mutation in a tumor suppressor gene allows cancer cells to continue growing and accumulating.
Make mistakes when repairing DNA errors. DNA repair genes look for errors in a cell's DNA and make corrections. A mutation in a DNA repair gene may mean that other errors aren't corrected, leading cells to become cancerous.
These mutations are the most common ones found in cancer. But many other gene mutations can contribute to causing cancer.

What causes gene mutations?
Gene mutations can occur for several reasons, for instance:

Gene mutations you're born with. You may be born with a genetic mutation that you inherited from your parents. This type of mutation accounts for a small percentage of cancers.
Gene mutations that occur after birth. Most gene mutations occur after you're born and aren't inherited. A number of forces can cause gene mutations, such as smoking, radiation, viruses, cancer-causing chemicals (carcinogens), obesity, hormones, chronic inflammation and a lack of exercise.
Gene mutations occur frequently during normal cell growth. However, cells contain a mechanism that recognizes when a mistake occurs and repairs the mistake. Occasionally, a mistake is missed. This could cause a cell to become cancerous.

How do gene mutations interact with each other?
The gene mutations you're born with and those that you acquire throughout your life work together to cause cancer.

For instance, if you've inherited a genetic mutation that predisposes you to cancer, that doesn't mean you're certain to get cancer. Instead, you may need one or more other gene mutations to cause cancer. Your inherited gene mutation could make you more likely than other people to develop cancer when exposed to a certain cancer-causing substance.

It's not clear just how many mutations must accumulate for cancer to form. It's likely that this varies among cancer types.
#source:
https://www.mayoclinic.org/diseases-conditions/cancer/symptoms-causes/syc-20370588




Business Problem
Description

Source: https://www.kaggle.com/c/msk-redefining-cancer-treatment/

Data: Memorial Sloan Kettering Cancer Center (MSKCC)

Download training_variants.zip and training_text.zip from Kaggle.

Context:
Source: https://www.kaggle.com/c/msk-redefining-cancer-treatment/discussion/35336#198462

Problem statement : 
Classify the given genetic variations/mutations based on evidence from text-based clinical literature.

Source/Useful Links
Some articles and reference blogs about the problem statement

https://www.forbes.com/sites/matthewherper/2017/06/03/a-new-cancer-drug-helped-almost-everyone-who-took-it-almost-heres-what-it-teaches-us/#2a44ee2f6b25
https://www.youtube.com/watch?v=UwbuW7oK8rk
https://www.youtube.com/watch?v=qxXRKVompI8
Real-world/Business objectives and constraints.
No low-latency requirement.
Interpretability is important.
Errors can be very costly.
Probability of a data-point belonging to each class is needed.
Machine Learning Problem Formulation
Data
Data Overview
Source: https://www.kaggle.com/c/msk-redefining-cancer-treatment/data
We have two data files: one conatins the information about the genetic mutations and the other contains the clinical evidence (text) that human experts/pathologists use to classify the genetic mutations.
Both these data files are have a common column called ID



Mapping the real-world problem to an ML problem
Type of Machine Learning Problem
        There are nine different classes a genetic mutation can be classified into => Multi class classification problem
Performance Metric
Source: https://www.kaggle.com/c/msk-redefining-cancer-treatment#evaluation

Metric(s):

Multi class log-loss
Confusion matrix
Machine Learing Objectives and Constraints
Objective: Predict the probability of each data-point belonging to each of the nine classes.

Constraints:

* Interpretability * Class probabilities are needed. * Penalize the errors in class probabilites => Metric is Log-loss. * No Latency constraints.