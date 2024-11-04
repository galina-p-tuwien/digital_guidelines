# Digital Guidelines
This document contains additional data supporting the Paper “Digitalising Guidelines: Requirement Definition and Compliance Enforcement in BIM Models”. The presented use cases demonstrate our method for the generation and application of digital guidelines in the AEC industry.

## Use Cases Based On the ISO 6946:2017, Section 6.7.2

It is to be noted that Section 6.7.2 describes a simplified method for the calculation of the total thermal resistance of a building component. This method is based on one typical part of the component, not on the entire component. For detailed calculations taking thermal bridges into account there is the ISO 10211. 

![Walls](/UC0_walls_.png)

*Fig.1. Typical wall footprints: (a) massive timber with an insulation layer, (b) acoustically decoupled wall with armed concrete inner shell, timber outer shell, and mineral wool as thermal insulation and acoustic dampener.*

Fig.1 demonstrates the difference between the entire construction, e.g., wall, and a representative, or typical, part. For example, Fig.1(a) shows a 0.40m section of the wall that contains both a timber column and the insulation between two columns. This section represents the inhomogeneous layer with the correct ratio of materials, which is enough for the application of the guideline. Fig.1(b) shows a more complex construction with three inhomogeneous layers. The representative section here is larger, 1.00m long, since it requires all combinations of inhomogeneities to be accounted for.

![Wall decomposition](/UC0_wall_decomposition_.png)

*Fig.2. Wall decomposition: (b) in geometric profiles, (c) in cells according to ISO 6946:2017, Section 6.7.2.*

The next question is one of modelling. Fig.2 shows the different ways the wall from Fig.1(b) can be decomposed into model elements. The model in Fig.2(b) groups adjacent elements of the same material, while the model in Fig.2(c) decomposes the typical section in layers and sections in accordance with ISO 6946:2017, Section 6.7.2.2, Figure 1. Consequently, the two approaches produce models of vastly different sizes.

However, a model resulting from Fig.2(b) can be adapted to fulfil the requirements of the model resulting from Fig.2(c). We will demonstrate this by applying the template we presented in the referenced paper (see also Fig.3) to the following four use cases:
- **Use Case 1**: Very small generic data model, allowing significant modification. A step-by-step application.
- **Use Case 2**: Small generic data model, simple example, allowing modification.
- **Use Case 3**: Small generic data model, complex example, not suitable for modification.
- **Use Case 4**: IFC, simple example, allowing modification.


![Templates](/UC4/iso6946_templates.png)
*Fig.3. The applicable templates as constructed in the accompanying paper.*

### Use Case 1: A Step By Step Application of ISO 6946:2017, Section 6.7.2

![UC4 Initial Situation](UC4/UCx4_1small.png)

*Fig.3. The initial situation: (a) the inhomogeneous wall and (b) the data model.*

![UC4 Original Model](UC4/UCx4_2.png)
*Fig.4. The initial instantiation of the data model in Fig.3(b), consisting of two wall elements and four profile elements.*

![UC4 Defining a Section](UC4/UCx4_3.png)
*Fig.5. Applying the SECTION template to a single existing element.*

![UC4 Defining a Cell](UC4/UCx4_4.png)
*Fig.6. Applying the CELL template to two existing elements.*

![UC4 Defining a Layer](UC4/UCx4_5.png)
*Fig.7. Applying the LAYER template by creating new elements and attaching them to existing ones.*

![UC4 Defining the Cumulative](UC4/UCx4_6.png)
*Fig.8. Applying the CUMULATIVE template to an existing element and extending it by two further elements.*

![UC4 Re-calculations](UC4/UCx4_7.png)
*Fig.9. Adding a calculation to fulfil a condition attached to the SECTION template.*

![UC4 Final Model](UC4/UCx4_8.png)
*Fig.10. The final result of applying the template.*

### Use Case 2: ISO 6946:2017, Section 6.7.2 applied to a Generic Data Model

The second use case involves the modelling of the wall presented in Fig.1(a). We have chosen a fairly generic data model that could represent the architect’s view. It is shown in the box in Fig.3(a). Abstract type *Element* can have *Data* attached to it.

![Class and Object Diagrams](/UC1_01b.png)
*Fig.3. A generic data model (a) and one possible instantiation (b).*

![Adapted Model](/UC1_02.png)
*Fig.4. The adapted model.*

![Adapted Model w Connectivity](/UC1_03.png)
*Fig.5. The adapted model with full connectivity.*

### Use Case 2: ISO 6946:2017, Section 6.7.2 applied to an unsuitable model

![Class and Object Diagrams](/UC3_01.png)
*Fig.6. The wall construction (a), the corresponding data model (b) and one possible instantiation (c).*

![Adapted Model](/UC3_02.png)
*Fig.7. Model adaptation: step 1.*

![Full Adapted Model](/UC3_03.png)
*Fig.8. Model adaptation: step 2.*

### Use Case 3: ISO 6946:2017, Section 6.7.2 applied to an IFC Model

![Typical IFC Wall](/UC2_01.png)
*Fig.9 An IFC wall with a layered structure.*

![IFC Wall w Profiles](/UC2_02.png)
*Fig.10 An IFC wall with a profile structure.*

![IFC Wall ISO 6946](/UC2_03.png)
*Fig.11 An IFC wall adapted for calculating its thermal conductivity according to ISO 6946:2017, Section 6.7.2.*



