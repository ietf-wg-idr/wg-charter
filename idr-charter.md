# Proposed IDR WG Re-Charter

The Border Gateway Protocol (BGP) (version 4) [RFC4271] was originally developed to support inter-domain IP routing over the Internet and other IP-based networks. The introduction of multiprotocol extensions [RFC4760] enabled BGP to support multiple address families, significantly broadening its applicability to a wide range of routing features and deployment scenarios.

The primary objective (and priority) of the Inter-Domain Routing (IDR) Working Group (WG) is to develop and maintain BGP as the standard inter-domain routing protocol deployed for IPv4 and IPv6 over the Internet.

Aligned with this priority, the IDR WG will develop and maintain BGP features, extensions, and mechanisms that are address-family independent and are considered core to the protocol’s operation. These are:

- Protocol-level aspects such as message encoding and processing (PDUs), support for different transports specific to BGP, session management, neighbor finite state machine (FSM), path selection, and associated procedures.
- BGP attributes used to convey information relevant to Network Layer Reachability Information (NLRIs), next-hop resolution, metrics, and other data integral to BGP operation.
- Capability advertisement mechanisms [RFC5492] used during session establishment to signal support for optional protocol features.
- Extended Communities [RFC4360], including support for Large and Wide Communities, for carrying metadata and policy-related information.
- Outbound Route Filtering (ORF) mechanisms [RFC5291][RFC5292] for policy-based control of route advertisement.
- Route constraint mechanisms such as Route Target Constraints [RFC4684] for limiting route propagation.
- Advertisement of tunnel encapsulation information [RFC9012] to support data plane flexibility.
- Advertisement of Segment Routing information via Prefix SID Attribute [RFC8669].
- Operation and optimization of Route Reflectors [RFC4456] and Confederations [RFC5065] for scalable iBGP deployments.
- Graceful Restart procedures [RFC4724] [RFC9494] for improving BGP session resiliency and convergence during restarts or failures.
- BGPsec [RFC8205] and BGP security related extensions other than the Resource Public Key Infrastructure (RPKI) related work undertaken in SIDROPS WG.

In addition, the WG will develop and maintain BGP features, extensions, and mechanisms for the following BGP address families for their respective deployments within operator networks (including but not limited to service provider, enterprise, and data center environments):

Track 1) Infrastructure (Underlay) Routing: These address families support the routing of infrastructure prefixes, commonly referred to as underlay routing:

- IPv4 and IPv6 unicast address families for networks outside of the public Internet.
- MPLS Labeled Unicast address family [RFC8277].
- Address families related to intent-aware underlay routing specified by the WG.

Track 2) Routing-Adjacent Information Dissemination: These address families enable BGP to carry information related to, or adjacent to, routing functionality:

- Dissemination of Flow Specification rules [RFC8955] and Flow Specification Version 2 [draft-ietf-idr-fsv2-ip-basic].
- Advertisement of link-state and other topology information using BGP-LS [RFC9552].
- Advertisement of Segment Routing (SR) Policies [RFC9830].
- Distribution of routing policies [draft-ietf-idr-rpd].
- Signaling for SD-WAN tunnel discovery [draft-ietf-idr-sdwan-edge-discovery].
- Advertisement of IPv4/IPv6 mappings [draft-ietf-idr-mpbgp-extension-4map6].

The IDR WG charter lists work areas as opposed to specific deliverables, reflecting the ongoing work, the extensible nature of the BGP, and the WG’s operational model. Milestones are added for specific deliverables as corresponding documents are adopted by the WG. These are tracked as they progress through WGLC. The WG maintains a long-standing policy that any protocol specification (excluding YANG modules) must have at least two independent implementations prior to advancing to publication.

The following work areas define the scope of activities for the WG, limited to the context of the BGP address families and core protocol extensions outlined above:

- Advancement of BGP specifications, including but not limited to [RFC4271], toward Internet Standard status, where appropriate.
- Resolution of protocol issues and incorporation of improvements based on operational experience and feedback from the operator community. This includes enhancements related to security, performance, scalability, protocol correctness, robustness, and operational simplicity.
- Development of YANG data models scoped to the WG's chartered BGP features and extensions to support the management of these features and extensions, with a focus on device models and capturing operational considerations, as appropriate.
- Definition of BGP protocol extensions to meet new requirements and use cases originating in other IETF WGs.
- Enhancements to BGP's path selection and forwarding behavior to support advanced load-balancing capabilities beyond Equal-Cost Multi-Path (ECMP), including unequal and weighted load-balancing based on parameters such as bandwidth.
- Protocol improvements and extensions to support BGP deployments in IPv6 networks, including IPv6-only environments and mechanisms that facilitate the transition from IPv4 to IPv6 and co-existence.

The primary focus of the WG will remain on the development of Standards Track BGP specifications. Adoption of experimental specifications may be done as an exception in consultation with the Responsible AD. The WG will not seek to publish documents focused on use cases, frameworks, or architectural definitions. As an exception, the WG may produce Informational documents capturing deployment experience or best practices for BGP features developed within the WG with the exception of those related to global Internet routing and BGP security that are covered by the GROW and SIDROPS WGs.

The WG may take up work on BGP protocol extensions to support the work happening in other IETF WGs following consultation with the relevant WG Chairs and Responsible ADs without the need for a recharter. The WG shall coordinate closely with the originating WG(s) that is responsible for the overall base framework, architecture, and requirements. Progression of such work in IDR WG shall follow the maturity (typically, adoption and WGLC milestones) of the corresponding base work in those WGs. Relevant WGs include, but are not limited to, CATS, SAVNET, SPRING, and TEAS, and, in the context of BGP-LS, LSR.

The IDR WG may consider adopting work related to new BGP address families, feature extensions, or work areas not explicitly listed above. However, adoption of such work will require demonstrated interest and sufficient expertise within the WG, and will be subject to a WG rechartering process (i.e., IDR will not become the WG that automatically adopts any BGP-related work).

Given the broad use of BGP across various WGs in the IETF, the IDR WG will provide advice and collaborate closely with other WGs developing or relying on BGP extensions and their BGP-related YANG data models. This includes BESS (VPN service-related BGP features), GROW (operational practices and monitoring via BMP), LSVR (BGP-SPF extensions), and SIDROPS (RPKI-related). The IDR WG will seek input from GROW and SIDROPS as appropriate, particularly with respect to operational and security considerations during the development of new BGP specifications. Likewise, the WG will seek review from V6OPS and 6MAN for IPv6-related extensions and from SRV6OPS for Segment Routing operational aspects.

The IDR WG is expected to review BGP-related work in other WGs that is specifically impacting core BGP protocol aspects and provide timely feedback during (but not limited to) WG adoption and WGLCs in those respective WGs. This feedback has no additional standing beyond any other community review.
