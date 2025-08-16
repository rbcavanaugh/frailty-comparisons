
<!-- README.md is generated from README.Rmd. Please edit that file -->

# Evaluating Frailty Index Integrity: Insights from an International Network Study

## Authors

**Robert Cavanaugh**<sup>1,2</sup>, **Chelsea Wong**<sup>3,4</sup>,
**Louisa Smith**<sup>5,1</sup>, **Maytal Bivas-Benita**<sup>6</sup>,
**Pinchas Akiva**<sup>6</sup>, **Tal El-Hay**<sup>6</sup>, **Ariela
Orkaby**<sup>3,4,7</sup>, **Chen Yanover**<sup>6</sup>, **Brianne
Olivieri-Mui**<sup>5,1,3</sup>

## Author Affiliations

1.  The Roux Institute, Northeastern University, Portland, ME
2.  MGH Institute of Health Professions, Boston, MA
3.  Hebrew SeniorLife, Harvard Medical School, Roslindale, MA
4.  Beth Israel Deaconess Medical Center, Boston, MA
5.  Northeastern University, Boston, MA
6.  KI Research Institute, Kfar Malal, Israel
7.  Veterans Affairs Medical Center, Boston, MA

## Repository Structure

    #> .
    #> ├── KI # Frailty output # Final aggregate data and extra output
    #> ├── README.Rmd
    #> ├── README.md
    #> ├── data # Frailty code lists
    #> ├── frailty-comparisons.Rproj
    #> ├── functions # Custom R functions and utilities
    #> ├── manuscript # Manuscript drafts and related files
    #> └── output # Final aggregate data and extra output

## Packages used

<div id="vxmueyfynr" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#vxmueyfynr table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
&#10;#vxmueyfynr thead, #vxmueyfynr tbody, #vxmueyfynr tfoot, #vxmueyfynr tr, #vxmueyfynr td, #vxmueyfynr th {
  border-style: none;
}
&#10;#vxmueyfynr p {
  margin: 0;
  padding: 0;
}
&#10;#vxmueyfynr .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 16px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}
&#10;#vxmueyfynr .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}
&#10;#vxmueyfynr .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}
&#10;#vxmueyfynr .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}
&#10;#vxmueyfynr .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}
&#10;#vxmueyfynr .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}
&#10;#vxmueyfynr .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}
&#10;#vxmueyfynr .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}
&#10;#vxmueyfynr .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}
&#10;#vxmueyfynr .gt_column_spanner_outer:first-child {
  padding-left: 0;
}
&#10;#vxmueyfynr .gt_column_spanner_outer:last-child {
  padding-right: 0;
}
&#10;#vxmueyfynr .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}
&#10;#vxmueyfynr .gt_spanner_row {
  border-bottom-style: hidden;
}
&#10;#vxmueyfynr .gt_group_heading {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}
&#10;#vxmueyfynr .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}
&#10;#vxmueyfynr .gt_from_md > :first-child {
  margin-top: 0;
}
&#10;#vxmueyfynr .gt_from_md > :last-child {
  margin-bottom: 0;
}
&#10;#vxmueyfynr .gt_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}
&#10;#vxmueyfynr .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}
&#10;#vxmueyfynr .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}
&#10;#vxmueyfynr .gt_row_group_first td {
  border-top-width: 2px;
}
&#10;#vxmueyfynr .gt_row_group_first th {
  border-top-width: 2px;
}
&#10;#vxmueyfynr .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}
&#10;#vxmueyfynr .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}
&#10;#vxmueyfynr .gt_first_summary_row.thick {
  border-top-width: 2px;
}
&#10;#vxmueyfynr .gt_last_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}
&#10;#vxmueyfynr .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}
&#10;#vxmueyfynr .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}
&#10;#vxmueyfynr .gt_last_grand_summary_row_top {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #D3D3D3;
}
&#10;#vxmueyfynr .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}
&#10;#vxmueyfynr .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}
&#10;#vxmueyfynr .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}
&#10;#vxmueyfynr .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
}
&#10;#vxmueyfynr .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}
&#10;#vxmueyfynr .gt_sourcenote {
  font-size: 90%;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
}
&#10;#vxmueyfynr .gt_left {
  text-align: left;
}
&#10;#vxmueyfynr .gt_center {
  text-align: center;
}
&#10;#vxmueyfynr .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}
&#10;#vxmueyfynr .gt_font_normal {
  font-weight: normal;
}
&#10;#vxmueyfynr .gt_font_bold {
  font-weight: bold;
}
&#10;#vxmueyfynr .gt_font_italic {
  font-style: italic;
}
&#10;#vxmueyfynr .gt_super {
  font-size: 65%;
}
&#10;#vxmueyfynr .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}
&#10;#vxmueyfynr .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}
&#10;#vxmueyfynr .gt_indent_1 {
  text-indent: 5px;
}
&#10;#vxmueyfynr .gt_indent_2 {
  text-indent: 10px;
}
&#10;#vxmueyfynr .gt_indent_3 {
  text-indent: 15px;
}
&#10;#vxmueyfynr .gt_indent_4 {
  text-indent: 20px;
}
&#10;#vxmueyfynr .gt_indent_5 {
  text-indent: 25px;
}
&#10;#vxmueyfynr .katex-display {
  display: inline-flex !important;
  margin-bottom: 0.75em !important;
}
&#10;#vxmueyfynr div.Reactable > div.rt-table > div.rt-thead > div.rt-tr.rt-tr-group-header > div.rt-th-group:after {
  height: 0px !important;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <thead>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="package">package</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="citation">citation</th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="package" class="gt_row gt_left">tidyverse</td>
