# Amapola Flyg — Customs Invoice Generator

A self-contained, offline web app that turns aircraft-part repair/sales orders into the
shipping paperwork Amapola Flyg AB needs, with destination-aware document rules.

Open **`index.html`** in any browser (Chrome, Edge, Firefox) — no install, no server.

## Features

- **Upload SO / SM / RO PDF(s)** — reads P/N, S/N, B/N, description, ship-to and
  destination directly from the order. Multiple files combine into one shipment.
- **Destination-aware documents**
  - EU → no customs document (AWB only)
  - Norway / UK / Africa / others → Customs Invoice
  - USA → Customs Invoice + CBP Form 3311 + Foreign Shipper's Declaration of U.S. Goods Returned
  - Brazil → Customs Invoice + Packing List + ISPM 15 wood-packaging certificate
- **Smart auto-fill** — built-in parts library fills manufacturer, country of origin and
  HS code; handling airport is chosen from the destination/address.
- **Customs invoice fields** — currency selector, net & gross weight, carrier + transport
  value, freight/insurance/tax, HS code, country of origin, reason for export.
- **Packing list** generation.
- **ISPM 15 wood-packaging certificate** — heat-treatment (HT) or fumigation (MB), with a
  dimensioned drawing of the box/pallet and the IPPC mark.
- **Digital signature** — draw or upload; appears on the documents.
- **Print / Save as PDF** built in.

## Notes

- Everything runs locally in the browser; data is not sent anywhere. The parts library and
  signature are stored in the browser's local storage.
- PDF order reading uses pdf.js loaded from a CDN, so the upload feature needs an internet
  connection the first time; the rest works fully offline.
- The ISPM 15 certificate is an accompanying declaration — the official IPPC stamp applied
  to the wood by the licensed treatment provider is the legal evidence of treatment.

## Maintainer

Amapola Flyg AB — Malmö-Sturup, Sweden.
