---
layout: page
title: Technology
permalink: /technology/
---



## Benefits

Trulyprotect's core technology is used to enable three major use cases:


<div class="row">
  <div class="small-12 medium-12 large-4 columns">
    <h3>Anti-Reverse Engineering</h3>
    <p>
      Predetermined functions or code segments that need to be kept secret may be encrypted in the executable. Trulyprotect's thin-hypervisor will execute the encrypted portions by decrypting and executing on-the-fly, while fully protecting the decrypted code from being revealed.
    </p>
  </div>
  <div class="small-12 medium-12 large-4 columns">
    <h3>Application Firewall</h3>
    <p>
      An entire system's executable code (OS, applications and drivers) is whitelisted (using cryptographic signatures). Trulyprotect's thin-hypervisor verifies that only signed instructions may execute. Attempts to execute any type of unrecognized or injected instructions will be immediately blocked. This eliminates all known cyber-attack methodologies including buffer-overflow, viruses, worms, rootkits and zero-day vulnerabilities.
    </p>
  </div>
  <div class="small-12 medium-12 large-4 columns">
    <h3>Data Protection</h3>
    <p>
      Operating systems employ memory management that segregates application data-spaces. However, an application's data space is not secure in the presence of a cyber-attack that has gained OS level privileges. Trulyprotect's thin-hypervisor is used to create data-enclaves that guarantee an applications data-privacy in any scenario. Only the (signed) owning application shall have access to its data-space while it is running, which will otherwise be kept encrypted in memory.
    </p>
  </div>
</div>







-----

## Technology in detail

<img src="/assets/img/TrulyProtect-illustration-tech.png" style="background-color: #000; border-radius: 4px;" class="float-center">

<div class="row">
  <div class="small-1 medium-1 large-2 columns">&nbsp;</div>
  <div class="small-10 medium-10 large-8 columns">
    <h3>Hypervisor, Remote attestation</h3>
    <p>
      Trulyprotect's core technology utilizes a thin-hypervisor to establish a secure and trusted environment on computer systems.
      The thin-hypervisor is remotely attested to guarantee its trustworthiness so it can be safely used to protect the system's executable code and data.
    </p>
    <p>
      A hypervisor is software, which may be hardware assisted, used to manage multiple virtual machines on a single system.
      The hypervisor virtualizes the hardware environment in a way that allows several operating systems to operate in parallel over the same physical hardware platform, without obstructing or impeding each other.
    </p>
    <p>
      Trulyprotect's technology takes advantage of the hypervisor's ability to control the hardware platform in order to secure the system's software and data. To minimize overhead, a special breed of hypervisor, called a thin-hypervisor, is used. The thin-hypervisor is configured to intercept only a small portion of events that allow it to protect an internal secret (such as a cryptographic key) and protect itself from subversion.
    </p>
    <p>
      To establish an execution environment protected by the thin-hypervisor, Trulyprotect provides a means to assure that the thin-hypervisor is setup correctly and is trustworthy. To do so, an attestation procedure is used to verify that the thin-hypervisor's executable code is authentic and that is has true control over the system's hardware. The attestation procedure is administered by an external system, such as a remote server or tamper-proof dongle. Once a thin-hypervisor is attested as trustworthy, the external system securely provides it with secret cryptographic keys, which may be then used safely in the protected system.
    </p>
  </div>
  <div class="small-1 medium-1 large-2 columns">&nbsp;</div>
</div>