<td headers="citation" class="gt_row gt_left">Wickham H, Averick M, Bryan J, Chang W, McGowan LD, François R,
Grolemund G, Hayes A, Henry L, Hester J, Kuhn M, Pedersen TL, Miller E,
Bache SM, Müller K, Ooms J, Robinson D, Seidel DP, Spinu V, Takahashi
K, Vaughan D, Wilke C, Woo K, Yutani H (2019). "Welcome to the
tidyverse." _Journal of Open Source Software_, *4*(43), 1686.
doi:10.21105/joss.01686 &lt;https://doi.org/10.21105/joss.01686&gt;.</td></tr>
    <tr><td headers="package" class="gt_row gt_left">DBI</td>
<td headers="citation" class="gt_row gt_left">R Special Interest Group on Databases (R-SIG-DB), Wickham H, Müller K
(2024). _DBI: R Database Interface_. doi:10.32614/CRAN.package.DBI
&lt;https://doi.org/10.32614/CRAN.package.DBI&gt;, R package version 1.2.3,
&lt;https://CRAN.R-project.org/package=DBI&gt;.</td></tr>
    <tr><td headers="package" class="gt_row gt_left">DatabaseConnector</td>
<td headers="citation" class="gt_row gt_left">Citation not available for DatabaseConnector</td></tr>
    <tr><td headers="package" class="gt_row gt_left">CDMConnector</td>
<td headers="citation" class="gt_row gt_left">Black A, Gorbachev A, Burn E, Catala Sabate M, Nika I (2025).
_CDMConnector: Connect to an OMOP Common Data Model_.
doi:10.32614/CRAN.package.CDMConnector
&lt;https://doi.org/10.32614/CRAN.package.CDMConnector&gt;, R package version
2.1.1, &lt;https://CRAN.R-project.org/package=CDMConnector&gt;.</td></tr>
    <tr><td headers="package" class="gt_row gt_left">glue</td>
<td headers="citation" class="gt_row gt_left">Hester J, Bryan J (2024). _glue: Interpreted String Literals_.
doi:10.32614/CRAN.package.glue
&lt;https://doi.org/10.32614/CRAN.package.glue&gt;, R package version 1.8.0,
&lt;https://CRAN.R-project.org/package=glue&gt;.</td></tr>
    <tr><td headers="package" class="gt_row gt_left">here</td>
<td headers="citation" class="gt_row gt_left">Müller K (2020). _here: A Simpler Way to Find Your Files_.
doi:10.32614/CRAN.package.here
&lt;https://doi.org/10.32614/CRAN.package.here&gt;, R package version 1.0.1,
&lt;https://CRAN.R-project.org/package=here&gt;.</td></tr>
    <tr><td headers="package" class="gt_row gt_left">allofus</td>
<td headers="citation" class="gt_row gt_left">Smith LH, Cavanaugh R (2024). "allofus: An R Package to Facilitate Use
of the All of Us Researcher Workbench." _Journal of the American
Medical Informatics Association_, ocae198. doi:10.1093/jamia/ocae198
&lt;https://doi.org/10.1093/jamia/ocae198&gt;.</td></tr>
    <tr><td headers="package" class="gt_row gt_left">keyring</td>
<td headers="citation" class="gt_row gt_left">Citation not available for keyring</td></tr>
  </tbody>
  &#10;  
</table>
</div>
