# OpenSSF Governance & Org Structure

## Charter

Overall governance of the OpenSSF is defined in [the Foundation Charter](https://cdn.platform.linuxfoundation.org/agreements/openssf.pdf). 


## Definitions

The OpenSSF is comprised of instances of the following categories of official groups:

- The **Governing Board** (GB) oversees the budget and legal status/structure of the OpenSSF. Board meetings may or may not be open to the public.
- **Committees** are formed by, and report to, the Board. Broadly speaking, Committees handle non-technical matters as needed by the GB, wherein a named set of people are tasked with handling a specific objective. Like the Board meetings, Committee meetings may or may not be open to the public.
- The **Technical Advisory Council** (TAC) is responsible for the general success of all Technical Initiatives (defined below). TAC meetings are generally open to the public, with the exception of special sessions. 
  - TAC membership is limited to seven (7) seats, with alternating elections every year. Contributors to Technical Initiatves may run, and each contributor may vote once in TAC elections. 
- Each **Technical Initiatives** (both Projects and Working Groups) is governed by its own Charter, which is approved by the TAC. Changes to a Charter must be approved first according to that Charter's terms and then by the TAC.
  - All Technical Initiatives are persistent open groups focused on a technical objective, with transparent proceedings that are open to the public, and vary in their objectives.
- A **Project** is a persistent and open group focused on the creation and ongoing support of open source licensed software (source code) and its supporting artifacts (documentation, etc). Projects usually manage one or more GitHub repos of their own, may have separate meetings, etc.
- A **Working Group** (WG) is also a persistent and open group focused on a particular aspect of the overall mission of the OpenSSF. Working Groups generally do not produce open source software as a primary artifact, though they often include some open source code, or even use licensed software, in fulfilment of their Charter.
  - WG's may be bounded in scope -- for example, their charter may specify that the WG will wrap up after a specific event, such as a publication.
  - WG's may also be unbounded in scope -- for instance, where an effort is expected to be ongoing in support of open source security indefinitely.
  

### TODO

* define **SIF**
* define **Services** 

## Ogranizational Chart

Legend:
- rounded box: entity is created by the OpenSSF governing charter
- square box: entity is created by the relevant body
- logical groupings are by convention rather than by charter


```mermaid
flowchart TB
    A([GoverningBoard])

    subgraph subC[Committees]
        direction TB
        Market[Marketing]
        Budget[Bugdet and Finance]
        Plan[Planning and Adivosry]
        Policy[Public Policy]
    end
    A <==> subC
    A ====> B([Technical Adivsory Council])

    subgraph subWG[Working Groups]
        BP[Best Practices]
        VD[Vulnerability Disclosures]
        IST[Identifying Security Threats]
        ST[Security Tooling]
        SCI[Supply Chain Integrity]
        SCP[Securing Critical Projects]

        BP ---> P2[Example project]
    end
    B ====> subWG

    B ----> P1[Example Project]

    subgraph subSIF[Special Initiative Funds]
        ss[SigStore]
        ao[Alpha-Omega]
        gti[GNU Toolchain Infra]
    end
    B ==technical oversight==> subSIF
    A --budgetary oversight--> subSIF
```