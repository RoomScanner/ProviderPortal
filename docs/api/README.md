# API notes

The API contract itself lives in [RoomScanner/Docs](https://github.com/RoomScanner/Docs/tree/main/api-contract) (TW-S06), not here. Use this folder for working notes before they go into the contract.

Every contract document must follow the format in [`api-contract/_TEMPLATE.md`](https://github.com/RoomScanner/Docs/blob/main/api-contract/_TEMPLATE.md). A `contract-format` check in the Docs repo blocks PRs that don't. Each endpoint gets a numbered heading, a protocol and requirement-ID table, a JSON example and a field table for every request and response, and a response-code table. That covers the Simplex, Medium and Ultimo contract requirements (TW-S06, TW-M01, TW-U04) together.

Contract due dates: Fri 20 Nov 2026 for Milestone 1, and Fri 1 Jan 2027 for Milestone 2.
