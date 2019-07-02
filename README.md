# CST Rosdep Rules

Public host for our custom rosdep rules

## Adding custom rules

Create a new file in `/etc/ros/rosdep/sources.list.d/` that points our list. The filename should use a lower number so it is processed first.

Our recomended filename is `10-cst.list`

And the contents of the file should be:

```
yaml https://github.com/casta-spes-tech/rosdep_rules/raw/master/rosdep_rules/python.yaml
```

Once you added the file make sure to run `rosdep update` (This has to be run without sudo)

You can test that the list was accepted by runnig `rosdep resolve <key-name>` for one of our custom keys

To test with different Os settings use 

```
rosdep resolve <key-name> --os=OS_NAME:OS_VERSION
```

