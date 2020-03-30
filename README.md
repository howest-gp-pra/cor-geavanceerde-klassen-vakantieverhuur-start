# cor-geavanceerde-klassen-vakantieverhuur-start

### zie panopto video voor uitleg project

Hier wordt enkel stap voor stap opgelijst wat je moet doen.  

In de Class Library maak je volgende klassen aan :  

* De klasse Verblijf  
  * Eigenschappen  
    * propfull  ID, string, readonly (dus setter verwijderen)  
    * propfull  Basisprijs, decimal : indien waarde < 0  => waarde = 0
    * propfull  VerminderdePrijs, decimal : indien waarde < 0  => waarde = 0
    * propfull  DagenVoorVermindering, byte, indien waarde > 100 => waarde = 100
    * propfull  Waarborg, decimal : indien waarde < 0  => waarde = 0   
    * propfull  MaxPersonen, int : indien waarde < 1 => waarde = 1, indien waarde > 20 => waarde = 20  
    * prop  StraatEnNummer, string  
    * prop  HuisNaam, string  
    * prop  Gemeente, string  
    * propfull  Postnummer, int : indien waarde < 1000 => waarde = 1000, indien waarde > 9999 => waarde = 9999  
    * prop  Microgolf, nullable bool  
    * prop  TV, nullable bool  
    * prop  Verhuurbaar, bool : standaardwaarde = true  
  * Constructor  
    1 argumentloze constructor die de prop ID (beter : private variabele id) vult met een nieuwe GUID

    

