# Volatile RAM Buffer Simulator Engine 💾

A low-latency virtual memory allocation and buffer management simulator built in native JavaScript. This repository demonstrates dynamic memory block addressing, fragmentation calculation loops, and real-time volatile stack visualization with zero processing lag.

## 🗂️ Architectural Overview

The simulation environment acts as a deterministic memory controller, capturing memory write/read operations, validating block boundaries, and processing memory deallocation algorithms through a modular state-update engine.

### ⚙️ Core Technical Features:
* **Volatile Stack Virtualization:** Simulates memory block distribution and addressing metrics instantly via isolated execution loops.
* **Overflow Boundary Protection:** Enforces strict limits to emulate hardware system leaks or memory corruption vectors.
* **Zero External Dependencies:** Built strictly with vanilla JavaScript, CSS, and HTML for direct hardware thread alignment.

## 🚀 Deployment Instructions

To run the RAM simulator engine locally or host it on any web environment:
1. Clone this repository to your local storage.
2. Ensure `index.html`, `style.css`, and `script.js` are in the same directory.
3. Open `index.html` in any standard modern web browser (Chrome, Brave, Edge).

*Developed for operating system memory analysis and core buffer logic prototyping.*

```mermaid
graph TD
    %% Estilo de nodos neón
    classDef safe color:#00ff66,fill:#000,stroke:#00ff66,stroke-width:2px;
    classDef alert color:#ff0033,fill:#000,stroke:#ff0033,stroke-width:2px;
    classDef process color:#00ffff,fill:#000,stroke:#00ffff,stroke-width:1px;

    Start([⚡ RAM Simulator Init]) --> Load[🚀 DOM Memory Matrix Rendered]
    Load --> Active[📡 Attached Operation Listeners Allocation/Deallocation]
    
    Active --> Wait{⌨️ Waiting for Memory Directive}
    
    Wait -- NO --> Wait
    Wait -- SÍ --> Capture[📥 Capture Address Size & Data Blocks]
    
    Capture --> Check{🔬 Inspect Memory Threshold Limits}
    
    Check -- Buffer Overflow --> Err[🚨 Trigger Memory Allocation Exception]:::alert
    Check -- Safe Bounds --> Route{🔀 Operation Router Switch-Case}
    
    Route -- Action: Allocate --> Alloc[⚙️ Assign Blocks & Update Allocation Table]:::process
    Route -- Action: Clear --> Free[⚙️ Run Garbage Collector Inversion Loop]:::process
    
    Err --> Output[🖥️ Flush Hardware Log Stream to Virtual Terminal]
    Alloc --> Output
    Free --> Output
    
    Output --> Return[🔄 Re-index Fragmented Spaces & Refresh UI Matrix]
    Return --> Wait

    class Start,Load,Active,Wait safe;
    class Capture,Check,Route,Alloc,Free,Output,Return process;
```
