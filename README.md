Very simple wrapper which simulate proper vector2/3 array in zscript.

## HOW TO USE IT?
Copy "thirdparty" folder into you mod folder, copy content of "zscript.zc" file into your mod zscript root file (optionally delete version nmumber if you already use one) and thats it.

Now you can initizalize vector2/3 array by using

```Vector2/3Array <name>;```

All functions which works for native arrays also woroks for wrapper in the same way and under the same name.
Only difference, it now have ``Get(index)`` method. It return vector from the array at specified index, since you dont have a direct access to array components, security reasons. So to iterate through vectors you should use
```csharp
Vector3Array example;
example.push(some vectors);
for(uint i = 0; i < example.size(); i++)
{
    vector3 vec = example.get(i);//<-- this will get you vector
    //now do something with it
}
```

To replace vector at specific index use ```Insert(index, vector)``` method.