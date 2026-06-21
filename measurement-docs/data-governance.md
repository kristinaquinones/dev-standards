# Data governance

## Overview

Data governance ensures that data is collected, stored, and used responsibly, ethically, and in compliance with regulations. This guide covers privacy compliance, data quality, access controls, and documentation for product managers and project managers.

## Privacy compliance basics

### Key Regulations

**GDPR (General Data Protection Regulation) - EU**

GDPR separates two different things: the principles that govern how you handle data, and the rights that individuals (data subjects) have.

**Principles (how you must handle data):**
- **Lawfulness, fairness, and transparency**: Process data lawfully and be open about it
- **Purpose Limitation**: Only collect data for stated purposes
- **Data Minimisation**: Collect only what's necessary
- **Accuracy**: Keep personal data accurate and up to date
- **Storage Limitation**: Keep data only as long as necessary for its purpose
- **Integrity and Confidentiality**: Keep data secure
- **Accountability**: Be able to demonstrate compliance

**Lawful basis:**
- You need a lawful basis to process personal data. Consent is only ONE of six lawful bases (consent, contract, legal obligation, vital interests, public task, legitimate interests).
- Where consent IS your basis, it must be freely given, specific, informed, and unambiguous (a clear opt-in, not pre-checked boxes), and easy to withdraw.

**Data subject rights (what individuals can ask of you):**
- **Right to Access**: Users can request their data
- **Right to Rectification**: Users can request correction of inaccurate data
- **Right to Erasure (Deletion)**: Users can request data deletion
- **Right to Data Portability**: Users can export their data
- **Right to Object/Restrict**: Users can object to or restrict certain processing

**What It Means for You:**
- Identify a lawful basis for each kind of processing, and get clear consent where consent is the basis you rely on
- Document what data you collect and why
- Provide ways for users to access, correct, and delete their data
- Only collect data you actually need, and keep it only as long as necessary

**CCPA (California Consumer Privacy Act) - California**

**Key Rights (as amended by CPRA, effective 2023):**
- **Right to Know**: Users can request what data is collected
- **Right to Delete**: Users can request data deletion
- **Right to Correct**: Users can request correction of inaccurate personal information
- **Right to Opt-Out**: Users can opt out of the sale or sharing of their personal information
- **Right to Limit Use of Sensitive Personal Information**: Users can limit how their sensitive personal information is used and disclosed
- **Non-Discrimination**: Can't discriminate against users who exercise rights

**What It Means for You:**
- Provide clear privacy notices
- Offer opt-out mechanisms
- Respond to user data requests
- Don't penalize users for exercising privacy rights

### Privacy Best Practices

**1. Transparency**
- Clear privacy policy explaining what you collect
- Plain language, not legal jargon
- Easy to find and understand
- Updated when practices change

**2. Consent**
- Explicit consent for data collection
- Clear opt-in, not pre-checked boxes
- Easy to withdraw consent
- Document consent decisions

**3. Data Minimization**
- Collect only what you need
- Don't hoard data "just in case"
- Regularly review what you collect
- Delete data you no longer need

**4. User Rights**
- Provide ways to access data
- Enable data deletion
- Support data export
- Respond to requests promptly

**5. Security**
- Protect data from unauthorized access
- Use encryption for sensitive data
- Limit who can access data
- Monitor for breaches

## Data quality practices

### Ensuring Data Accuracy

**1. Validation**
- Validate data at collection point
- Check for required fields
- Verify data formats
- Test data collection regularly

**2. Monitoring**
- Monitor for missing data
- Check for unexpected values
- Track data completeness
- Alert on data quality issues

**3. Documentation**
- Document what each data point means
- Explain how data is collected
- Note any limitations or caveats
- Keep documentation up to date

**4. Regular Audits**
- Review data quality periodically
- Identify and fix issues
- Remove bad or outdated data
- Improve collection processes

### Common Data Quality Issues

**Missing Data:**
- Some events not tracked
- Incomplete user profiles
- Gaps in time series data

**Incorrect Data:**
- Wrong event names
- Incorrect property values
- Misconfigured tracking

**Duplicate Data:**
- Events tracked multiple times
- Duplicate user records
- Redundant data points

**Outdated Data:**
- Data no longer relevant
- Stale user attributes
- Historical data that's misleading

## Access controls

### Who Can Access What

**1. Define Access Levels**
- **Public**: Anyone can see (aggregated, anonymized)
- **Team**: Product team members
- **Restricted**: Sensitive data, limited access
- **Admin**: Full access, data management

**2. Role-Based Access**
- **Viewers**: Can see dashboards and reports
- **Analysts**: Can query data and create reports
- **Admins**: Can configure tracking and manage data
- **Developers**: Can implement tracking code

**3. Data Sensitivity**
- **Public Data**: Aggregated metrics, truly anonymized data (see the note below; pseudonymized data does not belong here)
- **Internal Data**: User behavior, product usage
- **Sensitive Data**: PII, financial information
- **Restricted Data**: Personal details, private information

