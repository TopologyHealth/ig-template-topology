# Topology FHIR IG Template

This is the template for FHIR IGs created by Topology Health.

## Installation

### 1. Copy to Your IG Template Folder

Copy this entire repository into a `topology-template` folder of your FHIR IG project:

```bash
cp -r . /path/to/your-ig/topology-template/
```

### 2. Reference in ig.ini

Add the following line to your `ig.ini` file:

```ini
template = topology.base.template
```

The template folder will load the base FHIR template in the `template` folder and overwrite the necessary components with the `topology-template` when you conduct the build of your IG.

### 3. Building Your IG

After setting up the template, build your IG using the FHIR IG Publisher:

```bash
# Using the FHIR IG Publisher
java -jar publisher.jar -ig .

# Or using the provided scripts
./scripts/ant.xml
```

> Note there is no published in this repo. You will need to create an IG to use this template.

## File Structure

```
template/
├── content/assets/          # CSS, JavaScript, images, fonts
├── includes/               # HTML fragments and templates
├── layouts/                # Page layout templates
├── liquid/                 # Liquid template files
├── scripts/                # Build and processing scripts
└── config/                 # Configuration files
```

## Customization

The template uses CSS custom properties for easy theming:

```css
:root {
  --navbar-bg-color: #222373;    /* Main banner color - Topology Blue*/ 
  --btn-hover-color: #e7bad7;    /* Accent color - Topology Pink*/
  --stripe-bg-color: #e7bad7;    /* Header strip color - Topology Pink*/
}
```

## Help

For questions or issues with this template:

- Check the [FHIR IG Publisher documentation](https://confluence.hl7.org/display/FHIR/IG+Publisher+Documentation)
- Review the [HL7 IG Template Guide](https://confluence.hl7.org/display/FHIR/Implementation+Guide+Template+Guide)

## License

The Topology IG Template is based on the [HL7 template](https://github.com/HL7/ig-template-base).

This template is copyright Topology Health 2025.

## Version

Current version: 0.1.0

---

**Author**: [Topology Health](http://topology.health)  
**Canonical**: <http://topology.health/templates/topology.base.template>
