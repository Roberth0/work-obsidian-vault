- Monitor mode 
```bash
sudo ip link set wlp4s0 down
sudo iw wlp4s0 set monitor none
sudo ip link set wlp4s0 up
```

- Managed Mode
```bash
sudo ip link set wlp4s0 down
sudo iw wlp4s0 set type managed
sudo ip link set wlp4s0 up
```

