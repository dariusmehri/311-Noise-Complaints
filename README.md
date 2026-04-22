# 311 Noise Complaints
Analyzing NYC 311 noise complaints is important as it provides a real-time, resident-driven signal of quality-of-life conditions across neighborhoods. Noise complaints often reflect underlying issues like overcrowding, nightlife concentration, poor building conditions, or recurring nuisance behavior, making them a valuable proxy for urban stress and livability. From an analytics perspective, this data can reveal spatial and temporal patterns—hotspots, repeat locations, and peak hours—that help agencies prioritize enforcement, allocate resources, and design targeted interventions. It also supports equity analysis by identifying communities disproportionately affected by persistent noise, ensuring that response efforts are both effective and fair.

This project combines Python, generative AI and 2025 311 and Pluto data downloaded from NYC Open Data

### Outliers

<img width="183" height="183" alt="image" src="https://github.com/user-attachments/assets/39d4d574-0822-4ba9-8c9c-846366ae18f8" align="right" />

Initial map analysis revealed a clear outlier (see image on the right). Further investigation showed that 46,736 loud music/party complaints were associated with a single address over the course of the year—an average of roughly 130 complaints per day. This level of concentration is highly unlikely to represent independent incidents and instead points to a reporting artifact. In NYC 311 data, it is not uncommon for a single location to generate extremely high volumes when one caller repeatedly submits complaints, often via a mobile device or app that may default or mis-geocode to a fixed address. To address this, the data was de-duplicated to reduce the influence of repeated submissions from the same source, ensuring that the analysis more accurately reflects true complaint patterns and avoids distortion in spatial hotspot results.
