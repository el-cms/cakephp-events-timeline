# CakePHP events timeline

Events timeline for standard CakePHP actions. These events were taken from the [DebugKit's](#) Timeline

## Index, View
_Core Processing (Derived from `$_SERVER["REQUEST_TIME"]`)_

  - **Event**: `Controller.initialize` ([Cookbook](#))    
  - **Event**: `Controller.startup` ([Cookbook](#))
  - Controller action (`view`)	
    - `Cache.read` (_all used caches_) ([Cookbook](#))
  - **Event**: `Controller.beforeRender` ([Cookbook](#))
  - View Render start
    - **Event**: `View.beforeRender` ([Cookbook](#))
    - Render views, elements, cells...
    - **Event**: `View.afterRender` ([Cookbook](#))
    - **Event**: `View.beforeLayout` ([Cookbook](#))
    - Render layout, elements, cells... 
  - **Event**: `View.afterLayout` ([Cookbook](#))
  - **Event**: `Controller.shutdown` ([Cookbook](#))

### Diagram :
```sequence

participant Controller.initialize as A
participant Controller.startup as B
participant Controller.beforeRender as C
participant View.beforeRender as D
participant View.afterRender as E
participant View.beforeLayout as F
participant View.afterLayout as G
participant Controller.shutdown as H

Note right of B: Controller action
Note right of C: View render start
Note right of D: Render view elements
Note right of F: Render layout elements cells

A->B: xxx
B->C: xxx
C->D: xxx
D->E: xxx
E->F: xxx
F->G: xxx
G->H: xxx
```

## Add
## Edit
## Delete

## 	Found in files
**	\Cake\ORM\Behavior::implementedEvents()**
```
'Model.beforeMarshal' => 'beforeMarshal',
'Model.beforeFind' => 'beforeFind',
'Model.beforeSave' => 'beforeSave',
'Model.afterSave' => 'afterSave',
'Model.afterSaveCommit' => 'afterSaveCommit',
'Model.beforeDelete' => 'beforeDelete',
'Model.afterDelete' => 'afterDelete',
'Model.afterDeleteCommit' => 'afterDeleteCommit',
'Model.buildValidator' => 'buildValidator',
'Model.buildRules' => 'buildRules',
'Model.beforeRules' => 'beforeRules',
'Model.afterRules' => 'afterRules',
```
