``` r
library(gapminder)
library(tidyverse)
library(gt)
gapminder %>%
  group_by(year) %>%
  summarise(avg_lifeExp = round(mean(lifeExp),2)) %>%
  mutate(diff = round(avg_lifeExp - lag(avg_lifeExp),2)) %>%
  gt()
```

<table class="gt_table">
  
  <thead class="gt_col_headings">
    <tr>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1" scope="col">year</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1" scope="col">avg_lifeExp</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1" scope="col">diff</th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td class="gt_row gt_right">1952</td>
<td class="gt_row gt_right">49.06</td>
<td class="gt_row gt_right">NA</td></tr>
    <tr><td class="gt_row gt_right">1957</td>
<td class="gt_row gt_right">51.51</td>
<td class="gt_row gt_right">2.45</td></tr>
    <tr><td class="gt_row gt_right">1962</td>
<td class="gt_row gt_right">53.61</td>
<td class="gt_row gt_right">2.10</td></tr>
    <tr><td class="gt_row gt_right">1967</td>
<td class="gt_row gt_right">55.68</td>
<td class="gt_row gt_right">2.07</td></tr>
    <tr><td class="gt_row gt_right">1972</td>
<td class="gt_row gt_right">57.65</td>
<td class="gt_row gt_right">1.97</td></tr>
    <tr><td class="gt_row gt_right">1977</td>
<td class="gt_row gt_right">59.57</td>
<td class="gt_row gt_right">1.92</td></tr>
    <tr><td class="gt_row gt_right">1982</td>
<td class="gt_row gt_right">61.53</td>
<td class="gt_row gt_right">1.96</td></tr>
    <tr><td class="gt_row gt_right">1987</td>
<td class="gt_row gt_right">63.21</td>
<td class="gt_row gt_right">1.68</td></tr>
    <tr><td class="gt_row gt_right">1992</td>
<td class="gt_row gt_right">64.16</td>
<td class="gt_row gt_right">0.95</td></tr>
    <tr><td class="gt_row gt_right">1997</td>
<td class="gt_row gt_right">65.01</td>
<td class="gt_row gt_right">0.85</td></tr>
    <tr><td class="gt_row gt_right">2002</td>
<td class="gt_row gt_right">65.69</td>
<td class="gt_row gt_right">0.68</td></tr>
    <tr><td class="gt_row gt_right">2007</td>
<td class="gt_row gt_right">67.01</td>
<td class="gt_row gt_right">1.32</td></tr>
  </tbody>
  
  
</table>
</div>

<sup>Created on 2022-11-05 with [reprex v2.0.2](https://reprex.tidyverse.org)</sup>
