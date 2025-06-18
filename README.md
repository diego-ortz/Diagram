```mermaid
flowchart LR
  Start((Inicio))
  A[Medir O₂, Temp, Hum, Movimiento]
  B[Enviar datos a PCB (Motherboard)]
  C[Modelo de integración]
  D[Transformación de datos]
  E[Generar JSON]
  F[Insertar JSON en SQL Server]
  G[Replicar en Cloud detrás de SQL]
  H1[Enviar a ClusterHub (SQL)]
  H2[Enviar a Nexus (SQL)]
  End((Fin))

  Start --> A --> B --> C --> D --> E --> F --> G
  G --> H1 --> End
  G --> H2 --> End

Cerrar bloque mermaid
