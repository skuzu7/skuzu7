<div align="center">

<img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=700&size=28&pause=100&color=FF0000&background=000000&center=true&vCenter=true&width=435&lines=FATAL_ERROR:_SEGFAULT;CVE-2025-XXXX_DETECTED;MEMORY_CORRUPTION;REMOTE_CODE_EXECUTION" />

<br>

<a href="https://linkedin.com/in/SEU_USUARIO"><img src="https://img.shields.io/badge/EXPLOIT-LINKEDIN-000000?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
<a href="https://app.hackthebox.com/profile/SEU_ID"><img src="https://img.shields.io/badge/POC-HACKTHEBOX-000000?style=for-the-badge&logo=hack-the-box&logoColor=red"/></a>

</div>

### 🩸 `poc_exploit.c`

```c
#include <stdio.h>
#include <stdlib.h>

// TARGET:   Google Cloud Platform & K8s Infrastructure
// IMPACT:   Critical (Score: 10.0)
// STATUS:   Unpatched / In the Wild

void get_shell() {
    char *args[] = {"/bin/sh", NULL};
    execve(args[0], args, NULL);
}

int main() {
    printf("[!] Triggering Heap Overflow...\n");
    printf("[+] EIP Overwritten. Jumping to shellcode...\n");
    
    // Injecting malicious logic into business logic
    void (*payload)() = (void (*)()) &get_shell;
    payload();
    
    return 0; // Never reached
}
