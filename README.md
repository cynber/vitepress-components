# vitepress-components
 Various custom vitepress components

This repository is a collection of custom VitePress components that can be shared across multiple VitePress sites.

Everything in this repository will be copied to the `docs/.vitepress/theme/components/cynber-shared` directory of a VitePress site. As such, it should contain only the components you want to share across multiple VitePress sites.
   
Overview:
```
/vitepress-components
    /components
    - Component1.vue
    - Component2.vue
    ...
```

## Adding the Submodule to a VitePress Site

1. **Navigate to Your VitePress Site Directory**:

2. **Add the Submodule**:

```
git submodule add https://github.com/cynber/vitepress-components.git docs/.vitepress/theme/cynber-shared
```

3. **Initialize and Update the Submodule**:

```
git submodule update --init --recursive
```

4. **Commit the Changes**


## Using and Updating Submodules

**Cloning a new project**:

When cloning a VitePress site that includes submodules, remember to initialize them:

```
git clone --recurse-submodules <repo-url>
```

If you forgot to initialize the submodules when cloning, you can do so after cloning:

```
git submodule update --init --recursive
```

**After Cloning**:

```bash
git submodule update --remote docs/.vitepress/theme/components/cynber-shared
```
