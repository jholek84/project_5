# Analýza cestovního ruchu v ČR (2023–2024)

## O čem je tento projekt?
Vytvořil jsem interaktivní report v Power BI, který ukazuje, jak lidé v ČR cestovali v letech 2023 až 2024, kolik za to utráceli a kde nejčastěji nocovali. Jedná se o třetí verzi projektu.

## Co všechno jsem opravil.

* **Propojení dvou tabulek (Datový model):** Už nemám v projektu jen jednu tabulku. Podle rad z lekce jsem pomocí jazyka DAX vytvořil druhou tabulku – **Kalendár**. Obě tabulky jsem v Power BI propojil čárou (vztah 1:N). Díky tomu teď report funguje správně jako databáze.
* **Propojené filtry na všech stránkách:** Na druhou a třetí stranu jsem dokopíroval filtry pro Rok a Pohlaví a zapnul jejich synchronizaci. Když teď uživatel klikne na rok 2024 na první stránce, automaticky se mu vyfiltruje rok 2024 i na těch ostatních.
* **Jedna velká karta místo tří malých:** Sloučil jsem samostatné vizuály pro Náklady, Cesty a Noci do jedné hromadné karty. Pojmenoval jsem ji "Základní přehled o cestách". Nastavil jsem v ní pro každou hodnotu správné jednotky (miliony/tisíce), aby se čísla dobře četla jsem je zaokrouhlil.
* **Oprava textů a legend:** Prošel jsem všechny grafy a opravil nadpisy, aby přesně seděly s tím, co graf ukazuje. 
* **Čitelnost tabulky:** V tabulce na druhé stránce jsem zesvětlil barevné pruhy u podmíněného formátování. Černá čísla teď jdou lépe přečíst a pruhy je nepřekrývají.
* **Oprava formátu měny:** U všech peněžních údajů jsem ručně nastavil formát na koruny (**Kč**).

## Jak je report rozdělený?
Report má teď **3 samostatné a pojmenované stránky**, které na sebe logicky navazují:
1. **Základní přehled:** Hlavní velká čísla a grafy, jak lidé utráceli a kolik nocí kde strávili.
2. **Cíle cest:** Srovnání domácích a zahraničních cest za oba roky a nejčastější ubytovací zařízení a typy.
3. **Náklady:** Stránka, kde počítám průměrnou cenu za jednu cestu a jednu noc.

## Co najdete v tomto repozitáři?
* `CRU06AGEN.csv`: Původní data z ČSÚ, která jsem musel v Power Query nejdřív vyčistit (převést tečky v číslech na čárky, aby s nimi Power BI umělo počítat).
* `Analýza cestovního ruchu za roky 2023 - 2024.pbix`: Finální a opravený Power BI report.