**Anonymized vs. pseudonymized (this distinction matters legally):**
- **PII (personally identifiable information)**: personal data that identifies an individual (for example, name, email, device ID, or anything that can be tied back to a specific person).
- **Anonymized data**: irreversibly de-identified so no one can be re-identified. Truly anonymized data falls outside GDPR's scope.
- **Pseudonymized data**: still re-linkable to a person via a key or mapping (for example, hashed or tokenized identifiers). Under GDPR this is STILL personal data and must be protected accordingly.
- Do not treat pseudonymized data as "public" or anonymous. Only genuinely anonymized (irreversible) data can be handled as Public Data.

### Access Management

**1. Authentication**
- Require login for data access
- Use strong passwords or SSO
- Enable two-factor authentication
- Regularly review access

**2. Authorization**
- Grant minimum necessary access
- Review permissions regularly
- Remove access when people leave
- Document who has access to what

**3. Auditing**
- Log who accesses what data
- Monitor for unusual access
- Review access logs periodically
- Investigate suspicious activity

## Documentation requirements

### What to Document

**1. Data Collection**
- What data you collect
- Why you collect it
- How you collect it
- When you collect it

**2. Data Storage**
- Where data is stored
- How long you keep it
- How it's secured
- Who has access

**Retention (GDPR's storage-limitation principle):**
- Keep personal data only as long as necessary for its stated purpose
- Define retention periods for each kind of data, and enforce them
- Delete or anonymize data when it's no longer needed

**3. Data Usage**
- How data is used
- Who uses it
- What decisions it informs
- How it's shared (if at all)

**4. Data Definitions**
- What each metric means
- How it's calculated
- What data sources it uses
- Any limitations or caveats

### Documentation Best Practices

**1. Keep It Current**
- Update when practices change
- Review documentation regularly
- Remove outdated information
- Add new information promptly

**2. Make It Accessible**
- Store in central location
- Use clear, plain language
- Organize logically
- Make it searchable

**3. Include Examples**
- Show what data looks like
- Provide use cases
- Include sample queries
- Demonstrate workflows

## Governance for Small Teams/Indie Projects

### Simplified Approach

**1. Start Simple**
- Basic privacy policy
- Document key data points
- Simple access controls
- Regular reviews

**2. Use Built-in Features**
- Leverage tool privacy features
- Use platform compliance tools
- Take advantage of templates
- Follow tool best practices

**3. Focus on Essentials**
- Privacy compliance basics
- Data quality for key metrics
- Access controls for sensitive data
- Documentation for important data

**4. Scale as Needed**
- Add complexity as you grow
- Formalize processes when necessary
- Invest in tools when justified
- Don't over-engineer early on

### Practical Steps

**1. Privacy**
- Write clear privacy policy
- Get consent for data collection
- Provide data access/deletion
- Review privacy practices quarterly

**2. Data Quality**
- Validate key events
- Monitor for issues
- Document key metrics
- Fix problems promptly

**3. Access**
- Limit who can access data
- Use tool access controls
- Review permissions monthly
- Remove access when needed

**4. Documentation**
- Document key data points
- Explain important metrics
- Keep privacy policy updated
- Share knowledge with team

## Compliance checklist

### Privacy Compliance

- [ ] Privacy policy written and published
- [ ] Consent obtained for data collection
- [ ] User rights supported (access, deletion, export)
- [ ] Data minimization practiced
- [ ] Security measures in place
- [ ] Breach response plan documented

### Data Quality

- [ ] Data validation implemented
- [ ] Quality monitoring in place
- [ ] Documentation complete
- [ ] Regular audits scheduled
- [ ] Issues tracked and resolved

### Access Controls

- [ ] Access levels defined
- [ ] Permissions assigned appropriately
- [ ] Authentication required
- [ ] Access reviewed regularly
- [ ] Audit logs maintained

### Documentation

- [ ] Data collection documented
- [ ] Metrics defined clearly
- [ ] Privacy practices documented
- [ ] Documentation kept current
- [ ] Team trained on practices

## Common pitfalls

**1. Collecting Too Much**
- Problem: Hoarding data "just in case"
- Solution: Collect only what you need, delete what you don't

**2. Poor Documentation**
- Problem: No one knows what data means
- Solution: Document everything, keep it current

**3. Weak Access Controls**
- Problem: Everyone has full access
- Solution: Grant minimum necessary access

**4. Ignoring Privacy**
- Problem: Not thinking about regulations
- Solution: Understand requirements, implement basics

**5. No Quality Monitoring**
- Problem: Bad data leads to bad decisions
- Solution: Monitor quality, fix issues promptly

## Related topics

- [Analytics Strategy](analytics-strategy.md) - Planning data collection responsibly
- [Data Collection & Instrumentation](analytics-strategy.md#data-collection--instrumentation) - Privacy considerations in tracking

