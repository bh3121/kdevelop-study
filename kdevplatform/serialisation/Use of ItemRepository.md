### KDevelop Repositories


[Code Model](#code-model) 
[Definition Map](#definition-map) 
[Environment Lists](#environment-lists) 
[Environment Information](#environment-information) 
[Identifier Repository](#identifier-repository) 
[Qualified Identifier Repository](#qualified-identifier-repository) 
[Importer Map](#importer-map) 
[Instantiation Information Repository](#instantiation-information-repository) 
[Persistent Declaration Table](#persistent-declaration-table) 
[Type Repository](#type-repository) 
[Use Map](#use-map) 
[file modification repository](#file-modification-repository) 
[file modification sets](#file-modification-sets) 
[Comment Repository](#comment-repository) 
[Recursive Imports](#recursive-imports) 
[String Index](#string-index) 
[Counters](#counters) 
[parsing_environment_data](#parsing_environment_data) 
[available_top_context_indices](#available_top_context_indices) 


> when a repository is created which uses ItemRepository , a seperate {Repository File Name}_dyanmic file will also be created
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

__Description__ 

___

#### Qualified Identifier Repository

```
ItemRepository<ConstantQualifiedIdentifierPrivate, QualifiedIdentifierItemRequest>
```

__Location__ : duchain/identifier.cpp:334 \
__Class__ :  

__Description__ 

___

#### Importer Map

```
ItemRepository<ImportersItem, ImportersRequestItem> 
```

__Location__ : duchain/importers.cpp:109 \
__Class__ : `ImportersPrivate`

__Description__ \
Maps declaration-ids to Importers \
Global mapping of Declaration-Ids to contexts that import the associated context, protected through DUChainLock. This is used as an alternative to the local importers list within DUContext, only for indirect imports(Across different files, or with templates).

___

#### Instantiation Information Repository

```
ItemRepository<InstantiationInformation, AppendedListItemRequest<InstantiationInformation> >
```

__Location__ : duchain/instantiationinformation.cpp:119 \
__Class__ :  

__Description__ 

___

#### Persistent Declaration Table

```
ItemRepository<PersistentSymbolTableItem, PersistentSymbolTableRequestItem, true, false>
```

__Location__ : duchain/persistentsymboltable.cpp:138 \
__Class__ : `PersistentSymbolTablePrivate`

__Description__ \
Maps declaration-ids to declarations. \
Global symbol-table that is stored to disk, and allows retrieving declarations that currently are not loaded to memory.
___

#### Type Repository

```
ItemRepository<AbstractTypeData, AbstractTypeDataRequest>
```

__Location__ : duchain/types/typerepository.cpp:91 \
__Class__ :  

__Description__ 

___

#### Use Map

```
ItemRepository<UsesItem, UsesRequestItem> 
```

__Location__ : duchain/uses.cpp:109 \
__Class__ : `UsesPrivate`

__Description__ \
Maps declaration-ids to Uses. \
Global mapping of Declaration-Ids to top-contexts, protected through DUChainLock.

___

#### file modification repository

```
ItemRepository<FileModificationPair, FileModificationPairRequest, true, false>
```

__Location__ : language/editor/modificationrevisionset.cpp:92 \
__Class__ : 

__Description__ \
set of modification-revisions assigned to file-names.

___

#### file modification sets

```
ItemRepository<SetNodeData, SetNodeDataRequest, false, false, sizeof(SetNodeData)>
```

__Location__ : language/editor/modificationrevisionset.cpp:113 \
__Class__ : 

__Description__ 

___

#### Comment Repository

```
ItemRepository<StringData, StringRepositoryItemRequest, false, true> 
```

__Location__ : duchain/declaration.cpp:69 \
__Class__ : 

__Description__ 

___

#### Recursive Imports

```
ItemRepository<SetNodeData, SetNodeDataRequest, false, false, sizeof(SetNodeData)>
```

__Location__ : duchain/topducontext.cpp:51 \
__Class__ : 

__Description__ 

___

#### String Index

```
ItemRepository<IndexedStringData, IndexedStringRepositoryItemRequest, false, false>
```

__Location__ : serialization/indexedstring.cpp:159 \
__Class__ : `IndexedStringRepositoryManager`

__Description__ 

___

#### Counters

```
Not a ItemRepository just a file
```

__Location__ : serialization/itemrepositoryregistry.cpp:302 \
__Class__ : 

__Description__ 

___

#### parsing_environment_data

```
Not a ItemRepository just a file
```

__Location__ : duchain/duchain.cpp:313 \
__Class__ : `DUChainPrivate`

__Description__ 

___

#### available_top_context_indices

```
Not a ItemRepository just a file
```

__Location__ : duchain/duchain.cpp:330 \
__Class__ : `DUChainPrivate`

__Description__ 

___

