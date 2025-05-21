# Data Management Plan

## Data description and collection or re-use of existing data

### How will new data be collected or produced and/or how will existing data be re-used?

Existing data will be sourced from a legacy Microsoft Access database that has since been migrated to a MySQL instance, accessible at: https://www.lab451.cloud/Reggio/index.php.

The data will be collected, analyzed, and processed using Python scripts, which are documented in the following sections: [Analysis](/analysis/), [Processing](/processing/).

There are no significant constraints identified at this stage, aside from the requirement to extract data specific to the Romagna region and generate a filtered subset for further use.

Data provenance and transformation steps will be fully documented using Jupyter Notebooks.


### What data (for example the kind, formats, and volumes), will be collected or produced?

The dataset is primarily derived from a legacy Microsoft Access database and consists mostly of textual information.

To ensure long-term accessibility and ease of use—particularly when working with Python—data will be made available in open, standard formats, with CSV chosen as the primary format. Additionally, plans are in place to convert the data into RDF to enhance interoperability and support reuse in semantic web contexts. This conversion may occur either:

- Directly, using Python scripts or materialization tools such as Morph-KGC, or
- Indirectly, by importing the data into Semantic Web–oriented content management systems such as Omeka S, WissKI, or ResearchSpace.

The database is structured in three main tables:
- **Castelli** (2000 rows)
    - _IdCastello_: int
    - _IdVeteroDb_: str
    - _IdRifVeteroDb_: str
    - _Castello_: str
    - _NumeroSullaCarta_: int
    - _EsistenzaDubbia_: int bool
    - _Toponimo_: str
    - _IdProvincia_: int
    - _provincia_: str
    - _Comune_: str
    - _Localita_: str
    - _Localizzazione_: int cat
    - _RifCTR_: str
    - _RifIGM_: str
    - _CondizioneAttuali_: int cat
    - _UsoAttuale_: str
    - _RifFotoAerea_: NULL
    - _Planimetria_: str
    - _InterventiRicognitivi_: str
    - _DescrizioneSito_: str
    - _EdificioIsolato_: int bool
    - _ComplessoEdilizio_: int bool
    - _InsediamentoFortificato_: int bool
    - _AttPrecastrensi_: str
    - _CartografiaStorica_: str
    - _IconografiaStorica_: str
    - _RestauriInStile_: str
    - _CostruzioniNeomedievali_: str
    - _Note_: str

- **Vicende** (39757 rows)
    - _IdVicenda_: int
    - _IdVeteroDb_: str
    - _IdRifVeteroDb_: str
    - _IdBibliografia_: int
    - _IdBibliografiaProvv_: int
    - _IdCastello_: int
    - _Datazione_: str
    - _DataNA_: int
    - _DataNM_: int
    - _DataNG_: int
    - _Avvenimento_: str
    - _Altro_: str
    - _VolumeRiferimento_: str
    - _PaginaRiferimento_: int
    - _NumeroDocumento_: str
    - _Denominazione_: str
    - _Appartenenza_: str
    - _TitoloPossesso_: str
    - _StruttureIndicate_: str
    - _Pieve_: str
    - _Parrocchia_: str
    - _DistrettoCivile_: str

- **Bibliografia** (1190 rows)
    - _IdBibliografia_: int
    - _Autore_: str
    - _Titolo_: str
    - _DescrizioneOpera_: str
    - _Sede_: str
    - _Annata_: str
    - _LuogoPubblicazione_: str
    - _CuratoreEdizione_: str
    - _CasaEditrice_: str
    - _ISBN_: int
    - _Pagine_: str
    - _EdizioniSuccessive_: str
    - _VolPiuVol_: str

- ~~Log Bibliografia~~
- ~~Log Vicende~~
- ~~Rif vetero DB~~
- ~~Province~~

Additional data (such as _latitude_ and _longitude_) will be added.

Zipped CSV files: 16.9 MB

Unzipped CSV files: 43.9 MB

## Documentation and data quality

### What metadata and documentation (for example the methodology of data collection and way of organising data) will accompany the data?

    • Indicate which metadata will be provided to help others identify and discover the data.
    • Indicate which metadata standards (for example DDI, TEI, EML, MARC, CMDI) will be used.
    • Use community metadata standards where these are in place.
    • Indicate how the data will be organised during the project, mentioning for example conventions, version control, and folder structures.
Consistent, well-ordered research data will be easier to find, understand, and re-use.
    • Consider what other documentation is needed to enable re-use. This may include information on the methodology used to collect the data, analytical and procedural information, definitions of variables, units of measurement, and so on.
    • Consider how this information will be captured and where it will be recorded for example in a database with links to each item, a ‘readme’ text file, file headers, code books, or lab notebooks.

### What data quality control measures will be used?

Data quality will be ensured through data processing, the definition of a protocol that defines value formats, and the representation of some data values with controlled vocabularies when possible.

## Storage and backup during the research process

### How will data and metadata be stored and backed up during the research?

Data will be stored in:
* The MySQL database
* Locally on at least two different drives
* Sharepoint

### How will data security and protection of sensitive data be taken care of during the research?

The data will be accessible to the team members on the frontend service serving the MySQL tables and on the SharePoint.

## Legal and ethical requirements, codes of conduct

### How will other legal issues, such as intellectual property rights and ownership, be managed? What legislation is applicable?

Data owner: ...

License: ...

## Data sharing and long-term preservation

### How and when will data be shared? Are there possible restrictions to data sharing or embargo reasons?

Data repository: ...

The data will be retained for ...

The data will be made available at ...

### How will data for preservation be selected, and where data will be preserved long-term (for example a data repository or archive)?

The foreseeable uses for the data include:
- Research in history, architecture, cultural heritage studies
- Research in bibliographic studies
- Data source for historical and descriptive information for Italian castles

### What methods or software tools are needed to access and use data?

How to access and reuse the data: ...

### How will the application of a unique and persistent identifier (such as a Digital Object Identifier (DOI)) to each data set be ensured?

The data will receive a proper DOI through ...

## Data management responsibilities and resources

### Who (for example role, position, and institution) will be responsible for data management (i.e. the data steward)?

    • Outline the roles and responsibilities for data management/stewardship activities for example data capture, metadata production, data quality, storage and backup, data archiving, and data sharing. Name responsible individual(s) where possible. 
    • For collaborative projects, explain the co-ordination of data management responsibilities across partners.
    • Indicate who is responsible for implementing the DMP, and for ensuring it is reviewed and, if necessary, revised
    • Consider regular updates of the DMP.

### What resources (for example financial and time) will be dedicated to data management and ensuring that data will be FAIR (Findable, Accessible, Interoperable, Re-usable)?

    • Explain how the necessary resources (for example time) to prepare the data for sharing/preservation (data curation) have been costed in. Carefully consider and justify any resources needed to deliver the data. These may include storage costs, hardware, staff time, costs of preparing data for deposit, and repository charges.
    • Indicate whether additional resources will be needed to prepare data for deposit or to meet any charges from data repositories. If yes, explain how much is needed and how such costs will be covered.