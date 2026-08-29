# Results package

Run hash: a7b4d04-dirty
Mode: normalised
Seed: 42
Bootstrap draws: 2000

## Decision log

- **station screening**: PASS. all eleven stations pass; smallest guard factor 1.59
- **pre-treatment slope gap**: FAIL. furthest interval edge 5.830 percentage points per year, category: bounded reporting
- **leads test**: FAIL. joint test that the 6 pre-policy half-years are zero, p 0.049 under the resampled covariance
- **combined pre-trend gates**: FAIL. slope gap gives 'bounded reporting', leads escalate, reporting mode: bounded reporting
- **false-onset checks**: PASS. largest usable ratio 2.17 versus main-model ratio 3.21

## station_roles

```
station      city        tier      onset    perimeter  anchor
FR04143     Paris attribution 2017-07-01 Paris proper    True
FR04055     Paris attribution 2017-07-01 Paris proper    True
FR04004     Paris attribution 2017-07-01 Paris proper   False
FR04131     Paris attribution 2017-07-01 Paris proper   False
FR20062      Lyon attribution 2022-09-01         Lyon    True
FR20017      Lyon attribution 2022-09-01         Lyon   False
FR20046      Lyon attribution 2022-09-01         Lyon   False
FR03043 Marseille attribution 2022-09-01    Marseille    True
FR03014 Marseille attribution 2022-09-01    Marseille   False
FR04329     Paris   mechanism 2019-07-01    ring road    True
FR03006 Marseille   mechanism 2022-09-01    Marseille    True
```

## panel_shape

```
     city station  station_months      first       last
    Paris FR04004              45 2022-01-01 2025-12-01
    Paris FR04055              69 2019-12-01 2025-12-01
    Paris FR04131              48 2022-01-01 2025-12-01
    Paris FR04143              78 2013-01-01 2019-08-01
    Paris FR04329             156 2013-01-01 2025-12-01
     Lyon FR20017              64 2020-06-01 2025-12-01
     Lyon FR20046             136 2013-01-01 2025-12-01
     Lyon FR20062             154 2013-01-01 2025-12-01
Marseille FR03006             142 2013-01-01 2025-12-01
Marseille FR03014              71 2020-01-01 2025-12-01
Marseille FR03043             150 2013-01-01 2025-12-01
```

## window_counts

```
           window      start        end  attribution_station_months
      full record 2013-01-01 2025-12-31                         815
   primary sample 2013-01-01 2022-08-31                         516
   clean contrast 2017-07-01 2022-08-31                         309
       pre-window 2013-01-01 2016-06-30                         162
precursor segment 2016-07-01 2017-06-30                          45
```

## dose_geography

```
     city                                                           source
    Paris arrondissements plus commune-level residual (0.215% of vehicles)
     Lyon arrondissements plus commune-level residual (0.056% of vehicles)
Marseille arrondissements plus commune-level residual (0.022% of vehicles)
```

## dose_unknown_share

```
 year     Lyon  Marseille    Paris
 2011 0.000050   0.000006 0.000002
 2012 0.000035   0.000011 0.000008
 2013 0.000050   0.000014 0.000008
 2014 0.000030   0.000008 0.000007
 2015 0.000025   0.000011 0.000005
 2016 0.000015   0.000014 0.000007
 2017 0.000034   0.000027 0.000005
 2018 0.000039   0.000019 0.000003
 2019 0.000034   0.000019 0.000005
 2020 0.000029   0.000016 0.000005
 2021 0.000019   0.000013 0.000005
 2022 0.000024   0.000019 0.000003
 2023 0.000020   0.000014 0.000004
 2024 0.000025   0.000011 0.000003
 2025 0.000025   0.000011 0.000005
 2026 0.000025   0.000003 0.000005
```

## dose_by_city_year

```
 year  Paris   Lyon  Marseille
 2013 0.0000 0.0000     0.0000
 2014 0.0000 0.0000     0.0000
 2015 0.0000 0.0000     0.0000
 2016 0.0990 0.0000     0.0000
 2017 0.0998 0.0000     0.0000
 2018 0.0817 0.0000     0.0000
 2019 0.1216 0.0000     0.0000
 2020 0.0976 0.0000     0.0000
 2021 0.0813 0.0000     0.0000
 2022 0.0704 0.0251     0.0303
 2023 0.0626 0.0210     0.0817
 2024 0.0543 0.0504     0.0707
 2025 0.1592 0.1701     0.0613
```

