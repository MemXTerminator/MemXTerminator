---
comments: true
---

# Usage

## GUI

This software has a user-friendly GUI. To use this software:

First enter into the conda environment you create or you have installed the `MemXTerminator`, like:

```bash

conda activate mxt

```

Then simply type:

```bash

MemXTerminator gui &
```

You should see the interface now:

![GUI](../assets/images/gui.png){: .small}
<span class="caption">MemXTerminator GUI</span>

## Fix Map ID

If you get the error like this during the membrane subtraction:

> ValueError: Map ID string not found - not an MRC file, or file is corrupt

It's due to the `mrcfile` python library. 

For more details you can refer to these links:

* [Handling corrupt or bad-header MRC files #544](https://github.com/ComputationalCryoEM/ASPIRE-Python/issues/544)
* [Permissive read mode](https://mrcfile.readthedocs.io/en/stable/usage_guide.html#permissive-read-mode)

You can use this command to fix the `.mrc` files:

```bash

MemXTerminator fixmapid <path_to_mrc_file>
```
