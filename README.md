# Path Protocol Models

This repository contains a collection of models to consider multiparty message-forwarding protocols as part of a submission to a conference. These models are built inside the Tamarin prover tool using the framework established in our paper.

Analysis was performed on R-type Amazon Web Services machines because of the high memory requirements caused by changing the bounds.

## Layout

The root folder contains ./pi-oracle.py, the Oracle file used to improve Tamarin's heuristic search. Other than this, the models are each split into separate folders. Each folder contains the following files:

- A `.spthy` file which contains the protocol's implementation into Tamarin
- `.pdf` and `.jpg` files containing a message sequence chart showing the protocol's intended execution
- A `README` file contains any additional notes about the protocol in question

The following protocols are modelled:

- `mctls/` models the record phase of the mcTLS protocol (citation [33] in our paper)
- `mbtls/` models the record phase of the mbTLS protocol (citation [32] in our paper)
- `matls/` models the record phase of the maTLS protocol (citation [26] in our paper)
- `Chaum/` models a primitive onion protocol using nested encryption, such as proposed by Chaum (citation [8] in our paper)
- `TOR-Establishment/` models the circuit establishment protocol of the TOR scheme (citation [41] in our paper)
- `TOR-Record/` models the data exchange protocol of the TOR scheme (citation [41] in our paper)
- `HORNET-Record/` models the record phase of the HORNET mixnet protocol (citation [9] in our paper)
- `Lightning/` models the Lightning payment protocol (citation [35] in our paper)
- `LightningSig/` models a extension of the Lightning payment protocol using a chained signature to ensure path symmetry (proposed in our paper)