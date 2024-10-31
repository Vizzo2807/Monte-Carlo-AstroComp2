# Monte-Carlo-AstroComp2
This code simulates the creation and evolution of a stellar population. It generates star masses according to the Kroupa IMF, assigns birth times, and classifies each star as either on the main sequence or as a remnant (white dwarf, neutron star, or black hole) based on its mass and age. It calculates the fractions of each stellar type.

# Stellar Population Simulation

This project simulates the evolution and distribution of stellar masses for a range of star populations using the Kroupa Initial Mass Function (IMF). The code generates samples of stars with different masses, assigns birth times, and calculates final stellar remnants based on their masses and lifetimes.

## Project Structure

- **IMF Simulation**: Generates stellar masses following the Kroupa IMF, with sample sizes of 100, 1,000, 10,000, 100,000, and 1,000,000 stars.
- **Stellar Lifetimes and Remnants**: Calculates the time each star spends in the main sequence (MS) phase and classifies stars as main sequence, white dwarfs (WDs), neutron stars (NSs), or black holes (BHs).
- **Final Mass Calculation**: Determines final masses of stellar remnants based on initial-to-final mass relations (IFMR) for each type.
- **Distribution Visualization**: Produces histograms to visualize distributions of star masses and ages across different population sizes.

## Main Functions

1. `imf_kroupa(m)`: Computes the probability of a star having mass `m` based on the Kroupa IMF.
2. `generar_masas_por_imf(cantidad_estrellas, masa_min, masa_max)`: Generates stellar masses for a given number of stars, filtered by the IMF.
3. `calculate_tms(mass)`: Calculates the time a star of given mass will remain in the main sequence phase.
4. `classify_remnant(mass)`: Classifies a star as a White Dwarf, Neutron Star, or Black Hole based on its mass.
5. `process_stellar_data(masas, birth_times, num_estrellas)`: Processes data for each population to classify stars and calculate their ages and masses.
6. `neutron_star_mass(M_ZAMS)` and `black_hole_mass(M_ZAMS)`: Calculate the final masses for neutron stars and black holes based on the initial masses and specified conditions.

## Results

The project generates histograms and calculates the fractions of each stellar type for different sample sizes, comparing them with observed distributions in the Milky Way.

## Visualizations

- **Mass Distribution**: Histograms show the distribution of masses across different samples.
- **Age Distribution**: Histograms visualize the age distributions for each type of remnant.
- **Fraction Analysis**: The final fraction of each type (MS, WD, NS, BH) is compared for accuracy in modeling stellar populations.

## Requirements

The code is written in Python and requires the following libraries:
- `numpy`
- `matplotlib`

## Usage

1. Run the code to generate star populations, calculate final masses, and classify stellar remnants.
2. View histograms for mass and age distributions.
3. Analyze the resulting fractions of stellar types across population sizes.

## Keywords

- stars: formation
- stars: mass function
- stars: neutron
- stars: black holes
- stars: white dwarfs
- galaxy: stellar content
