---
title: DNS Underscore Resource Record Extension for Incremental Record Types
abbrev: DNS Underscore RRT Extension
docname: draft-zhou-dns-underscore-rrt-extension-latest
category: info
updates: RFC 1035 (if applicable)
ipr: trust200902
keyword: DNS, Underscore, Resource Record
author:
  -
    ins: Zainan Zhou
    name: Zainan Zhou
    org: D3Serve Labs Inc.
    email: zzn@zzn.im
date: 2023-07-26
---

# Abstract {#abstract}

This document proposes a mechanism for incrementally adding new resource record types to the Domain Name System (DNS) by utilizing underscores as a prefix to the proposed record resource identifier. The usage of underscores provides a common and consistent way to introduce new record types while ensuring compatibility with existing DNS implementations.

# Status of This Memo {#status}

This Internet-Draft is submitted in full conformance with the provisions of BCP 78 and BCP 79.

# Copyright Notice {#copyright}

Copyright (c) 2023 IETF Trust and the persons identified as the document authors. All rights reserved.

# Table of Contents {#contents}

1. [Introduction](#introduction)
2. [Motivation and Rationale](#rationale)
3. [Defining New Resource Record Types](#defining)
4. [Examples of Existing Usage](#examples)
5. [Security Considerations](#security)
6. [IANA Considerations](#iana)
7. [Acknowledgments](#acknowledgments)
8. [References](#references)

# Introduction {#introduction}

The Domain Name System (DNS) is a critical infrastructure for resolving domain names to various types of data, including IP addresses, mail exchange servers, and other information. Over time, the DNS community has recognized the need for new resource record types to accommodate emerging technologies and applications.

# Motivation and Rationale {#rationale}

The DNS community has recognized the need for new resource record types to accommodate emerging technologies and applications. However, the introduction of new record types should be done in a manner that is both consistent and compatible with existing DNS implementations.

## Common and Consistent Usage

The DNS has seen various ad hoc uses of underscores as a naming convention for introducing new record types. By standardizing the usage of underscores as the prefix for proposed record resource identifiers, we establish a common naming convention that can be followed across different implementations. This ensures that the introduction of new record types is more coherent and easy to understand for the DNS community.

## Compatibility with Existing Implementations

The proposed mechanism is designed to be backward-compatible with existing DNS implementations. By using a TXT record to associate data with the new record resource identifier, we avoid conflicts with existing record types while still accommodating new requirements. Additionally, this approach allows older DNS servers to ignore new record types, maintaining stability in the DNS infrastructure.

## WebKit CSS Practice

The usage of underscores for introducing new features or experimental properties is not limited to the DNS. In the realm of web technologies, the WebKit engine, which powers browsers like Safari, has adopted a similar approach in CSS. In WebKit, CSS properties with names starting with an underscore are used to signify experimental or internal features that are not yet part of the official CSS specification.

# Defining New Resource Record Types {#defining}

To propose a new resource record type using the underscore mechanism, the following steps should be followed:

1. Choose a meaningful and concise record resource identifier, which will be used as the proposed record type name.
2. Concatenate the underscore character (_) with the chosen record resource identifier. This creates the new record type's name that will be used in the DNS queries and zone files.
3. Define the format and semantics of the new record type. This specification should be documented in an RFC or other authoritative document.
4. Use a TXT record to carry the associated data for the new record type. This TXT record should be named using the new record type's name (including the underscore).

# Examples of Existing Usage {#examples}

This section provides examples of existing practices that use the underscore naming convention for introducing new record types.

# Security Considerations {#security}

The introduction of new record types using the underscore mechanism should be approached with caution to avoid potential security concerns. When defining new record types, the following security considerations should be taken into account:

1. Ensure that the proposed record resource identifier is unique and does not conflict with existing DNS record types or other underscore-based record types.
2. Carefully define the format and semantics of the new record type to avoid ambiguities and misinterpretations.
3. Consider potential security implications when using the TXT record to carry data associated with the new record type. Prevent data injection or other vulnerabilities that could be exploited by malicious actors.
4. Clearly document the security implications and considerations for the new record type in the corresponding RFC or specification.

# IANA Considerations {#iana}

This document does not require any actions from IANA.

# Acknowledgments {#acknowledgments}

[Acknowledgment of contributors, reviewers, or others as appropriate]

# References {#references}

## Normative References

[List of any normative references]

## Informative References

[List of any informative references]

# Authors' Addresses

Zainan Zhou
D3Serve Labs Inc.
zzn@zzn.im
