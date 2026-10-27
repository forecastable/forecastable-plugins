# Collection: Crossbeam Matching Engine

Source: https://help.crossbeam.com/en/collections/3034361-crossbeam-matching-engine. Captured September 30th, 2026.


## Overview of Crossbeam's Matching Process (HC 10492031)
URL: https://help.crossbeam.com/en/articles/10492031-updated-matching-process-with-duns

In this article:
- Overview of Crossbeam's Matching Process
- How DUNS Impacts Matching
- FAQ
Crossbeam ensures high-confidence data matching by prioritizing accuracy and minimizing false positives. Our algorithm evaluates multiple data points, emphasizing unique identifiers like domain names and email addresses. Customers cannot modify the algorithm, ensuring consistency. DUNS is now an additional matching dimension.

### How DUNS Impacts Matching
DUNS (Data Universal Numbering System) number is a globally recognized identifier that strengthens our confidence in matches, improving accuracy and consistency for our customers.

How DUNS Impacts Matching:
- If a DUNS number is present and matches between records, the records are considered a match.
- If a DUNS number is present but does not match, the records are not considered a match.
- If a DUNS number is not present, we revert to our standard matching algorithm, which includes URL

Key Considerations:
- The DUNS number field must be manually mapped per Data Source
- If available, DUNS takes precedence over other matching criteria
- For records without a DUNS number, Crossbeam continues to use its existing confidence-based algorithm.

### FAQ
Is DUNS supported for all data sources? You can map DUNS data for any data source.
There are some limitations on mapping DUNS data retroactively for CSVs and G-Sheets. If you run into issues, please reach out to support.

Does Crossbeam strip out any dashes in DUNS numbers? Yes, this means 123456789 matches 12-345-6789.

Does Crossbeam only support DUNS fields that are type “text” from CRMs? Yes, DUNS numbers from CRMs that are type “number” may not work properly within our matching. DUNS numbers may have a leading 0, which will get removed if the field type is 0, causing us to be unable to match with high confidence in our system.

Does Crossbeam currently support DUNS+4 numbers?
No, we do not currently support DUNS+4 numbers. ​ Context: Businesses may choose to append four extra alphanumeric characters to their DUNS number. This is called a DUNS+4 number. The suffix is for the use of the business (for example, to identify different electronic funds transfer accounts). It has no significance otherwise and is not tracked by Dun & Bradstreet.

Can I retroactively select more than one DUNS column name for file uploads?
No, Crossbeam can only retroactively select one DUNS column name for file uploads. For file uploads, if there are currently multiple files that have DUNS data where the files have different column names for DUNS.
- Crossbeam cannot retroactively map multiple different DUNS column names, we can only choose 1
- For any additional data that is added, we CAN add a different column name for DUNS at the time of upload
- Understanding Crossbeam Matching
- Upload a CSV File and Map Your Fields
- Crossbeam Product Release Notes--02/04/2025
- Crossbeam Product Release Notes 11/6/2025
- The Crossbeam Matching Engine: Our Secret Sauce


## 12871671-the-crossbeam-matching-engine-our-secret-sauce.html (HC 12871671)
URL: https://help.crossbeam.com/en/articles/12871671-the-crossbeam-matching-engine-our-secret-sauce

As a self-certified data nerd, I’m proud to say that Crossbeam is a true powerhouse of a data platform. Data pipelines, security, user management, interfaces, integrations… the list goes on. But there is one rarely-discussed piece of Crossbeam’s data stack that touches every iota of value we produce for our customers: The Crossbeam Matching Engine.

When we talk about “Matching” here, we’re talking about matching data points across company lines: Making sure that “my account” and “your account” actually represent the same company or that “my contact” and “your contact” are actually the same person.
In this article, we’ll dig into “the matching problem” that Crossbeam has tackled over many years, and a glimpse into some of the secret sauce that powers our engine today.


