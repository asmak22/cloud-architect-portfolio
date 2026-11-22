
# ComixRus – Functional Requirements

| ID | Requirement | Priority |
|---|---|---|
| FR-01 | Writers must be able to register and submit comic books through a writer portal. | High |
| FR-02 | Editors must be able to review, approve or reject submissions before publication. | High |
| FR-03 | Customers must be able to browse comic descriptions and sample content without registering. | High |
| FR-04 | Customers must be able to register and securely authenticate. | High |
| FR-05 | Registered customers must be able to purchase digital comic books. | High |
| FR-06 | The platform must integrate with Stripe and PayPal for payment processing. | High |
| FR-07 | Customers must receive permanent access to comics they have purchased. | High |
| FR-08 | The platform must maintain customer purchase history and a digital library. | High |
| FR-09 | The platform must send asynchronous notifications for relevant events, such as submission updates and purchases. | Medium |
| FR-10 | Administrators must be able to manage published comics and catalogue information. | Medium |

## Assumptions

- Writers and editors have different access permissions.
- Customers do not need an account to view samples.
- A successful payment must be confirmed before granting access to a purchased comic.
- Purchased comics remain available to customers even if the comic is subsequently removed from public sale.

## Outstanding Questions

- What file formats will writers be allowed to upload?
- What is the maximum comic book file size?
- Can customers download purchased comics, or only read them online?
- Can editors request changes to submissions?
- What happens if a payment succeeds but the platform fails to grant access?
