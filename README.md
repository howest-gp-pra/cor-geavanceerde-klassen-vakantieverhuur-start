# cor-geavanceerde-klassen-vakantieverhuur-start

### zie panopto video voor uitleg project

Hier wordt enkel stap voor stap opgelijst wat je moet doen.  

In de Class Library maak je onder Entiteiten volgende klassen aan :  

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
* De klasse Vakantiehuis
  Erft over van Verblijf
  * Eigenschappen
    * prop Vaatwas, nullable bool
    * prop Wasmachine, nullable bool
    * prop Houtkachel, nullable bool
  * ToString wordt overschreven : "H - huisnaam - gemeente"
* De klasse Caravan
  Erft over van Verblijf
  * Eigenschappen
    * prop PersoonlijkSanitair, nullable bool
  * ToString wordt overschreven : "C - huisnaam - gemeente" 
* De klasse Persoon
  * Eigenschappen
    * prop Naam, string
    * prop Voornaam, string
    * prop Adres, string
    * prop Gemeente, string
    * prop Land, string
    * prop Telefoon, string
    * prop Email, string
* De klasse Huurder
  Erft over van Persoon
  * Eigenschappen
    * prop IsBlackListed, bool, standaardwaarde = false

In de Class Library maak je onder Services volgende klassen aan :   
* De klasse Verblijven
  * STATISCHE veld
    * List<Verblijf> AlleVerblijven
  * STATISCHE void methode Initialiseer 
    Deze methode vult het statische veld AlleVerblijven met wat testmateriaal.  
    Onderaan deze tekst kan je de voorbeeldgegevens die ik in dit project gebruik terugvinden.
 
 WPF : MainWindow
 * Zorg er voor dat bij opstart de listbox lstVerblijven gevuld wordt met alle vakantieverblijven
 * in cmbSoorten zijn reeds 3 items opgenomen : "Alle verblijven", "Vakantiehuisjes" en "Caravans".  
   Wordt "Alle verblijven" geselecteerd, dan toon je in lstVerblijven alle verblijven.  
   Wordt "Vakantiehuisjes" geselecteerd, dan toon je enkel de vakantiehuisjes.  
   Wordt "Caravans" geselecteerd, dan toon je enkel de caravans.  

