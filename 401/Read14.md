# Matplotlib

- Matplotlib is probably the single most used Python package for 2D-graphics. It provides both a very quick way to visualize data from Python and publication-quality figures in many formats

### IPython and the pylab mode

- IPython is an enhanced interactive Python shell that has lots of interesting features including named inputs and outputs, access to shell commands, improved debugging and much more

### pyplot

- Pyplot provides a convenient interface to the matplotlib object-oriented plotting library. It is modeled closely after Matlab(TM).

## Simple plot

The first step is to get the data for the sine and cosine functions:

        ```
        import numpy as np

        X = np.linspace(-np.pi, np.pi, 256, endpoint=True)
        C, S = np.cos(X), np.sin(X)
        ```

X is now a NumPy array with 256 values ranging from -π to +π (included). C is the cosine (256 values) and S is the sine (256 values).

### Annotate some points

Let's annotate some interesting points using the annotate command. We choose the 2π/3 value and we want to annotate both the sine and the cosine.

        ```
        t = 2*np.pi/3
        plt.plot([t,t],[0,np.cos(t)], color ='blue', linewidth=1.5, linestyle="--")
        plt.scatter([t,],[np.cos(t),], 50, color ='blue')

        plt.annotate(r'$\sin(\frac{2\pi}{3})=\frac{\sqrt{3}}{2}$',
                    xy=(t, np.sin(t)), xycoords='data',
                    xytext=(+10, +30), textcoords='offset points', fontsize=16,
                    arrowprops=dict(arrowstyle="->", connectionstyle="arc3,rad=.2"))

        plt.plot([t,t],[0,np.sin(t)], color ='red', linewidth=1.5, linestyle="--")
        plt.scatter([t,],[np.sin(t),], 50, color ='red')

        plt.annotate(r'$\cos(\frac{2\pi}{3})=-\frac{1}{2}$',
                    xy=(t, np.cos(t)), xycoords='data',
                    xytext=(-90, -50), textcoords='offset points', fontsize=16,
                    arrowprops=dict(arrowstyle="->", connectionstyle="arc3,rad=.2"))
        ```

### Subplots

With subplot you can arrange plots in a regular grid. You need to specify the number of rows and columns and the number of the plot. Note that the gridspec command is a more powerful alternative.

Examples:

        ```
        from pylab import *

        subplot(2,1,1)
        xticks([]), yticks([])
        text(0.5,0.5, 'subplot(2,1,1)',ha='center',va='center',size=24,alpha=.5)

        subplot(2,1,2)
        xticks([]), yticks([])
        text(0.5,0.5, 'subplot(2,1,2)',ha='center',va='center',size=24,alpha=.5)

        # plt.savefig('../figures/subplot-horizontal.png', dpi=64)
        show()
        ```
        ```
        from pylab import *
        import matplotlib.gridspec as gridspec

        G = gridspec.GridSpec(3, 3)

        axes_1 = subplot(G[0, :])
        xticks([]), yticks([])
        text(0.5,0.5, 'Axes 1',ha='center',va='center',size=24,alpha=.5)

        axes_2 = subplot(G[1,:-1])
        xticks([]), yticks([])
        text(0.5,0.5, 'Axes 2',ha='center',va='center',size=24,alpha=.5)

        axes_3 = subplot(G[1:, -1])
        xticks([]), yticks([])
        text(0.5,0.5, 'Axes 3',ha='center',va='center',size=24,alpha=.5)

        axes_4 = subplot(G[-1,0])
        xticks([]), yticks([])
        text(0.5,0.5, 'Axes 4',ha='center',va='center',size=24,alpha=.5)

        axes_5 = subplot(G[-1,-2])
        xticks([]), yticks([])
        text(0.5,0.5, 'Axes 5',ha='center',va='center',size=24,alpha=.5)

        #plt.savefig('../figures/gridspec.png', dpi=64)
        show()
        ```

### Animation

animation in matplotlib was not an easy task and was done mainly through clever hacks. However, things have started to change since version 1.1 and the introduction of tools for creating animation very intuitively, with the possibility to save them in all kind of formats (but don't expect to be able to run very complex animations at 60 fps though).

The easiest way to make a live animation in matplotlib is to use one of the `Animation` classes

In both cases it is critical to keep a reference to the instance object. The animation is advanced by a timer (typically from the host GUI framework) which the Animation object holds the only reference to. If you do not hold a reference to the Animation object, it (and hence the timers), will be garbage collected which will stop the animation.

### Scatter Plots

Color is given by angle of (X,Y).

        ```
        import numpy as np
        import matplotlib.pyplot as plt

        n = 1024
        X = np.random.normal(0,1,n)
        Y = np.random.normal(0,1,n)
        T = np.arctan2(Y,X)

        plt.axes([0.025,0.025,0.95,0.95])
        plt.scatter(X,Y, s=75, c=T, alpha=.5)

        plt.xlim(-1.5,1.5), plt.xticks([])
        plt.ylim(-1.5,1.5), plt.yticks([])
        # savefig('../figures/scatter_ex.png',dpi=48)
        plt.show()

        ```

### Pie Charts

You need to draw arrows twice.

Starting from the code above, try to reproduce the graphic on the right taking care of colors and orientations.

        ```
        import numpy as np
        import matplotlib.pyplot as plt

        n = 8
        X,Y = np.mgrid[0:n,0:n]
        T = np.arctan2(Y-n/2.0, X-n/2.0)
        R = 10+np.sqrt((Y-n/2.0)**2+(X-n/2.0)**2)
        U,V = R*np.cos(T), R*np.sin(T)

        plt.axes([0.025,0.025,0.95,0.95])
        plt.quiver(X,Y,U,V,R, alpha=.5)
        plt.quiver(X,Y,U,V, edgecolor='k', facecolor='None', linewidth=.5)

        plt.xlim(-1,n), plt.xticks([])
        plt.ylim(-1,n), plt.yticks([])

        # savefig('../figures/quiver_ex.png',dpi=48)
        plt.show()
        ```

### 3D Plots

You need to use contourf.

        ```
        import numpy as np
        import matplotlib.pyplot as plt
        from mpl_toolkits.mplot3d import Axes3D

        fig = plt.figure()
        ax = Axes3D(fig)
        X = np.arange(-4, 4, 0.25)
        Y = np.arange(-4, 4, 0.25)
        X, Y = np.meshgrid(X, Y)
        R = np.sqrt(X**2 + Y**2)
        Z = np.sin(R)

        ax.plot_surface(X, Y, Z, rstride=1, cstride=1, cmap=plt.cm.hot)
        ax.contourf(X, Y, Z, zdir='z', offset=-2, cmap=plt.cm.hot)
        ax.set_zlim(-2,2)

        # savefig('../figures/plot3d_ex.png',dpi=48)
        plt.show()
        ```