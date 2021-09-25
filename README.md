# ansible-wireguard-server

Simple Ansible role to install Wireguard and setup VPN(s) using it. This role has been tested in Ubuntu and Arch Linux.

      ## Usage

      The simplest configuration consists of:

      ```yaml
      - name: Simple Example
        hosts: localhost
        roles:
          - role: ansible-wireguard-server
        vars:
          mobiles: True
          wireguard:
            domain: vpn.example.org
            networks:
              - name: wg0
                network_segment: 192.168.17
                server_port: 57034
                nat: True
                enable: False
            clients:
              - name: client1
                client_number: 2
                mobile: True
      ```

