# custom-controls (obsolete)

> [!IMPORTANT]
> **This repository is no longer maintained. Its successor is
> [abap2UI5-addons/custom-controls](https://github.com/abap2UI5-addons/custom-controls).**

The controls here are still installable, but they receive no fixes. Everything
in this repository was ported to the successor: the spreadsheet export as
`ExportSpreadsheet`, and the favicon is now part of abap2UI5 itself
(`z2ui5_cl_xml_view_cc=>favicon( )`) and needs no addon at all.

#### Why the successor is better

* **The JavaScript is real UI5 code, not an ABAP string literal.** Here every
  control ships as JS embedded in ABAP and injected into each view that uses it.
  In the successor the controls live in their own BSP (`Z2UI5CC`), generated
  from plain `.js` files — so they are syntax-checked in CI, editable in an
  editor, loaded once by the browser and cached, instead of travelling with
  every view again.
* **They behave like ordinary controls.** One builder class per control, one
  `render( )` call, properties bind two-way and events arrive in `on_event` just
  like for `sap.m` controls.
* **External libraries are loaded on demand** (Chart.js, bwip-js, driver.js,
  Font Awesome, animate.css, ImageMapster) from a URL you can override, so
  systems without internet access can serve them from their own BSP.
* **More controls, one place.** Nine controls, including everything from the old
  [js-libraries](https://github.com/abap2UI5-addons/js-libraries-obsolet)
  repository — signature pad, spreadsheet export, form validation, charts,
  barcodes, product tours, Font Awesome, animations and clickable image maps.

#### What was here

#### Favicon
<img width="800" alt="image" src="https://github.com/user-attachments/assets/a4dbaeee-071e-4b1c-b701-b37799d97d1a">

#### Spreadsheet (xlsx)
<img width="800" alt="image" src="https://github.com/user-attachments/assets/4fb90a2b-feb9-46ae-98e2-d9974505619f">
