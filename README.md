# Trupanion (trupanion)

Trupanion is a pet medical insurance provider for cats and dogs, best known for its patented software that pays participating veterinary hospitals directly at checkout (VetDirectPay) rather than reimbursing pet owners after the fact. Trupanion operates a partner developer portal (Azure API Management) that exposes Partner APIs for Quotes, Enrollments, and Offers, plus a Vet Portal / VetDirectPay integration used by veterinary practice management systems such as ezyVet, IDEXX, and DaySmart Vet.

**Access is partner-gated.** There is no openly published API reference. To obtain access, a partner must be approved through Trupanion's Partner Program; approved partners and practice management vendors are issued OAuth client credentials (a client ID and client secret) plus a subscription key. Practice management integrations download those credentials and send the file to `TruExLaunch@Trupanion.com` to complete onboarding. Because the operation-level endpoint reference sits behind partner sign-in, the APIs described here are **modeled from Trupanion's public partner and portal materials, not fabricated from a documented endpoint list** (`endpointsModeled: true`).

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/trupanion/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/trupanion/refs/heads/main/apis.yml)

## Tags

- Pet Insurance
- Insurance
- Veterinary
- InsurTech
- Direct Pay
- Partner API

## Timestamps

- **Created:** 2026-07-03
- **Modified:** 2026-07-03

## APIs

> All endpoints are partner-gated and modeled. Trupanion's sandbox developer portal ([api-documentation.trupanion.com](https://api-documentation.trupanion.com/)) names the Partner APIs for Quotes, Enrollments, and Offers but exposes the operation reference only after partner sign-in.

### Trupanion Quotes API

Partner API for generating and retrieving Trupanion pet insurance quotes (species, breed, age, location, and coverage inputs) so partners can surface a monthly premium in their own enrollment flow.

- **Human URL:** [https://api-documentation.trupanion.com/](https://api-documentation.trupanion.com/)

#### Tags

- Quotes
- Pricing
- Insurance

### Trupanion Enrollments API

Partner API for converting a quote into an active Trupanion policy - submitting pet, owner, and payment details to enroll a member and bind coverage.

- **Human URL:** [https://api-documentation.trupanion.com/](https://api-documentation.trupanion.com/)

#### Tags

- Enrollments
- Policies
- Insurance

### Trupanion Offers API

Partner API for retrieving Trupanion offers and promotional coverage programs (for example, breeder, shelter, and retail partner offers) that a partner can present to a pet owner.

- **Human URL:** [https://api-documentation.trupanion.com/](https://api-documentation.trupanion.com/)

#### Tags

- Offers
- Promotions
- Partnerships

### Trupanion Vet Portal / VetDirectPay Integration

Software integration behind Trupanion's VetDirectPay - the patented ability to submit a treatment invoice and pay the veterinary hospital directly at checkout, often before the pet owner leaves the exam room. Consumed by veterinary practice management systems (ezyVet, IDEXX, DaySmart Vet) that configure a Trupanion API partner integration using an issued client ID and client secret.

- **Human URL:** [https://vet.trupanion.com/](https://vet.trupanion.com/)

#### Tags

- Direct Pay
- Claims
- Veterinary
- Practice Management

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/trupanion)
- [Website](https://www.trupanion.com/)
- [Documentation](https://api-documentation.trupanion.com/)
- [Getting Started](https://sandbox-trupanionapi.developer.azure-api.net/getting-started)
- [Partner Program](https://www.trupanion.com/about/partner-with-trupanion)
- [Sign Up](https://sandbox-trupanionapi.developer.azure-api.net/signin)

## Pricing

Trupanion prices are consumer insurance premiums (a monthly premium per pet, driven by species, breed, age, and location, covering 90% of eligible costs with no payout limits in most states). There is no separate, published price for API access - the partner APIs and the free Vet Portal / VetDirectPay integration are provisioned to approved partners and veterinary hospitals rather than sold as a metered API product.

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