#### The matching problem
Matching may sound like a simple problem at first, but it quickly spirals into a complex, multifaceted surface:
- What happens when we need to match across different CRM platforms who organize concepts differently (i.e. HubSpot vs. Salesforce vs. a Google Sheet?)
- What happens when companies have distinct data points that don’t overlap at all (i.e. one has a name, another has a domain, a third has a contact?)
- How do you weigh a name vs. a domain vs. an email vs. a DUNS Number vs. a physical address etc etc etc…
- How do you handle subsidiaries and company hierarchies?
For example, what if one company has an account named “Delta” that represents Delta Airlines, but another has one called “Delta” that represents Delta Faucets? They shouldn’t match. But in another case, a company could have a record with the domain delta.com and another’s account has a domain of deltaairlines.com? They SHOULD match (the airline owns both domains, and one redirects to another).

Getting this right across millions of companies (and billions of CRM records) is the whole ballgame, and the Crossbeam Matching Engine is the star.


#### Why matching matters
In simple terms, matching is the core of our trust engine, and trust is our business.
Most companies use Crossbeam to enable rules that say something like “if this account matches a customer in my partner’s CRM, then share the details from our CRM.” As a result, the brain that decides when “a match is a match” is also the trust engine that governs how and when data changes hands across companies.

If the matching algorithm gets it wrong, that can come in two flavors: False Positives and False Negatives.

False Positives

If we accidentally declare something a match that isn’t really one, it’s a big deal. This is called a “false positive.”

We have a very low tolerance for false positives, as they can result in data unintentionally being shared. We take extreme care to make sure that each “match” is supported by a strong level of statistical and hard data evidence.

False Negatives

The flip side is “false negatives,” where we “miss” a match and fail to identify it. This is also painful, but more on the value creation side. Every match that we miss is a missed opportunity for new business and ROI for our customers. This creates motivation for us to make the algorithm as robust and multifaceted as we can to ensure every match is found without creating false negatives. Over time, this has been the driving motivator to make the algorithm more robust.


#### The evolution of matching
Crossbeam’s current matching engine is built around a highly controlled, facts-based framework designed to ensure accuracy. It follows a clear process to narrow raw CRM data down to the most trusted identifiers:
- ‍ Data cleaning. From potentially hundreds of CRM fields, we focus only on those that are most actively present, updated, and exclusive (on their own or in combination): company name, domain, phone numbers, emails, and the like. These are cleaned, normalized, and reduced to a consistent root format. ‍
- Quality filtering: We automatically remove junk data, test domains, and placeholder records that can distort matching outcomes. ‍
- Network-informed enrichment. When a record is partially complete but there is a high quality unique identifier (or set of them) present, the engine is able to look for common associations that are observable across and anonymized and aggregated slices of our data set. These allow us to do proprietary enrichment to further fortify the record and find common properties even if the starting point made the records disparate. ‍
- Matching: Once the data is sanitized, matching happens through strict comparison. If the data points align, it is a match. If they do not, it is not.
As we continue to invest in matching, we are seeing the system become smarter and more context-aware. This natural evolution is allowing us to scale with our growing ecosystem and diverse universe of customer types while still maintaining the highest standards of accuracy and trust.

Here are a few areas where we’re currently investing:

1. Expanding the data points that power matching ​ We are moving beyond the most common CRM properties to include a richer set of account attributes: phone numbers, tax IDs, DUNS identifiers, and detailed location data. ​ For small businesses and franchises that often lack consistent domains, we will extract brand or franchise names from social profiles and marketplace pages, turning previously ignored data into valuable matching inputs. All these new fields will be normalized and structured so that they can be compared intelligently across systems.

2. Early detection and adaptive classification ​ Before matching even begins, we will identify and classify records by type. It will detect and exclude junk data, recognize duplicate entries, and apply tailored logic for different business categories such as franchises or large enterprises. For example, if a phone number appears across too many CRM records, it will automatically be discounted, while domains shared across multiple accounts will be flagged as potential franchise indicators.

3. Multi-attribute enrichment powered by ecosystem data ​ With more than 30,000 companies in our network, Crossbeam has a unique view into how real-world data behaves across CRMs via anonymized, aggregated slices of that data. We will leverage that intelligence, mapping which fields tend to co-occur within real companies across the ecosystem. ‍ If an account record is missing key details, the system will use this knowledge to infer the most likely associated attributes (such as websites, phone numbers, or country code) creating a more complete, consolidated record. This network-level enrichment strengthens inputs before they ever reach the matching stage, improving precision and uncovering matches that would otherwise be invisible.

