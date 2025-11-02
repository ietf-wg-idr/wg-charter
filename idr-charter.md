# Proposed IDR WG Re-Charter

The Border Gateway Protocol (BGP) (version 4) \[RFC4271\] was originally developed to support inter-domain IP routing over the Internet and other IP-based networks. The introduction of multiprotocol extensions \[RFC4760\] enabled BGP to support multiple address families, significantly broadening its applicability to a wide range of routing features and deployment scenarios. 

The primary objective (and priority) of the Inter-Domain Routing (IDR) Working Group (WG) is to develop and maintain BGP as the standard inter-domain routing protocol deployed for IPv4 and IPv6 routing over the Internet. 

In addition, the WG will work on the development and support of the following BGP address families for their respective deployments within operator networks (including but not limited to service provider, enterprise, and data center environments):

**Infrastructure (Underlay) Routing:** These address families support the routing of infrastructure prefixes, commonly referred to as underlay routing:

* IPv4 and IPv6 unicast address families for networks outside the public Internet.  
* Labeled Unicast address family \[RFC8277\].  
* Intent-aware underlay routing, as defined in \[draft-ietf-idr-bgp-car\] and \[RFC9832\].

**Routing-Adjacent Information Dissemination:** These address families enable BGP to carry information related to, or adjacent to, routing functionality:

* Dissemination of Flow Specification rules \[RFC8955\] and its enhanced version.  
* Advertisement of link-state and other topology information using BGP-LS \[RFC9552\].  
* Advertisement of Segment Routing (SR) Policies \[RFC9830\].  
* Distribution of routing policies \[draft-ietf-idr-rpd\].  
* Signaling for SD-WAN tunnel discovery \[draft-ietf-idr-sdwan-edge-discovery\].  
* Advertisement of IPv4/IPv6 mappings \[draft-ietf-idr-mpbgp-extension-4map6\].

Also, the IDR WG will develop and maintain BGP features, extensions, and mechanisms that are largely address-family independent and may be considered core to the protocol’s operation. These are:

* Protocol-level aspects such as message encoding and processing (PDUs), session management, neighbor finite state machine (FSM), path selection, and associated procedures.  
* BGP attributes used to convey information relevant to Network Layer Reachability Information (NLRIs), next-hop resolution, metrics, and other data integral to BGP operation.  
* Capability advertisement mechanisms \[RFC5492\] used during session establishment to signal support for optional protocol features.  
* Extended Communities \[RFC4360\], including support for Large and Wide Communities, for carrying metadata and policy-related information.  
* Advertisement of tunnel encapsulation information \[RFC9012\] to support data plane flexibility.  
* Route constraint mechanisms such as Route Target Constraints \[RFC4684\] for limiting route propagation.  
* Operation and optimization of Route Reflectors \[RFC4456\] and Confederations \[RFC5065\] for scalable iBGP deployments.  
* Outbound Route Filtering (ORF) mechanisms \[RFC5291\]\[RFC5292\] for policy-based control of route advertisement.  
* Graceful Restart procedures \[RFC4724\] \[RFC9494\] for improving BGP session resiliency and convergence during restarts or failures.
* BGPSec \[RFC8205\] and BGP security related extensions other than the Resource Public Key Infrastructure (RPKI) related work undertaken in SIDROPS WG.

The IDR WG charter lists work areas as opposed to work items, reflecting the ongoing work, the extensible nature of the BGP, and the WG’s operational model. Specific work items and associated documents are captured in the WG milestones, which highlight the most significant and time-sensitive deliverables. Milestones will track progress through WGLC, in line with the WG’s long-standing policy that any protocol specification (excluding YANG modules) must have at least two independent implementations prior to advancing to publication.

The following work areas define the scope of activities for the WG, limited to the context of the BGP address families and core protocol extensions outlined above:

* Advancement of BGP specifications, including but not limited to \[RFC4271\], toward Internet Standard status, where appropriate.  
* Resolution of protocol issues and incorporation of improvements based on operational experience and feedback from the operator community. This includes enhancements related to security, performance, scalability, protocol correctness, robustness, and operational simplicity.  
* Development of YANG data models to support the management of BGP features standardized by the WG, with a focus on device models and capturing operational considerations, as appropriate.  
* Definition of BGP protocol extensions to meet new requirements and use cases originating in other IETF working groups.  
* Enhancements to BGP’s path selection and forwarding behavior to support advanced load-balancing capabilities beyond Equal-Cost Multi-Path (ECMP), including unequal and weighted load-balancing based on parameters such as bandwidth.  
* Protocol improvements and extensions to support BGP deployments in IPv6 networks, including IPv6-only environments and mechanisms that facilitate the transition from IPv4 to IPv6.

The primary focus of the WG will remain on the development of Standards Track BGP specifications. Adoption of experimental specifications may be done as an exception in consultation with the Responsible AD. The WG will not seek to publish documents focused on use cases, frameworks, or architectural definitions. As an exception, the WG may produce Informational documents capturing deployment experience or best practices for BGP features developed within the WG.

The IDR WG may consider adopting work related to new BGP address families, feature extensions, or work areas not explicitly listed above. However, adoption of such work will require demonstrated interest and sufficient expertise within the WG, and will be subject to a rechartering process (i.e., IDR will not become the WG that automatically adopts any BGP work).

As listed in the work areas, the WG may take up work on BGP extensions to support the work happening in other WGs following consultation with the relevant WG Chairs and Responsible ADs. The WG shall coordinate closely with the originating WG(s) responsible for the overall framework, architecture, and requirements. Progression of such work in IDR WG shall follow the maturity (specifically the adoption and WGLC milestones) of the corresponding base work in those WGs.  Relevant WGs include, but are not limited to, SPRING, TEAS, CATS, SAVNET, and, in the context of BGP-LS, LSR.

Given the broad use of BGP across various WGs in the IETF, the IDR WG will collaborate closely with other WGs developing or relying on BGP extensions. This includes BESS (VPN service-related BGP features), LSVR (BGP-SPF extensions), GROW (operational practices and monitoring via BMP), and SIDROPS (routing security operations and RPKI). The IDR WG will seek input from GROW and SIDROPS as appropriate, particularly with respect to operational and security considerations during the development of new BGP specifications. Likewise, the WG will seek review from V6OPS for IPv6-related extensions.

The IDR WG is expected to review BGP-related work in other WGs that is specifically impacting core BGP protocol aspects and provide timely feedback during (but not limited to) WG adoption and last calls in those respective WGs.
