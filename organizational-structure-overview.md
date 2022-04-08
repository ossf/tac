# OpenSSF Governance & Org Structure

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