``` r
library(dplyr)
library(gt)
library(broom)

mtcars %>%
  do(tidy(t.test(.$mpg ~ .$vs))) %>%
  gt()
```

<table class="gt_table">
  
  <thead class="gt_col_headings">
    <tr>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1" scope="col">estimate</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1" scope="col">estimate1</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1" scope="col">estimate2</th>
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
    <tr><td class="gt_row gt_right">-7.940476</td>
<td class="gt_row gt_right">16.61667</td>
<td class="gt_row gt_right">24.55714</td>
<td class="gt_row gt_right">-4.667053</td>
<td class="gt_row gt_right">0.0001098368</td>
<td class="gt_row gt_right">22.71576</td>
<td class="gt_row gt_right">-11.46251</td>
<td class="gt_row gt_right">-4.418445</td>
<td class="gt_row gt_left">Welch Two Sample t-test</td>
<td class="gt_row gt_left">two.sided</td></tr>
  </tbody>
  
  
</table>
</div>

<sup>Created on 2022-11-05 with [reprex v2.0.2](https://reprex.tidyverse.org)</sup>
