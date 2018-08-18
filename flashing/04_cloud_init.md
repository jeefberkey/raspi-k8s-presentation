<!SLIDE>

# cloud-init

    @@@ yaml
    #cloud-config
    # vim: syntax=yaml
    #
    ---
    hostname: <%= host %>
    manage_etc_hosts: true

    users:
    - name: nick
      gecos: "Nick Miller"
      sudo: ALL=(ALL) NOPASSWD:ALL
      shell: /bin/bash
      groups: users,docker,video,input
      passwd: $6$ipbhis2s$7VItsYdE91SyRzOEzGB1J7A9PDAE6Od7K5X88DlWJTbKENhxIbR5.q.hQT/xOzOOZBvo1RfIcy/tEj7li1Zg4/
      lock_passwd: false
      ssh_pwauth: true
      chpasswd: {expire: true}
      ssh-authorized-keys:
      - <%= File.read(File.expand_path('~/.ssh/id_rsa.pub')).chomp %>

    locale: "en_US.UTF-8"
    timezone: "America/New_York"
