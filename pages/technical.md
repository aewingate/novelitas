---
title: Technical Documentation
layout: about
permalink: /technical.html
# Edit the markdown on in this file to describe your collection
# Look in _includes/feature for options to easily add features to the page
---
# Technical Documentation
{% include feature/nav-menu.html sections="Items Chosen;Imaging Standards;Metadata Standards;" %}
## Items Chosen
The items selected for imaging were chosen because they were already owned by the creator of this site, and the publications are all in the public domain. All items in the collection have been fully digitized and they have received OCR treatment using ABBYY FineReader 15. This means that all of the PDF files are searchable, both within the files themselves and using the search bar of the site (you will have to open the PDF file to view the text, however). Due to time constraints, the OCR has not been corrected, but the quality of the OCR is generally quite good despite the fact that the print quality is somewhat poor.  
## Imaging Standards
The pamphlet novels were photographed using a home set up due to the ongoing COVID-19 pandemic. Items were placed on a black book cushion and lit from above using a lamp covered with parchment paper to diffuse the light (see photo). The actual photos were taken with the Camera app of an iPad Pro. These photos are 72dpi.  

The photos were then transferred to a laptop and perspective cropped in Photoshop and saved as JPGs on the highest quality setting. No color adjustments were made to the photos. Then the photos were underwent the OCR process in ABBYY Fine Reader and saved as searchable PDFs.  

{% include feature/image.html objectid="/images/dig_setup.jpg" width="50" caption="Home digitization set-up, October 2020, Bloomington, IN" %}

Under normal circumstances, the pamphlet novels would be scanned on a flat bed scanner, especially since they lay very flat. They would be scanned with color calibration cards to ensure faithful color, and the ppi of the photos would likely be higher. The images could then be processed by ABBYY Fine Reader and any OCR errors would be manually corrected. A searchable PDF complying to the PDF/A standard would be saved to ensure long-term storage sustainability.  

## Metadata Standards
The metadata for this project concentrates on accurately representing a variety of features of the items that are helpful to its bibliographic description and other features that might be of interest to viewers. For this reason, the metadata scheme uses a selection of Dublin Core elements and custom elements for the item type "text." The values of individual elements are subject to both custom and established controlled vocabularies and content standards such as the Library of Congress Name Authority File or Internet MIMEtype.  

Below is an explanation of what Dublin Core and text item type elements are used and what standards have been applied to their input.  
### Dublin Core elements  
#### Title - required, 1 value allowed
The title element contains the title of the work. This information is taken from the title page of the novel, not the cover since the author's name and the series are often more typographically prominent on the cover. Titles are formatted according to Spanish capitalization conventions where only the first word and any proper nouns are capitalized.  

Examples: Las superhembras, El hombre negro  

