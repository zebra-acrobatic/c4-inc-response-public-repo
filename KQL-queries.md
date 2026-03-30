## Example 1: Detecting Failed Login Attempts
This query identifies failed login attempts from the `DeviceLogonEvents` table.

```kql
DeviceLogonEvents
| where ActionType in ("LogonFailed")
| where AccountDomain in ("tdm")
```

=== "Targetting a Specific Workstation"
    ```kql
    DeviceLogonEvents
    | where DeviceName in ("a103-01.tdm.local")
    ```

=== "Focusing on a Specific User"
    ```kql
    DeviceLogonEvents
    | where AccountName in ("smitha")  
    ```
## Example 2: Network Connections from a Specific Device
This query retrieves network connection events from the `DeviceNetworkEvents` table for a specific device.
```kql
DeviceNetworkEvents
| where DeviceName in ("a103-01.tdm.local")
```

### Contribute Your Own Queries
Feel free to contribute your own KQL queries to this documentation! If you have a useful query that you think would benefit others, please submit a pull request with your query and a brief description of what it does and how it can be used in investigations.

To do this, go to the Github page: 
