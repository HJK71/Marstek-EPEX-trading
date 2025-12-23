# Marstek-EPEX-trading
Charge you're Marstek's at the lowest price and discharge at the highest price
******************************************************************************
Make sure you install the following applications:
Installation via HACS:
• Cheapest hours
• custom-gauge-card
• markdown card
• Card mod
• dynamic energy prices from Zonneplan, Tibber or any provider that suites you.
*******************************************************************************
Create package file
Make a new file under packages, i.e "Marstek_epex.Yaml"
Paste the packagefile code into it.
Make sure you have something like this in you're configuration.yaml: 
#packages#
homeassistant:
  packages: !include_dir_named packages
******************************************************************************  
Add a manual card to you're dashboard and paste the lovelace code in it.
Make another manual card and paste the debug code in it. (only for test purposes)
******************************************************************************
User manual:

Settings:

1. Epex trading active: batteries charge and discharge based on dynamic rates (default Zonneplan). For other providers, replace Zonneplan string with your own provider. See also the manual for “Cheapest hours.”

2.    Revenue loss: adjustable, but at 2000 Watt charging and 2300 Watt discharging, this is around 20%. Default setting is 18%

3.    Revenue loss this month: the average revenue loss of your battery this month. This can increase when you are not running in EPEX mode!

4. Depreciation: battery wear costs are based on a lifespan of 6000 cycles. 6000x5Kwh/purchase price. With a purchase price of around 1300-1400 euros, this will be around 5 cents. Default setting is 5 cents, but this can be adjusted.

5.    Maximum charging price: when day trading is not profitable, it can still be useful to fully charge the battery at a good price. Default 15 cents. Adjustable at your discretion.

6.    Minimum discharge price: when day trading is not profitable, it can still be useful to discharge the battery (provided it is charged) at an attractive price. The default setting is 40 cents, but this can be adjusted as desired.

7. Daily returns: discharge price x discharge consumption – charge price x charge consumption. This is the daily return, taking losses into account, but excluding depreciation costs.

8. Total returns: same as above, but for the entire battery life.


