# DataXAct

## Proposed solution:
_Preprocessing:_
<ol>
  <li>Merge common columns:</li>
<ul>
  <li>Merging combines information from multiple datasets into a single dataset. </li>
  <li>It is performed based on common columns or keys present in both datasets.</li>
  <li>Merging allows consolidation of data and creation of a unified dataset for analysis or modeling.</li>
<ul/>
<li>Drop rows with missing target values:</li>
<ul>
  <li>Missing target values hinder accurate analysis or model training.</li>
  <li>Dropping rows with missing target values ensures a clean dataset.</li>
  <li>It guarantees the availability of complete information for model training or analysis.</li>
</ul>
<li> Use Imputer to Replace Feature Values:</li>
<ul>
  <li>Imputation fills in missing values in features or input variables.</li>
  <li>Missing values can occur due to data collection errors or incomplete records.</li>
  <li>Imputation ensures the dataset is complete and usable for model training.</li>
  <li>Common techniques include mean imputation, median imputation, or using advanced methods like regression or machine learning algorithms for prediction.<br/>
</ul>

![image](https://github.com/asitsngh/DataXAct/assets/137433061/f1fd0116-d42a-4535-9bf0-70ec147433d1)
