Initial Access via SSH

Much like with RDP on Windows, SSH is both powerful and often poorly defended - in fact, both protocols are tracked under the External Remote Services MITRE technique. A lot of threat groups run vast botnets to scan the Internet for systems with exposed SSH and access them in two primary ways: via a stolen key or a breached password. Let's see how it usually happens:

Common risks when using key-based authentication:

Threat actors access a service or source code where private SSH keys have been stored
(Like a GitHub repository or Ansible automation server containing SSH credentials)
Threat actors steal SSH keys to a server by infecting an admin's laptop with a data stealer
Additional risks when using password-based authentication:

An IT admin sets a weak SSH password for a quick test and forgets to revert the changes
An IT support enables SSH for a contractor who sets the password to "12345678"
A network engineer accidentally exposes an old, insecure SSH server to the Internet
Most real-world Linux attacks, such as those by the Outlaw group, start from one of the scenarios above. However, you should also be aware of more advanced risks like a vulnerability in the SSH server itself, notably Erlang/OTP or SSH session hijacking, that you will learn in more advanced rooms.

For this task, open the VM and remind yourself how to work with SSH logs.
You can start from: cat /var/log/auth.log | grep "sshd"
