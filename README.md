# SecureScore module

This is a beta version of my SecureScore Module. This module allows you to get your secure scores for easy documentation, or modify the secure score settings. I'm going to be adding a method to also allow to third party approvals.

# Installation instructions

This module has been published to the PowerShell Gallery. Use the following command to install:  

    install-module SecureScore


# Usage

     ######### Secrets #########
     $ApplicationId         = 'AppID'
     $ApplicationSecret     = 'AppSecret'
     $TenantID              = 'TenantID'
     $RefreshToken          = 'LongRefreshToken'
     $ExchangeRefreshToken = 'LongExchangeToken'
     $UPN = "UPN-Used-To-Generate-Tokens"
     ######### Secrets #########


    get-securescore -TenantID 'OneTenant.onmicrosoft.com' -upn $upn -ApplicationSecret $ApplicationSecret -ApplicationId $ApplicationId -RefreshToken $RefreshToken

     set-securescore -TenantID 'OneTentant.onmicrosoft.com' -ControlName LowImpact -upn $upn -ApplicationSecret $ApplicationSecret -ApplicationId $ApplicationId -RefreshToken $RefreshToken -ExchangeToken $ExchangeRefreshToken 


  
**Examples:**

    $Score = get-securescore -TenantID 'OneTenant.onmicrosoft.com' -upn $upn -ApplicationSecret $ApplicationSecret -ApplicationId $ApplicationId -RefreshToken $RefreshToken

    $Score = get-securescore -AllTenants -upn $upn -ApplicationSecret $ApplicationSecret -ApplicationId $ApplicationId -RefreshToken $RefreshToken

# Contributions

Feel free to send pull requests or fill out issues when you encounter them. I'm also completely open to adding direct maintainers/contributors and working together! :)

# Future plans

Version 1.0 has basic functionality. will update in time.

- [x] Allow getting the secure score for all tenants
- [x] Allow modifying some of the Secure Score settings and perform best-practices
- [ ] Allow advanced Secure Score properties to be set