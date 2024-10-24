# pycols
A Python module for colorating console content
## Installation
### Using *pip*
You can install pycols via pip using
<li>in a commandline:</li><br/>

```
py -m pip install pycols
```
<br/>
<li>in a python script:</li><br/>

```python
import os
os.system('py -m pip install pycols')
```
## Usage
### Colorating content
<ol>
<li>Create a pycols.color object:

```python
import pycols
c = pycols.color()
```
This will initialize all three style elements pycols can alter: Style, Foreground and Background.</li>
<li>Given that you want to make a text e.g. red for an error, you can change this:

```python
print("An error occured")
```
easily to the following:
```python
code_red = c.col("RED")
print(code_red + "An error occured")
```
Here, the <code>color.col</code> search method is used.<br/>
There is also a search methods for background colors (<code>color.bcol</code>).<br/>
These two methods will automatically switch to searching for light colors with the <code>color.lcol</code> / <code>color.lbcol</code> methods,
when they detect a <code>"LIGHT_"</code> part in your color description.</li>
<li>Reset the coloring with one of the following:

```python
print(c.col("RESET"))
```
for resetting only the color of the foreground,
```python
print(c.bcol("RESET"))
```
for resetting only the color of the background,
```python
print(c.RESET)
```
for resetting only the current styling or finally
```python
print(c.RESET_ALL)
```
for resetting all of them.

</ol>

### Others
Use the following to get information about your release and the author of the module:
```python
pycols.about()
```
### More coming soon