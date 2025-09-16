- always derive and include tags in the article
- always end the article with `<!--more-->`, so it doesn't truncate
- include links to the pota website for parks
- include links to images recursively found
  in the `static/img` folder that will match by date.
  the links should be formatted with the gallery widget.
  here's an example:
  ```
  {{< gallery >}}
  {{< figure link="/img/2025/2025-05-18-pota-setup.jpg" caption="Setup" >}}
  {{< figure link="/img/2025/2025-05-18-pota-pole.jpg" caption="Pole spike" >}}
  {{< figure link="/img/2025/2025-05-18-pota-antenna.jpg" caption="Antenna" >}}
  {{< /gallery >}}
  ```
- in markdown lists, include only one space after the bullet
