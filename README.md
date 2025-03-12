# partageIntraAttaque
```BASH
function findTopParent(units: Unite[], targetId: string): Unite | undefined {
  let topParent: Unite | undefined;

  function findParent(unit: Unite) {
    if (unit.uniteEnfant) {
      for (const child of unit.uniteEnfant) {
        if (child.id === targetId || findParent(child)) {
          topParent = unit;
          return true;
        }
      }
    }
    return false;
  }

  for (const unit of units) {
    if (findParent(unit)) {
      break;
    }
  }

  return topParent;
}
```
