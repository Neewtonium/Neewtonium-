
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Windows Cybersecurity Techniques</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #fafafa;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #007BFF;
            color: white;
            padding: 20px 0;
            text-align: center;
        }
        header h1 {
            margin: 0;
            font-size: 2.5em;
        }
        section {
            background-color: white;
            padding: 20px;
            margin: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }
        h2 {
            color: #007BFF;
        }
        nav {
            background-color: #333;
            padding: 11px;
            text-align: center;
        }
        nav a {
            color: white;
 text-decoration: none;
            padding: 10px 20px;
            margin: 0 10px;
            border-radius: 5px;
        }
        nav a:hover {
            background-color: #007BFF;
        }
        .code {
            background-color: #2d2d2d;
            color: #fff;
            padding: 10px;
            border-radius: 5px;
            font-family: Courier, monospace;
            margin-top: 10px;
            white-space: pre-wrap;
            word-wrap: break-word;
        }
        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 15px 0;
            position: fixed;
            width: 100%;
            bottom: 0;
        }
        .btn {
            background-color: #007BFF;
            color: white;
            padding: 10px 20px;
            text-decoration: none;
            border-radius: 5px;
            margin-top: 20px;
        }
        .btn:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>

    <header>
        <h1>Windows Cybersecurity Techniques</h1>
        <p>Learn how to enhance your Windows security using various tools and methods</p>
    </header>

    <nav>
        <a href="#firewall">Firewall</a>
 <a href="#antivirus">Antivirus</a>
        <a href="#updates">System Updates</a>
        <a href="#bitlocker">BitLocker</a>
        <a href="#lockout">Account Lockout</a>
    </nav>

    <section id="firewall">
        <h2>1. Enable Windows Firewall</h2>
        <p>Windows Firewall is a key component in defending your system against external threats.</p>
        <h3>Graphical Method:</h3>
        <p>Go to <strong>Control Panel</strong> > <strong>System and Security</strong> > <strong>Windows Defender Firewall</strong>.</p>
        <h3>CMD Method:</h3>
        <div class="code">
            netsh advfirewall set allprofiles state on
        </div>
        <h3>PowerShell Method:</h3>
        <div class="code">
            Set-NetFirewallProfile -All -Enabled True
        </div>
    </section>

    <section id="antivirus">
        <h2>2. Enable Windows Defender Antivirus</h2>
        <p>Windows Defender helps protect your system from malware and viruses.</p>
        <h3>Graphical Method:</h3>
        <p>Go to <strong>Settings</strong> > <strong>Update & Security</strong> > <strong>Windows Security</strong> > <strong>Virus & Threat Protection</strong>.</p>
        <h3>CMD Method:</h3>
        <div class="code">
 "%ProgramFiles%\Windows Defender\MpCmdRun.exe" -SignatureUpdate
        </div>
        <h3>PowerShell Method:</h3>
        <div class="code">
            Set-MpPreference -DisableRealtimeMonitoring $false
        </div>
    </section>

    <section id="updates">
        <h2>3. Check for System Updates</h2>
        <p>Regular system updates keep your Windows secure by patching vulnerabilities.</p>
        <h3>Graphical Method:</h3>
        <p>Go to <strong>Settings</strong> > <strong>Update & Security</strong> > <strong>Windows Update</strong> > <strong>Check for Updates</strong>.</p>
        <h3>CMD Method:</h3>
        <div class="code">
            wmic qfe list brief /format:table
        </div>
        <h3>PowerShell Method:</h3>
        <div class="code">
            Get-HotFix
        </div>
    </section>

    <section id="bitlocker">
        <h2>4. Enable BitLocker Encryption</h2>
        <p>BitLocker provides full-disk encryption to protect your data in case of theft or unauthorized access.</p>
        <h3>Graphical Method:</h3>
        <p>Go to <strong>Control Panel</strong> > <strong>System and Security</strong> > <strong>BitLocker Drive Encryption</strong>.</p>
        <h3>CMD Method:</h3>
        <div class="code">
            manage-bde -on C:
 </div>
        <h3>PowerShell Method:</h3>
        <div class="code">
            Enable-BitLocker -MountPoint "C:" -EncryptionMethod Aes256
        </div>
    </section>

    <section id="lockout">
        <h2>5. Configure Account Lockout Policy</h2>
        <p>Setting an account lockout policy can help protect your system from brute-force attacks.</p>
        <h3>Graphical Method:</h3>
        <p>Open <strong>Local Group Policy Editor</strong> and go to <strong>Account Lockout Policy</strong>.</p>
        <h3>CMD Method:</h3>
        <div class="code">
            secpol.msc
        </div>
        <h3>PowerShell Method:</h3>
        <div class="code">
            Set-LocalUser -Name "username" -AccountNeverExpiresfalse
        </div>
    </section>

    <footer>
        <p>Windows Cybersecurity - Protect Your System, Secure Your Data</p>
        <a href="https://github.com/yourusername/your-repository" class="btn">Visit My GitHub</a>
    </footer>

</body>
</html>
 
