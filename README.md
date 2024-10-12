# How to Install KVM on Ubuntu

1. **Check if your CPU supports virtualization**:
   
   ```egrep -c '(vmx|svm)' /proc/cpuinfo```

3. **Check if KVM is working**:
   
   ```kvm-ok```

If the command kvm-ok is not found, you can install it using the following command:

   ```sudo apt install cpu-checker```


3. **Install necessary packages**:


   ```sudo apt install bridge-utils libvirt-clients libvirt-daemon-system qemu qemu-kvm```

4. **Start the Libvirt daemon**:


   ```sudo systemctl start libvirtd```

5. **Enable Libvirt to start on boot**:

 
   ```sudo systemctl enable libvirtd```

6. **Launch Virt-Manager**:
 

   ```virt-manager```

If Virt-Manager is not installed, you can install it using the following command:


   ```sudo apt install virt-manager```

if internet problem in VM use following command:


   ```sudo virt-manager```



# How to Remove KVM from linux Ubuntu

1. **Remove Virt-Manager and related packages**:


   ```sudo apt remove --purge virt-manager libvirt-daemon-system libvirt-clients qemu```

2. **Remove unused packages**:


    ```sudo apt autoremove```

3. **Purge configuration files**:


    ```sudo apt purge virt-manager libvirt-daemon-system libvirt-clients qemu```

4. **Clean up package cache**:


   ```sudo apt clean```
