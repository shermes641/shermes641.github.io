layout: post
title:  "Cleaning Up Populate DB"
date:   2016-08-30 11:09:34 -0600
categories: jekyll update
---
To load data from csv fixtures:
```from ph_model.fixtures.legacy_db import loader;loader.load()```

To clean up schema and data
```from ph_model.fixtures.common.cleanup import cleanup; cleanup()```

To load usages: loader.load_usage()
