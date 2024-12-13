```toml
date = "2024-12-13"
giscus = "Stereo Imager (BGZg)"
```

# Learn - Grid - Stereo Imager

[To the patch](../../effects/stereo_imager.md)

<video controls autoplay loop muted data-dir="right" data-px="350px" class="sp-inline-float">
  <source src="stereo_imager/build.mp4" type="video/mp4">
</video>

<!--Abgesehen von der Visualisierung ist ein `Stereo Imager` in Bitwig äusserst leicht zu entwerfen. In einem `FX Grid` schliesst man zunächst ein `Sum` Module an das `Audio Out` Module an, dann fügt man ein `Crossover-3` Module dem `Audio In` Module hinzu. Jedem `Band` Ausgang des `Crossover-3` Modules hängt man jeweils ein `Stereo Width` Module an. Zu guter Letzt verbindet man alle Ausgänge der `Stereo Width` Module mit dem `Sum` Module. Im Handumdrehen ist der `Stereo Imager` gebaut.-->

Apart from visualization, a `Stereo Imager` is extremely easy to design in Bitwig. In an `FX Grid`, first connect a `Sum` module to the `Audio Out` module, then add a `Crossover-3` module to the `Audio In` module. Attach a `Stereo Width` module to each `Band` output of the `Crossover-3` module. Finally, connect all the outputs of the `Stereo Width` modules to the `Sum` module. In no time at all, the `Stereo Imager` is built.

## Mode of Operation
 
<!--Die Eigenschaft des `Crossover-3` Modules, dass die aufgeteilten Frequenzbänder sich ohne Verluste oder Überlappungen nahtlos zusammenfügen lassen, erlaubt es die wahrgenommene spatiale Breite jedes Bandes einzeln anzupassen, ohne dass es zu Verzerrungen des Klangs kommt. Der Klang wird originalgetreu wiederhergestellt.-->

The property of the `Crossover-3` module, which allows the split frequency bands to seamlessly recombine without losses or overlaps, makes it possible to adjust the perceived spatial width of each band individually without causing sound distortions. The sound is faithfully reproduced.

<video controls autoplay loop muted>
  <source src="stereo_imager/reconstruct.mp4" type="video/mp4">
</video>