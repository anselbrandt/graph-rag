# Graph RAG

### Install Dependencies

```
brew install pkg-config cmake coreutils

or apt install pkg-config cmake coreutils
```

### Download Spacy Model

```
uv run spacy download en_core_web_sm
```

### GLiREL Labels

```
labels = {"glirel_labels": {
    'co-founder': {"allowed_head": ["PERSON"], "allowed_tail": ["ORG"]},
    'no relation': {},  # head and tail can be any entity type
    'country of origin': {"allowed_head": ["PERSON", "ORG"], "allowed_tail": ["LOC", "GPE"]},
    'parent': {"allowed_head": ["PERSON"], "allowed_tail": ["PERSON"]},
    'located in or next to body of water': {"allowed_head": ["LOC", "GPE", "FAC"], "allowed_tail": ["LOC", "GPE"]},
    'spouse': {"allowed_head": ["PERSON"], "allowed_tail": ["PERSON"]},
    'child': {"allowed_head": ["PERSON"], "allowed_tail": ["PERSON"]},
    'founder': {"allowed_head": ["PERSON"], "allowed_tail": ["ORG"]},
    'founded on date': {"allowed_head": ["ORG"], "allowed_tail": ["DATE"]},
    'headquartered in': {"allowed_head": ["ORG"], "allowed_tail": ["LOC", "GPE", "FAC"]},
    'acquired by': {"allowed_head": ["ORG"], "allowed_tail": ["ORG", "PERSON"]},
    'subsidiary of': {"allowed_head": ["ORG"], "allowed_tail": ["ORG", "PERSON"]},
    }
}
```