## dose_composition_paris

```
 year                step      class  share  banned
 2016 unclassified banned Crit'Air E 0.0021   False
 2016 unclassified banned Crit'Air 1 0.1571   False
 2016 unclassified banned Crit'Air 2 0.3648   False
 2016 unclassified banned Crit'Air 3 0.2831   False
 2016 unclassified banned Crit'Air 4 0.0727   False
 2016 unclassified banned Crit'Air 5 0.0213   False
 2016 unclassified banned Non classé 0.0990    True
 2016 unclassified banned    Inconnu 0.0000   False
 2019    Crit'Air 4 added Crit'Air E 0.0075   False
 2019    Crit'Air 4 added Crit'Air 1 0.2792   False
 2019    Crit'Air 4 added Crit'Air 2 0.3670   False
 2019    Crit'Air 4 added Crit'Air 3 0.2246   False
 2019    Crit'Air 4 added Crit'Air 4 0.0543    True
 2019    Crit'Air 4 added Crit'Air 5 0.0125    True
 2019    Crit'Air 4 added Non classé 0.0548    True
 2019    Crit'Air 4 added    Inconnu 0.0000   False
```

## weather_adjustment_screen

```
 coefficient  p_value  screening_level      result marseille_onset
   -0.334526 0.080572             0.05 not flagged      2022-09-01
```

## pretrend_slope_gap

```
                                           quantity  estimate_pct_yr  ci_lo_pct_yr  ci_hi_pct_yr  m_furthest_edge          category  blocks_calendar_years  usable_draws  station_months
Paris minus pooled comparators, pre-treatment slope           -1.915         -5.83         3.238             5.83 bounded reporting                      4          2000             162
```

## leads_joint_test

```
 terms_tested  chi2_bootstrap  p_bootstrap_governs  p_analytic_crosscheck  agree
            6          12.639               0.0491                 0.0053   True
```

## event_study_half_years

```
half_year      role  estimate_pct  analytic_se_log
  2013-H1      lead         3.070          0.07743
  2013-H2      lead        -0.408          0.07100
  2014-H1      lead         2.940          0.06460
  2014-H2      lead        -8.944          0.05245
  2015-H1      lead        -6.950          0.06749
  2015-H2      lead        -7.188          0.05942
  2016-H1 reference         0.000              NaN
  2016-H2 precursor        -7.368          0.05258
  2017-H1 precursor         2.691          0.07205
  2017-H2      post         1.284          0.04348
  2018-H1      post        12.616          0.06388
  2018-H2      post         5.296          0.05168
  2019-H1      post        25.236          0.06866
  2019-H2      post        16.752          0.04891
  2020-H1      post        66.242          0.05584
  2020-H2      post        41.356          0.06101
  2021-H1      post        60.078          0.06460
  2021-H2      post        47.492          0.05376
  2022-H1      post        51.911          0.05707
  2022-H2      post        56.687          0.05011
```

## residual_comovement

```
     city  Paris  Lyon  Marseille
    Paris  1.000 0.809      0.585
     Lyon  0.809 1.000      0.784
Marseille  0.585 0.784      1.000
```

## gate_outcome

```
slope_gap_category  slope_gap_m  leads_p  leads_escalates    final_category                                                      reporting_mode
 bounded reporting         5.83   0.0491             True bounded reporting range consistent with the data, with the smallest detectable effect
```

## primary_A

```
                                             quantity  estimate_pct  ci_lo_pct  ci_hi_pct  excludes_zero  analytic_se_log  bootstrap_se_log  usable_draws  blocks_calendar_years  station_months  stations
Primary A: Paris after July 2017, against comparators        13.661      5.483     23.281           True          0.05339           0.03984          2000                     10             516         9
```

## primary_A_inference_comparison

```
                         method  estimate_pct  ci_lo_pct  ci_hi_pct  excludes_zero  p_value
            resampled (governs)        13.661      5.483     23.281           True      NaN
analytic, correlation-corrected        13.661      2.369     26.198           True   0.0169
```

## dose_secondary

```
                                                             quantity  estimate_pct  ci_lo_pct  ci_hi_pct  excludes_zero  analytic_se_log  bootstrap_se_log  usable_draws
    Paris: effect per ten percentage points of prohibited fleet share         4.637     -1.810     11.782          False          0.03850           0.03293          2000
     Lyon: effect per ten percentage points of prohibited fleet share         6.349      2.512     11.308           True          0.03122           0.02132          2000
Marseille: effect per ten percentage points of prohibited fleet share         8.347     -2.114     21.500          False          0.05062           0.05553          2000
   Pooled: effect per ten percentage points of prohibited fleet share         5.867      2.182     10.544           True          0.02400           0.02039          2000
```

