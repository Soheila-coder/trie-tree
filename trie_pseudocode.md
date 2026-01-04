# Node Structure

Structure TrieNode:
    children : Map<Character, TrieNode>
    is_end_of_word : Boolean

--------------

# Trie Structure

Structure Trie:
    root : TrieNode



--------------

# Insert Operation

Function INSERT(word):
    current = root

    For each character c in word:
        If c not in current.children:
            current.children[c] = new TrieNode
        current = current.children[c]

    current.is_end_of_word = True

------------

# Search Operation

Function SEARCH(word):
    current = root

    For each character c in word:
        If c not in current.children:
            return False
        current = current.children[c]

    return current.is_end_of_word

-------------

# Prefix Search

Function STARTS_WITH(prefix):
    current = root

    For each character c in prefix:
        If c not in current.children:
            return False
        current = current.children[c]

    return True
