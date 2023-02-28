# Animancer-Unity
## How to use:
- Add the link below in manifest.json in folder Package ``for version 1.0.0``
```
"com.virtuesky.animancer": "https://github.com/VirtueSky/animancer-unity.git#1.0.0",
```

<details><summary>Template code</summary>
  
```
using Animancer;
using UnityEngine;

public class AnimController : MonoBehaviour
{
    public AnimancerComponent Animancer;
    public ClipTransition Walk;
    public ClipTransition Run;
    public ClipTransition Jump;
    public ClipTransition Dance;
  
  
    // Play anim walk
    public void PlayWalk()
    {
        if (!Animancer.IsPlaying(Walk))
        {
          var anim =  Animancer.Play(Walk);
          anim.Events.OnEnd = () =>
          {
                //Event when finish anim;
          };
        }
    }
  
  //play anim dance
    public void PlayDance()
    {
        if (!Animancer.IsPlaying(Dance))
        {
            Animancer.Play(Dance);
        }
    }
  
  // play anim run
    public void PlayRun()
    {
        if (!Animancer.IsPlaying(Run))
        {
           Animancer.Play(Run);
        }
    }
  
  //play anim jump
    public void PlayJump()
    {
        if (!Animancer.IsPlaying(Jump))
        {
             Animancer.Play(Jump);
        }
    }
}
```
  
</details>

- Now, you need to drag the corresponding animation to the inspector

![anim2](https://user-images.githubusercontent.com/56286032/218262858-5b74713e-ba61-4bec-84b6-d52d6fa6e907.png)

You can customize ``Fede Duration, Speed, Start Time and End Time`` of animation

## Note:
- Open ``scene Demo`` test (Drag Scene demo from folder Package/Animacer to Asset to Play)
- ([Document details](https://kybernetik.com.au/animancer/))

- (Package is attached at release)
