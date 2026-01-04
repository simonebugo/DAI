# 🗳️ Electoral Dynamics & Polarization 

An multi agent system developed in **NetLogo** to simulate how social influence, memory decay, and political fragmentation affect voter turnout and polarization.

## 📌 Project Overview

This project investigates the dynamics of opinion formation and voting behavior. The simulation explores a critical question: **How do individual memory (decay) and social bubbles (interaction radius) influence the outcome of democratic elections?**

The model simulates a population of agents ("turtles") who:
1.  Hold beliefs about various political parties.
2.  Influence each other through local interactions.
3.  Forget their convictions over time (Decay).
4.  Decide to vote only if their conviction exceeds a specific threshold.

## ⚙️ How It Works

### The Agents
Each agent has a set of `beliefs` (scores for each party). At every step (day):
* **Interaction:** Agents meet others within an `interaction-radius` and influence each other's beliefs.
* **Decay:** Beliefs decrease over time based on the `decay-factor`.
* **Affiliation:** If the belief for a party crosses a `threshold`, the agent joins that party. If it drops, they become neutral (abstentionist).

### Key Parameters
| Parameter | Description |
| :--- | :--- |
| `num-parties` | Number of competing parties (e.g., 2, 4, 6). |
| `decay-factor` | How fast opinions fade (0.5 = fast forgetting, 0.95 = strong memory). |
| `interaction-radius` | The size of the agent's interaction range. |
| `population` | Total number of voters in the simulation. |

## 📊 Key Findings

Analysis performed on **1,600+ simulations** performed with the behaviourspace tool of netlogo using Python (Pandas/Seaborn) revealed:

1.  **Memory is Crucial for Democracy:** There is a direct correlation between the `decay-factor` and turnout. If agents "forget" too fast (Decay < 0.6), turnout collapses to near zero.
2.  **The Two-Party Trap:** Systems with only 2 parties show extreme polarization (high variance) and "Winner-takes-all" outcomes. Multi-party systems (6 parties) distribute votes more evenly, reducing polarization.
3.  **Social Radius Impact:** Surprisingly, expanding the social radius does not significantly reduce the gap between the winner and the runner-up; the party system structure matters more than individual connectivity.


