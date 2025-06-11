
# Opportunities for Improvement: Beyond KNN Classification

While the original project successfully leveraged a **K-Nearest Neighbors (KNN)** classifier to label pitch types with high accuracy (~97%), there are multiple areas where this approach can be expanded, refined, and made more interactive for exploratory and performance-focused use cases — especially in the context of my *PitchDNA* system. Below is a breakdown of actionable improvements and innovations.

---

## 1. Dimensionality Reduction with UMAP for Visualization & Insights

**Why?**  
Pitch data lives in a high-dimensional feature space (speed, spin, movement, etc.). While this is great for modeling, it makes **intuition and pattern recognition difficult**.

**Improvement:**
- Integrate **UMAP (Uniform Manifold Approximation and Projection)** to reduce pitch features into a **2D plane**, enabling clear visual mapping.
- Use this to:
  - Visually **cluster pitch types** (fastballs vs. sliders).
  - **Spot outliers** or ambiguous pitches.
  - Help players/coaches understand how a pitch compares to MLB norms.

---

## 2. Feature Engineering

**Why?**  
The model only uses a handful of raw statcast features. But pitch behavior is **complex and influenced by derived attributes.**

**Improvements:**
- Add features like:
  - **Spin efficiency**
  - **Release extension**
  - **Axis tilt or spin axis**
  - **Pitch tunneling metrics**
- Combine velocity + spin to estimate **movement efficiency** or deception.

Better features = more signal → better classification and similarity results.

---

## 3. Combine Classification with Similarity Search

**Why?**  
KNN is currently used just for classification. But my PitchDNA concept expands this into **pitch comparability**, which is a much more powerful, player-facing tool.

**How to Improve:**
- After predicting a pitch type, use **KNN or UMAP proximity** to find the **most similar existing pitches** in the MLB database.
- Return those along with statcast video or overlays (already on your roadmap).
- You can even highlight pitches that are outliers within their class — helping a player know if they throw a **"weird but effective"** slider.

---

## 4. Model Confidence and Interpretability

**Why?**  
A good model doesn’t just output labels — it explains its choices.

**Improvement:**
- Display **confidence levels or probability distributions** (e.g., “70% likely to be a cutter, 25% slider”).
- Use tools like **SHAP or LIME** to show what features drove the prediction — was it spin? break? velocity?

This empowers users to **trust and learn from the model.**

---

## 5. Predict or Suggest Ideal Pitch Archetypes

Long-term, you can extend the model to **recommend how a pitcher's pitch could evolve** (e.g., "Your slider is closest to [X], but adding 3 inches of horizontal break would make it closer to [MLB All-Star Y].").

This adds **training value and progression tracking**—a big selling point for minor leaguers and coaches.

---

## 🚀 Final Thoughts

The baseline KNN model offers a solid foundation, but the future of pitch analysis lies in **interpretability, interactivity, and insight**. My PitchDNA system is on the right path by combining visual tools, similarity engines, and player comparisons in a way that transforms raw pitch data into meaningful feedback.
