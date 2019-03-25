# Test
Wikipedia page

An Interrupt Request Level (IRQL) is a hardware independent means with which Windows prioritizes interrupts that come from the system's processors. On processor architectures which Windows runs on, hardware generates signals which are sent to an interrupt controller. The interrupt controller sends an interrupt request (or IRQ) to the CPU with a certain priority level, and the CPU sets a mask which causes any other interrupts with a lower priority to be put into a pending state, until the CPU releases control back to the interrupt controller. If a signal comes in at a higher priority, then the current interrupt will be put into a pending state, the CPU sets the interrupt mask to the priority and places any interrupts with a lower priority into a pending state until the CPU finishes handling the new, higher priority interrupt.[1]

Windows maps not only hardware interrupt levels to its internal interrupt table, but also maps software interrupts. The mappings in this table are called Interrupt Request Levels, or IRQLs, and a separate IRQL is kept for each processor in a multiprocessor system. The IRQL values are specific to the x86, IA64 and AMD64 processor architectures that Windows can run on, though theoretically they can support other CPUs that use a similar interrupt scheme (such as the DEC Alpha and MIPS, which were supported briefly on early versions of Windows). What this essentially means is that APCs (Asynchronous procedure calls), user threads and kernel mode operations can be interrupted and the system must run them at an IRQL lower than the thread scheduler (or "dispatcher").[2] 

https://en.wikipedia.org/wiki/IRQL_(Windows)
А на русском можно - ничего же не понятно
