
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Windows Cybersecurity Techniques</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #f4f4f4;
            color: #333;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #4CAF50;
            color: white;
            padding: 15px;
            text-align: center;
        }
        nav {
            background-color: #333;
            overflow: hidden;
        }
        nav a {
            float: left;
            display: block;
            color: white;
            text-align: center;
            padding: 14px 20px;
            text-decoration: none;
        }
        nav a:hover {
 background-color: #ddd;
            color: black;
        }
        section {
            padding: 20px;
            margin: 20px;
            background-color: white;
            border-radius: 8px;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
        }
        h2 {
            color: #4CAF50;
        }
        footer {
            text-align: center;
            padding: 10px;
            background-color: #333;
            color: white;
            position: fixed;
            width: 100%;
            bottom: 0;
        }
        .code-block {
            background-color: #2e2e2e;
            color: white;
            padding: 10px;
            border-radius: 5px;
            font-family: 'Courier New', monospace;
            white-space: pre-wrap;
            word-wrap: break-word;
        }
        .highlight {
            color: #ff9800;
        }
        .btn {
            background-color: #4CAF50;
            color: white;
            padding: 10px 20px;
            border: none;
            cursor: pointer;
            border-radius: 5px;
            text-decoration: none;
        }
        .btn:hover {
            background-color: #45a049;
        }
    </style>
</head>
<body>

    <header>
 <h1>Windows Cybersecurity Techniques</h1>
        <p>Learn how to enhance your Windows security with useful techniques and commands</p>
    </header>

    <nav>
        <a href="#firewall">Firewall</a>
        <a href="#antivirus">Antivirus</a>
        <a href="#updates">System Updates</a>
        <a href="#bitlocker">BitLocker</a>
        <a href="#lockout">Account Lockout</a>
    </nav>

    <div class="container">

        <!-- Firewall Section -->
        <section id="firewall">
            <h2>1. Enable Windows Firewall</h2>
            <p>Windows Firewall is a crucial security feature that protects your system from unauthorized access.</p>
            <p><strong>Graphical Method:</strong> Go to <strong>Control Panel</strong> > <strong>System and Security</strong> > <strong>Windows Defender Firewall</strong>.</p>
            <p><strong>CMD Method:</strong></p>
            <div class="code-block">
                netsh advfirewall set allprofiles state on
            </div>
            <p><strong>PowerShell Method:</strong></p>
            <div class="code-block">
                Set-NetFirewallProfile -All -Enabled True
            </div>
        </section>

        <!-- Antivirus Section -->
        <section id="antivirus">
<h2>2. Enable Windows Defender Antivirus</h2>
            <p>Windows Defender provides built-in antivirus protection that helps protect your system from malware and viruses.</p>
            <p><strong>Graphical Method:</strong> Go to <strong>Settings</strong> > <strong>Update & Security</strong> > <strong>Windows Security</strong> > <strong>Virus & Threat Protection</strong>.</p>
            <p><strong>CMD Method:</strong></p>
            <div class="code-block">
                "%ProgramFiles%\Windows Defender\MpCmdRun.exe" -SignatureUpdate
            </div>
            <p><strong>PowerShell Method:</strong></p>
            <div class="code-block">
                Set-MpPreference -DisableRealtimeMonitoring $false
            </div>
        </section>

        <!-- System Updates Section -->
        <section id="updates">
            <h2>3. Check for System Updates</h2>
            <p>Regular updates keep your system secure by patching vulnerabilities.</p>
            <p><strong>Graphical Method:</strong> Go to <strong>Settings</strong> > <strong>Update & Security</strong> > <strong>Windows Update</strong> > <strong>Check for Updates</strong>.</p>
            <p><strong>CMD Method:</strong></p>
            <div class="code-block">
wmic qfe list brief /format:table
            </div>
            <p><strong>PowerShell Method:</strong></p>
            <div class="code-block">
                Get-HotFix
            </div>
        </section>

        <!-- BitLocker Section -->
        <section id="bitlocker">
            <h2>4. Enable BitLocker Encryption</h2>
            <p>BitLocker provides full-disk encryption to protect your data in case of theft or unauthorized access.</p>
            <p><strong>Graphical Method:</strong> Go to <strong>Control Panel</strong> > <strong>System and Security</strong> > <strong>BitLocker Drive Encryption</strong>.</p>
            <p><strong>CMD Method:</strong></p>
            <div class="code-block">
                manage-bde -on C:
            </div>
            <p><strong>PowerShell Method:</strong></p>
            <div class="code-block">
                Enable-BitLocker -MountPoint "C:" -EncryptionMethod Aes256
            </div>
        </section>

        <!-- Account Lockout Section -->
        <section id="lockout">
            <h2>5. Configure Account Lockout Policy</h2>
            <p>Setting an account lockout policy can prevent brute-force attacks on your system.</p>
 <p><strong>Graphical Method:</strong> Open <strong>Local Group Policy Editor</strong> and navigate to <strong>Account Lockout Policy</strong>.</p>
            <p><strong>CMD Method:</strong></p>
            <div class="code-block">
                secpol.msc
            </div>
            <p><strong>PowerShell Method:</strong></p>
            <div class="code-block">
                Set-LocalUser -Name "username" -AccountNeverExpiresfalse
            </div>
        </section>

        <footer>
            <p>Windows Cybersecurity Techniques - Learn, Implement, Protect</p>
            <a href="https://github.com/yourusername/your-repository" class="btn">Visit my GitHub</a>
        </footer>

    </div>

</body>
</html>


