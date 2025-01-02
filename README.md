# vitepress-components

This repository is a collection of custom VitePress components that can be shared across multiple VitePress sites. It currently exists solely for my personal use, but I am open to suggestions and improvements. In the future, I may create an NPM package for these components.

If you would like to use these components in your own VitePress site, you can add this repository as a submodule. Please note that this repository is a work in progress and may change frequently. Similarly, you can use this repository as a template for your own shared components.

Everything in this repository will be copied to the `docs/.vitepress/theme/components/cynber-shared` directory of a VitePress site. As such, it should contain only the components you want to share across multiple VitePress sites.
   
Overview:
```
/vitepress-components
    /components
    - Component1.vue
    - Component2.vue
    ...
```

## Add the Submodule to an existing VitePress Site

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

### Updating the GitHub Pages deploy script

If you are using GitHub Pages to deploy your VitePress site, you will need to update the deploy script:

Add `with: submodules: recursive` to the checkout step:
``` yaml
# ...
    steps:
      - name: Checkout
        uses: actions/checkout@v4
        with:
          submodules: recursive
# ...
```

Add a step to initialize and update the submodules:
``` yaml
# ...
      - name: Initialize and update submodules
        run: |
          git submodule update --init --recursive
# ...
```

## Clone a VitePress Site with Submodules

When cloning a VitePress site that includes submodules, remember to initialize them:

```
git clone --recurse-submodules <repo-url>
```

If you forgot to initialize the submodules when cloning, you can do so after cloning:

```
git submodule update --init --recursive
```

## Update the Submodule to the Latest Version

```bash
git submodule update --remote
```


