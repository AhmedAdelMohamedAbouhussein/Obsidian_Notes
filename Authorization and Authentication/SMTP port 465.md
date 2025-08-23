## SMTP port 587

While port 25 is used for relaying email messages from server to server, port 587 is the default SMTP port for message submissions. When a mail client submits messages to your email server, that client typically connects via port 587.

## SMTP port 465

587 isn’t the only SMTP port known for its security properties. Port 465 is also recognized by some organizations as a secure SMTP port. However, unlike a port 587 SMTP connection, where a client must issue the STARTTLS command to upgrade from a plaintext (a.k.a. cleartext) SMTP connection to a TLS-encrypted connection, a port 465 SMTP connection applies TLS encryption automatically.

This alternate SMTP email encryption mechanism, wherein a TLS connection is established right from the start, is known as Implicit TLS. The use of Implicit TLS for email submission and access is defined in [RFC 8314](https://datatracker.ietf.org/doc/html/rfc8314) and applies not only to SMTP, but also to Post Office Protocol v3 (POP3 ) and Internet Message Access Protocol (IMAP). SMTP, IMAP and POP3 are all Transmission Control Protocol (TCP) protocols for email.