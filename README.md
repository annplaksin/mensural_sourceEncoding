# mensural_sourceEncoding

This repository contains a customization of MEI to facilitate a descriptive encoding of 
mensural music sources. It combines the MEI Mensural customization with the approach of 
a page-based data structure as it is used by [Verovio](https://www.verovio.org/structure.xhtml).

To display the choir book layout, an additional element `<panel>` has been included, as well as a 
container for lyrics within a system.
All newly added elements and attributes belong to a new namespace (url of this repo).

Example:
```xml
<body>
  <mdiv type="section">
    <pages>
      <page>
        <mse:panel n="1" type="part">
          <system n="1">
            <staff>
              <layer>
                <!-- ... -->
              </layer>
            </staff>
            <lyrics>
              <verse>
                <syl></syl>
              </verse>
            </lyrics>
          </system>
        </mse:panel>
      </page>
    </pages>
  </mdiv>
</body>  
```

The compiled ODD and Relax NG schema has been created with MEI 3.0.0.