# External Authentication

Whenever an app having external auth is installed, the external auth url will receive a request with fields. We would be sending the api-key provided by the user with every workflow process completion to the url mentioned inside of the workflows.

```
{
  "apiKey": string,
  "locationId": string[],
  "companyId": string || null,
  "excludedLocations": string[],
  "approveAllLocations": boolean || null
}
```

**NOTE**: External auth verification only happens when the user installs app in Location.

## Explanation of all the keys present

- apiKey: It is the API key that is entered by the user during app installation. It would always be present.
- approveAllLocations: It is a flag to indicate if the application was installed using bulk installation.
- locationId: It contains array of locationIds where the application was installed. It can be empty if the user has installed application from agency and used bulk installation.
- companyId: It contains the agencyId if the application was installed from agency, it will be null when application was installed from location.
- excludedLocations: It contains array of locationIds, it is populated when user uses the bulk installation feature and deselects some of the locations while installing app. It will be empty when application was installed from location.

**NOTE:** When the user uses bulk installation feature to install the application, developer would be required to fetch all the locations present in the agency (which can be fetched using /locations/search) and remove excludedLocations from the list of locations fetched, to get the number of locations where the application was installed.
