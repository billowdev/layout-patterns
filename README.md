# layout-patterns


```
Table LanguagePattern {
  id int [pk, increment] // Primary Key
  name varchar
  description text
  created_at timestamp
  updated_at timestamp
}

Table CSSProperty {
  id int [pk, increment] // Primary Key
  name varchar
  value varchar
  description text
}

Table HTMLTemplate {
  id int [pk, increment] // Primary Key
  name varchar
  description text
  created_at timestamp
  updated_at timestamp
}

Table PatternCSSMapping {
  id int [pk, increment] // Primary Key
  pattern_id int [ref: > LanguagePattern.id] // Foreign Key to LanguagePattern
  css_property_id int [ref: > CSSProperty.id] // Foreign Key to CSSProperty
}

Table TemplatePatternMapping {
  id int [pk, increment] // Primary Key
  template_id int [ref: > HTMLTemplate.id] // Foreign Key to HTMLTemplate
  pattern_id int [ref: > LanguagePattern.id] // Foreign Key to LanguagePattern
}

```
