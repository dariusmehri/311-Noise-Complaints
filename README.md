# 311 Noise Complaints
Analyzing NYC 311 noise complaints is important as it provides a real-time, resident-driven signal of quality-of-life conditions across neighborhoods. Noise complaints often reflect underlying issues like overcrowding, nightlife concentration, poor building conditions, or recurring nuisance behavior, making them a valuable proxy for urban stress and livability. From an analytics perspective, this data can reveal spatial and temporal patterns—hotspots, repeat locations, and peak hours—that help agencies prioritize enforcement, allocate resources, and design targeted interventions. It also supports equity analysis by identifying communities disproportionately affected by persistent noise, ensuring that response efforts are both effective and fair.

This project leverages Python, generative AI, and 2025 311 and PLUTO datasets sourced from NYC Open Data to analyze noise complaint patterns. The analysis is conducted at the community district level, enabling consistent spatial comparisons across neighborhoods.

### Outliers

<img width="210" height="210" alt="image" src="https://github.com/user-attachments/assets/39d4d574-0822-4ba9-8c9c-846366ae18f8" align="right" />

Initial map analysis revealed a clear outlier in the in the Bronx (see image on the right). Further investigation showed that 46,736 loud music/party complaints were associated with a single address in the Wakefield, Williamsburg community district over the course of the year—an average of roughly 130 complaints per day. This level of concentration is highly unlikely to represent independent incidents and instead points to a reporting artifact. In NYC 311 data, it is not uncommon for a single location to generate extremely high volumes when one caller repeatedly submits complaints, often via a mobile device or app that may default or mis-geocode to a fixed address. To address this, the data was de-duplicated to reduce the influence of repeated submissions from the same source, ensuring that the analysis more accurately reflects true complaint patterns and avoids distortion in spatial hotspot results.

### Summary Statistics
#### Borough and Location Type

After the outliers were dropped, there were 356,694 noise complaints in 2025.

When adjusted for borough population, noise complaints are relatively evenly distributed across New York City, with Brooklyn accounting for 28%, followed by Manhattan at 26%, the Bronx at 23%, and Queens at 20%, while Staten Island represents just 3%. This distribution suggests that, on a per-capita basis, noise-related quality-of-life concerns are most pronounced in Brooklyn and Manhattan, likely reflecting higher density, nightlife activity, and mixed residential-commercial land use, whereas Staten Island remains comparatively less impacted.

Noise complaints are primarily concentrated in residential settings, with 54% originating from residential buildings or houses, followed by 31% from streets and sidewalks and 6% from stores or commercial locations. This distribution indicates that most noise issues are tied to everyday living environments and public spaces.

Noise complaints are predominantly submitted through digital channels, with 58% filed online and an additional 27% via mobile phones, while landline calls account for 16%. This distribution highlights a strong shift toward digital engagement with 311 services, suggesting that most residents prefer the convenience of online and mobile platforms over traditional phone-based reporting.

<img width="954" height="512" alt="image" src="https://github.com/user-attachments/assets/bf11eb39-583b-446a-9cb5-9b631b162979" />

#### Incident Hour

The temporal pattern of 311 noise complaints shows a clear nighttime concentration. More than half of all complaints (54%) occur between 8 PM and 2 AM, reflecting peak periods of social activity and residential disturbance. Complaints reach their lowest point at 6 AM, accounting for just 1.5% of the total, before steadily increasing throughout the day. Activity builds into the evening, ultimately peaking at 10 PM with 39,857 complaints, representing 11.2% of all calls. This pattern highlights a strong correlation between noise complaints and typical evening and late-night human activity.

<img width="927" height="571" alt="image" src="https://github.com/user-attachments/assets/c5c50049-5af4-431f-a732-9fe5f0be77f8" />





