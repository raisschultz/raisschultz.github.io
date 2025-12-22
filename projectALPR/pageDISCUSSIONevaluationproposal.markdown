---
layout: page
title: Evaluation and Proposed Changes 
permalink: /projectALPR/proposedchanges/
---
# Evaluation of the Technology
ALPR technology provides legitimate public safety benefits, especially at the community level. Local departments and campus agencies use ALPRs to recover stolen vehicles, respond to Amber and Silver Alerts, and support targeted investigations.

The problems arise not from the technical capabilities of ALPRs, but from the scale, breadth of access, and data-sharing practices. The ACLU has documented widespread, often misunderstood cross-jurisdictional sharing of ALPR data, including long retention periods and millions of queries made by agencies far removed from where the data was collected.<sup id="fn1_ref"><a href="#fn1">1</a></sup> The case of Bridgewater, VA shows how quickly “local” surveillance becomes national surveillance.

These risks have greater impact at the federal level. Compared to community use, federal ALPR operations involve wider geographic reach, more extensive multi-agency data integration, links to immigration-enforcement databases, longer retention periods, and far less transparency. The Associated Press found that CBP and ICE use ALPR networks to track vehicles far inland and incorporate travel histories into immigration investigations.<sup id="fn2_ref"><a href="#fn2">2</a></sup> This is a fundamentally different use case, transforming ALPRs from local crime-prevention tools into components of a nationwide surveillance infrastructure.

ALPRs contribute to a panopticon effect, where the possibility of being monitored causes people to alter their natural behaviors.<sup id="fn3_ref"><a href="#fn3">3</a></sup> This chilling effect is especially harmful for immigrants, activists, and marginalized communities who may be disproportionately targeted or impacted by federal access to ALPR networks.

Finally, the centralized database model used by vendors like Flock Safety creates a serious cybersecurity risk. The University of Michigan’s STPP program warns that centralized ALPR repositories become high-value targets, and a breach would expose detailed movement patterns of millions of people.<sup id="fn4_ref"><a href="#fn4">4</a></sup>

ALPRs are not inherently harmful, and they should not be eliminated. They should also not be expanded, especially not federally. Instead, they must be governed by strict, enforceable regulations that define retention, access, sharing, oversight, and transparency. ALPRs should remain in use only as tightly controlled, narrowly scoped community-safety tools.

# Proposed Improvements and Changes for ALPR Technology

## Proposals for Law Enforcement 

**1. Strict Data-Retention Limits**
* Adopt 30-day retention unless tied to an active investigation.  
>Aligns with concerns by the ACLU about excessive long term storage of data for pending investigations.<sup id="fn2_ref"><a href="#fn2">2</a></sup>

**2. Require Warrants for Historical Movement Queries**

* Like any other surveillance technology, a judge should need to approve its use and deployment.   
>Aligns with concerns raised by the Congressional Research Service about prolonged, warrantless location tracking.<sup id="fn5_ref"><a href="#fn5">5</a></sup>

**3. Public-Facing Transparency Policies**

* Publish retention periods, camera locations, audit schedules, and all agencies with access to ALPR data   
>Aligns with recommendations from the D.C. Police Complaints Board (PCB)<sup id="fn6_ref"><a href="#fn6">6</a></sup>

**4. Prohibit ALPR Surveillance of First Amendment-Protected Activity**

* Explicitly forbid tracking targeted tracking of attendees to protests, political events, religious gatherings, or healthcare clinics.  
>Directly supported by PCB’s call to revise MPD General Order 303.09.<sup id="fn6_ref"><a href="#fn6">6</a></sup>

**5. Mandatory Audit Logs and Misuse Penalties**

* Regular audits to detect unauthorized lookups (e.g., romantic partners, neighbors)  

**6. Community Access to Personal ALPR Records**

* Public mechanisms (like a Freedom of Information Act request) allowing individuals to request data about their own vehicle.  
>Based on PCB’s recommendation for public access procedures.<sup id="fn6_ref"><a href="#fn6">6</a></sup>

## Proposals for Policymakers 

**1. Uniform Statewide ALPR Legislation**

* Statutes should define:
  >retention periods,
  >warrant requirements,
  >audit obligations,
  >reporting rules,
  >and penalties for misuse, in accordance with the proposals outlined for law enforcement. 

**2. Restrict Federal Access to Local ALPR Data**

* No sharing with ICE or CBP for civil immigration enforcement without a warrant.  
* Federal contracts should require their own specialized, specific systems from vendors they enter contracts with, rather than co-opting existing data collected for a different purpose.   
>Addresses the concerns raised by AP’s investigation of federal ALPR use.<sup id="fn2_ref"><a href="#fn2">2</a></sup>  

**3. Mandated Annual Transparency Reports**

* Reports should include: number of queries, number of external agencies with access, all incidents of misuse, and all ALPR systems deployed.  
>Reflects PCB’s transparency recommendations.<sup id="fn6_ref"><a href="#fn6">6</a></sup>

**4. Require Public Disclosure of Vendor Contracts**

* All terms of ALPR contracts with vendors must be public, including: data-ownership terms, vendor-initiated sharing conditions, federal access provisions.  
>Addresses ACLU findings about misleading assumptions around vendor data-sharing.<sup id="fn1_ref"><a href="#fn1">1</a></sup>

