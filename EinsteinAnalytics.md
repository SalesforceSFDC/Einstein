* Salesforce data is normalized, which means that related data in different objects is “joined” together.
* denormalized, meaning that some of the preprocessing work is already done.
* Analytics datasets compress and index their contents, so querying is super fast.

## Dataflow
Use the dataflow to extract data from Salesforce objects. The dataflow is a set of instructions in JavaScript Object Notation (JSON) that runs to extract data and create datasets. These instructions specify which objects and fields you want to extract data from and the names of the datasets you want to create. The dataflow also has other uses, such as joining data together, but for now we just focus on its extraction skills.

## Dataset Builder
dataset builder generates the JSON instructions needed to build a dataset and adds the instructions to your dataflow. The dataflow then does the actual building.
