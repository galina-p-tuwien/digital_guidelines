# Digital Guidelines
This document contains additional data supporting the Paper “Digitalising Guidelines: Requirement Definition and Compliance Enforcement in BIM Models”. The presented use cases demonstrate our method for the generation and application of digital guidelines in the AEC industry.

## Use Cases Based On the ISO 6946:2017, Section 6.7.2

It is to be noted that Section 6.7.2 describes a simplified method for the calculation of the total thermal resistance of a building component. This method is based on one typical part of the component, not on the entire component. For detailed calculations taking thermal bridges into account there is the ISO 10211. 

![Walls](/UC0_walls_.png)

*Fig.1. Typical wall footprints: (a) massive timber with an insulation layer, (b) acoustically decoupled wall with armed concrete inner shell, timber outer shell, and mineral wool as thermal insulation and acoustic dampener.*

![Wall decomposition](/UC0_wall_decomposition_.png)

*Fig.2. Wall decomposition: (b) in geometric profiles, (c) in cells according to ISO 6946:2017, Section 6.7.2.*

### Use Case 1: ISO 6946:2017, Section 6.7.2 applied to a Generic Data Model

![Class and Object Diagrams](/UC1_01b.png)
*Fig.3. A generic data model (a) and one possible instantiation (b).*

![Adapted Model](/UC1_02.png)
*Fig.4. The adapted model.*

![Adapted Model w Connectivity](/UC1_03.png)
*Fig.5. The adapted model with full connectivity.*

### Use Case 1: ISO 6946:2017, Section 6.7.2 applied to an IFC Model

![Typical IFC Wall](/UC2_01.png)
*Fig.6 An IFC wall with a layered structure.*

![IFC Wall w Profiles](/UC2_02.png)
*Fig.7 An IFC wall with a profile structure.*

![IFC Wall ISO 6946](/UC2_03.png)
*Fig.8 An IFC wall adapted for calculating its thermal conductivity according to ISO 6946:2017, Section 6.7.2.*

