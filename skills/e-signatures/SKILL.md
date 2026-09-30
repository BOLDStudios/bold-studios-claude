---
name: e-signatures
description: Send documents for signature and track them with BOLD Sign. Use when the user needs a contract, agreement, release, split sheet or any document signed, wants to know who has signed, needs an audit trail, or wants to cancel a signature request.
---

# E-signatures with BOLD Sign

## Sending a document

1. Collect the document, each signer's name and email, and whether order matters (for example, the client signs before the company countersigns).
2. Call `sign_create_document` ($0.10 per envelope, however many signers). Set the signing order when it matters.
3. The response contains one private signing link per signer. BOLD does not email signers. Give the links to the user and tell them to send each link only to its signer, because each link works as that person's signature key.
4. Offer to draft the short message the user can send with each link.

## Tracking

- `sign_list_documents` lists every request with its status.
- `sign_get_document` shows one request: who has signed, who is next, who declined.
- When everyone has signed, say so and offer the audit trail.

## Audit trail

`sign_audit_trail` returns the full record: consent, each signature, timestamps and addresses. Share it only with the sender, and recommend they keep it with the signed document.

## Voiding

`sign_void_document` cancels a request so no one else can sign it. Confirm with the user first, and tell them to let signers know.

## Good practice

- Put names exactly as they appear on legal ID.
- For anything with legal weight, remind the user that BOLD Sign records consent and intent but does not replace advice from a lawyer on the document itself.
