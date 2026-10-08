# atlas-avis-db

Base de donnees PostgreSQL 16, provisionnee via DxP (golden path `postgresql`,
ADR S0-076). Adaptee au dev/qualif -- pas de haute disponibilite, pas de
backup automatique. Pour la production, utilisez un service manage externe
(Azure Database for PostgreSQL, RDS...) ou le golden path `postgresql-ha`
(ADR S0-076 D5, si CloudNativePG est installe par le PE).

## Connexion

Les credentials sont dans le Secret `dxp-db-atlas-avis-db` du namespace
du service, jamais en dur dans ce depot.

## Stockage

PVC de 5Gi (valeur fixe pour l'instant, voir dxp-gp-template.yaml).
