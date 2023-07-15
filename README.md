# ETH-Scriptions Collections Standards

#### A place for creators &amp; builders to organize ordinal collections!

## Getting Started

**_Artists_**

Collection creators can format their collection data using the `inscriptions.json` and `meta.json` format below to be
listed on all platforms using the standard!

**_Steps_**

1. Create your `inscriptions.json` and `meta.json` files in the format provided below
    - Check out [this](https://jsonlint.com/) file formatting tool!
2. Add to the registry by creating a pull request including new collections that follow the standard
3. Websites can use the registry to include the ordinal collections provided on their websites!

## File Structure

```
 .
 ├── ...
 └── collections
     └── [collection-name]
          ├── inscriptions.json
          └── meta.json
```

## Collection Metadata `meta.json`

```
{
  "name": "",                    # inscription name
  "inscription_icon": "",        # collection cover inscription id
  "supply": "",                  # total supply
  "slug": "",                    # directory name
  "description": "",             # collection description
  "twitter_link": "",            # official twitter
  "discord_link": "",            # official discord
  "website_link": ""             # official website
}
```

## Inscription Data `inscriptions.json`

```
[
  {
    "id": "",                    # inscription id
    "meta": {
      "name": ""                 # inscription name
    }
  },
  ...
]
```

## Expanding Inscription Data

Collections can be organized using `status` and `rank`

```
[
  {
    "id": "",
    "meta": {
      "name": "",
      "status": "",               # inscription theme
      "rank":                     # inscription rarity rank
      "content_uri":              # inscription content URI
    }
  },
  ...
]
```

Artists can assign unqiue traits to ordinals with `attributes`

```
[
  {
    "id": "",
    "meta": {
      "rank": ,
      "name": ""
      "attributes": [
        {
          "trait_type": "",        # trait category
          "value": "",             # trait value
          "status": "",            # trait theme
          "percent": ""            # percent of inscriptions in collection with trait
        },
        ...
      ]
    }
  },
  ...
]
```

## Here is an example of a completed collection inscription

Your meta.json file will look like this:

```
{
  "name": "ETH Scriptions",
  "inscription_icon": "0x105b9e469377123241df04ea72020b26320726fe17211dd384d4a6eaf06d7eb7",
  "supply": "1000",
  "slug": "eth-scriptions",
  "description": "Eth-scriptions [ES] is a platform that provides dApps
to support the development of Ethscriptions.",
  "twitter_link": "https://twitter.com/eth_scriptions",
  "discord_link": "https://discord.com/invite/urSjj39X23",
  "website_link": "https://eth-scriptions.com/"
}
```

Your inscriptions.json file will look like this:

```
[
  {
    "id": "0x105b9e469377123241df04ea72020b26320726fe17211dd384d4a6eaf06d7eb7",
    "meta": {
      "name": "ETH Scriptions #1",
      "status": "Rare",
      "rank": 1,
      "content_uri": "data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABgAAAAYCAYAAADgdz34AAAAu0lEQVR42mNgGAWjAAb+owGYGMWGYjMc2RKquhqXJSRb9p9EQBVL1nUnEmURRYbPzveF89EtpChiNSI2ohgKomFiFPsAZIhO4FQwRrYAJgZTTnQ8ICsGBQnIMBBX0y4FxRcwMWT3kJOZUIIDGcPESLIA3SKYBfgwurvIsgAWVDADsVlAciqCcfG5HmQxSA0l5RKKgfGynHCM7AOKiyR84U+Vkho57JGTLtWqAjQXU9VwBmyphuqVGSUWAAAxL08QNk6n2gAAAABJRU5ErkJggg=="
      "attributes": [
        {
          "trait_type": "Background",
          "value": "Sun sun",
          "status": "Rare",
          "percent": "2.90%"
        },
        {
          "trait_type": "Holes",
          "value": "rose blossom",
          "status": "Rare",
          "percent": "2.90%"
        }
      ]
    }
  },
  {
    "id": "0x105b9e469377123241df04ea72020b26320726fe17211dd384d4a6eaf06d7eb7",
    "meta": {
      "name": "ETH Scriptions #2",
      "status": "Common",
      "rank": 2,
      "content_uri": "data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABgAAAAYCAYAAADgdz34AAAAu0lEQVR42mNgGAWjAAb+owGYGMWGYjMc2RKquhqXJSRb9p9EQBVL1nUnEmURRYbPzveF89EtpChiNSI2ohgKomFiFPsAZIhO4FQwRrYAJgZTTnQ8ICsGBQnIMBBX0y4FxRcwMWT3kJOZUIIDGcPESLIA3SKYBfgwurvIsgAWVDADsVlAciqCcfG5HmQxSA0l5RKKgfGynHCM7AOKiyR84U+Vkho57JGTLtWqAjQXU9VwBmyphuqVGSUWAAAxL08QNk6n2gAAAABJRU5ErkJggg=="
      "attributes": [
        {
          "trait_type": "Background",
          "value": "Darkness",
          "status": "Common",
          "percent": "34.78%"
        },
        {
          "trait_type": "Holes",
          "value": "grey skies",
          "status": "Uncommon",
          "percent": "4.35%"
        }
      ]
    }
  },
  ...
]
```
