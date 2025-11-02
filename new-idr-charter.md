**Proposed IDR WG Re-Charter**

The Border Gateway Protocol (BGP) (version 4) \[RFC4271\] was originally developed for inter-domain IP routing over the Internet and other IP-based networks.

The primary goal of the Inter-Domain Routing (IDR) Working Group (WG) is to develop and maintain BGP and to support its deployment as the standard inter-domain routing protocol deployed for IPv4 and IPv6 routing over the Internet.

The WG will also work on the development and support of the routing of infrastructure prefixes (commonly referred to as underlay routing) using BGP in deployments within operator networks (including but not limited to service provider, enterprise, and data center environments). Besides the IPv4 and IPv6 unicast address families, this also includes labeled unicast address families and intent-aware underlay routing (as defined in \[draft-ietf-idr-bgp-car\] and \[RFC9832\]).

The IDR WG will develop and maintain BGP features, extensions, and mechanisms that are largely address-family independent and may be considered core to the protocol’s operation. These are:

- Protocol-level aspects such as message encoding and processing (PDUs), session management, neighbor finite state machine (FSM), path selection, and associated procedures.
- BGP attributes used to convey information relevant to Network Layer Reachability Information (NLRIs), next-hop resolution, metrics, and other data integral to BGP operation.
- Capability advertisement mechanisms \[RFC5492\] used during session establishment to signal support for optional protocol features.
- Communities, including Extended Communities \[RFC4360\], Large and Wide Communities, for carrying metadata and policy-related information.
- Route constraint mechanisms such as Route Target Constraints \[RFC4684\] for limiting route propagation.
- Operation and optimization of Route Reflectors \[RFC4456\] and Confederations \[RFC5065\] for scalable iBGP deployments.
- Outbound Route Filtering (ORF) mechanisms \[RFC5291\] \[RFC5292\] for policy-based control of route advertisement.
- Graceful Restart procedures \[RFC4724\] \[RFC9494\] for improving BGP session resiliency and convergence during restarts or failures.
- BGPSec \[RFC8205]\ and BGP security related extensions other than the Resource Public Key Infrastructure (RPKI) related work undertaken in SIDROPS WG.

The IDR WG charter lists work areas as opposed to work items, reflecting the ongoing work, the extensible nature of BGP, and the WG’s operational model. Specific work items and associated documents are captured in the WG milestones, which highlight the most significant and time-sensitive deliverables. Milestones will track progress through WGLC, in line with the WG’s policy that any protocol specification (excluding YANG modules) should have at least two independent implementations prior to advancing to publication.

The following work areas define the scope of activities for the WG, limited to the context of the BGP address families and core protocol extensions outlined above:

- Advancement of BGP specifications, including but not limited to \[RFC4271\], toward Internet Standard status, where appropriate.
- Resolution of protocol issues and incorporation of improvements based on operational experience and feedback from the operator community. This includes enhancements related to security, performance, scalability, protocol correctness, robustness, and operational simplicity.
- Enhancements to BGP’s path selection and forwarding behavior to support advanced load-balancing capabilities beyond Equal-Cost Multi-Path (ECMP), including unequal and weighted load-balancing based on parameters such as bandwidth.
- Development of YANG data models to support the management of BGP features standardized by the WG, with a focus on device models and capturing operational considerations, as appropriate.
- Definition of BGP extensions to meet new requirements and use cases originating in other IETF working groups.
- Protocol improvements and extensions to support BGP deployments in IPv6 networks, including IPv6-only environments and mechanisms that facilitate the transition from IPv4 to IPv6.

The primary focus of the WG will remain on the development of Standards Track BGP specifications. Adoption of experimental specifications may be done as an exception in consultation with the Responsible AD. The WG will not seek to publish documents focused on use cases, frameworks, or architectural definitions. As an exception, the WG may produce Informational documents capturing deployment experience or best practices for BGP features developed within the WG.

