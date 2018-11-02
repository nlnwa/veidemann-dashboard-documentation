---
title: "Schedule"
weight: 3
---

{{% notice info %}}
Used by [crawljob](../crawljob)
{{% /notice %}}


[metadata](../#veidemann-meta).  


![schedule overview](/img/schedule/veidemann_dashboard_crawlscheduleconfig.png)



Field                              | Function
-----------------------------------|-------------------------------
[Minute](#cron-exp-minute)         | 
[Hour](#cron-exp-hour)             | 
[Dom](#cron-exo-dom)               | 
[Month](#cron-exp-month)           | 
[Dow](#cron-exp-dow)               | 
[Valid from](#schedule-valid-from) | 
[Valid to](#schedule-valid-to)   | 




### Cron 
--------

<pre> 
<b style="color: green"> * * * * * </b>  Uttrykk
 | | | | |
 | | | | |___________ Day of week
 | | | |
 | | | |_____________ Month
 | | |
 | | |_______________ Day of month
 | |
 | |_________________ Hour
 |
 |___________________ Minute

</pre>  
    
* Wildcard (__*__):   
<pre>
  <b style="color: green">* * * * * </b>  means:
</pre>  

* Comma (__,__): 
  <pre>
  <b style="color: green">59 11 * * 1,2,3,4,5 </b>
  </pre>  

* Slash (__/__): 
Could be used as &ast;/c og a-b/c.  
<pre>
  <b style="color: green">*/5 * * * *</b>
  
  (0:00, 0:05, 0:10, 0:15 etc.).  
  <b style="color: green">3-18/ 5 * * * *</b>
    
  (0:03, 0:08, 0:13, 0:18, 1:03, 1:08 etc.). 
</pre>

#### Minute {#cron-exp-minute}
--------------------------------


{{% notice note %}}
Example:
{{% /notice %}}

<pre>
<b style="color: green">5 * * * *</b>
  

<b style="color: green">* * * * *</b>
</pre>



#### Hour {#cron-exp-hour}
--------------------------
{{% notice note %}}
Example:
{{% /notice %}}

<pre>
<b style="color: green">* 12 * * Mon</b>  


</pre>

#### Day of month {#cron-exp-dom}
-------------------------------

{{% notice note %}}
Example:
{{% /notice %}}

<pre>
<b style="color: green">* 12 1-15,17,20-25 * *</b>  

<b style="color: green">* 12 10-16/2 * *</b>  

</pre>


#### Month {#cron-exp-month}
----------------------------

{{% notice note %}}
Example:
{{% /notice %}}

<pre>
<b style="color: green">0 12 1 1,sep-dec *</b>
</pre>

#### Day of week {#cron-exp-dow}
------------------------------

{{% notice note %}}
Example:
{{% /notice %}}

<pre>
<b style="color: green">59 11 * * 1,2,3,4,5</b>  
  
<b style="color: green">59 11 * * 1-5</b>  

Same as above.
</pre>

### Valid from/to
------------------

{{% notice info %}}
All dates are given in <b>UTC</b>
{{% /notice %}}

![valid from datepicker](/img/schedule/veidemann_dashboard_schedule_validfrom.png)