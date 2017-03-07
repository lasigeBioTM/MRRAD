## Commands used to run NOBLE Coder:

```$ java -jar NobleCoder-1.0.jar -terminology radlex -input [portuguese reports path] -output [output path] -search all-match```

```$ java -jar NobleCoder-1.0.jar -terminology radlex -input [portuguese reports path] -output [output path] -search best-match```

## Uploading RadLex ontology to NOBLE

The RadLex ontology .owl file had to be edited before it could be correctly processed and uploaded to NOBLE Coder. In the original .owl file the properties  "Preferred_name" and "Synonym" are considered to be DatatypeProperty and this had to be changed to AnnotationProperty. That is, where in the file was

```xml
<owl:DatatypeProperty rdf:ID="Preferred_name">
</owl:DatatypeProperty>
```

It was changed to:

```xml
<owl:AnnotationProperty rdf:ID="Preferred_name">
</owl:AnnotationProperty>
```

And the analogous thing for the "Synonym" property.
