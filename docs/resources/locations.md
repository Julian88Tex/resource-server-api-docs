## Resources

# Locations

### Attributes

Field          | Type         | Note      | Description                         
---------------|--------------|-----------|------------------------------------
`id`           | `integer`    | read-only | Unique location ID.
`name`         | `string`     |           | The name of the location.
`address`      | `string`     |           | The location's street address website.
`unit`         | `string`     |           | The address unit, such as suite or level number.
`city`         | `string`     | required  | The location's city.
`state`        | `string`     | required  | The location's 2-letter state abbreviation.
`zip_code`     | `string`     |           | The location's USPS Zip code.
`lat`          | `float`      | read-only | The latitude of the location.
`long`         | `float`      | read-only | The longitude of the location.
`is_primary`   | `boolean`    |           | Whether or not this is the associated resource's primary location. Default is `false`, unless no other location exists.

### Endpoints on Organizations

#### `GET /v1/organizations/:organization_id/locations`

Returns the locations of an organization.

#### `POST /v1/organizations/:organization_id/locations`

Creates a new location of an organization.

#### `GET /v1/organizations/:organization_id/locations/:id`

Returns a specific location with the following nested resources:

- [`phones`](phones.md)
- [`schedule`](schedule.md)

#### `PUT /v1/organizations/:organization_id/locations/:id`

Updates a location of an organization.

#### `DELETE /v1/organizations/:organization_id/locations/:id`

Deletes a location of an organization.

#### Permissions

* Only resource owners and admins can manage locations, schedules, and phone numbers.
