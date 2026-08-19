# Asset rights review

Date checked: 2026-08-19. Reviewer: Keith Hughitt (conclusion approved) with
agent-assisted research.

## Scope

Every image under `sprites/` was generated between 2026-07-31 and 2026-08-02
via the OpenRouter images endpoint, model `openai/gpt-5.4-image-2`,
provider-pinned to OpenAI, no BYOK key. Per-image evidence:
`sprites/<member>/provenance.json` (full request, prompt, image digest, cost).

## Documents reviewed

| Document | Version / effective date | URL | Date checked |
| --- | --- | --- | --- |
| OpenRouter Terms of Service | "Last Updated: July 29, 2026" — in force on all three generation dates | https://openrouter.ai/terms | 2026-08-19 |
| Model Terms for openai/gpt-5.4-image-2 | No version or effective date stated in the document; current text as retrieved on the date checked. OpenRouter publishes no model-specific terms for this slug; the URL in this row is what it records as the OpenAI provider's "Terms of Service" at https://openrouter.ai/provider/openai | https://openai.com/policies/row-terms-of-use/ | 2026-08-19 |
| OpenAI output-ownership terms | "Effective: January 1, 2026" — in force on all three generation dates | https://openai.com/policies/services-agreement/ | 2026-08-19 |
| OpenAI Sharing & publication policy (incorporated by the agreement above) | No version or effective date stated in the document; current text as retrieved on the date checked | https://openai.com/policies/sharing-publication-policy/ | 2026-08-19 |

Retrieval notes. `openai.com` refused direct automated requests (HTTP 403), so
the three OpenAI documents were read through the `r.jina.ai` text proxy
(e.g. `https://r.jina.ai/https://openai.com/policies/services-agreement/`),
which returns the live page as text. No archived snapshot service was reachable
from the review environment, so for the two OpenAI documents that state no
effective date, the current text is the best available evidence and it is
recorded as current-as-of the date checked rather than as-of-generation. The
two documents that do state a date — the OpenRouter Terms of Service and the
OpenAI Services Agreement — both took effect before 2026-07-31 and so are the
versions that governed the generation runs.

## Findings

1. **Ownership/assignment:** No document claims the outputs for the platform.
   OpenRouter §6.1 keeps input rights with the user and delegates output rights
   downward: "You retain copyright and any other proprietary rights that you may
   hold in the Input. Your ownership rights in the Output are set forth in the
   Model Terms for each Model you use." §5.1 binds the user to those Model
   Terms. The terms OpenRouter records for the OpenAI provider (its "Terms of
   Use") assign outputs to the user — "you (a) retain your ownership rights in
   Input and (b) own the Output. We hereby assign to you all our right, title,
   and interest, if any, in and to Output" — and themselves route API use to
   OpenAI's business terms: "Our Business Terms govern use of ChatGPT
   Enterprise, our APIs, and our other services for businesses and developers."
   Those business terms are the OpenAI Services Agreement, which "only applies
   to use of OpenAI's APIs, ChatGPT Enterprise, ChatGPT Business, ChatGPT for
   Clinicians, and other services for customers who are businesses and
   developers," and which assigns identically: "As between Customer and OpenAI,
   to the extent permitted by applicable law, Customer: (a) retains all
   ownership rights in Input; and (b) owns all Output. OpenAI hereby assigns to
   Customer all OpenAI's right, title, and interest, if any, in and to Output."
   The chain therefore leaves whatever rights exist in the sprites with this
   project, and no document conditions distribution or sublicensing of outputs
   on the platform's permission, so relicensing under CC BY 4.0 is permitted.
   Two limits on that statement, both recorded rather than resolved here: the
   assignment is expressly "if any," so it transfers whatever rights OpenAI
   holds without warranting that copyright subsists in a machine-generated
   image at all; and OpenRouter's §6.2 logging licence (a "worldwide,
   perpetual, irrevocable, non-exclusive, royalty-free, fully paid right and
   license (with the right to sublicense) to host, store, transfer, display,
   perform, reproduce, modify for the purpose of formatting for display, adapt,
   translate, and prepare derivative works of, and distribute your User
   Content") is non-exclusive and so does not impair this project's own grant.

2. **Obligations:** Two conditions must be carried into `LICENSE-assets`, both
   from OpenAI's Sharing & publication policy, which the Services Agreement
   incorporates by reference along with the Usage Policies. For content created
   with the API the policy requires that "The published content is attributed to
   your name or company" and that "The role of AI in formulating the content is
   clearly disclosed in a way that no reader could possibly miss"; its
   social-media clause states the same pair as "Attribute the content to your
   name or your company" and "Indicate that the content is AI-generated in a way
   no user could reasonably miss." The policy's wording for the second clause
   speaks of "written content," so its application to generated images is by
   analogy rather than by its letter; the pack meets it either way by stating
   the AI origin plainly. A third restriction is recorded but deliberately not
   carried into the asset licence: Services Agreement §3.3(e) bars using Output
   "to develop artificial intelligence models that compete with OpenAI's
   products and services." That binds this project and OpenRouter as OpenAI's
   counterparties; it is not a condition CC BY 4.0 can impose on downstream
   recipients, since CC BY 4.0 forbids adding restrictions to the grant. It is
   noted here so the record is complete, not as a licence term. Nothing in any
   of the four documents requires a watermark, C2PA metadata, or any provenance
   marking in the image files themselves.

3. **Attribution party:** Nothing requires naming OpenAI or OpenRouter as an
   author or rights-holder. The only attribution obligation found runs the other
   way: the Sharing & publication policy requires the published content be
   attributed to "your name or company," i.e. to Keith Hughitt. OpenRouter's
   terms impose no attribution condition on outputs at all, and the OpenAI
   documents' sole related prohibition is against the opposite misrepresentation
   — the Terms of Use list, among prohibited uses, "Represent that Output
   was human-generated when it was not." Naming Keith Hughitt as the CC BY 4.0
   attribution party, alongside a plain statement that the sprites are
   AI-generated, satisfies both.

## Conclusion

Conclusion: PASS — the outputs may be distributed and licensed under
CC BY 4.0 with attribution to Keith Hughitt, subject to: the pack being
attributed to Keith Hughitt's name; and the pack disclosing that the sprites
are AI-generated in a way no reader could possibly miss.