4. Weighted, confidence-based scoring ​ The new engine will calculate a confidence score for every potential overlap. Each attribute contributes to the overall score according to its reliability and context. ‍ For a large enterprise, a domain match may be sufficient. For a franchise, additional signals like phone number, location, or brand alignment might be required to reach the same confidence level. These confidence scores will allow for ranked results, smarter automation thresholds, and human review where needed.

5. Continuous improvement through AI ​ It’s worth noting that matching billions of data points against each other is not necessarily a job that is best solved by an LLM, although LLMs introduce opportunities to help us analyze, weigh, ideate, and iterate on the logic we apply. In other words, we’re not training a custom LLM to do this job or using our data as training data. We’re just better at building our matching engine because LLMs are our co-pilots in creating continuous improvements.

AI models will guide how attributes are weighted, how thresholds are tuned, and how exceptions are handled. Over time, these models will learn from real match outcomes and adjust parameters to optimize accuracy. ‍ The system will also perform automatic evaluations to refine preprocessing rules and improve how different attributes contribute to overall confidence.

The result is an engine that is smarter, scalable, and increasingly autonomous. It learns from the ecosystem itself, gets more accurate with every record, and delivers cleaner, high-confidence matches.


#### Conclusion
Matching sits at the heart of Crossbeam’s value, and it’s only getting smarter. As our network expands and our data grows richer, the Matching Engine continues to evolve from a deterministic system into an adaptive intelligence that learns from billions of real-world relationships. It’s not just about finding overlaps anymore, it’s about understanding them, ranking them, and enabling our users to act on them with confidence. Every improvement we make here compounds across the entire Crossbeam ecosystem, sharpening the insights that power our products.

This is why we call it our “secret sauce.” Matching is the invisible engine that turns trust into action and data into revenue. It’s the quiet superpower that ensures our platform scales accurately, securely, and ethically across tens of thousands of connected companies. As we look ahead, the Matching Engine will remain the foundation for everything we build, from ecosystem-wide analytics to AI-driven revenue orchestration, fueling the next generation of ecosystem intelligence.
- Understanding Crossbeam Matching
- Crossbeam Overview for Compliance Teams
- Crossbeam MCP Server
- Understanding Crossbeam AI and Data Use


## Overview (HC 14693133)
URL: https://help.crossbeam.com/en/articles/14693133-how-to-troubleshoot-missing-overlaps

In this article:
- Overview
- Common Causes Website Domain Mismatch Missing Website Domain Account Record Not Included in a Shared Population
- Website Domain Mismatch
- Missing Website Domain
- Account Record Not Included in a Shared Population
- Troubleshooting Steps Step 1: Search for the Account Record in Crossbeam Step 2: Confirm the Account Record Is in a Shared Population Step 3: Compare Website Domains Step 4: Compare Company Names Step 5: When to Contact Support
- Step 1: Search for the Account Record in Crossbeam
- Step 2: Confirm the Account Record Is in a Shared Population
- Step 3: Compare Website Domains
- Step 4: Compare Company Names
- Step 5: When to Contact Support
If you expect to see an account as an overlap but do not, it does not necessarily mean something is broken. Crossbeam identifies overlaps using specific matching logic. If any part of that logic doesn't align on both sides of the partnership, the overlap won't appear.
In most cases, this is caused by one of the following:
- Website domains do not match
- One or both account records are missing a website domain
- The account record isn't included in a shared Population
Use the troubleshooting steps below to identify the root cause.
✍️ Note
Crossbeam cannot view or disclose a partner's Population configuration due to data-sharing limitations. You will need to coordinate with your partner to verify their setup.

### Common Causes

#### Website Domain Mismatch
Crossbeam primarily matches accounts using website domains. If the domains differ, the accounts won't match.

These will match :
- acme.com
- www.acme.com
- https://acme.com
These will not match :
- shop.acme.com and acme.com
- acme.com and acme.net

#### Missing Website Domain
If a website domain is not available, Crossbeam falls back to matching by company name.

Company names are normalized before matching by removing punctuation, common business suffixes (such as "Inc." or "LLC"), and accent characters. However, abbreviations, trade names, or alternate spellings may still prevent a match.
🤓 Learn more in Understanding Crossbeam Matching .

