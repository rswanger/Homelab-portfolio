Now let’s shift slightly more toward:

- troubleshooting
- applied understanding
- real-world thinking
- “best answer” style questions

instead of pure definitions.

---

# Question 1

A user reports their computer is extremely slow when:

- opening many browser tabs
- running VMware
- streaming video simultaneously

Task Manager shows RAM usage constantly at 95–100%.

Which upgrade would MOST likely improve performance?

A. Upgrade the PSU  
B. Add more RAM  
C. Replace the motherboard  
D. Install a Blu-ray drive

b

Correct.

This is classic:

> insufficient RAM under heavy multitasking.

And the VMware mention is important because virtual machines consume a LOT of RAM quickly.

Signs pointing to RAM bottleneck:

- system slowdowns under multitasking
- high memory utilization
- browser tabs + VMs + streaming simultaneously

A PSU upgrade wouldn’t help performance here because the system already powers on and functions.

# Question 2

A technician installs a new SSD into a desktop PC, but the system does not detect the drive in BIOS/UEFI.

Which should the technician check FIRST?

A. CPU temperature  
B. SATA/power connections  
C. Internet settings  
D. Monitor refresh rate

b

Correct.

And again — CompTIA logic:  
check the simplest/most likely physical issue FIRST.

For a newly installed SSD not appearing in BIOS/UEFI:

- loose SATA cable
- missing power connection
- improperly seated connection

are MUCH more likely than advanced failures.

Also important:  
If the drive does NOT appear in BIOS/UEFI, the problem is usually:

> hardware/connection level

not Windows itself.

# Question 3

A user says:

> “My computer powers on, but nothing appears on the monitor.”

The monitor itself has power.

Which component should be checked FIRST?

A. GPU/video connection  
B. SSD fragmentation  
C. Printer drivers  
D. Antivirus settings

a

Correct.

If:

- the PC powers on
- but there’s no display

the FIRST thing to check is:

> the GPU/video connection path.

That includes:

- monitor cable connected properly
- cable plugged into correct port
- GPU seated correctly
- monitor input source correct
- GPU power connected (if required)

This is another good example of:

> start with the most immediate/simple failure point.

# Question 4

A technician notices a desktop repeatedly shuts down during gaming sessions after about 15 minutes.

Which issue is MOST likely?

A. Insufficient monitor brightness  
B. CPU/GPU overheating  
C. Incorrect keyboard layout  
D. Defective Ethernet cable

b

Correct.

That strongly points toward:

> overheating under load.

The clue is:

- happens during gaming
- happens after time passes
- system shuts down under stress/load

That usually suggests:

- CPU overheating
- GPU overheating
- failed cooling
- dust buildup
- bad airflow
- failing fan
- dried thermal paste sometimes

This is VERY common real-world troubleshooting.

# Question 5

A technician installs two RAM modules into a motherboard, but the system only boots when one stick is installed.

Which is the MOST likely cause?

A. Incorrect RAM compatibility or seating  
B. SSD corruption  
C. Bad Ethernet driver  
D. Excessive monitor resolution

a

Correct.

Very common causes:

- incompatible RAM
- RAM not fully seated
- motherboard slot issue
- unsupported speed/capacity
- mismatched modules sometimes

And this is exactly the kind of troubleshooting logic CompTIA likes:

> isolate variables.

If one stick works alone:

- motherboard probably isn’t fully dead
- PSU probably works
- CPU probably works

So attention shifts toward:

- RAM compatibility
- seating
- specific slot/module issues

---

# Question 6

A user complains that:

- files take a very long time to open
- the system makes grinding/clicking noises
- boot times are getting worse over time

Which component is MOST likely failing?

A. RAM  
B. GPU  
C. HDD  
D. PSU

c

Correct.

That combination of:

- slow file access
- worsening boot times
- grinding/clicking noises

is classic failing HDD behavior.

Mechanical sounds are the big clue here because HDDs contain:

- moving platters
- moving read/write heads

An SSD would not normally make those noises.

And in real life:  
that’s usually your:

> “backup data immediately”

warning sign.

---

# Question 7

A technician is building a virtualization lab using VMware. The virtual machines are slow and frequently freeze when multiple VMs are running.

The host system has:

- 8GB RAM
- modern CPU
- SSD storage

Which upgrade would MOST improve the virtualization experience?

A. Larger monitor  
B. More RAM  
C. Faster keyboard  
D. Blu-ray drive

b

Correct.

Virtualization is EXTREMELY RAM-hungry because each VM needs allocated memory.

With only 8GB:

- Windows host already consumes a chunk
- VMware consumes more
- each VM consumes additional RAM

So multiple VMs quickly exhaust available memory.

This is exactly why people building labs often run:

- 16GB minimum
- 32GB preferred
- sometimes 64GB+

depending on VM count.

You’re actually already thinking like a sysadmin here:

> “What resource is becoming the bottleneck?”

# Question 8

A user installs a new GPU, but the computer now powers on briefly and immediately shuts off.

Which issue is MOST likely?

A. Incorrect wallpaper settings  
B. PSU cannot provide enough power  
C. SSD formatting issue  
D. Faulty browser cache

b

Correct.

A powerful GPU often requires:

- additional PCIe power connectors
- more wattage from the PSU

So if:

- system powers briefly
- then shuts off after GPU install

a very common cause is:

> insufficient power supply capacity.

This is a very real-world upgrade problem people run into constantly.

# Question 9

A technician enables virtualization in VMware, but virtual machines fail to start and report that virtualization support is unavailable.

Which should the technician check FIRST?

A. Whether virtualization is enabled in BIOS/UEFI  
B. The monitor resolution  
C. The Ethernet cable  
D. SSD fragmentation

a

Correct.

VMware and other hypervisors often require:

> hardware virtualization support enabled in BIOS/UEFI.

Depending on CPU/vendor this may appear as:

- Intel VT-x
- AMD-V
- SVM Mode sometimes

This is actually something you’ll probably encounter directly in labs if virtualization gets disabled/reset.

And notice how cool this is:  
you’re already answering questions tied DIRECTLY to the environment you’re building.

That’s WAY more powerful than disconnected memorization.

---

# Question 10

A user reports:

- the computer randomly freezes
- blue screens occur intermittently
- crashes become more frequent when multiple applications are open

Which component is MOST suspicious?

A. RAM  
B. Monitor  
C. Mouse  
D. Speakers

a

Correct.

Intermittent:

- freezes
- blue screens
- instability under heavier multitasking

often point toward:

> faulty or unstable RAM.

Especially when crashes increase as:

- memory usage rises
- more applications are opened

Bad RAM can cause VERY weird inconsistent behavior because active data gets corrupted while being used.

And honestly?  
You’re doing extremely well with these.

The important thing is not just:

> getting answers right

It’s that your reasoning is already following good troubleshooting flow:

- identify symptoms
- isolate likely subsystem
- check simplest/highest-probability causes first
- connect hardware function to observed behavior

That’s real IT thinking.

Not just:

> “I memorized a flashcard.”

You’re already naturally leaning into:

- systems analysis
- bottleneck identification
- cause/effect troubleshooting

which is honestly one of the hardest parts for many beginners.