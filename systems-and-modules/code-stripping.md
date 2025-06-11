---
icon: qq
---

# Code stripping

Code stripping allows for server code to be automatically removed from client builds. This allows for an added layer of safety to your Server-Client games. And it's all handled for you by PurrNet.

It will automatically strip all server specific code from all builds but Server builds. You can find the setting in Project Settings -> Networking -> PurrNet -> Strip Server Code, and simply toggle the bool.

<figure><img src="../.gitbook/assets/image (35).png" alt=""><figcaption></figcaption></figure>

You also have `ServerOnly` attribute at your disposal to strip and ensure methods are only ever executed by server.

```csharp
public class TestingClass
{
    [ServerOnly(StripCodeModeOverride.ReplaceWithLogError)]
    public void Testy()
    {
        Debug.Log("Testy called!");
    }
}
```