#### Creator - required, multiple values allowed
The creator element is used to denote the author. Authors are listed in the pamphlet novels by their given name and/or a pseudonym or alternate name. For this reason, at least one of the values for creator will follow the content and formatting of the [Library of Congress Name Authority File](https://id.loc.gov/authorities/names.html) and that value will be hyperlinked to the URI for that name authority file. Having this link to the authority file URI definitively identifies the author. Additionally, the LOC Name Authority File links to the Virtual International Authority File (VIAF) record for a given author, which in turn links to the name authority files of the author in systems all around the world. If a pseudonym or alternate name of an author is included on the title page or cover of the work, that will be inputted as a second value in the element. Pseudonyms will be followed by "(pseud.)".  

Examples: [Sardou, Victorien, 1831-1908](https://id.loc.gov/authorities/names/n79072967.html); Colombine (pseud.), La Condesa de Pardo Bazán  

#### Date - required, 1 value allowed
Date element contains the value of the date of publication which is important to include in any sort of bibliographic item. The dates are formatted according to the [W3C date format](https://www.w3.org/TR/NOTE-datetime) which allows for dates to be inputted in this way:  
- YYYY-MM-DD
- YYYY-MM
- YYYY

All of the items included in this digital library have a full month, year, day publication date since it was a weekly publication, meaning that all of the dates are in the YYYY-MM-DD format.  

Example: 1916-11-18 to denote November 11, 1916  

#### Publisher - required, 1 value allowed
While all of the items in this collection are technically published by Prensa Popular, I wanted to follow the bibliographic convention of representing the imprint as it appears in the item. Additionally, there is no particularly consistent placement in the items for the publisher and even for the same series the publisher/printer listed may change. Therefore, the value for this element is whatever entity is listed as the publisher and/or printer in the item itself. If no publisher or printer is listed, then the publisher will be entered as [Prensa Popular]. 

Examples: Imprenta y Talleres de La Novela Corta, Tipografia Antonio Palomino  

#### Format - required, 2 values required
The format element has two required values: the number of pages (not including the front and back covers) and the digital format of the item. The number of pages is an Arabic numeral followed by "pp" and the digital format corresponds to the [Internet MIMEtype](https://www.iana.org/assignments/media-types/media-types.xhtml).

Examples: 32pp, pdf  

#### Language - required, multiple values allowed
While all of the items currently in the digital library are in Spanish, other issues of the series sometimes contain significant portions in other languages, such as [Francfort: juguete cómico tetralingue by Vital Aza](https://t.co/ah97YtWLMn?amp=1), which contains dialogue in German, French, Spanish, and Catalan. If that item were to be formally incorporated into the collection (instead of being linked to on the [Other Issues in La Novela Teatral]), it would be appropriate to list other languages in the language field. The values for the language element use the 3-letter language codes listed in the [ISO 639-2](https://en.wikipedia.org/wiki/List_of_ISO_639-2_codes).  

Examples: spa, eng  

#### Description - optional
The description element contains a short description of the plot. As I have not read all of the pamphlet novels, this is an optional element.  

#### Rights - required, 1 value allowed
The rights element describes the copyright status and any other restrictions to the use of the item. All of the items in the digital library were published between 1916 and 1925, so they are in the public domain, and I am placing no additional restrictions on them. Therefore, the value of the rights element for all items is simply "public domain".  

#### Identifier - required, 1 value allowed
The identifier uniquely identifies the item in the digital library. Identifiers are formatted as title_YYYY. The title is in camel case and ignores any initial articles (un, una, unos, unas, el, la, los, las). The searchable PDFs included on each item page also reflect this format.

Examples: Superhembras_1923, Pasiones_1917  

#### Translator - required if present, multiple values allowed
Occasionally within the different series, they published a work in translation. In these cases, the translator is listed in this field in order to not be confused with the original author in the creator element. Like the creator element, the values of the translator element are formatted according to the [Library of Congress Name Authority File](https://id.loc.gov/authorities/names.html) and that value will be hyperlinked to the URI for that name authority file.  

Example: [Rios, Luis de los](https://id.loc.gov/authorities/names/n90694180.html)

#### Series - required, 1 value allowed
Prensa Popular specifically published different works in different series, so it's important to represent this in the metadata for these items. Currently, the only allowed values are La Novela Corta, La Novela Cómica, and La Novela Teatral. If the digital library were to incorporate other series (Frine, Flirt, etc.), then those values would also be allowed.  

#### Year (Magazine/Journal) - required, 1 value allowed
The year (magazine/journal) element does not mean the year of publication. That is specified by the date element. Issues from all three series are listed inside the pamphlet novels as belonging to a specific year in a Roman numeral format, similar to the volume of an academic journal. The value of this element is the Roman numeral listed in each issue.  

Examples: I, IV, VII  

#### Number (Magazine/Journal) - required, 1 value allowed
The number along with the year definitely identifies the publication sequence of the issues in each series. Interestingly, the numbering is continuous across all years, so even just the number can tell you where an issue falls in the publication sequence. The values for this field are inputted as Arabic numerals since that is how they are printed in the pamphlet novels themselves. On the "other issues" page of each series' exhibit, the links are organized sequentially according to the issue number.  

Examples: 27, 55, 86

#### Place of Publication - required, 1 value allowed
The publication place for an item is an important bibliographic detail to the description of a book, so it is a required element for items in this library. It is only required to list the city name or the country name if no city is provided. In a few of the items in this library, the publication place on the item is spelled incorrectly in the item (Madird instead of Madrid), so the publication place should just be the place spelled correctly. The Spanish spelling for the city should be used (e.g. Zaragoza, not Saragossa; Sevilla, not Seville). 

Example: Madrid  

#### Price - required, 1 value allowed
The price is another interesting feature of these items. Since it is listed on the item itself and the price changed over time for some of these series, it was important to note the price. The currency for the price is often abbreviated on the actual item, but for the value of this element, I decided it was important to spell it out fully.

Examples: 5 céntimos, 30 céntimos  

#### Physical Dimensions - required, 1 value allowed
Because these are physical objects rendered as digital facsimiles online, it can be hard to get a sense of the size of an object from a PDF. Using the physical dimensions element helps to return some sense of size to the viewer. Dimensions are expressed in inches.

Examples: 5.25in x 7.75in  

#### Advertisement - required, multiple values allowed
Aside from the texts themselves, the advertisements in these items are some of the most interesting aspects of the pamphlet novels. I have tried to represent the item being advertised, what kind of item it is, who is advertising it (if different from the product), and where the advertisement occurs in the item.  

Within the item metadata, advertisements are formatted as follows:  
Name of the product (brief description of product) [location in pamphlet novel]  
OR  
Name of the product (brief description of product) advertised by Advertiser Name [location in pamphlet novel]  

Examples: 
La Novela Corta (list of previous issues of La Novela Corta) [front inside cover]  
La Novela Corta (list of 3 upcoming issues of La Novela Corta) [front inside cover]  
Walk-Over (shoes) [back inside cover]  
La Flor de Oro (hair dye) [back inside cover]  
Doña María de Padilla (pamphlet novel issue) advertised by La Novela Teatral [back inside cover]  
Osram (lightbulbs) [back outside cover]  

While the advertisements are searchable from the main search bar, the advertisements are an important enough aspect of these pamphlet novels that I felt they deserved their own page and for the advertising information to be aggregated together in their own table. Therefore, the advertising data has been transformed into an AwesomeTable on the Advertising page.  