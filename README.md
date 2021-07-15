# OpenAIPendulum
State of the pendulum = [Angular position, Angular velocity]

Action space is a discrete set of size 3, [-1, 0, 1]. Apply continuous acceleration clockwise, counter clockwise and do nothing.
We use a softmax policy for this as the action space is discrete.

The reward = the angular distance of the pendulum from the top most position

Since this is a low dimentional state space (2 dimentions) and the range of this spcae is also limited, Tile coding works well here.

Also a systematic sweep ensures that we get optimal values for the step sizes for the actor and the critic.
