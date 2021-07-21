Minimal reproduction for: https://github.com/pnpm/pnpm/issues/3609

```bash
# Build image
docker buildx build --load -t test-pnpm-postinstall -f apps/test-app/Dockerfile .
# Run and open shell inside container
docker run --rm -it --entrypoint sh test-pnpm-postinstall
# Now inside container
/monorepo/apps/test-app $ ls
# Only node_modules and package.json - no test.txt
```
