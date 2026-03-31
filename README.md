config.vm.box → використовує Ubuntu 22.04 (ubuntu/jammy64)

network → задає IP 192.168.100.100

provider virtualbox → виділяє:
2 CPU
4096 MB RAM

provision shell → встановлює Java 17

trigger.after up → автоматично запускає Spring Boot додаток
