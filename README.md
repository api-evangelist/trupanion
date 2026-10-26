# Trupanion (trupanion)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
