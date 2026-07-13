# NYC Council Fiscal Suite — network allowlist reference

The suite works in any normal browser (Open Data is reachable there). This list is
for opening the Claude Code on the web environment's egress policy so the live
panels can be verified from the sandbox. Config docs:
https://code.claude.com/docs/en/claude-code-on-the-web

## Tier 1 — Core (unblocks all live budget/priority/impact panels)
data.cityofnewyork.us        # ALL NYC Open Data / Socrata — one entry covers every dataset below
  mwzb-yiwb   Expense Budget by object class  -> expense dashboard, stage timeline, line items, Mayor's options, Forecaster momentum, workforce
  39g5-gbp3   Expense Budget Funding All Source -> funding split/agencies, MC fiscal strip, simulator baseline
  2cmn-uidm   Capital Commitment Plan          -> capital budget & cost risk
  872g-cjhh   City Council Districts (GeoJSON)  -> impact-map district choropleth
  ye4r-qpmp   Census demographics by council district -> priority signals (income/poverty)
  erm2-nwe9   311 Service Requests             -> priority signals (service demand), district intel
  4d7f-74pe   Discretionary Funding 2009-2021  -> historical funding explorer
  5uac-w243   NYPD complaints YTD              -> funding map
  k397-673e   Citywide payroll                 -> vendor/workforce

## Tier 2 — Map rendering (choropleth)
a.tile.openstreetmap.org
b.tile.openstreetmap.org
c.tile.openstreetmap.org
server.arcgisonline.com      # satellite layer
cdnjs.cloudflare.com         # Leaflet library

## Tier 3 — Economic / macro (optional panels)
api.census.gov
data.census.gov
fred.stlouisfed.org
api.fiscaldata.treasury.gov
api.usaspending.gov
www.bls.gov
data.ny.gov
dol.ny.gov

## Tier 4 — Other live pulls
council.nyc.gov              # Schedule C / budget PDFs
webapi.legistar.com          # Transparency Resolutions
legistar.council.nyc.gov

## Tier 5 — AI Assistant (optional)
api.anthropic.com            # Claude
generativelanguage.googleapis.com  # Gemini

## Not needed (link-outs that open in the browser, not fetches)
checkbooknyc.com, comptroller.nyc.gov, ibo.nyc.gov, www.nyc.gov,
projects.propublica.org, guidestar.org, opencorporates.com, zillow.com, google.com

## Note
The suite has CORS-proxy fallbacks (corsproxy.io, api.allorigins.win) for CORS-blocked
calls; these were denied by the egress proxy. Allowlisting data.cityofnewyork.us
directly makes them unnecessary — leave them off.

Minimum for full verification of this session's work: data.cityofnewyork.us + the
three *.tile.openstreetmap.org hosts.
