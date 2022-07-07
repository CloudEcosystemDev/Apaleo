# <p align="center" width="100%"> <img src="./logo.png" width="250" height="250"> </p> 
# <p align="center" width="100%"> apaleo Inventory API OIH Connector </p>

## Description

A generated OIH connector for the apaleo Inventory API API (version v1).

Generated from: https://api.apaleo.com/swagger/inventory-v1/swagger.json<br/>
Generated at: 2022-07-07T23:51:17+02:00

## API Description

Setup and manage <b>properties</b> (hotels, etc.) and all the entites in them to rent out:<br/>
<b>Units</b> such as rooms, parking lots, beds, meeting rooms, etc. Units can be combined into <b>groups</b> (single rooms, double rooms).<br/>

## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Creates a property
> Use this call to create a new property.<br>You must have at least one of these scopes: 'properties.create, setup.manage'.<br/>

*Tags:* `Property`

#### Input Parameters
* `Idempotency-Key` - _optional_ - Unique key for safely retrying requests without accidentally performing the same operation twice. <br/>
We'll always send back the same response for requests made with the same key, <br/>
and keys can't be reused with different request parameters. Keys expire after 24 hours.<br/>

### Check if a property exists
> Check if a property exists by id.<br>You need to be authorized (no particular scope required)<br/>

*Tags:* `Property`

#### Input Parameters
* `id` - _required_ - The id of the property.<br/>

### Get a property
> Get a property by id.<br>You need to be authorized (no particular scope required)<br/>

*Tags:* `Property`

#### Input Parameters
* `id` - _required_ - The id of the property.<br/>
* `languages` - _optional_ - 'all' or comma separated list of two-letter language codes (ISO Alpha-2)<br/>
* `expand` - _optional_ - List of all embedded resources that should be expanded in the response. Possible values are: actions. All other values will be silently ignored.<br/>

### Allows to patch unit
> Here's a list of allowed operations:<br/>> <br/>
> - Set unit condition<br/>> <br/>
> - Set unit description<br/>> <br/>
> - Set unit name<br/>> <br/>
> - Set unit unitGroupId<br/>> <br/>
> - Set unit maxPersons<br/>> <br/>
> - Add unit attribute<br/>> <br/>
> - Remove unit attribute<br>You must have at least one of these scopes: 'units.manage, setup.manage'.<br/>

*Tags:* `Unit`

#### Input Parameters
* `id` - _required_ - The id of the unit.<br/>

### Get a unit
> Get a unit by id.<br>You must have at least one of these scopes: 'units.read, setup.read, setup.manage'.<br/>

*Tags:* `Unit`

#### Input Parameters
* `id` - _required_ - The id of the unit.<br/>
* `languages` - _optional_ - 'all' or comma separated list of two-letter language codes (ISO Alpha-2)<br/>
* `expand` - _optional_ - List of all embedded resources that should be expanded in the response. Possible values are: property, unitGroup. All other values will be silently ignored.<br/>

### Delete a unit
> Use this call to delete a unit.<br>You must have at least one of these scopes: 'units.delete, setup.manage'.<br/>

*Tags:* `Unit`

#### Input Parameters
* `id` - _required_ - The id of the unit.<br/>

### Allows to patch one or more units
> Here's a list of allowed operations:<br/>> <br/>
> - Set unit condition<br/>> <br/>
> - Set unit description<br/>> <br/>
> - Set unit name<br/>> <br/>
> - Set unit unitGroupId<br/>> <br/>
> - Set unit maxPersons<br/>> <br/>
> - Add unit attribute<br/>> <br/>
> - Remove unit attribute<br>You must have at least one of these scopes: 'units.manage, setup.manage'.<br/>

*Tags:* `Unit`

#### Input Parameters
* `unitIds` - _required_

### Check if a unit exists
> Check if a unit exists by id.<br>You must have at least one of these scopes: 'units.read, setup.read, setup.manage'.<br/>

*Tags:* `Unit`

#### Input Parameters
* `id` - _required_ - The id of the unit.<br/>

### Allows to modify property
> Here's a list of allowed operations:<br/>> <br/>
> - Replace Name<br/>> <br/>
> - Add, replace and remove Description<br/>> <br/>
> - Replace CompanyName<br/>> <br/>
> - Add, replace and remove ManagingDirectors<br/>> <br/>
> - Replace CommercialRegisterEntry<br/>> <br/>
> - Replace TaxId<br/>> <br/>
> - Replace Location<br/>> <br/>
> - Add, replace and remove BankAccount<br/>> <br/>
> - Replace PaymentTerms<br/>> <br/>
> - Set IsTemplate<br>You must have at least one of these scopes: 'properties.manage, setup.manage'.<br/>

