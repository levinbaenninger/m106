# Namenskonventionen

## Tabellen

- Namen im Singular
- PascalCase

## Attribute

- Attributnamen im Singular
- PascalCase
- Primärschlüssel: TabelleId
- Fremdschlüssel: ParenttabelleId

## Constraints

- Primärschlüssel: PK_Tabelle
- Fremdschlüssel: FK_Tabelle_Attributname_ParentTabelle
- Check: CK_Tabelle_Beschreibung
- Default: DF_Tabelle_Attributname
- Unique: UQ_Tabelle_Attributname
- Index: IDX_Tabelle_Attributname
