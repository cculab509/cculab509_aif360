About Dataset
=
<p>Our dataset is based on the Taipei City Transportation Bureau's 2020 traffic accident data. </p>
<p>It contains 213,872 records with 105 fields. </p>
<p>Our goal is to identify any bias in the data.</p>

Description of the data
-
We selected the following six fields to detect bias in the dataset:'Gender'	'Delivery_Type'	'Age'	'Vehicle types'	'Accident type'	'Degree of injury'.
+ In the 'Gender' field, we set males as 1 and females as 2, we also removed records with blank fields, animal-related accidents, and hit-and-run accidents.
+ In the 'Delivery_Type' field, we set 1 to delivery drivers and 0 to non-delivery drivers, we also removed records with blank fields.
+ In the 'Age' field, we set people under the age of 18 as 1, people between the ages of 19 and 64 as 2, and people over the age of 65 as 3, we also removed records with blank fields.
+ In the 'Vehicle types' field, we set B03 (private passenger car) as 1, C03 (standard heavy motorcycle) as 2, and all others as 0, we also removed records with blank fields.
* In the 'Accident type' field, we set blank fields to 0 and non-blank fields to 1.
* In the 'Degree of injury' field, we converted it to "Is there no injury?" and set "No injury" to 1 and all others to 0.

About Code
=
<p>This program is used to detect bias in data.</p>
<p>We referenced the example "demo_mdss_detector.ipynb" in AIF360.</p>
<p>We detected bias in the 2020 Taipei traffic accident data, mainly using the indicator of whether the number of injuries is zero.</p>
<p>We found that the presence of blank fields in the "Accident type and form" column would bias the prediction of the number of injuries.</p>
