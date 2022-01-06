## **Deploy SPfx package to app catalog**
[Blogpost that describes step by step](https://elischei.com/deploy-your-spfx-solution-using-pnp-powershell/)

```powershell
Connect-PnPOnline "yourtenantURL" -Interactive

$appcatalogURL = Get-PnPTenantAppCatalogUrl

$appCatConnection = Connect-PnPOnline $appcatalogURL -ReturnConnection -Interactive

Add-PnPApp -Path "./project-wp.sppkg" -Connection $appCatConnection -Publish
```
If you allready know the appcatalog url you can connect to it directly
```powershell
Connect-PnPOnline "appcatalogurl" -Interactive

Add-PnPApp -Path "./project-wp.sppkg"  -Publish 

```

### **Making the app avialable tenant wide**
Use -SkipFeatureDeployment to centrally deployed the solution across the tenant.
```powershell
Add-PnPApp -Path "./project-wp.sppkg" -Connection $appCatConnection -Publish -SkipFeatureDeployment
```

### **Update exisiting app**
Use -Overwrite to update an exisiting solution.
```powershell
Add-PnPApp -Path "./project-wp.sppkg" -Publish -Overwrite
```
