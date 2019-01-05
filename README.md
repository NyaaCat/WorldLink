# WorldLink
Simple drop-in replacement for Multiverse NetherPortal that links corresponding nether and the end worlds.

# Configuration

`config.yml`

```
links:
  v1:
    END: v1_the_end
    NETHER: v1_nether
  v2:
    END: v2_the_end
    NETHER: v2_nether
  some_world:
    END: end1
    NETHER: nether2  # can be different names
```

On first load (config creation), the plugin will scan all loaded worlds and link them automatically if the world names match `{world}_nether` and `{world}_the_end`.

# Commands & Permissions

| Command | Permission Node | Description |
| --- | --- | --- |
| `/worldlink link world1 n:world1_nether e:world1_the_end` | `worldlink.link` | Link corresponding nether and the end world. Requires at least `n` or `e` argument |
| `/worldlink unlink world2 n:world3_nether` | `worldlink.unlink` | Unlink nether or the end world from a specific overworld. Requires at least `n` or `e` argument |

The plugin uses PaperSpigot API to allow mobs go through nether portals.

# License

MIT
