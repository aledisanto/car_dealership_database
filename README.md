# Car Dealership Database System (Progettazione Concettuale, Logica e Fisica)

Questo repository contiene l'intero flusso di progettazione e l'implementazione fisica di una base di dati relazionale dedicata alla gestione completa di un **Concessionario di Automobili**. 

Il progetto è stato sviluppato come elaborato pratico per l'esame di *Basi di Dati* nel corso di Laurea Triennale in *Ingegneria Elettronica e Informatica* presso l'**Università degli Studi di Trieste**.

## Obiettivo del Progetto
L'obiettivo dell'elaborato è la modellazione e la realizzazione di un sistema informativo efficiente in grado di mappare i requisiti operativi del concessionario, garantendo l'integrità dei dati e l'ottimizzazione delle interrogazioni frequenti. Il sistema gestisce in modo integrato:
* L'anagrafica dei clienti e del personale interno.
* Il catalogo delle automobili disponibili (suddivise per categorie, alimentazione e specifiche tecniche).
* I flussi commerciali di compravendita e i servizi post-vendita, inclusi i registri dettagliati delle manutenzioni e delle riparazioni d'officina.

## Fasi della Progettazione Sviluppate

### 1. Analisi dei Requisiti e Progettazione Concettuale
* **Definizione dei Requisiti:** Raccolta e formalizzazione delle specifiche di business del concessionario.
* **Schema Entity-Relationship (E-R):** Creazione del modello concettuale iniziale identificando entità, attributi, identificatori primari e cardinalità delle relazioni.
* **Dizionario dei Dati:** Definizione formale del significato di ciascuna entità e relazione, integrando l'analisi dei vincoli non esprimibili graficamente sul diagramma.

### 2. Progettazione Logica e Ristrutturazione
* **Analisi dei Volumi:** Stima del carico computazionale e delle frequenze delle operazioni per ottimizzare le prestazioni delle query.
* **Ristrutturazione dello Schema E-R:** Eliminazione delle generalizzazioni/gerarchie, analisi e rimozione delle ridondanze e scelta finale delle chiavi primarie stabili.
* **Traduzione nel Modello Relazionale:** Conversione dello schema ristrutturato in tabelle logiche, definendo chiavi esterne (*Foreign Keys*) e vincoli di integrità referenziale.

### 3. Progettazione Fisica e Codice SQL
* **DDL (Data Definition Language):** Scrittura degli script di creazione delle tabelle con l'assegnazione accurata dei domini dei dati.
* **Logica di Business (Trigger):** Sviluppo di trigger avanzati per automatizzare i controlli di consistenza logica non nativi del DBMS, come:
  * `controlloCarburante`: Impedisce l'inserimento di configurazioni di alimentazione inconsistenti (es. veicoli contrassegnati contemporaneamente come solo elettrici e a combustione).
  * `controlloPatenteCliente`: Valida la congruenza tra la patente posseduta dal cliente e la categoria di automobile selezionata per l'acquisto.
  * Gestione dello storico dei guasti e dello stato di sanamento delle vetture post-riparazione.

## Contenuto della Repository
* **`DI_SANTO_ALESSANDRO_IN0500902.pdf`**: pdf contenente l'intero lavoro svolto (redatto in **LaTex**) completo di **codice SQL** per la generazione automatica dello schema, delle tabelle e di tutti i trigger di controllo.
* **`DI_SANTO_ALESSANDRO_IN0500902.tex`**: codice sorgente `.tex` da cui è stato ricavato il pdf di cui sopra.

---
*Studente: Alessandro Di Santo*  
*Professore: Andrea De Lorenzo*  
*Corso: Basi di Dati*  
*Dipartimento di Ingegneria e Architettura — Università degli Studi di Trieste*
