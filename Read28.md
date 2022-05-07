# **Read28: RecyclerView for displaying lists of data**


## **Steps for implementing your RecyclerView**

* First of all, decide what the list or grid is going to look like. Ordinarily you'll be able to use one of the RecyclerView library's standard layout managers.

* Design how each element in the list is going to look and behave. Based on this design, extend the ViewHolder class. Your version of ViewHolder provides all the functionality for your list items. Your view holder is a wrapper around a View, and that view is managed by RecyclerView.

* Define the Adapter that associates your data with the ViewHolder views.


## How to plan your layout:

##### The RecyclerView library provides three layout managers, which handle the most common layout situations:
* LinearLayoutManager arranges the items in a one-dimensional list.
* GridLayoutManager arranges all items in a two-dimensional grid
* StaggeredGridLayoutManager is similar to GridLayoutManager, but it does not require that items in a row have the same height (for vertical grids) or items in the same column have the same width (for horizontal grids). The result is that the items in a row or column can end up offset from each other.


## How to implementing your adapter and view holder:
### **you need to override three key methods:**
* onCreateViewHolder()
* onBindViewHolder()
* getItemCount()



# **Explanation:**
![](https://i.stack.imgur.com/Okt2i.png)
