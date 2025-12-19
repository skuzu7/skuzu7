<div align="center">

<img src="https://readme-typing-svg.herokuapp.com?font=Courier+Prime&weight=400&size=25&pause=1000&color=808080&background=000000&center=true&vCenter=true&width=435&lines=ENTROPY_INCREASING...;CONTROL_IS_AN_ILLUSION;I_AM_THE_GLITCH;SYSTEM_HALTED" />

<br>

<a href="https://linkedin.com/in/SEU_USUARIO"><img src="https://img.shields.io/badge/LINKEDIN-VOID-000000?style=for-the-badge&logo=linkedin&logoColor=555"/></a>
<a href="https://app.hackthebox.com/profile/SEU_ID"><img src="https://img.shields.io/badge/HTB-ROOT-000000?style=for-the-badge&logo=hack-the-box&logoColor=555"/></a>

</div>

```c
// memory_dump.c

void* reality = NULL;

struct Operator {
    char* archetype;
    char* philosophy;
    void* target;
};

int main() {
    struct Operator me;
    
    me.archetype  = "Red Team // Phantom";
    me.philosophy = "Security is just a delay, not a barrier.";
    me.target     = 0xDEADBEEF; // GCP_K8s_Infrastructure

    // While the blue team sleeps, we traverse the graph.
    while(1) {
        escalate_privileges();
        remain_unseen();
    }
}
