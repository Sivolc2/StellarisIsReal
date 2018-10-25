# StellarisIsReal
Awesome stuff with SpaceApps!
Overview of project, direction, requirements, and workloads:

The goal is to understand and use the air quality map of the USA and correlate with asthma cases. (additional diseases later)
Using machine learning classification algorithms, we can make predictions about future asthma rates in 2020-2030 (Potentially also used to make predictions in other countries).
This data will be displayed on a website for anyone who is curious, where we show our process and a slider, to show changes over time.

Process:

Data
	On CO2, Ozone, metal-based polutants in PPM
	CDC pollutants by state (and region possibly)

Processing
	k-nearest neighbours predictor for correlations between 

Visualization
	Shaded graphs of states by color and gradient
	Website interface for displaying graphs across timesteps 

------Tasks:
	Process data on CO2, Ozone, (metal-based pollutants if time allows)
		Download data
		Convert into pandas dataframe (ideally)
		Cut data into squares of equal area. 
			Average values across the square
		Store as single dataframe
			Labelled by pollutant
			Labelled by long/lat coordinates
				(can be center or edges depending on preference)
	
------Build ML model
		I'm not going to write all the steps but it's essentially
		Implement k-means algo using just data from state air quality and lung ailment rates
		Try it again with our awesome data
			Tons of troubleshooting
			Rewrite the algo, mash it up with some decision tree analysis
		Take output as set of confidence intervals around each region versus lung cancer rates
		Build a statistical likelihood for getting xyz lung problem
		Repeat over time!
		Build a time dependent signal processing CNN
			Predict based on growth rates given by UN/USA census based on population
		Apply to other countries!
------Visualiation
		Take dataframe with results and graph them
			Use Tableau to build time dependent visualizations
		Make a website
			Simple buttons for interface
		Upload to website and build update pipeline
		Think up cool ways to visualize the data better. 3D? 4D?
		
