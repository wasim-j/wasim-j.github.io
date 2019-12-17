[UP](./index.md)

# &lt;meta&gt;
Represents metadata that cannot be represented by other HTML meta-related elements

syntax:

	<meta charset="UTF-8"></meta>
	<meta http-equiv="" content=""></meta>
	<meta name="" content=""></meta>

## Properties

### http-equiv related
The attribute is named http-equiv(alent) because all the allowed values are names of particular HTTP headers:
- "content-security-policy"
- "refresh"

### name related
This attribute defines the name of a piece of document-level metadata. It should not be set if one of the attributes itemprop, http-equiv or charset is also set.
- application-name
- author
- description
- generator
- keywords
- referrer
- creator
- googlebot
- publisher
- robots
- slurp
- [viewport](./viewport.md)