# ALTOgraf

ALTOgraf is a framework designed to bridge Internet routing topology data with Application-Layer Traffic Optimization (ALTO) standards. It ingests data extracted from the [asmap/kartograf](https://github.com/asmap/kartograf) project to generate standard-compliant ALTO information resources and serves them through custom server-client implementations.

## Overview

The primary objective of ALTOgraf is twofold:

1. **Map Generation from Kartograf Data:**
   Extracts Autonomous System (AS) and IP mapping data produced by `kartograf` and transforms it into:
   - **Network Maps:** Grouping IP prefixes into Provider-defined Identifiers (PIDs).
   - **Cost Maps:** Defining topological routing and distance metrics between PIDs.
   - **Property Maps:** Associating specific properties (e.g., ASN, geolocation, routing attributes) with PIDs and endpoint identifiers.

2. **IETF RFC Compliant Server & Client Implementations:**
   Provides reference implementations conforming to IETF ALTO specifications:
   - **ALTO Server:** Exposes the generated Network, Cost, and Property maps via standard RESTful endpoints compliant with RFC 7285 and related extensions.
   - **ALTO Client:** A lightweight client to query the Information Resource Directory (IRD), filter maps, and consume ALTO services for traffic optimization.

## Key Standards & References

- [RFC 7285](https://datatracker.ietf.org/doc/html/rfc7285) - Application-Layer Traffic Optimization (ALTO) Protocol
- [RFC 9240](https://datatracker.ietf.org/doc/html/rfc9240) - ALTO Property-Map Service
- [asmap/kartograf](https://github.com/asmap/kartograf) - Autonomous System mapping toolchain

```bash
git clone [https://github.com/YOUR_USERNAME/ALTOgraf.git](https://github.com/YOUR_USERNAME/ALTOgraf.git)
cd ALTOgraf
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
