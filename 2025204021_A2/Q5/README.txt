# Q5

Data Dictionary Tool implemented: open `data_dictionary.html` in a browser.

Features:
- Paste / load JSON, XML, or raw SQL DDL (CREATE TABLE) to build an interactive data dictionary.
- Auto-infers relationships from foreign key references.
- Interactive pan/zoom relationship diagram with node focus & orphan table highlighting.
- Filtering by column data types and text search across table/column names & comments.
- Metrics summary (tables, columns, PK count, relationship count).
- Export static HTML report (with full dictionary & relationships list) or print to PDF (browser print styles included).
- Sample schema insertion & JSON formatter.
- Experimental regex-based DDL parser (simple PK/FK; refine manually if needed).

How to Use:
1. Open the file in a modern browser (Chrome/Firefox/Edge).
2. Click "Insert Sample" to see a working example.
3. Prepare your own schema JSON (see instructions embedded in the page) or:
   - Load XML using the provided XML format.
   - Paste raw CREATE TABLE statements then "Parse SQL DDL".
4. Click "Generate Dictionary" to render tables & diagram.
5. Use search box and type pills to filter.
6. Click a node to highlight its neighborhood; double-click to zoom focus; "Fit Diagram" to reset.
7. Export:
   - Click "Export Static HTML" for an archive-friendly artifact.
   - Use browser Print -> Save as PDF for PDF version.

Generating JSON From Databases: Brief (full commands inside page):
- PostgreSQL: Query information_schema (sample command embedded) -> schema.json -> copy/paste.
- MySQL: Similar JSON aggregation query -> schema.json.
- SQLite: Use `.schema` then DDL parse or custom script.
- Others: Query system catalogs (see on-page guidance).

Limitations:
- DDL parser: limited support (no complex composite FKs or CHECK parsing).
- Diagram export not embedded in static HTML (re-run interactive tool for diagram view).

File: `Q5/data_dictionary.html`

