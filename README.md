# Oklahoma Turpike Authority Toll Data

Normalized toll data for Oklahome Turnpike Authority turnpikes.

The data is scraped from https://www.pikepass.com/toll/AllTollRates.aspx

Last updated: 2018-10-14

## Files

### `turnpikes.csv`

| Column | Data Type | Description |
|-|-|-|
| `id` | long | Unique identifier |
| `name`| string | Turnpike name (quoted) |
| `description` | string | Turnpike description (quoted) |


### `exits.csv`

| Column | Data Type | Description |
|-|-|-|
| `id` | long | Unique identifier |
| `turnpike_id` | long | Turnpike ID from `turnpikes.csv` |
| `name` | string | Exit/entry description |
| `has_entry` | bool | _Not used, set to 1_ |
| `has_exit` | bool | _Not used, set to 1_ |

### `turnpikes.csv`

| Column | Data Type | Description |
|-|-|-|
| `id` | long | Unique identifier |
| `turnpike_id` | long | Turnpike ID from `turnpikes.csv` |
| `entry_id` | long | Origination exit ID from `exits.csv` |
| `exit_id` | long | Destination exit ID from `exits.csv` |
| `axles` | int | Axle count this toll applies to (2 - 6) |
| `cash_toll` | decimal | Cash toll rate |
| `disc_toll` | decimal | Discounted "PikePass" toll rate |

## Disclaimer

This repository (and the data contained within) is neither affiliated with nor endorsed by anyone associated with the Oklahoma Turnpike Authority or the State of Oklahoma.

## Contributing and License

This repository (including all data) is released into the Public Domain. Please open an issue if you find any errors or omissions. Contributions and corrections to the repository should be submitted by pull request.
