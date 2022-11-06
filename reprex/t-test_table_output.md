``` r
library(dplyr)
library(gt)
library(broom)

mtcars %>%
  group_by(vs) %>%
  do(tidy(t.test(.$mpg))) %>%
  gt()
```
<table class="gt_table">
  
  <thead class="gt_col_headings">
    <tr>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1" scope="col">estimate</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1" scope="col">statistic</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1" scope="col">p.value</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1" scope="col">parameter</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1" scope="col">conf.low</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1" scope="col">conf.high</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col">method</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col">alternative</th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr class="gt_group_heading_row">
      <td colspan="8" class="gt_group_heading">0</td>
    </tr>
    <tr class="gt_row_group_first"><td class="gt_row gt_right">16.61667</td>
<td class="gt_row gt_right">18.26056</td>
<td class="gt_row gt_right">1.316696e-12</td>
<td class="gt_row gt_right">17</td>
<td class="gt_row gt_right">14.69679</td>
<td class="gt_row gt_right">18.53655</td>
<td class="gt_row gt_left">One Sample t-test</td>
<td class="gt_row gt_left">two.sided</td></tr>
    <tr class="gt_group_heading_row">
      <td colspan="8" class="gt_group_heading">1</td>
    </tr>
    <tr class="gt_row_group_first"><td class="gt_row gt_right">24.55714</td>
<td class="gt_row gt_right">17.08213</td>
<td class="gt_row gt_right">2.750107e-10</td>
<td class="gt_row gt_right">13</td>
<td class="gt_row gt_right">21.45141</td>
<td class="gt_row gt_right">27.66287</td>
<td class="gt_row gt_left">One Sample t-test</td>
<td class="gt_row gt_left">two.sided</td></tr>
  </tbody>
  
  
</table>
</div>

<sup>Created on 2022-11-05 with [reprex v2.0.2](https://reprex.tidyverse.org)</sup>
