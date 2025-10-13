## Let's test alternative physical situations!

This lesson will allow you to collaborate with your fellow students to create a simulated physics experiment, but with different physical laws compared to what we know.

You are tasked with breaking up into groups, creating a group repository, and picking some physics experiment.

Within each group, one team will change the laws of physics (slightly, please!) and generate simulated data.

The other team will then prepare code to analyze this simulated data and try to figure out what was changed.

The change to physical laws may be something minor (e.g. a perturbation), or something more extreme (e.g. misunderstood physics).


### Example

Let's say group 1 has 4 students. They decide to modify gravity and study it by observing orbital periods around some object.

You could change the force of gravity to include another term:
    F_{g} = \frac{G m_{1} m_{2}}{r^{2}} -> G m_{1} m_{2} \left( r^{-2} + A r^{-3} \right)

This is one of the few times I will say you don't need to really worry about units, but in my example, A has units length.

Some group members will work on coding the experiment.
Split it up into multiple functions and define some workflow to run through each stage.

These functions could be:
    def new_gravity(m1, m2):
        code that computes equation above
        return F_{g}
    def measure_distance(accuracy=0.05):
        code that gives scatter to the true value
        return measurement
    def estimate_mass_object(accuracy=0.05):
        as above, can simulate looking up mass from different sources
        return mass_planet
    def measure_orbital_period(n_cycles, uncertanty=5):
        as above, but only add error to the start / stop times of ~5
        return orbit

    def simulate_measurements(number_students=25, **kwargs):
        measurements = []
        for student in range(number_students):
            code to compute measured value of gravity

        return measurements


The other members will focus on analyzing the output of the experiment.
Treat masses as known.

These could be:

    def plot_my_data(measurements):
        plotting code
        pass

    def fit_polynomial(measurements, polynomial_order=3):
        code which computes best fit via chi-squared
        return coefficients

    def convert_coefficients_to_physical_params(coefficients):
        code which uses known values such as mass to learn what A is
        alternatively, you can use this to check G
        return physical_values

    def find_uncertainties(measurements):
        code which computes error of our estimates
        return uncertainties


    
        
        
        
        



        