## dose_variation_by_city

```
     city  dose_min  dose_max  dose_mean
    Paris       0.0    0.1592     0.0722
     Lyon       0.0    0.1701     0.0168
Marseille       0.0    0.0817     0.0101
```

## weather_model_fit_sensitivity

```
station  refits  mean_monthly_sd  as_pct_of_level  seconds
FR04143      50           0.1208            0.808      300
FR20062      50           0.1100            0.840      704
FR03043      50           0.0965            0.838      664
```

## S4_later_era_descriptive

```
     city  station_months  mean_pm25
    Paris              45     11.645
     Lyon              87     11.015
Marseille              64     10.333
```

## surrounding_area_coverage

```
station first_month last_month  station_months  mean_pm25
FR04002     2013-01    2025-12             139     11.906
FR04034     2013-01    2025-12             153     11.603
FR04150     2021-02    2025-12              37      9.767
FR04156     2013-01    2025-12             155     11.431
```

## sensitivities

```
                                                       sensitivity  estimate_pct  ci_lo_pct  ci_hi_pct  shift_from_headline  station_months  stations                                                                                                                note
S1 commune-boundary variant, Lyon station outside the city removed        13.449      3.673     24.037               -0.212             407         8                                                          also serves as the check on that station's 2024 record gap
                                     S2 equal city-month weighting        13.740      5.346     22.817                0.079             516         9                                                     each represented city receives equal total weight in each month
                                   S3 longest-record stations only        13.449      2.755     24.693               -0.212             332         4                        FR04143, FR04055, FR20062, FR03043; Paris pair kept separate, each with its own fixed effect
                                  S4 earlier era only, to end 2019        13.744      4.865     24.755                0.083             320         5                    December 2019 still uses the replacement Paris station; the pandemic and later years are removed
                                       S5 pandemic months excluded        13.702      3.606     24.755                0.041             427         9                                                                                     March 2020 to June 2021 dropped
                                   S6 Olympics period, full window        13.704        NaN        NaN                  NaN             815         9 summer 2024 held separately, its own coefficient -9.86 percent; excluding those months instead gives +13.70 percent
                               S7 final year excluded, full window        13.706        NaN        NaN                  NaN             721         9               2025 carries a further restriction step and provisional fleet data; including it gives +13.71 percent
                                 S8 meteorology-only normalisation         9.516      3.456     15.372               -4.145             516         9                                            all time features removed; broad sensitivity rather than a leakage bound
                                    S9 surrounding-area comparison           NaN        NaN        NaN                  NaN             484         4                                                     descriptive path reported in P2; no common verified legal onset
```

## placebo_family

```
                                        placebo  coefficient  resampled_se  ratio as_large_as_headline                                                            sample  station_months
                   Paris start moved to 2014-01      -0.0564        0.0438  1.288                False                 before July 2017; precursor controlled separately             207
                   Paris start moved to 2015-01      -0.0400        0.0396  1.010                False                 before July 2017; precursor controlled separately             207
                   Paris start moved to 2016-01       0.0263        0.0629  0.418                False                 before July 2017; precursor controlled separately             207
Shared Lyon-Marseille onset, 2022-09 (not used)          NaN           NaN    NaN                  NaN both cities treated together, so there is no untreated comparison               0
  Lyon versus Marseille, invented start 2018-01       0.0847        0.0390  2.171                False            comparator cities through August 2022; neither treated             392
```

## roadside_increment_summary

```
     city  months  mean_log_increment     sd
Marseille     139              0.1878 0.0911
    Paris     148              0.2164 0.1040
```

## increment_did