#### Account Record Not Included in a Shared Population
An account must be included in a shared Population for both organizations before it can appear as an overlap.

If the account doesn't meet a Population's filters or the Population isn't shared with your partner, the overlap won't appear.

### Troubleshooting Steps

#### Step 1: Search for the account
From the side navigation in Crossbeam, use the search bar to open the account record detail page.

From the account record page, confirm:
- The account belongs to a Population If it shows No Populations, it won't appear as an overlap
- If it shows No Populations, it won't appear as an overlap
- The website domain imported into Crossbeam
- The company name imported into Crossbeam
Ask your partner to search for the same account in their Crossbeam account. The account record must belong to a shared Population on both sides before an overlap can appear.

#### Step 2: Confirm the account Is in a Shared Population
- Navigate to Data → Populations
- Click on the relevant Population to open it
- Review the Population filters
- Confirm the account meets the Population's filter criteria, then click the Close button
- Confirm the Population is shared with the correct partner: Click the three-dot menu, select Partner-specific Sharing Search the partner name in the table and confirm the Population is shared
- Click the three-dot menu, select Partner-specific Sharing
- Search the partner name in the table and confirm the Population is shared
If needed, update the Population filters and allow the changes to sync.
Learn more: How to Edit a Population
✍️ Note
Both organizations must include the account record in a shared Population for the overlap to appear. Ask your partner to verify the same on their side.

#### Step 3: Compare Website Domains
If the account record is included in a shared population, verify the website domain.
- Open the account record in Crossbeam
- Note the value in the Website field
- Ask your partner to confirm the domain value they have for the same account
If the domains differ, update the value in your CRM and wait for the next sync to complete.

Crossbeam automatically normalizes common formatting differences such as https://, www., and trailing slashes before matching. However, true subdomains (for example, shop.acme.com ) and different top-level domains (for example, acme.net ) are treated as different domains.

#### Step 4: Compare Company Names
If neither side has a website domain, Crossbeam attempts to match using company names.
- Review the Company Name value in Crossbeam
- Ask your partner to confirm the company name they have for the same account
If the names differ significantly, update the value in your CRM and allow the next sync to complete.

#### Step 5: When to Contact Support
If you've confirmed that:
- The account record exists in shared Populations on both sides
- The website domains match, or the company names align when a website domain isn't available
and the overlap still does not appear, contact Crossbeam Support with:
- The account name
- The website domain
- The partner organization name
- Screenshots showing the account record in your shared Population

- Installation Guide: Crossbeam for Salesforce (v2)
- Setting Up a Crossbeam Ecosystem Overlaps Related List in Salesforce
- How to Set Up the Partner Account CRM Integration
- How to Create a Combined Overlap and Partner Account Report Type in Salesforce


## Matching Overview (HC 3160297)
URL: https://help.crossbeam.com/en/articles/3160297-understanding-crossbeam-matching

In this article:
- Matching Overview Domain Names Email Addresses DUNS Phone Brand/Marketplace
- Domain Names
- Email Addresses
- DUNS
- Phone
- Brand/Marketplace
- Putting It All Together

😎 Pro Tip
Want to take a deeper dive into how the Crossbeam Matching Engine works? Check out this article .

Crossbeam identifies overlaps between company data sets, which raises a key question: when are two records a match? That’s where our matching algorithm comes in.
The algorithm is guided by confidence. Because matches often trigger data sharing, Crossbeam requires very high confidence before declaring a match. False positives (incorrect matches) are far worse than false negatives, and the algorithm is designed accordingly.
We compare multiple record properties to calculate a confidence score, giving extra weight to unique attributes. Customers cannot modify the matching algorithm.

Here are the key data points used in matching.
✍️ Note
Use the Crossbeam Co-Selling Preset when syncing your data to get the most accurate matching. Click here to learn how to edit data sync fields.

#### Domain Names
Domain names are a source of high-confidence company matches, as no two companies can have the same domain. We run domain names through a standardization process to ensure that inconsistencies in formatting don't create false positives. We also maintain a growing awareness of cases where multiple domains are owned by the same company so that indirect matches can be made. Things to note about domain names:
- Crossbeam will strip out anything after the top level domain (TLD), i.e. google.com will match google.com/en
- Subdomains are not stripped out, and will not match the main domain alone, i.e. flights.google.com will not match google.com
- Capitalization and slashes do not matter, i.e. GoOgle.com will match google.com
- TLD differences (.com vs .net) will be treated as separate accounts, i.e. google.com will not match google.net

