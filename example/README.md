# Troubleshooting

Caso ocorrra o problema de permissão

```
ts=2023-03-17T19:26:55.661Z caller=query_logger.go:113 level=error component=activeQueryTracker msg="Failed to create directory for logging active queries"
ts=2023-03-17T19:26:55.661Z caller=query_logger.go:91 level=error component=activeQueryTracker msg="Error opening query log file" file=/prometheus/data/queries.active err="open data/queries.active: no such file or directory"
panic: Unable to create mmap-ed active query log
```

Criar a pasta com permissão
```
mkdir prometheus_data

sudo chown -R 65534:65534 prometheus_data

```
