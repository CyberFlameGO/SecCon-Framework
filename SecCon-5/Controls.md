The controls enabled in SECCON 5 are specifically chosen to minimize impact to
users and applications, while enforcing a reasonable level of security.

| Feature                           | Config                              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Defender ATP EDR          | Deployed to all devices             | The Windows Defender ATP endpoint detection and response capabilities provides near real-time actionable advance attacks detections, enables security analysts to effectively prioritize alerts, unfold the full scope of a breach and take response actions to remediate the threat. When a threat is detected, alerts are be created in the system for an analyst to investigate. Alerts with the same attack techniques or attributed to the same attacker are aggregated into an entity called incident. Aggregating alerts in this manner makes it easy for analysts to collectively investigate and respond to threats. Windows Defender ATP EDR is expected to have no impact to users or applications, and therefore can be deployed in a single step to all devices.                                                                                                     |
| Windows Defender                  | Enabled for all compatible hardware | Windows Defender Credential Guard uses virtualization-based security to isolate secrets so that only privileged system software can access them. Unauthorized access to these secrets can lead to credential theft attacks, such as Pass-the-Hash or Pass-The-Ticket. Windows Defender Credential Guard prevents these attacks by protecting NTLM password hashes, Kerberos Ticket Granting Tickets, and credentials stored by applications as domain credentials. There is a small risk to application compatibility, as applications will break if they require:                                                                                                                                                                                                                                                                                                                |
| Credential Guard                  |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Microsoft Edge                    | Default browser                     | Microsoft Edge provides a differentiated security experience on Windows 10, compared to Internet Explorer 11 (IE11). While you may still need to leverage IE11 for compatibility with some sites, Microsoft recommends configuring Microsoft Edge as the default browser, and building an Enterprise Mode Site List to redirect to IE11 only for those sites that require it. Microsoft recommends leveraging either Windows Analytics or Enterprise Site Discovery to build the initial Enterprise Mode Site List, and then gradually deploying this configuration using the Rings methodology.                                                                                                                                                                                                                                                                                  |
| Windows Defender Application Guard | Enabled on compatible hardware      | Windows Defender Application Guard uses a hardware isolation approach. If an employee goes to an untrusted site through either Microsoft Edge or Internet Explorer, Microsoft Edge opens the site in an isolated Hyper-V-enabled container, which is separate from the host operating system. This container isolation means that if the untrusted site turns out to be malicious, the host PC is protected, and the attacker can't get to your enterprise data. There is a small risk to application compatibility, as some applications may require interaction with the host PC but may not yet be on the list of trusted web sites for Application Guard. Microsoft recommends leveraging either Windows Analytics or Enterprise Site Discovery to build the initial Network Isolation Settings, and then gradually deploying this configuration using the Rings methodology. |
|                  |                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |

-   Kerberos DES encryption support

-   Kerberos unconstrained delegation

-   Extracting the Kerberos TGT

-   NTLMv1

As such, Microsoft recommends deploying using the Ring methodology.