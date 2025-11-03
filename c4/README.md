# C4 Model Landscape

This folder contains C4 Model diagrams for the Orders, Payment, and Delivery microservices.

- C1: System Context — c4-system-context.puml
- C2: Container — c4-containers.puml
- C3: Component — per service (hosted in each service repo)
  - meetup-2025-orders-service/docs/c4/component.puml
  - meetup-2025-payment-service/docs/c4/component.puml
  - meetup-2025-delivery-service/docs/c4/component.puml

Navigation
- Navigation links are embedded in the diagrams; export to SVG for clickable navigation.
- GitHub Actions automatically renders and publishes the SVGs to GitHub Pages for each repo.

Generate locally
- make (or ./generate.sh) to regenerate code-level puml files and SVGs if PlantUML is available.

Troubleshooting (IDE previews)
- Some IDE PlantUML renderers error on non-standard C4 macros (e.g., ComponentPort). We replaced these with standard Component elements labeled as "Port" to maximize compatibility.
- If you see include errors, enable URL includes for PlantUML in your IDE settings (often named "Allow URL includes" or similar), because these files use `!includeurl` for C4-PlantUML.
- Alternatively, render locally:
  - Install PlantUML and Graphviz.
  - Run: `cd meetup-2025-landscape/c4 && ./generate.sh` (produces .svg files you can open in a browser).
