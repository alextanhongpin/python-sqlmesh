# python-sqlmesh

```bash
$ pipenv --python 3.11
$ pipenv shell
$ (python-sqlmesh) pipenv install <your package>
```


Follow the tutorial [here](https://sqlmesh.readthedocs.io/en/stable/quick_start/#1-create-a-sqlmesh-project).

```bash
$ sqlmesh init
$ sqlmesh plan
$ sqlmesh plan dev

# Perform some updates in models/incremental_model.sql
# Validate changes are made in dev.
$ sqlmesh fetchdf "select * from sqlmesh_example__dev.incremental_model"

# Changes are not made in prod.
$ sqlmesh fetchdf "select * from sqlmesh_example.incremental_model"

# Apply changes to prod.
$ sqlmesh plan

# Validate changes made in dev.
$ sqlmesh fetchdf "select * from sqlmesh_example.incremental_model"
```
