### Uses of `ItemRepository`

___

#### Code Model

```
ItemRepository<CodeModelRepositoryItem, CodeModelRequestItem> 
```

__Location__ : duchain/codemodel.cpp:157 \
__Class__ : `CodeModelPrivate` 

__Description__ \
Persistent store that efficiently holds a list of identifiers and their kind for each declaration-string.
___

#### Definition Map

```
ItemRepository<DefinitionsItem, DefinitionsRequestItem> 
```

__Location__ : duchain/definitions.cpp:143 \
__Class__ : `DefinitionsPrivate` 

__Description__ \
Maps declaration-ids to definitions. \
Global mapping of one Declaration-Ids to multiple Definitions, protected through DUChainLock.
___

#### Environment Lists

```
ItemRepository<EnvironmentInformationListItem, EnvironmentInformationListRequest> 
```

__Location__ : duchain/duchain.cpp:1104 \
__Class__ : `DUChainPrivate` 

__Description__ \
Maps filenames to a list of top-contexts/environment-information.
___

#### Environment Information

```
ItemRepository<EnvironmentInformationItem, EnvironmentInformationRequest>
```

__Location__ : duchain/duchain.cpp:1106 \
__Class__ : `DUChainPrivate` 

__Description__ \
Maps top-context-indices to environment-information item.
___

#### Identifier Repository

```
ItemRepository<ConstantIdentifierPrivate, IdentifierItemRequest>
```

__Location__ : duchain/identifier.cpp:164 \
__Class__ :  

__Description__ \

___

