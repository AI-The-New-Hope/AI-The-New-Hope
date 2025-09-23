# Project: Find the Pleiades Star Cluster in Gaia with Machine Learning

**Audience:** non-astronomy students with basic Python + data-science skills  
**Estimated time:** 6–8 hours (including reading, coding, plots, and write-up)

---

## 1. What you will do
1. **Query Gaia** (ESA’s all-sky survey) using the **Codex CLI** and retrieve astrometric data (RA, Dec, parallax, pmra, pmdec, photometry) in a region around the **Pleiades**.  
2. **Clean and standardize** key features.  
3. **Cluster** the data with a simple unsupervised algorithm (e.g., **DBSCAN**) to separate the cluster from field stars.  
4. **Visualize** the result before/after clustering.  
5. **Check the color–magnitude diagram (CMD)** to verify the cluster looks astrophysically reasonable.

---

## 2. Background
- **Gaia** provides precise measurements of stars:
  - `ra, dec` — sky position in degrees.  
  - `parallax` (mas) — related to distance: `distance [pc] ≈ 1000 / parallax [mas]`.  
  - `pmra, pmdec` (mas/yr) — proper motion (movement across the sky).  
  - `phot_g_mean_mag`, `bp_rp` — brightness and color.  

- **Open cluster (Pleiades):** a group of stars with **similar distance and motion** → they appear as a clump in parameter space.  
- **CMD (Color–Magnitude Diagram):** plot `bp_rp` vs. `phot_g_mean_mag` (with inverted y-axis). A real cluster shows a **main sequence curve**.

---

## 3. Deliverables
- A **Jupyter notebook** (or Python script) that:
  1. Queries Gaia data using Codex CLI.  
  2. Preprocesses and clusters the data.  
  3. Produces plots (before/after clustering, CMD).  

- **Three PNG figures**:
  1. Proper motion plane (before and after clustering).  
  2. Sky map (RA vs. Dec, cluster highlighted).  
  3. CMD of final cluster members.  

- A short **PDF report (≤3 pages)** answering the questions in Section 8.

---

## 4. Tools
- Python 3.10+, with **numpy, pandas, matplotlib, scikit-learn, astropy**.  
- **Codex CLI** for Gaia queries.  
- Jupyter Notebook or VS Code.

Install example:
```bash
pip install numpy pandas matplotlib scikit-learn astropy
