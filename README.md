# esprima-custom-keywords
Fork of esprima, which allows to use custom keywords

> *SPOILER* This fork is unlinked from original esprima repository
> and not using UMD format, one could be added easily though.

## Usage

This module is distributed via npm, run `npm i esprima-custom-keywords` just where you need it.
The main change against origin esprima is new method `setKeywords` which accepts good old JO with following structure:
`KEY: value`

```javascript
var esprima = require('esprima-custom-keywords');
esprima.setKeywords({...});

...

esprima.tokenize(sourceWithCustomKeywords);
```

## List of required keywords
As this fork uses cutom keywords, they should be explicitely defined before any parsing call.
This could be done in any way you like it, just pass the constructed set to `#setKeywords` method.
Default JS Keywords subset will look like following giantic list:
```txt
{ 
  VAR: 'var',
  LET: 'let',
  CONST: 'const',
  FOR: 'for',
  IF: 'if',
  ELSE: 'else',
  SWITCH: 'switch',
  CASE: 'case',
  BREAK: 'break',
  DEFAULT: 'default',
  TRY: 'try',
  CATCH: 'catch',
  FINALLY: 'finally',
  WHILE: 'while',
  DO: 'do',
  FUNCTION: 'function',
  THIS: 'this',
  RETURN: 'return',
  CONTINUE: 'continue',
  DELETE: 'delete',
  WITH: 'with',
  IN: 'in',
  OF: 'of',
  AS: 'as',
  NEW: 'new',
  THROW: 'throw',
  ENUM: 'enum',
  EXPORT: 'export',
  IMPORT: 'import',
  SUPER: 'super',
  IMPLEMENTS: 'implements',
  INTERFACE: 'interface',
  PACKAGE: 'package',
  VOID: 'void',
  CLASS: 'class',
  EXTENDS: 'extends',
  PRIVATE: 'private',
  PROTECTED: 'protected',
  PUBLIC: 'public',
  STATIC: 'static',
  YIELD: 'yield',
  EVAL: 'eval',
  ARGUMENTS: 'arguments',
  TRUE: 'true',
  FALSE: 'false',
  NULL: 'null',
  TYPEOF: 'typeof',
  INSTANCEOF: 'instanceof',
  DEBUGGER: 'debugger',
  FROM: 'from'
}
```
