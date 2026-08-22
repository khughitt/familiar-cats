# Asset rights review

Date checked: 2026-08-21. Reviewer: Keith Hughitt (conclusion approved) with
agent-assisted research.

## Scope

Images under `sprites/` were generated between 2026-07-31 and 2026-08-21
via the OpenRouter images endpoint, model `openai/gpt-5.4-image-2`,
provider-pinned to OpenAI, no BYOK key. Per-image evidence:
`sprites/<member>/provenance.json` (full request, prompt, image digest, cost).

## Documents reviewed

| Document | Version / effective date | URL | Date checked |
| --- | --- | --- | --- |
| OpenRouter Terms of Service | "Last Updated: July 29, 2026" — in force on all generation dates | https://openrouter.ai/terms | 2026-08-21 |
| Model Terms for openai/gpt-5.4-image-2 | "Published: January 1, 2026" and "Effective: January 1, 2026". OpenRouter publishes no model-specific terms for this slug — neither the model page, its providers tab, nor the endpoints API carries a terms field — so the URL in this row is what OpenRouter records as the OpenAI provider's "Terms of Service" at https://openrouter.ai/provider/openai | https://openai.com/policies/row-terms-of-use/ | 2026-08-21 |
| OpenAI output-ownership terms (OpenAI Services Agreement) | "Effective: January 1, 2026" — in force on all generation dates | https://openai.com/policies/services-agreement/ | 2026-08-21 |
| OpenAI Sharing and Publication Policy (incorporated by the agreement above) | No version or effective date stated in the document; current text as retrieved on the date checked | https://openai.com/policies/sharing-publication-policy/ | 2026-08-21 |
| Creative Commons Attribution 4.0 International legalcode (the licence being applied, cited in Finding 2) | Version 4.0 International | https://creativecommons.org/licenses/by/4.0/legalcode.en | 2026-08-21 |

Retrieval notes. The OpenRouter and OpenAI documents were read directly from
their official pages. The Sharing and Publication Policy states no effective
date, so its current text is recorded as current-as-of the date checked rather
than as-of-generation. The three documents that do state a date — the
OpenRouter Terms of Service, OpenAI Terms of Use, and OpenAI Services Agreement
— all took effect before 2026-07-31 and so cover every generation run. The
2026-08-21 recheck found no substantive change to the findings or conclusion.

The Services Agreement addresses the undated-policy problem directly. §17
defines its incorporated policies as "the Service-Specific Terms, Sharing and
Publication Policy, and Usage Policies", and pins their version: "The version
of OpenAI Policies applicable to Customer are those in effect on the most
recent effective date between either the Agreement, Customer's most recent
Order Form, or Services renewal." What that settles: the obligations that
applied to the generation runs are a fixed, dated text, not whatever wording
happens to be live on any later reading. What it does not settle: the pinning
date is a fact about OpenRouter's own contract with OpenAI, which this project
cannot observe, and the policies carry no effective date of their own, so the
pinned text cannot be identified or retrieved from outside. The conditions in
Finding 2 are therefore recorded from the current text, on the assumption —
unverifiable from public sources — that the current wording of those two
conditions matches the pinned version.

## Findings