```
                           quantity  estimate_pct  ci_lo_pct  ci_hi_pct  excludes_zero  analytic_se_log  bootstrap_se_log  usable_draws                                                               window                    construction  months  station_months
           July 2019 ring-road step        10.259     -6.852     28.779          False          0.06648           0.08279          2000                                          January 2013 to August 2022            full-history primary     116             207
June 2021 additional ring-road step         3.115    -17.623     22.397          False          0.04916           0.10061          2000                                          January 2013 to August 2022            full-history primary     116             207
           July 2019 ring-road step        10.259     -5.812     28.023          False          0.06491           0.07912          2000 January 2013 to December 2025 (Marseille confound after August 2022) full-history, extended endpoint     156             287
June 2021 additional ring-road step         0.533    -13.321     17.171          False          0.05407           0.07840          2000 January 2013 to December 2025 (Marseille confound after August 2022) full-history, extended endpoint     156             287
           July 2019 ring-road step        27.494     22.101     34.163           True          0.05235           0.02528          2000                                          January 2019 to August 2022          near-event sensitivity      44              81
June 2021 additional ring-road step         3.115     -7.599     10.783          False          0.04947           0.04683          2000                                          January 2019 to August 2022          near-event sensitivity      44              81
```

## roadside_increment_half_years

```
half_year  estimate_pct  ci_lo_pct  ci_hi_pct      role
  2013-H1        33.801     27.829     45.761      lead
  2013-H2         5.573     -9.509     17.448      lead
  2014-H1        22.148     14.954     35.934      lead
  2014-H2        40.338     34.320     48.687      lead
  2015-H1        20.864     16.934     27.357      lead
  2015-H2        20.415     15.672     32.402      lead
  2016-H1        27.936     21.394     60.284      lead
  2016-H2         9.626      5.817     24.295      lead
  2017-H1        -2.011     -5.223      3.168      lead
  2017-H2        13.931      9.435     20.940      lead
  2018-H1        16.756     12.886     22.846      lead
  2018-H2         2.534     -1.346     10.061      lead
  2019-H1         0.000      0.000      0.000 reference
  2019-H2        11.545      6.989     19.592      post
  2020-H1        27.697     21.105     34.349      post
  2020-H2        37.596     32.753     56.577      post
  2021-H1        29.721     25.378     36.452      post
  2021-H2        31.563     25.643     39.714      post
  2022-H1        33.882     29.402     40.657      post
  2022-H2        25.110      5.975     35.058      post
```

## roadside_increment_leads_test

```
 terms_tested  chi2_bootstrap  p_bootstrap
           12         573.995          0.0
```

## roadside_against_roadside

```
                           quantity  estimate_pct  ci_lo_pct  ci_hi_pct  excludes_zero  analytic_se_log  bootstrap_se_log  usable_draws     series                        window                    construction  months
           July 2019 ring-road step        15.526      2.730     31.441           True          0.03543           0.05884          2000 normalised   January 2013 to August 2022            full-history primary     102
June 2021 additional ring-road step        -3.839    -16.288     10.334          False          0.01279           0.06945          2000 normalised   January 2013 to August 2022            full-history primary     102
           July 2019 ring-road step        15.419      4.036     31.240           True          0.03505           0.05864          2000 normalised January 2013 to December 2025 full-history, extended endpoint     142
June 2021 additional ring-road step        -9.813    -20.508      0.859          False          0.02956           0.06026          2000 normalised January 2013 to December 2025 full-history, extended endpoint     142
           July 2019 ring-road step         5.646      2.827      9.329           True          0.01033           0.01634          2000 normalised   January 2019 to August 2022          near-event sensitivity      44
June 2021 additional ring-road step        -3.535     -7.502      0.601          False          0.01324           0.02097          2000 normalised   January 2019 to August 2022          near-event sensitivity      44
           July 2019 ring-road step        15.667     -2.582     42.221          False          0.06308           0.09355          2000        raw   January 2013 to August 2022            full-history primary     102
June 2021 additional ring-road step       -11.532    -29.102     10.964          False          0.03804           0.10994          2000        raw   January 2013 to August 2022            full-history primary     102
           July 2019 ring-road step        15.476     -0.685     40.953          False          0.06177           0.08742          2000        raw January 2013 to December 2025 full-history, extended endpoint     142
June 2021 additional ring-road step       -15.036    -30.779      0.073          False          0.03916           0.08896          2000        raw January 2013 to December 2025 full-history, extended endpoint     142
           July 2019 ring-road step         4.036    -13.464     22.218          False          0.06138           0.09061          2000        raw   January 2019 to August 2022          near-event sensitivity      44
June 2021 additional ring-road step       -11.784    -20.955      1.092          False          0.04308           0.06364          2000        raw   January 2019 to August 2022          near-event sensitivity      44
```

## roadside_direct_half_years

