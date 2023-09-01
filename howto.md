## Changing Nozzles

You can follow the instructions on [this page](https://help.prusa3d.com/article/changing-replacing-the-nozzle-mini_134235). Take extreme caution. Personally, I keep the hotend hot throughout the whole process.

Here is the crucial points:

1. Heat the heatblock _above_ your normal printing temperature. Example, if the hottest material you print is PETG, printed at 245C, heat the heatblock to 265C at the very least.
2. You tighten the ${\normalsize{\textcolor{green}{\texttt{nozzle}}}}$ against the ${\normalsize{\textcolor{green}{\texttt{heatbreak}}}}$, _not_ the ${\normalsize{\textcolor{red}{\texttt{heatblock}}}}$. You can make this happen by controlling how much you thread the heatbreak into the heatblock. If you've done things correctly, at the end, when everything has been tightened, there will be a gap between the nozzle and the heatblock. Aim for about 0.5mm, but the exact length of the gap is not important.
3. Do not overtighten because you will stripe threads or break the nozzle. A [torque wrench](https://www.thingiverse.com/thing:4738816) is highly recommended; you want roughly 1-1.5N\*m of torque..

<div align='center'>
    <img src="./images/heatblock/nozzle-heatblock-gap.jpg" height="200" alt='hotend'/>
    <img src="./images/nozzle-gap.jpg" height="200" alt='hotend'/>
</div>

## Calibrate Esteps

[This part](https://thangs.com/designer/MihaiDesigns/3d-model/Extruder%20E-steps%20calibration%20tool-47802) is useful in this process, though not necessary.

1. Prepare extruder

```
M83
```

2. Extrude 100mm in 60 seconds

```
G1 E100 F100
```

3. Formula

```
New Config Value = Old Config Value * (Actual Extruded Amount/Target Extruded Amount)
```

[Back](./README.md#heatblock)