1. **Ownership/assignment:** No party in the chain asserts ownership of the
   outputs, but the chain does not close on this project by an express
   assignment, and the reason is that these were non-BYOK calls. The step-by-step
   position:

   OpenRouter takes no ownership. §6.1 supplies the definitions — "You may
   provide input into the Services, which may include images, data, text, and
   other types of work ("Input") and receive an output from the Services based
   on your Input ("Output", and collectively, the Input and Output are "User
   Content")" — grants a licence in that User Content — "By making any User
   Content available through the Service, you hereby grant to OpenRouter a
   non-exclusive, transferable, worldwide, royalty-free license, with the right
   to sublicense, to use, host, cache, store, reproduce, transmit, publicly
   display, publicly perform, publish, distribute and modify (for formatting
   purposes only), your User Content solely in connection with operating and
   providing the Service and, depending on the permission you grant for certain
   features, to provide to other users, individuals, and/or organizations" —
   and then disclaims the ownership question rather than answering it: "You
   retain copyright and any other proprietary rights that you may hold in the
   Input. Your ownership rights in the Output are set forth in the Model Terms
   for each Model you use." The
   separate §6.2 logging licence (a "worldwide, perpetual, irrevocable,
   non-exclusive, royalty-free, fully paid right and license (with the right to
   sublicense) to host, store, transfer, display, perform, reproduce, modify for
   the purpose of formatting for display, adapt, translate, and prepare
   derivative works of, and distribute your User Content, in whole or in part, in
   any media formats and through any media channels now known or hereafter
   developed, for purposes of providing the Services to you and for our own
   commercial and business purposes") applies where prompt logging is opted into.
   Neither grant is confined to service operation on its face: §6.1's extends to
   providing User Content "to other users, individuals, and/or organizations"
   where the user grants that permission, and §6.2's reaches OpenRouter's "own
   commercial and business purposes". What the analysis turns on is that both are
   expressly non-exclusive, so neither impairs this project's own grant, and
   neither is an ownership claim.

   §6.1 hands the question to the Model Terms, and §5.1 binds the user to them:
   "you agree, and will ensure that your Authorized Users and customers agree,
   to comply with the applicable terms for each Model". The Model Terms
   OpenRouter records for the OpenAI provider are OpenAI's Terms of Use, which
   assign outputs to the reader of that document: "you (a) retain your ownership
   rights in Input and (b) own the Output. We hereby assign to you all our
   right, title, and interest, if any, in and to Output."

   The privity step. That Terms of Use document also states "Our Business Terms
   govern use of ChatGPT Enterprise, our APIs, and our other services for
   businesses and developers" — so on its own terms it does not govern API
   calls. The document that does is the OpenAI Services Agreement, which "only
   applies to use of OpenAI's APIs, ChatGPT Enterprise, ChatGPT Business,
   ChatGPT for Clinicians, and other services for customers who are businesses
   and developers", and whose assignment runs to "Customer" — defined in its
   preamble as "the organization agreeing to these terms" — not to the end user:
   "As between Customer and OpenAI, to the extent permitted by applicable law,
   Customer: (a) retains all ownership rights in Input; and (b) owns all Output.
   OpenAI hereby assigns to Customer all OpenAI's right, title, and interest, if
   any, in and to Output." Because these calls were non-BYOK, the OpenAI account
   holder — and therefore OpenAI's "Customer" — is OpenRouter, not this project.
   No document in the chain expressly re-assigns OpenAI's transferred interest
   onward from OpenRouter to the end user. OpenRouter's flow-down clause runs
   the other way: §5.2 ("Flow-Down to Authorized Users") requires "that all of
   your Authorized Users and customers access and use the Service and Models
   only in accordance with this Agreement, any documentation provided by
   OpenRouter on the Site and Service, and the applicable Model Terms", and adds
   "You will be responsible for all acts and omissions of your Authorized Users,
   including any violation of applicable Model Terms." It flows obligations
   down; it does not flow the ownership assignment through.

   This is recorded as an open limit, not resolved. What can be said on the
   sources is narrower than an unbroken chain of title: OpenAI has assigned away
   whatever interest it held; OpenRouter, the assignee, claims no ownership of
   Output and takes only non-exclusive licences in it, while
   directing the user to Model Terms whose operative sentence assigns Output to
   the person using the model; and no document anywhere bars the user from
   distributing or sublicensing Output. So no party asserts a right adverse to
   this project, and relicensing under CC BY 4.0 is permitted by the terms — but
   the user's position rests on OpenRouter disclaiming the question plus the
   recorded Model Terms' assignment language, not on an express grant from
   OpenRouter. Two further limits, recorded on the same footing: the assignment
   is expressly "if any", so it transfers whatever rights OpenAI holds without
   warranting that copyright subsists in a machine-generated image at all; and
   nothing here is a warranty of title, only a finding that the terms permit
   the grant.

2. **Obligations:** The operative source is OpenAI's Sharing and Publication
   Policy. The obligation to obey it sits in Services Agreement §3.3
   (Restrictions) — "Customer will not, and will not permit End Users to: (a) use
   the Services or Customer Content in a way that violates applicable laws or
   OpenAI Policies" — which, these being non-BYOK calls, binds OpenRouter
   directly as OpenAI's Customer and reaches this project only through
   OpenRouter §5.2's flow-down of Model Terms compliance, the same indirect
   route as §3.3(e) below. §17 (Definitions) supplies the term, defining
   "OpenAI Policies" as "the Service-Specific Terms, Sharing and Publication
   Policy, and Usage Policies" and pinning which version applies. It speaks to
   this pack twice over. Its social-media section opens "Posting your own
   prompts or completions to social media is generally permissible, as is
   livestreaming your usage or demonstrating our products to groups of people",
   which reaches images by its letter — it is not limited to text. Its
   published-works section is so limited by its introduction ("Creators who wish
   to publish their first-party written content (e.g., a book, compendium of
   short stories) created in part with the OpenAI API are permitted to do so
   under the following conditions:"), and that qualifier governs every bullet in
   that section, so distributing a sprite pack falls under it only by analogy.
   Both sections impose the same pair of conditions, and they are the two
   carried into `LICENSE-assets`:

   - Attribution: "The published content is attributed to your name or company"
     (published works); "Attribute the content to your name or your company"
     (social media).
   - Disclosure: "The role of AI in formulating the content is clearly disclosed
     in a way that no reader could possibly miss, and that a typical reader would
     find sufficiently easy to understand" (published works); "Indicate that the
     content is AI-generated in a way no user could reasonably miss or
     misunderstand" (social media). Both halves matter: the disclosure must be
     conspicuous *and* intelligible to an ordinary reader.

   The disclosure's content is fixed by what the policy adds after the
   published-works list. First: "For instance, one must detail in a Foreword or
   Introduction (or some place similar) the relative roles of drafting, editing,
   etc." Then: "People should not represent API-generated content as
   being wholly generated by a human or wholly generated by an AI, and it is a
   human who must take ultimate responsibility for the content being published."
   A bare "these sprites are AI-generated" would therefore be wrong in the other
   direction. The disclosure must name the human role and responsibility as well
   as the AI one, which is why the conclusion's second condition is phrased as
   AI-generated at Keith Hughitt's direction and his responsibility.

   Why the remaining bullets of both lists are not carried into the licence. Two
   further bullets appear in the published-works list. "Topics of the content do
   not violate OpenAI's Content Policy or Terms of Use, e.g., are not related to
   adult content, spam, hateful content, content that incites violence, or other
   uses that may cause social harm" is a content-topic restriction on what this
   project publishes,
   satisfied on its face by pixel-art cats, and not a term a licence grants
   downstream. "We kindly ask that you refrain from sharing outputs that may
   offend others" is framed as a request, not an obligation. The social-media
   list — the one that reaches these images by its letter — carries three further
   bullets, excluded for the same kind of reason. "Manually review each
   generation before sharing or while streaming." is a duty owed at generation
   time, discharged before publication and not something a recipient could
   perform. "Do not share content that violates our Content Policy or that may
   offend others." is again a content-topic restriction on this project's own
   publication, satisfied on its face by pixel-art cats. "If taking audience
   requests for prompts, use good judgment; do not input prompts that might
   result in violations of our Content Policy." governs live prompting, which
   distributing a finished pack does not involve. None becomes a licence
   sentence.

   One further restriction is recorded and deliberately not carried into the
   asset licence: Services Agreement §3.3(e) bars Customer from "except for a
   Permitted Exception, use Output to develop artificial intelligence models
   that compete with OpenAI's products and services", where a "Permitted
   Exception" means "Customer using Output to: (a) develop artificial
   intelligence models primarily intended to categorize, classify, or organize
   data (e.g., embeddings or classifiers), if these models are not distributed
   or made commercially available to third parties; and (b) fine tune or
   customize models provided as part of OpenAI's fine-tuning or other Services
   set forth on the Pricing Page." Under non-BYOK that clause binds OpenRouter
   directly, as OpenAI's Customer, and reaches this project only through
   OpenRouter §5.2's flow-down of Model Terms compliance. Either way it is not a
   condition CC BY 4.0 can carry. §2(a)(5)(A) of that licence ("Offer from the
   Licensor – Licensed Material") provides: "Every recipient of the Licensed
   Material automatically receives an offer from the Licensor to exercise the
   Licensed Rights under the terms and conditions of this Public License." The
   offer each downstream recipient receives is therefore fixed as this Public
   License's own terms, which leaves no slot for a licensor-added non-compete.
   §2(a)(5)(B) ("No downstream restrictions") adds: "You may not offer or impose
   any additional or different terms or conditions on, or apply any Effective
   Technological Measures to, the Licensed Material if doing so restricts
   exercise of the Licensed Rights by any recipient of the Licensed Material."
   That second clause is addressed to "You", defined in §1 as "the individual or
   entity exercising the Licensed Rights under this Public License", so it
   constrains those passing the material on rather than the licensor's original
   grant; §2(a)(5)(A) is the clause that fixes what the licensor's own offer
   contains. It is noted here so the record is complete, not as a licence term.
   Nothing in any of the four platform documents requires a watermark, C2PA
   metadata, or any provenance marking inside the image files themselves.

3. **Attribution party:** Nothing requires naming OpenAI or OpenRouter, and the
   Services Agreement affirmatively discourages it. §10 (No Publicity): "Except
   with express prior written permission in each instance, neither Party will:
   (i) include the other Party's name or logo on their websites, media, or
   marketing materials; or (ii) make any public statement about its relationship
   with the other Party or this Agreement." Naming OpenAI as a rights-holder or
   co-author in the licence would be exactly the sort of statement that clause
   restrains between the parties to it. The only attribution obligation found
   runs the other way: the Sharing and Publication Policy requires the published
   content be attributed to "your name or company", i.e. to Keith Hughitt.
   OpenRouter's terms impose no attribution condition on outputs at all. The
   OpenAI Terms of Use's sole related provision is the mirror-image prohibition,
   listing among prohibited uses "Represent that Output was human-generated when
   it was not." Naming Keith Hughitt as the CC BY 4.0 attribution party,
   alongside a disclosure that states both the AI role and his own, satisfies
   all of these. Recording the provenance facts in
   `sprites/<member>/provenance.json`, which names the model and endpoint as
   evidence rather than as marketing attribution, is descriptive and outside
   §10's subject matter.

## Conclusion

Conclusion: PASS — the outputs may be distributed and licensed under
CC BY 4.0 with attribution to Keith Hughitt, subject to: the pack being
attributed to Keith Hughitt's name; and the pack disclosing the sprites' origin
in a way no reader could possibly miss and that a typical reader would find
sufficiently easy to understand, stating that they were AI-generated at Keith
Hughitt's direction and are his responsibility, rather than presenting them as
wholly human-generated or wholly AI-generated.
