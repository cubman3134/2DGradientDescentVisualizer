import numpy as np
import matplotlib.pyplot as plt

def func_y(x):
    y = 50 * np.sin(x) + (x ** 2)
    return y

cur_x = 7
rate = 0.1
precision = 0.000001
previous_step_size = 1
max_iters = 1000
iters = 0
df = lambda x: 50*np.cos(x)+2*x

x = np.arange(-10, 10, 0.01)
y = func_y(x)
init = cur_x
fig, ax = plt.subplots()
plt.plot(x, y, lw = 0.9, color = 'k')
ax.set_xlim([min(x), max(x)])
ax.set_xlabel(r'$x$')
ax.set_ylabel(r'$y$')

while previous_step_size > precision and iters < max_iters:
    prev_x = cur_x
    cur_x = cur_x - rate * df(prev_x)
    previous_step_size = abs(cur_x - prev_x)
    iters = iters + 1
    plt.scatter(cur_x, func_y(cur_x), s=20)
    print("Iteration", iters, "\nX value is", cur_x)
plt.legend(["Step Size = " + str(rate)])
plt.savefig("x" + str(init) + "r" + str(rate) + "gradiant.png")
