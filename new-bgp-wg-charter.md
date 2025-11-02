**Proposed %new-bgp% WG Charter**

The Border Gateway Protocol (BGP) (version 4) \[RFC4271\] was originally developed to support inter-domain routing for both IPv4 and IPv6 across the Internet and other IP-based networks. The introduction of multiprotocol extensions \[RFC4760\] enabled BGP to support multiple address families, significantly broadening its applicability to a wide range of routing features and deployment scenarios.

The %new-bgp% Working Group (WG) is focused on the development and maintenance of BGP address families that extend BGP to carry information related to, or adjacent to, routing functionality within operator networks (including but not limited to service provider, enterprise, and data center environments). These address families are:

- Advertisement of link-state and other topology information using BGP-LS \[RFC9552\].
- Advertisement of Segment Routing (SR) Policies \[draft-ietf-idr-sr-policy-safi\].
- Dissemination of Flow Specification rules \[RFC8955\] and its enhanced version.
- Distribution of routing policies \[draft-ietf-idr-rpd\].
- Distribution of IPSec tunnel information for SD-WAN \[draft-ietf-idr-sdwan-edge-discovery\].
- Advertisement of IPv4/IPv6 mappings \[draft-ietf-idr-mpbgp-extension-4map6\].

The %new-bgp% WG charter lists work areas as opposed to work items, reflecting the ongoing work, the extensible nature of BGP, and the WG’s operational model. Specific work items and associated documents are captured in the WG milestones, which highlight the most significant and time-sensitive deliverables. Milestones will track progress through WGLC, in line with the WG’s policy that any protocol specification (excluding YANG modules) should have at least two independent implementations prior to advancing to publication.

The following work areas define the scope of activities for the WG, limited to the context of the BGP address families outlined above and their extensions:

- Definition of BGP extensions to meet new requirements and use cases originating in other IETF working groups.
- Resolution of issues and incorporation of improvements based on operational experience and feedback from the operator community. This includes enhancements related to security, performance, scalability, correctness, robustness, and operational simplicity.
- Development of YANG data models to support the management of BGP features standardized by the WG, with a focus on device models and capturing operational considerations, as appropriate.
- Improvements and extensions to support BGP deployments in IPv6 networks, including IPv6-only environments and mechanisms that facilitate the transition from IPv4 to IPv6.

The primary focus of the WG will remain on the development of Standards Track BGP protocol specifications. Adoption of experimental specifications may be done as an exception in consultation with the Responsible AD. The WG will not seek to publish documents focused on use cases, frameworks, or architectural definitions. As an exception, the WG may produce Informational documents capturing deployment experience or best practices for BGP features developed within the WG.

As listed in the work areas, the WG may take up work on BGP extensions to support the work happening in other WGs following consultation with the relevant WG Chairs and Responsible ADs. The WG shall coordinate closely with the originating WG(s) responsible for the overall framework, architecture, and requirements. Progression of such work in %new-bgp% WG shall follow the maturity (specifically the adoption and WGLC milestones) of the corresponding base work in those WGs. Relevant WGs include, but are not limited to, SPRING, TEAS, CATS, SAVNET, and, in the context of BGP-LS, LSR.

The WG is expected to coordinate closely with the IDR WG. Any extensions that impact core BGP protocol behavior, including modifications to the BGP finite state machine, message formats, best-path selection procedures, or the definition of new path attributes, must be cross-posted to the IDR WG for review at least during WG adoption and last-call. The WG will also coordinate with the LSVR WG on re-use of BGP-LS extensions in the BGP-SPF work undertaken by the LSVR WG.

**List of WG documents** **(as of Sep 23, 2025):**

**Note:** The documents with (*) will have milestones attached to begin with and further milestones will be added as necessary.

**Active:**

<https://datatracker.ietf.org/doc/draft-ietf-idr-bgp-ls-link-mtu/>

[**https://datatracker.ietf.org/doc/draft-ietf-idr-sr-policy-path-segment/**](https://datatracker.ietf.org/doc/draft-ietf-idr-sr-policy-path-segment/) (*)

[**https://datatracker.ietf.org/doc/draft-ietf-idr-bgp-ls-sr-policy-nrp/**](https://datatracker.ietf.org/doc/draft-ietf-idr-bgp-ls-sr-policy-nrp/) (*)

<https://datatracker.ietf.org/doc/draft-ietf-idr-flowspec-interfaceset/>

[**https://datatracker.ietf.org/doc/draft-ietf-idr-flowspec-redirect-ip/**](https://datatracker.ietf.org/doc/draft-ietf-idr-flowspec-redirect-ip/) (*)

[**https://datatracker.ietf.org/doc/draft-ietf-idr-bgpls-sr-vtn-mt/**](https://datatracker.ietf.org/doc/draft-ietf-idr-bgpls-sr-vtn-mt/) (*)

<https://datatracker.ietf.org/doc/draft-ietf-idr-bgp-srmpls-elp/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-sr-te-policy-attr/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-ts-flowspec-srv6-policy/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-sr-policy-seglist-id/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-bgp-ls-sr-epe-over-l2bundle/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-sdwan-edge-discovery/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-sr-policy-metric/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-flowspec-nvo3/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-mpbgp-extension-4map6/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-flowspec-srv6/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-flowspec-network-slice-ts/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-bgp-ifit-capabilities/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-sr-policy-ifit/>

[**https://datatracker.ietf.org/doc/draft-ietf-idr-bgp-ls-sr-policy-path-segment/**](https://datatracker.ietf.org/doc/draft-ietf-idr-bgp-ls-sr-policy-path-segment/) (*)

<https://datatracker.ietf.org/doc/draft-ietf-idr-sr-policy-path-mtu/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-flowspec-l2vpn/>

**Expired:**

[**https://datatracker.ietf.org/doc/draft-ietf-idr-fsv2-ip-basic/**](https://datatracker.ietf.org/doc/draft-ietf-idr-fsv2-ip-basic/) (*)

[**https://datatracker.ietf.org/doc/draft-ietf-idr-sr-policy-nrp/**](https://datatracker.ietf.org/doc/draft-ietf-idr-sr-policy-nrp/) (*)

<https://datatracker.ietf.org/doc/draft-ietf-idr-bgpls-inter-as-topology-ext/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-bgp-ls-te-path/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-flowspec-v2/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-bier-te-path/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-rpd/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-bgp-ls-isis-flood-reflection/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-flowspec-path-redirect/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-bgp-ls-sr-service-segments/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-bgp-flowspec-label/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-flowspec-mpls-match/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-sr-p2mp-policy/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-bgp-ls-bgp-only-fabric/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-ls-trill/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-bgp-ls-node-admin-tag-extension/>





