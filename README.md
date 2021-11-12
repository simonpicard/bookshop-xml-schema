# bookshop-xml-schema

## Context

A bookshop wants to record its information in XML format. The bookshop consists of two departments:
1. A departement ”scientific products” offering:
    - _scientific books._ For each scientific book, its title, a list of all authors or a list of editors (but not both), publisher, and year of publication must be mentioned. Optionally, a scientific book can also be specified an abstract, an edition, and ISBN number.
    - _scientific journals._ For each scientific journal, the title, volume, number, lits of editors or list of authors (but not both), and year of publication should be mentioned. Optionally, the publisher and impact factor can be mentioned. If an impact factor is mentioned, it should be accompanied with the year in which the impact factor is valid. In addition, for each journal a table of contents listing all the articles in the journal (with the title, list of authors, and start page, end page) should be mentioned. Optionally, the (start page, end page) pair may be replaced by simply mentioning the article number.
1. A departement “leisure products” containing:
    - _leisure books._ For each leisure book, its title, list of all authors, publisher, year of publication must be mentioned, as well as its genre (possible values for genre are limited to ”thriller”, ”horror”, ”sci/fi”, ”romance”, and ”literature”). Optionally, a leisure book can also be specified by an edition and the number of pages that the book contains.
    - _leisure periodicals._ For each leisure periodical, its title, price, and publisher must be mentioned.

## Goal

Devise a way to represent the above information (including the division in departments) in XML. Define an accompanying XML Schema Definition, taking into account the required/optional fields above. Use the schema specialization where possible. Both the scientific books and the leisure books should be represented by the <book> tag. Define the “genre” field using attributes. Make sure to put all the bookshop-specific elements in a namespace.

## Results

__XML model__: `src/model.xml`
__XSD specifications__: `src/model.xsd`
__XML example__: `src/test.xml`