#### Email Address
Email addresses are a source of high confidence person matches, as no two people can have the same email address. These addresses are run through a similar cleansing and standardization process as domains. Emails also have a bonus benefit of helping with company match resolution, as we can often determine that companies match based on them having matching people. When certain quality conditions are met, we can also use the domain name of contacts as a matching property for companies.

#### DUNS
DUNS (Data Universal Numbering System) number is a globally recognized identifier that strengthens our confidence in matches, improving accuracy and consistency for our customers.
How DUNS Impacts Matching:
- If a DUNS number is present and matches between records, the records are considered a match.
- If a DUNS number is present but does not match, the records are not considered a match.
- If a DUNS number is not present, we revert to our standard matching algorithm, which includes URL

#### Phone
Phone number matching identifies overlaps between accounts that share the same valid phone number, even when their domains don’t match. This ensures you capture connections that would otherwise be missed in traditional domain-based matching. Crossbeam automatically normalizes, validates, and deduplicates phone numbers using international standards, removing invalid or test data to deliver accurate, high-confidence matches.


#### Brand/Marketplace
Brand matching enhances the Crossbeam Matching Engine by identifying overlaps between accounts that share the same brand name, even when their domains differ. This helps uncover connections across franchise networks, marketplace listings, and multi-brand organizations that traditional domain-based matching might miss. Crossbeam automatically parses, normalizes, and validates brand data from multiple sources, such as social profiles or marketplace URLs, to deliver accurate, high-confidence matches between related entities.


### Putting It All Together
While individual properties like domain, email, DUNS, phone, and brand provide the foundation for high-confidence matches, real-world names alone are low-confidence. Crossbeam’s algorithm combines multiple dimensions to validate matches, ensuring accuracy while minimizing false positives.

The matching engine is continuously evolving, adding new fields and data points to improve match quality. Occasional minor shifts in match rates are normal and reflect improvements in the methodology.

### FAQ
How does DUNS matching work?
Read more about it here .

Can you match using other dimensions?
Not currently, no, but our matching engine is always getting more intelligent as we add more matching dimensions.

- Crossbeam Overview for Compliance Teams
- Crossbeam Product Release Notes--02/04/2025
- Updated Matching Process with DUNS
- The Crossbeam Matching Engine: Our Secret Sauce
- Understanding Crossbeam AI and Data Use


## Report Incorrect Matches (HC 5246994)
URL: https://help.crossbeam.com/en/articles/5246994-report-incorrect-matches

In this article:
- Report Incorrect Matches
- View Reported Incorrect Matches
- FAQs

The Crossbeam matching engine delivers the industry's most accurate account matches. It continuously improves through user feedback and third-party data validation, bridging data gaps to find overlaps in first and second-party datasets.

While our matching algorithm is highly accurate, dirty data in your or your partner's CRM may lead to incorrect matches.
You can report incorrect matches to Crossbeam:

- When viewing an Account, you'll see a button on the right that says Report an Incorrect Match :

- Clicking this will prompt you to give us some data to help determine why the match is incorrect:

Click Send Report when you are done.

### Viewing Reported Incorrect Matches
If you or your partner has reported a match as incorrect, you will see an indication of the report in the partner section of the Account page:

This is currently the only place to view Incorrect Match Reports.

### FAQs
What happens next?
Your report is used as an input to our matching engine, which will learn from any mistakes and improve matching based on your reports.

When does Crossbeam let me know that a match was removed?
Crossbeam does not respond to Incorrect Match Reports. They are used to train our matching engine, and are not treated as individual support requests. If you have an issue with a match that requires immediate resolution, please reach out to your customer support manager or email us at support@crossbeam.com . <!-- VALIDATE-OK[person-address]: verbatim public Crossbeam Help Center text -->
- Understanding Crossbeam Matching
- Snowflake Integration
- Installation Guide: Crossbeam for Salesforce (v2)
- Crossbeam Overview for Compliance Teams
- The Crossbeam Matching Engine: Our Secret Sauce