As listed in the work areas, the WG may take up work on BGP extensions to support the work happening in other WGs following consultation with the relevant WG Chairs and Responsible ADs. The WG shall coordinate closely with the originating WG(s) responsible for the overall framework, architecture, and requirements. Progression of such work in IDR WG shall follow the maturity (specifically the adoption and WGLC milestones) of the corresponding base work in those WGs.

Given the broad use of BGP across various WGs in the IETF, the IDR WG will collaborate closely with other WGs developing or relying on BGP extensions. This includes BESS (VPN service-related BGP features), %new-bgp% (use of BGP for dissemination of routing-adjacent information), LSVR (BGP-SPF extensions), GROW (operational practices and monitoring via BMP), and SIDROPS (routing security operations and RPKI). The IDR WG will seek input from GROW and SIDROPS as appropriate, particularly with respect to operational and security considerations during the development of new BGP specifications. Likewise, the WG will seek review from V6OPS for IPv6-related extensions.

The IDR WG is expected to review BGP-related work in other WGs that is specifically impacting core BGP protocol aspects and provide timely feedback during (but not limited to) WG adoption and last calls in those respective WGs.

**List of WG documents** **(as of Sep 23, 2025):**

**Note:** The documents with (*) will have milestones attached to begin with and further milestones will be added as necessary.

**Active:**

[**https://datatracker.ietf.org/doc/draft-ietf-idr-link-bandwidth/**](https://datatracker.ietf.org/doc/draft-ietf-idr-link-bandwidth/) (*)

<https://datatracker.ietf.org/doc/draft-ietf-idr-5g-edge-service-metadata/>

[**https://datatracker.ietf.org/doc/draft-ietf-idr-rfc4360-bis/**](https://datatracker.ietf.org/doc/draft-ietf-idr-rfc4360-bis/)  (*)

<https://datatracker.ietf.org/doc/draft-ietf-idr-rt-derived-community/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-vpn-prefix-orf/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-bgp-ct-srv6/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-bgp-fwd-rr/>

[**https://datatracker.ietf.org/doc/draft-ietf-idr-linklocal-capability/**](https://datatracker.ietf.org/doc/draft-ietf-idr-linklocal-capability/)  (*)

[**https://datatracker.ietf.org/doc/draft-ietf-idr-entropy-label/**](https://datatracker.ietf.org/doc/draft-ietf-idr-entropy-label/)  (*)

<https://datatracker.ietf.org/doc/draft-ietf-idr-dynamic-cap/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-bgp-generic-metric/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-performance-routing/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-bgp-bfd-strict-mode/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-bgp-rpki-yang/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-multinexthop-attribute/>

**Expired:**

<https://datatracker.ietf.org/doc/draft-ietf-idr-registered-wide-bgp-communities/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-wide-bgp-communities/>

[**https://datatracker.ietf.org/doc/draft-ietf-idr-bgp-model/**](https://datatracker.ietf.org/doc/draft-ietf-idr-bgp-model/)  (*)

<https://datatracker.ietf.org/doc/draft-ietf-idr-legacy-rtc/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-bgp-fsm-iana/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-rtc-hierarchical-rr/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-bgp-attribute-announcement/>

<https://datatracker.ietf.org/doc/draft-haas-idr-bgp-diffract/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-bgp-autoconf-considerations/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-bgp-nh-cost/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-rs-bfd/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-rtc-no-rt/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-bgp-bestpath-selection-criteria/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-bgp-ipv6-rt-constrain/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-sla-exchange/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-custom-decision/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-aspath-orf/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-sla-exchange-impl/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-reserved-extended-communities/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-enhanced-gr/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-add-paths-guidelines/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-ix-bgp-route-server-implementation/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-bgp4-mibv2/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-bgp4-mibv2-tc-mib/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-enhanced-refresh-impl/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-bgp-multisession/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-bgp-issues/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-best-external/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-mrai-dep/>

<https://datatracker.ietf.org/doc/draft-ietf-idr-rfc4760bis/>