```
half_year  estimate_pct  ci_lo_pct  ci_hi_pct      role
  2013-H1        14.342      9.397     19.383      lead
  2013-H2        -4.958    -13.093      2.071      lead
  2014-H1       -10.522    -15.057     -2.808      lead
  2014-H2        -5.788    -11.754      0.734      lead
  2015-H1       -12.556    -16.332     -8.032      lead
  2015-H2        -3.585    -10.499      4.258      lead
  2016-H1       -10.107    -14.315     -4.606      lead
  2016-H2       -21.494    -27.358    -15.092      lead
  2017-H1       -24.788    -28.487    -21.135      lead
  2017-H2       -10.323    -15.975     -4.550      lead
  2018-H1        -4.773     -9.310     -0.008      lead
  2018-H2        -3.626     -9.789      2.541      lead
  2019-H1         0.000      0.000      0.000 reference
```

## roadside_direct_leads_test

```
 terms_tested  chi2_bootstrap  p_bootstrap
           12         456.534          0.0
```

## minimum_detectable_effects

```
                              design  bootstrap_se_log  mde_log  smallest_detectable_reduction_pct  station_months                                                                                                                           note
   Paris alone, before against after           0.04647  0.13011                             12.200              41 no comparator city; 1 station in the pre-window, so station effects are omitted as they would absorb the only station entirely
full design, weather-adjusted series           0.04340  0.12153                             11.444             162                                                                              three cities, station and common calendar effects
      full design, unadjusted series           0.10370  0.29035                             25.200             162                                               same design, other series; the pair measures what the weather modelling is worth
```

## run_summary

```
                          item                               value
                          mode                          normalised
                        commit                       a7b4d04-dirty
                          seed                                  42
               bootstrap draws                                2000
                      stations                                  11
   station-months, full record                                1113
station-months, primary sample                                 516
      pre-treatment assessment                   bounded reporting
            false-onset checks                4 usable, 1 not used
        main model coefficient             +13.66% [+5.48, +23.28]
                interpretation bounded by pre-treatment assessment
```

## leave_one_station_out

```
omitted      city  estimate_pct  change_from_main  station_months_left  stations_left                                                                                          status
FR20062      Lyon        14.256             0.595                  402              8                                                                                       estimated
FR03043 Marseille        13.954             0.293                  406              8                                                                                       estimated
FR20046      Lyon        13.449            -0.212                  407              8                                                                                       estimated
FR20017      Lyon        13.658            -0.003                  489              8                                                                                       estimated
FR03014 Marseille        13.663             0.002                  484              8                                                                                       estimated
FR04055     Paris        13.662             0.001                  486              8                                                                                       estimated
FR04004     Paris        13.661            -0.000                  508              8                                                                                       estimated
FR04131     Paris        13.661             0.000                  508              8                                                                                       estimated
FR04143     Paris           NaN               NaN                  438              8 not estimable: exog does not have full column rank. If you wish to proceed with model estimatio
```

## leave_one_station_out_intervals

```
    quantity  estimate_pct  ci_lo_pct  ci_hi_pct  excludes_zero  analytic_se_log  bootstrap_se_log  usable_draws omitted      city
Omit FR20062        14.256      5.828     23.187           True          0.05160           0.03832          2000 FR20062      Lyon
Omit FR03043        13.954      6.222     26.747           True          0.05715           0.04543          2000 FR03043 Marseille
Omit FR20046        13.449      3.673     24.037           True          0.06835           0.04706          2000 FR20046      Lyon
```

## exploratory_surrounding_area_path

```
half_year  paris_proper_pct  surrounding_area_pct  difference        period
  2013-H1           -17.699                -4.898      12.801 before launch
  2013-H2           -20.477               -16.356       4.121 before launch
  2014-H1           -17.803                -5.337      12.466 before launch
  2014-H2           -27.292               -21.284       6.008 before launch
  2015-H1           -25.700               -11.020      14.680 before launch
  2015-H2           -25.890               -17.102       8.788 before launch
  2016-H1           -20.151                -6.866      13.285 before launch
  2016-H2           -26.034               -22.999       3.035 before launch
  2017-H1           -18.002                -9.347       8.655 before launch
  2017-H2           -19.125               -19.160      -0.035 before launch
  2018-H1           -10.077                -3.031       7.046 before launch
  2018-H2           -15.922               -14.651       1.271 before launch
  2019-H1             0.000                 0.000       0.000     reference
  2019-H2            -6.775               -11.361      -4.586   launch half
  2020-H1            32.743                 3.094     -29.649  after launch
  2020-H2            12.872                -9.097     -21.969  after launch
  2021-H1            27.821                -0.175     -27.996  after launch
  2021-H2            17.772               -11.321     -29.093  after launch
  2022-H1            21.300                -6.736     -28.036  after launch
  2022-H2            25.113               -23.338     -48.451  after launch
```

