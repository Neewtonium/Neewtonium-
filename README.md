
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
            background-color: #f9f9f9;
            margin: 0;
            padding: 0;
            color: #333;
        }
        header {
            background-color: #1e3d58;
            color: white;
            padding: 20px;
            text-align: center;
            border-bottom: 4px solid #007BFF;
        }
        header h1 {
            margin: 0;
            font-size: 3em;
        }
        header p {
            font-size: 1.2em;
            margin-top: 5px;
        }
        nav {
            background-color: #007BFF;
            padding: 15px;
            text-align: center;
        }
        nav a {
            color: white;
            text-decoration: none;
            padding: 12px 30px;
            margin: 0 15px;
            font-size: 1.1em;
            border-radius: 5px;
            transition: background-color 0.3s;
        }
        nav a:hover {
            background-color: #004c8c;
        }
        .container {
 width: 85%;
            margin: 20px auto;
        }
        section {
            background-color: white;
            padding: 20px;
            margin-bottom: 20px;
            border-radius: 8px;
            box-shadow: 0px 2px 10px rgba(0, 0, 0, 0.1);
        }
        h2 {
            color: #007BFF;
            font-size: 2em;
        }
        .code {
            background-color: #2d2d2d;
            color: white;
            padding: 12px;
            border-radius: 5px;
            font-family: 'Courier New', monospace;
            white-space: pre-wrap;
            word-wrap: break-word;
        }
        footer {
            background-color: #333;
            color: white;
            padding: 15px;
            text-align: center;
        }
        .btn {
            background-color: #007BFF;
            color: white;
            padding: 12px 25px;
            text-decoration: none;
            border-radius: 5px;
            font-size: 1.2em;
        }
        .btn:hover {
            background-color: #004c8c;
        }
    </style>
</head>
<body>

    <header>
        <h1>Windows Cybersecurity Techniques</h1>
        <p>Enhance your system's security using simple methods and commands</p>
    </header>

    <nav>
<a href="#firewall">Firewall</a>
        <a href="#antivirus">Antivirus</a>
        <a href="#updates">Updates</a>
        <a href="#bitlocker">BitLocker</a>
        <a href="#lockout">Lockout</a>
    </nav>

    <div class="container">

        <section id="firewall">
            <h2>1. Enable Windows Firewall</h2>
            <p>Windows Firewall is an essential tool for protecting your system from unauthorized access.</p>
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
            <p>Windows Defender helps protect your system from malware and other malicious threats.</p>
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
            <p>Keeping your system up to date ensures it is secure from known vulnerabilities.</p>
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
 <p>BitLocker ensures that your data is encrypted, making it unreadable to unauthorized users.</p>
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
            <p>Account lockout policies help protect your system from brute-force attacks by locking accounts after several failed login attempts.</p>
            <h3>Graphical Method:</h3>
            <p>Open <strong>Local Group Policy Editor</strong> and navigate to <strong>Account Lockout Policy</strong>.</p>
            <h3>CMD Method:</h3>
            <div class="code">
                secpol.msc
            </div>
            <h3>PowerShell Method:</h3>
            <div class="code">
                Set-LocalUser -Name "username" -AccountNeverExpiresfalse
            </div>
        </section>
[1/2, 23:05] ChatGPT: <footer>
            <p>Windows Cybersecurity Techniques - Keep Your System Secure</p>
            <a href="https://github.com/yourusername/your-repository" class="btn">Visit My GitHub</a>
        </footer>

    </div>

</body>
</html>
