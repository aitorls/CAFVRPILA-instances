# CAFVRPILA-instances

In this repostory there are the benchmark instances to test the CAFVRPILA problem. 

## Dependecies

Works with Python 3.8+ and only depends on pandas and json.

## Example usage

To read the instances you must import pandas library for python and following the next procedure:


```python
import json 

instance_name = "Instance_4.json" 
instance_dir  = os.path.join(DIR_INSTANCES, instance_name)
with open(instance_dir, 'r') as f:
    instance_data = json.load(f)
```

The `instance` is compose of the set of tasks, depots, vehicles, implement and their compatibilities.

```python
>>> instance_data.keys()
['Operations', 'Vehicles', 'Implements', 'Tasks', 'Depots', 'Coords', 'Vehicle_autonomy', 'Vehicle_depot', 'Vehicle_cost', 'Implement_capacity', 'Implement_depot', 'Implement_cost', 'Task_Demands', 'Implements_per_operation', 'Implements_per_vehicle', 'Tasks_per_operation']
```


The `solution` of each `instance` is a json with the whole information about vehicle and implement routes.


```python
import json

solution_name = "Solutions_util_util/Instance_4.json.sol.json" # Capacity 100, Implement depots +DI, Vehicles 10, autonomy 1000, Depots +DV
solution_dir  = os.path.join(DIR_SOLUTIONS, solution_name)
with open(solution_dir, 'r') as f:
    solution_data = json.load(f)    
```


```python
>>> solution_data.keys()
['Vehicle_7', 'Vehicle_2', 'Vehicle_6', 'Vehicle_3', 'Vehicle_10', 'Vehicle_1', 'Vehicle_4', 'Vehicle_9', 'Vehicle_8', 'Vehicle_5', 'Implement_1', 'Implement_2', 'Implement_3', 'Implement_4', 'Implement_5', 'Implement_6', 'Implement_7', 'Implement_8', 'Implement_9', 'Implement_10', 'Implement_11', 'Implement_12', 'Implement_13', 'Implement_14', 'Implement_15', 'Implement_16', 'Implement_17', 'Implement_18', 'Implement_19', 'Implement_20', 'Implement_21', 'Implement_22', 'Implement_23', 'Implement_24', 'Implement_25', 'Implement_26', 'Implement_27', 'Implement_28', 'Implement_29', 'Implement_30', 'Implement_31', 'Implement_32', 'Implement_33', 'Implement_34', 'Implement_35', 'Implement_36', 'Implement_37', 'Implement_38', 'Implement_39', 'Implement_40', 'Implement_41', 'Implement_42', 'Implement_43', 'Implement_44', 'Implement_45', 'Implement_46', 'Implement_47', 'Implement_48', 'Implement_49', 'Implement_50']

>>> solution_data["Vehicle_4"]
['Depot_Vehicle_4', 'Depot_Implement_21', 'Task_169', 'Task_156', 'Task_161', 'Task_151', 'Task_192', 'Task_148', 'Depot_Implement_21', 'Depot_Vehicle_4']
```

