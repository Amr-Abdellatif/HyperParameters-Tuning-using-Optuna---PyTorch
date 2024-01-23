1. Intro : A simple optimization problem:

   1. Define `objective` function to be optimized. Let's minimize `(x - 2)^2`
   2. Suggest hyperparameter values using `trial` object. Here, a float value of `x` is suggested from `-10` to `10`
   3. Create a `study` object and invoke the `optimize` method over 100 trials

2. Example 101 :

   1. ````import optuna
      def objective(trial):
          x = trial.suggest_float('x', -10, 10)
          return (x - 2) ** 2
         
      study = optuna.create_study()
      study.optimize(objective, n_trials=100)
      study.best_params  # E.g. {'x': 2.002108042}```
      you see the eqn. is (x-2)**2 -> x should be 2
      ````

3. Lets talk about general steps :
   1. Define an objective function to be maximized or Minimized.
   2. Suggest values of the hyperparameters using a trial object.
   3. Create a study object and optimize the objective function.
   4. Optimize the study (objective function , Trials)
   5. Get the pruned and complete trials inside variables
   6. print the best trial
4. In this repo i setup a basic Optuna hyper-parameter object for PyTorch basic model applied to MNIST dataset
