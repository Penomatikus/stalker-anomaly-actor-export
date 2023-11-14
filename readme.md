# stalker-anomaly-actor-export

Script registeres a callback for `save_state` and exports the following to  `<path-to-your-anomaly-installation>\appdata\logs\actor.json`:
  - general health information: health, psi, radiation
  - most statistics of the actor you can see in the pda
  - the equipment names in all 12 slots
  - the current and actual protection stats of the helmet and outfit if any

This is not feature complete. There are more details to come:
  - current and actual values of equiped weapons characteristics
  - real descriptions and names of the equipment
  - equiped arties with current and actual characteristics
  - overall current and actual sum of each protection type 

## Requirements
This script depends on the [stalker-anomaly-json](https://github.com/Penomatikus/stalker-anomaly-json) repository. Make sure to install it before using the actor-export script.

## JSON Output Example

```json
{
	"actor": {
		"status": {
			"health": 0.799988,
			"psi": 1,
			"rad": 0
		},
		"general": {
			"rep": 30,
			"rank": 183,
			"name": "Stalker",
			"community": "actor_stalker"
		},
		"statistics": {
			"tasks": {
				"failed": 0,
				"active": 2,
				"cancelled": 0,
				"completed": 0
			},
			"artys": {
				"found": 4,
				"detected": 0
			},
			"kills": {
				"monster": 7,
				"enemy": 2,
				"friend": 0,
				"neutral": 0
			},
			"misc": {
				"psi_storms": 0,
				"articles": 11,
				"smash": 8,
				"emissions": 0,
				"disguised": 0
			}
		},
		"equipment": {
			"detector": "detector_advanced",
			"weigth": 44.850910,
			"outfit": {
				"boom": {
					"current": 10.000000,
					"actual": 9.999996
				},
				"chem": {
					"current": 12.000000,
					"actual": 11.999995
				},
				"shock": {
					"current": 7.500000,
					"actual": 7.499997
				},
				"condition": 1.000000,
				"psi": {
					"current": 0,
					"actual": 0
				},
				"strike": {
					"current": 0.400000,
					"actual": 0.400000
				},
				"name": "novice_outfit",
				"burn": {
					"current": 0,
					"actual": 0
				},
				"wound": {
					"current": 9.090909,
					"actual": 9.090905
				},
				"rad": {
					"current": 0,
					"actual": 0
				}
			},
			"helmet": {
				"boom": {
					"current": 1.300000,
					"actual": 0.973725
				},
				"chem": {
					"current": 8.800000,
					"actual": 6.591369
				},
				"shock": {
					"current": 1.000000,
					"actual": 0.749019
				},
				"condition": 0.749019,
				"psi": {
					"current": 1.200000,
					"actual": 0.898823
				},
				"strike": {
					"current": 0,
					"actual": 0
				},
				"name": "helm_resp",
				"burn": {
					"current": 0,
					"actual": 0
				},
				"wound": {
					"current": 0.727273,
					"actual": 0.544741
				},
				"rad": {
					"current": 17.272726,
					"actual": 12.937605
				}
			},
			"money": 2938,
			"backpack": "itm_backpack",
			"weapon_1": "wpn_pm",
			"weapon_2": "wpn_svt40",
			"grenade": "grenade_smoke",
			"torch": "device_torch_dummy",
			"bolt": "bolt",
			"artefact": "?",
			"binoculars": "wpn_binoc_inv",
			"knife": "wpn_knife",
			"pda": "device_pda_1"
		}
	}
}
