
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
