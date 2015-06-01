
This is a modification upon [`rfc6902-json-diff`](https://github.com/cqql/rfc6902-json-diff-js) that **doesn't** satisfy RFC6902.

Changes :
* for leaf operations
  * upon an `add` or `replace` operation, retain the new value in a `newValue` property
  * upon a `remove` or `replace` operation, retain the new value in an `oldValue` property
  * if values of a field referred to by an identical path are equal (according to `lodash.isEqual`) across the compared objects, this is considered as a `keep` operation. Both `newValue` and `oldValue` are defined
* no change for non-leaf nodes
