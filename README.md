# Concert Ticket Booking System - Fitts' Law HCI Experiment

An interactive HCI experiment that applies **Fitts' Law** to a simulated concert ticket booking scenario. The system evaluates pointing performance under different target sizes and movement distances using a three-stage ticket-booking task.

---

## 1. Overview

Concert ticket sales often require users to complete multiple time-sensitive interactions. Small targets, long cursor movements, and rapid sequential actions may increase movement time and selection errors.

This project simulates a ticket-booking process:

> **Lock Ticket → Select Seat → Confirm Payment**

The experiment investigates how target difficulty affects users' movement time and pointing performance.

---

## 2. Experimental Design

### Task Flow

The experiment consists of three sequential stages:

| Stage  | Task            |
| ------ | --------------- |
| Step 1 | Lock Ticket     |
| Step 2 | Select Seat     |
| Step 3 | Confirm Payment |

Participants complete:

* **3 practice trials**
* **15 formal trials × 3 stages = 45 target acquisitions**

Practice data are excluded from the formal analysis.

### Target Conditions

The experiment uses pre-designed target configurations with different:

* Target sizes
* Target positions
* Movement distances

These configurations are designed to produce different levels of pointing difficulty.

---

## 3. Fitts' Law

The experiment uses the Shannon formulation:

$$
ID = \log_2\left(\frac{A}{W'} + 1\right)
$$

where:

* **ID** = Index of Difficulty
* **A** = Movement amplitude
* **W′** = Effective target width

Movement time is modeled using:

$$
MT = a + b(ID)
$$

For rectangular targets, an angle-of-approach correction is applied to estimate the effective target width. Circular targets use their diameter as the effective width.

---

## 4. Data Collection & Analysis

For each successful target acquisition, the system records information including:

* Movement Time (MT)
* Movement Amplitude (A)
* Effective Width (W′)
* Index of Difficulty (ID)
* Throughput
* Target geometry
* Misses

Missed clicks outside the active target are recorded as selection errors.

After the formal experiment, the system performs a linear regression between **ID and MT** and reports:

* Regression equation
* R²
* Performance metrics
* Step-level results

Throughput is calculated as:

$$
TP = \frac{ID}{MT_{sec}}
$$

Experimental data can also be exported as a CSV file for further analysis.

---

## 5. Target Preview

Before each trial, a dashed ghost preview indicates the upcoming target location.

This provides participants with advance visual information and allows them to prepare for the next pointing movement. The pre-cueing effect should be considered when interpreting the results.

---

## 6. Results

The results dashboard provides:

* Movement Time vs. ID regression plot
* R² value
* Throughput
* Error information
* Step-level performance
* CSV data export

---

## 7. Limitations

* The experiment simulates a high-pressure ticket-booking scenario but does **not** directly measure physiological stress.
* The ghost preview may influence visual preparation and pointing behavior.
* Target configurations are pre-designed rather than directly specifying exact ID values.
* Effective width is estimated geometrically rather than from empirical endpoint distributions.
* Results from a single experimental session should not be generalized to human pointing performance as a whole.

---

## 8. Getting Started

Clone the repository and open `index.html` in a modern web browser. No backend server is required.

```bash
git clone <your-repository-url>
cd <your-repository-folder>
```

Then open:

```text
index.html
```

---

## 9. Demo

* **Live Demo:** [https://cheeen712.github.io/HW1_Fitts-Law-HCI-Experiment/](https://cheeen712.github.io/HW1_Fitts-Law-HCI-Experiment/)

* **Video:** <貼上你錄製的操作影片連結，例如 YouTube 或 Google Drive>
