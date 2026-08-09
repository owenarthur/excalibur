# Chargebook

This is the illustrative charge ledger for the Excalibur scaffold.

Excalibur does not ship a runtime in this scaffold. The purpose of this file is to show how a charge model can stay legible at the manifest level.

Base cast charge defaults to `0` unless a cast explicitly says otherwise.

## Spellbook: `adept`

| Cast | Charge | Notes |
| --- | ---: | --- |
| `codex_emanation` | `0` | Base cost is `0`; the coding subrun still draws charge from the current run and widens implementation work explicitly. |
| `echo_emanation` | `0` | Base cost is `0`; each same-model subrun still draws charge from the current run. |
| `genius_emanation` | `0` | Base cost is `0`; the stronger model pass still draws charge from the current run. |
| `halt_activity` | `0` |  |
| `kimi_emanation` | `0` | Base cost is `0`; the alternate-model pass still draws charge from the current run. |
| `list_spellbooks` | `0` |  |
| `open_spellbook` | `0` |  |
| `reclaim_charge` | `0` | Ritual-gated recovery path. Charge recovery stays explicit instead of silently refilling. |
| `relay_to_summoner` | `0` |  |
| `send_signal` | `0` |  |
| `send_user_update` | `0` |  |

## Spellbook: `artifact`

| Cast | Charge | Notes |
| --- | ---: | --- |
| `archive_artifact` | `0` | Local artifact management should stay cheap. |
| `create_artifact` | `0` | Durable work product is core, not a premium path. |
| `create_artifact_folder` | `0` |  |
| `edit_artifact` | `0` | Revising durable output should stay cheap. |
| `list_artifacts` | `0` |  |
| `move_artifact` | `0` |  |
| `read_artifact` | `0` |  |
| `search_artifacts` | `0` |  |

## Spellbook: `corpus`

| Cast | Charge |
| --- | ---: |
| `list_corpus_files` | `0` |
| `read_corpus_file` | `0` |
| `search_corpus` | `0` |

## Spellbook: `media`

| Cast | Charge |
| --- | ---: |
| `conjure_image` | `3` |
| `enshrine_graphic` | `0` |
| `render_visual_guide` | `0` |
| `trace_media` | `0` |

## Spellbook: `memory`

| Cast | Charge |
| --- | ---: |
| `delete_memory_file` | `0` |
| `list_memory_files` | `0` |
| `move_memory_file` | `0` |
| `read_memory_file` | `0` |
| `search_memories` | `0` |
| `write_memory_file` | `0` |

## Spellbook: `network`

| Cast | Charge |
| --- | ---: |
| `inspect_network_artifact` | `0` |
| `list_network_artifacts` | `0` |
| `publish_network_artifact` | `0` |
| `update_network_artifact_status` | `0` |

## Spellbook: `portal`

| Cast | Charge | Notes |
| --- | ---: | --- |
| `inspect_portal` | `0` |  |
| `list_portals` | `0` |  |
| `moon_phase` | `0` | Local celestial computation should not require network cost. |
| `read_celestial_state` | `0` |  |
| `update_portal_section` | `0` | Portal state updates should stay cheap. |

## Spellbook: `questbook`

| Cast | Charge |
| --- | ---: |
| `archive_quest` | `0` |
| `create_quest_folder` | `0` |
| `edit_quest` | `0` |
| `list_questbook` | `0` |
| `move_quest` | `0` |
| `read_quest` | `0` |
| `search_questbook` | `0` |
| `write_quest` | `0` |

## Spellbook: `ritual`

| Cast | Charge |
| --- | ---: |
| `list_rituals` | `0` |
| `read_ritual` | `0` |

## Spellbook: `web`

| Cast | Charge |
| --- | ---: |
| `behold_page` | `0` |
| `download_pdf` | `2` |
| `enshrine_snapshot` | `2` |
| `scry_url` | `0` |
| `trace_links` | `0` |
| `walk_branch` | `0` |
| `web_search` | `2` |
| `website_to_pdf` | `2` |

## Spellbook: `working`

| Cast | Charge |
| --- | ---: |
| `begin_working` | `0` |
| `cease_working` | `0` |
| `inspect_working` | `0` |
| `list_workings` | `0` |
| `record_checkpoint` | `0` |