*Tags:* `Property`

#### Input Parameters
* `id` - _required_ - The id of the property.<br/>

### Allows to modify unit attribute
> Here's a list of allowed operations:<br/>> <br/>
> - Replace / Remove Description<br>You must have at least one of these scopes: 'unitattributes.manage, setup.manage'.<br/>

*Tags:* `UnitAttribute`

#### Input Parameters
* `id` - _required_ - Id of unit attribute<br/>

### Check if a unit attribute exists
> Check if a unit attribute exists<br>You must have at least one of these scopes: 'unitattributes.read, setup.read, setup.manage'.<br/>

*Tags:* `UnitAttribute`

#### Input Parameters
* `id` - _required_ - The id of the unit attribute.<br/>

### Deletes unit attribute
> Deletes unit attribute<br>You must have at least one of these scopes: 'unitattributes.delete, setup.manage'.<br/>

*Tags:* `UnitAttribute`

#### Input Parameters
* `id` - _required_ - Id of unit attribute<br/>

### Create a unit attribute
> Use this call to create a new unit attribute.<br>You must have at least one of these scopes: 'unitattributes.create, setup.manage'.<br/>

*Tags:* `UnitAttribute`

#### Input Parameters
* `Idempotency-Key` - _optional_ - Unique key for safely retrying requests without accidentally performing the same operation twice. <br/>
We'll always send back the same response for requests made with the same key, <br/>
and keys can't be reused with different request parameters. Keys expire after 24 hours.<br/>

### Create a unit group
> Use this call to create a new unit group.<br>You must have at least one of these scopes: 'unitgroups.create, setup.manage'.<br/>

*Tags:* `UnitGroup`

#### Input Parameters
* `Idempotency-Key` - _optional_ - Unique key for safely retrying requests without accidentally performing the same operation twice. <br/>
We'll always send back the same response for requests made with the same key, <br/>
and keys can't be reused with different request parameters. Keys expire after 24 hours.<br/>

### Get a unit group
> Get a unit group by id.<br>You must have at least one of these scopes: 'unitgroups.read, setup.read, setup.manage'.<br/>

*Tags:* `UnitGroup`

#### Input Parameters
* `id` - _required_ - The id of the unit group.<br/>
* `languages` - _optional_ - 'all' or comma separated list of two-letter language codes (ISO Alpha-2)<br/>
* `expand` - _optional_ - List of all embedded resources that should be expanded in the response. Possible values are: property. All other values will be silently ignored.<br/>

### Check if a unit group exists
> Check if a unit group exists by id.<br>You must have at least one of these scopes: 'unitgroups.read, setup.read, setup.manage'.<br/>

*Tags:* `UnitGroup`

#### Input Parameters
* `id` - _required_ - The id of the unit group.<br/>

### Get unit attribute by id
> Get unit attribute by id<br>You must have at least one of these scopes: 'unitattributes.read, setup.read, setup.manage'.<br/>

*Tags:* `UnitAttribute`

#### Input Parameters
* `id` - _required_ - The id of the unit attribute<br/>

### Create a unit
> Use this call to create a new unit.<br>You must have at least one of these scopes: 'units.create, setup.manage'.<br/>

*Tags:* `Unit`

#### Input Parameters
* `Idempotency-Key` - _optional_ - Unique key for safely retrying requests without accidentally performing the same operation twice. <br/>
We'll always send back the same response for requests made with the same key, <br/>
and keys can't be reused with different request parameters. Keys expire after 24 hours.<br/>

### Create multiple units
> Use this call to create multiple units, following a naming rule.<br>You must have at least one of these scopes: 'units.create, setup.manage'.<br/>

*Tags:* `Unit`

#### Input Parameters
* `Idempotency-Key` - _optional_ - Unique key for safely retrying requests without accidentally performing the same operation twice. <br/>
We'll always send back the same response for requests made with the same key, <br/>
and keys can't be reused with different request parameters. Keys expire after 24 hours.<br/>

### Replace a unit group
> Use this call to modify a unit group.<br>You must have at least one of these scopes: 'unitgroups.manage, setup.manage'.<br/>

*Tags:* `UnitGroup`

#### Input Parameters
* `id` - _required_ - The id of the unit group.<br/>

### Delete a unit group
> Use this call to delete a unit group.<br>You must have at least one of these scopes: 'unitgroups.delete, setup.manage'.<br/>

*Tags:* `UnitGroup`

#### Input Parameters
* `id` - _required_ - The id of the unit group.<br/>

## License

: Apaleo<br/>
                    <br/>

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