## s1_s3_reproducibility_check

```
sensitivity  estimate_pct_full_precision  station_months  stations
         S1                    13.449054             407         8
         S3                    13.448616             332         4
```

## Notes

- Panel built in normalised mode: 1113 station-months, 11 stations, 2013-01 to 2025-12.
- Largest unknown-class share: 4.98e-05; largest count: 10 vehicles.
- Dose is the share of the local private-car fleet in classes banned in that station's perimeter, reported per ten percentage points in the models. Stations outside a restricted perimeter carry zero throughout. Fleet figures are final through the 2023 edition and provisional after.
- The Paris dose at each step is the sum of the shares marked banned. Reading the two years together shows how much comes from adding a class and how much from the fleet having turned over in between.
- The fitted weather adjustment is not flagged by this 5% screening test. This does not prove that treatment information is absent.
- S8 separately checks sensitivity to the time features in the weather models.
- Pre-window bootstrap: 86.5% same-month donor, 13.5% same-station donor-year fallback, 0.0% station-pool fallback; residual scale 1.1818; 2000 of 2000 fits used.
- Paris contributes 1 background station(s) to the pre-treatment window (FR04143), against 3 across the comparators, so the Paris side of this gap is the less precisely estimated of the two.
- Event study bootstrap: 74.8% same-month donor, 6.5% same-station donor-year fallback, 18.7% station-pool fallback; residual scale 1.1762; 2000 of 2000 fits used.
- The leads test is a screening rule. A result above 5% does not prove that the pre-treatment paths were parallel.
- Unexplained monthly movement is correlated across the cities, 0.58 to 0.81, weakest between the two furthest apart. That is consistent with regional episodes reaching all three together, which is what the comparison assumes; it is supporting evidence rather than proof.
- Primary estimate bootstrap: 74.8% same-month donor, 6.5% same-station donor-year fallback, 18.7% station-pool fallback; residual scale 1.1503; 2000 of 2000 fits used.
- The pre-treatment assessment is bounded. This coefficient is shown as a model output, not as a stand-alone causal answer.
- Precursor segment (mid-2016 to mid-2017) held separately: +0.13 percent, standard error 0.0491. It is not part of the main estimate and is reported so the period is visibly accounted for rather than absorbed into either side of the comparison.
- Both inference methods agree on whether the effect is distinguishable from zero.
- Half-yearly estimates: 6 before the restriction, 2 covering the earlier partial measure, 11 after. Mean after +35.00 percent, range +1.28 to +66.24.
- City-specific dose model bootstrap: 70.5% same-month donor, 3.3% same-station donor-year fallback, 26.3% station-pool fallback; residual scale 1.1215; 2000 of 2000 fits used.
- The city-specific coefficients allow different dose associations. The pooled coefficient imposes one common association and is shown only as a comparison.
- Across the selected stations, the average monthly fitted-component variation is 0.81% to 0.84% of the station level. This is a model-stability diagnostic, not an adjustment to the panel interval.
- Equal city-month weighting: Paris contributes 8 of 12 months in 2019. Missing month numbers: [2, 9, 10, 11].
- Meteorology-only estimate +9.52% versus main-model estimate +13.66%; difference -4.14 percentage points.
- No scalar treatment coefficient is estimated for the surrounding-area panel because the included communes do not share one verified onset.
- Across the 6 variants with a comparable estimate, the main-model estimate of +13.66 percent moves at most -4.14 points, under 'S8 meteorology-only normalisation'. Unavailable variants are listed with the reason.
- Main-model comparison ratio: +0.1280 / 0.0398 = 3.21.
- The primary mechanism window ends before Marseille's restriction. The full-window coefficients may be affected by Marseille's treated background area. The joint lead test governs interpretation: rejection means that the mechanism coefficients remain supporting rather than causal, even if an interval excludes zero.
- Only one roadside station is available in each city, so site-specific changes cannot be separated from changes in traffic. The direct lead test must also be considered before interpreting the step estimates. A rejected lead test makes the coefficients supporting rather than causal.
- The full design detects a reduction of 11.4 percent on the better of the two series against 25.2 percent on the other, so the weather modelling changes what is detectable by 13.8 percentage points. Paris alone, without a comparator, needs 12.2 percent.
- The results files are written after the exploratory diagnostics below.