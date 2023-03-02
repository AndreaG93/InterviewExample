# Domanda 4 - Esercizio

Supponiamo di avere il seguente schema relazionale:

    IMPIEGATO(CodiceFiscale, Nome, Cognome)
    PROGETTO(CodiceProgetto, Nome)
    PARTECIPAZIONE(CodiceFiscale, CodiceProgetto)

Dove:
1. <code>CodiceFiscale</code> è **chiave primaria** di <code>IMPIEGATO</code>.
2. <code>CodiceProgetto</code> è **chiave primaria** di <code>PROGETTO</code>.
3. <code>CodiceProgetto</code> e <code>CodiceFiscale</code> in <code>PARTECIPAZIONE</code> rappresentano due **vincoli di integrità referenziale** con gli omonimi attributi in <code>IMPIEGATO</code> e <code>PROGETTO</code>.

>## Usando l'approccio **Code First** di **Entity Framework**, scrivi il codice e i comandi necessari per creare le suddette relazioni in una base dati.