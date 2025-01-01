# Home Assistant Add-on: LetsEncrypt Mythic Beasts

## How to use

1. Create an API Key from the Mythic Beasts control panel
   - See Step 1 here: https://www.mythic-beasts.com/support/domains/letsencrypt_dns_01
2. Configure this add-on
   1. Enter your email address. This will be used by LetsEncrypt to send you notifications.
   2. Enter the FQDN of the domain you are looking to secure
      - E.g. if your Home Assistant server is at homeassistant.example.org then enter homeassistant.example.org
    3. Enter your API key in the format: domain APIkey Secret
      - E.g. example.org ucykkqh8srztsn7b bL4jnTjPIHNXFOgaLC6SA1-QWp4l0J
3. Run the add-in
4. The add-in will run and then terminate, saving certificates into Home Assistant's /ssl directory
5. You can monitor the add-in from the Add-in's Logs page

By default the add-on doesn't automatically renew certifications. You will need to start the add-on each time that you want to try to renew. You could do that with an automation in Home Assistant