**5. Independent Oversight Bodies**

* States should create independent oversight authorities with powers to audit, investigate, and enforce compliance.    
>Aligns with civil-liberties standards for surveillance oversight.<sup id="fn7_ref"><a href="#fn7">7</a></sup>  

## Proposals for Vendors (Flock Safety)

The most significant reform needed from ALPR vendors is a fundamental shift in how the ALPR data is stored, accessed, and controlled. Many of the issues that have been identified with the use of ALPR technology, particularly by federal agencies, stem from the vendor-controlled cloud model. To resolve these issues, vendors must restructure their systems so that communities, not the vendor, retain full possession and authority over their ALPR data.

**1. End Centralized Data Storage and Transition to a Decentralized Architecture**

* Vendors should no longer store ALPR data in a single, centralized cloud repository. Instead:  
  >Each community’s data should be stored locally, within its own jurisdiction and under its direct control.  
  >Flock should not possess backups, mirrors, or cloud copies of community ALPR data.  
  >Data from one jurisdiction should not be accessible to any other, unless explicitly authorized by that community.  
  >Vendors should provide the hardware and software, but no access pathway to the stored data.  

This eliminates the structural problem where federal agencies can obtain ALPR data by going directly to the vendor. If Flock does not hold the data, it cannot disclose it; voluntarily or under federal pressure. Any federal request would have to go through normal judicial and legal channels, restoring accountability and local control.

This proposal also addresses concerns raised in the STPP report warning that centralized ALPR repositories create massive cybersecurity and privacy risks, as they function as single high-value targets.<sup id="fn4_ref"><a href="#fn4">4</a></sup> A decentralized model reduces the attack surface and ensures no single breach compromises nationwide movement data.

**2. Strengthen Community-Owned Security Infrastructure**

* Although data would be locally stored, vendors should still provide:
  >encryption standards,  
  >secure software frameworks,  
  >regular security updates,  
  >and configuration guidance.  

Local storage does not eliminate the need for security; it changes its focus. Rather than protecting a giant national vault, the goal becomes ensuring each community deployment is secure and that no technical backdoors exist for vendor access.

**3. Mandatory Third-Party Audits for Privacy and Integrity**

* Audits remain essential, but their purpose shifts under this model. Audits should verify:
  >that the vendor does not retain access to local ALPR data;  
  >that no backdoors or federal/vendor-side channels exist;  
  >that local data is securely stored and retained consistent with community policy;  
  >And that interstate or federal sharing cannot occur absent explicit community authorization.  

**4. Community-Centered Data-Sharing Dashboards**

* Communities should retain full control over whether and how their data is shared. A dashboard supplied, but not operated or controlled by the vendor should allow communities to:
>see every access of their ALPR data;  
>authorize or revoke any sharing;
>document audit logs and queries transparently to the public.  

This aligns with transparency principles emphasized by the Police Complaints Board (PCB), which stressed the importance of public visibility over data access and third-party use.<sup id="fn6_ref"><a href="#fn6">6</a></sup>

**5. Privacy-First Default System Settings**

* Vendors should implement by default: short retention periods (the minimum necessary for function), opt-in sharing settings, and alerts when communities activate inter-agency sharing.  
>These defaults ensure that privacy is embedded into the design rather than reliant on user configuration.

With a shift to decentralized, community-controlled data, the largest ethical concerns and risks with  ALPR systems can be prevented. Vendors should no longer function as data controllers, but as technology providers, supporting systems designed to protect the community, without infringing on their rights and civil liberties. 

Footnotes

<sup id="fn1">1 American Civil Liberties Union. You Are Being Tracked: How License Plate Readers Are Being Used to Record Americans’ Movements. https://www.aclu.org/you-are-being-tracked 
</sup>  
<sup id="fn2">2 Associated Press. “U.S. Border Patrol Is Monitoring U.S. Drivers and Detaining Those with ‘Suspicious’ Travel Patterns.” 2025.
https://apnews.com/article/immigration-border-patrol-surveillance-drivers-ice-trump-9f5d05469ce8c629d6fecf32d32098cd </sup>  
<sup id="fn3">3 Seymour, Kimberley, et al. “Big Brother: The Effects of Surveillance on Fundamental Aspects of Social Vision.” Neuroscience of Consciousness 2024, no. 1 (2024)
https://academic.oup.com/nc/article/2024/1/niae039/7920510 </sup>  
<sup id="fn4">4 Science, Technology, and Public Policy Program (STPP). Automated License Plate Readers Are Widely Used — and Subject to Abuse. University of Michigan, 2023.
https://stpp.fordschool.umich.edu/news/2023/automated-license-plate-readers-widely-used-subject-abuse </sup>  
<sup id="fn5">5 Congressional Research Service. Automated License Plate Readers (ALPRs) and the Fourth Amendment, IF13068.
https://www.congress.gov/crs/product/IF13068 </sup>  
<sup id="fn6">6 Police Complaints Board (Office of Police Complaints, Washington D.C.). Report on Automated License Plate Readers https://policecomplaints.dc.gov/release/police-complaints-board-releases-report-automated-license-plate-readers </sup>  
<sup id="fn7">7 American Civil Liberties Union. “Privacy & Surveillance.” 
https://www.aclu.org/issues/national-security/privacy-and-surveillance </sup>
