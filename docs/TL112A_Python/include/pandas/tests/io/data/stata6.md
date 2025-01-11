---
layout: default
title: stata6
nav_order: 29
parent: Python (TL112A)
---
{% raw %}
| byte\_ | int\_  | long\_      | float\_              | double\_             | date_td    | string\_                                                                                                                                                                                                                                             | string_1 |
|--------|--------|-------------|----------------------|----------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------|
| 0      | 0      | 0           | 0                    | 0                    | 1960-01-01 | a                                                                                                                                                                                                                                                    | a        |
| 1      | 1      | 1           | 1                    | 1                    | 3014-12-31 | ab                                                                                                                                                                                                                                                   | b        |
| -1     | -1     | -1          | -1                   | -1                   | 2014-12-31 | abc                                                                                                                                                                                                                                                  | c        |
| 100    | 32740  | -2147483647 | -1.7010000002777e+38 | -2.000000000000e+307 | 1970-01-01 | This string has 244 characters, so that ir is the maximum length permitted by Stata. This string has 244 characters, so that ir is the maximum length permitted by Stata. This string has 244 characters, so that ir is the maximum length permitted | d        |
| -127   | -32767 | 2147483620  | 1.7010000002777e+38  | 8.000000000000e+307  | 1970-01-02 | abcdefghijklmnopqrstuvwxyz                                                                                                                                                                                                                           | e        |

{% endraw %}