<body>
  <div>
    <span>
    <h2>Set up Ngrok to be launched automatically and run the tunnels set in the config file</h2>
    </span>
    <span>
      <ol>
        <li>Download and install [NGROK](https://ngrok.com/)</li>
        <li>Copy ngrok folder to /usr/local/bin/</li>
        <li>Rename or Copy /usr/local/bin/ngrok/ngrok.yml.example to /usr/local/bin/ngrok/ngrok.yml</li> 
        <li>Tweak the settings in the newly copied/renamed /usr/local/bin/ngrok/ngrok.yml config (token, tunnels, etc...)</li>
        <li>In /usr/local/bin/ngrok/ngrok.sh, change the path to ngrok exe if you installed it in a different path</li>
        <li><b>chmod 744 /usr/local/bin/ngrok/ngrok.sh</b></li>
        <li>Copy ngrok.service to /etc/systemd/system</li>
        <li><b>chmod 664 /etc/systemd/system/ngrok.service</b></li>
        <li><b>systemctl daemon-reload</b></li>
        <li><b>systemctl enable ngrok.service</b></li>
      </ol>
    </span>
    <span>
      If you want to check that everything is working:
      <ol>
        <li>
          <ul>
            <li><b>systemctl start ngrok.service</b></li>
            <li>Check on [your dashboard](https://dashboard.ngrok.com/status) that tunnels are running</li>
          </ul>
        </li>
        <li>Reboot your system and check if the tunnels are running</li>
     </ol>
    </span>
  </div>
</body>
