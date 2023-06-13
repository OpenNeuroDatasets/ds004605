# NIH | NIMH | EDB: Phenotyping and DTI (2012-2017)

A comprehensive dataset characterizing a transdiagnostic sample of youth in terms of clinical assessments, structural magnetic resonance imaging (MRI), and diffusion tensor imaging (DTI).

All data collected in this protocol are broadly shared in the OpenNeuro repository, in the Brain Imaging Data Structure (BIDS) format.  In addition, basic pre-processing scripts are shared on GitHub.  This dataset will allow a wide array of investigations into psychopathology in youth.

This dataset is licensed under the [Creative Commons Zero (CC0) v1.0 License](https://creativecommons.org/publicdomain/zero/1.0/).

## Participant Eligibility and Characteristics

To be eligible for the study, participants were aged 8 to 20 years. Youth were included if they met the criteria for attention-deficit/hyperactivity disorder (ADHD) characterized by inattention, hyperactivity, or disruptive mood dysregulation disorder (DMDD), where irritability is the core symptom, or did not meet the criteria for any psychiatric disorder (i.e., healthy volunteer, HV) assessed with the KSADS. Exclusion criteria were: neurological disorders, autism spectrum disorders, psychosis, bipolar disorders, substance use, MRI contraindications, and full-scale IQ<70. Institutional Review Board approval, parent or guardian consent, and child assent were obtained.

To characterize the sample, we collected data on participants' race/ethnicity, parental income, and use of psychotropic medication. 

## Clinical Measures

Participants completed: Affective Reactivity Index (youth-ARI), Wechsler Abbreviated Scale of Intelligence (WASI)

Participants' parents/caregivers completed several assessments: Affective Reactivity Index (parent-ARI), Conners Comprehensive Behavioral Rating Scale (CBRS), Screen for Children’s Affective Reactivity–Home (SCAR-H)

Clinicians completed: Kiddie Schedule for Affective Disorders (KSADS)

## MRI

The MRI protocol included:

* Diffusion weighted scan with a single-shot echo planar imaging sequence (TR = 6751 ms, TE = 79 ms, 62 axial slices, 2.5 mm slice thickness, FoV = 240 mm2, matrix size = 96 x 96). We obtained five unweighted images and 75 images with diffusion gradients (6: b = 300 s/mm2, 69: b = 1000 s/mm2) performed across four runs
* T2-weighted scan with a fast spin-echo sequence/fat suppression (TR = 7500 ms, TE = 100 ms, 100 axial slices, slice thickness = 1.7 mm, no gap, FoV = 240 × 192 mm, matrix size = 256 × 192)
* T1-weighted scan (TR = 7.6 ms, TE = 3.5 ms, slice thickness = 1 mm, no gap, matrix size = 256 × 256)

## Description of data formats and preparation

### Clinical Measures Data

Relevant clinical measures can be found in the phenotype.tsv file, with each measure described in the phenotype.json file. In several columns, there exist `n/a` values, indicating that the question may have been skipped over by the participant or not presented or asked to the participant.

Scripts with sample analysis steps (e.g., factor analyses) can be found in our Github repository.

### BIDS-standard MRI

For anatomical images in this study the format used was NifTI. The images were acquired with a 3 Tesla field strength and were oriented in the axial plane. Visual inspection was performed to exclude any images with significant artifacts or distortions.

We have anonymized the structural MRI scans by performing defacing in accordance with the [DSST Defacing Pipeline](https://github.com/nih-fmrif/dsst-defacing-pipeline/).

### BIDS-standard DTI

For DTI images, the format used was also NifTI. The images were also acquired on a 3 Tesla scanner and oriented on the axial plane.

Preprocessing was performed using TORTOISE software package version 3.2 and FA maps were generated using TBSS in FSL.

Information about the DTI directions removed and example analysis scripts can be found in our Github repository. 
