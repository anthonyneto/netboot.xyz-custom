## netboot.xyz-custom

### testing
```
docker run -it --rm \
  --name ipxe-test \
  --net=host \
  --privileged \
  -v /etc/qemu/bridge.conf:/etc/qemu/bridge.conf \
  anthonyneto/qemu \
  qemu-system-x86_64 \
  -nodefaults \
  -boot order=n \
  -smp 2 \
  -m 4096 \
  -serial stdio \
  -net nic,model=virtio \
  -net bridge,br=br0 \
  -nographic
```
