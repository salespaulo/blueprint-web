#### sed-it-name-app
- Node Version 9.11.1
- Node Package Manager Version 5.6.0

Projeto maven parent para agrupar os projetos *nodejs* e *reactjs*

```
$> sudo docker run -d                           \
    --name <nome_container>                     \
    --network <nome_rede>                       \
    -p 4000:4000 sed-it-name-app
```

### Change project name

Execute following shell scripts:
```
for i in `find . -type f -name "*" | grep -v node_modules | grep -v \/node\/ | grep -v \/node_tmp\/ | grep -v .git` \
    ; do echo $i                                 \
    && sed 's/sed-it-name-app/test-it/g' $i > x  \
    && cat x > $i                                \
    && rm x                                      \
    ; done
```

```
for i in `find . -type f -name "*" | grep -v node_modules | grep -v \/node\/ | grep -v \/node_tmp\/ | grep -v .git` \
    ; do echo $i                                        \
    && sed 's/sed-it-group-app/test-it-group/g' $i > x  \
    && cat x > $i                                       \
    && rm x                                             \
    ; done
```

```
for i in `find . -type f -name "*" | grep -v node_modules | grep -v \/node\/ | grep -v \/node_tmp\/ | grep -v .git` \
    ; do echo $i                                 \
    && sed 's/sed-it-prime-number/17/g' $i > x   \
    && cat x > $i                                \
    && rm x                                      \
    ; done
```
