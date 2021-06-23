# android_kernel_docker

- A repository that contains a kconfig to enable docker support in android kernels

# usage

- If you are using SLMK, you don't need these configs

> CONFIG_MEMCG 

> CONFIG_MEMCG_SWAP

- You can add this to your tree by doing this command

```bash
git subtree add --prefix=docker https://github.com/cyberknight777/android_kernel_docker main
```

- Then go to arch/yourtargetarchitecture/Kconfig and add this line below:

> source "docker/Kconfig"

- Next you would need to enable all the options in Utilities except for this one(if you use SLMK): 

> CONFIG_DOCKER_SWAP

- Once that's done feel free to compile and use your kernel which has docker enabled now :)

## Tested on Kernels 4.14, 4.4, and 4.9

# Credits

- grilix for his base docker kconfig. 
https://github.com/grilix/kernel-docker-support
