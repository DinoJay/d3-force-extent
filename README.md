# d3-force-extent

Tired of keeping nodes within your viewport. With this force you can specify the min and max position for your nodes. It works also with rectangles. Add the force to your d3.simulation like that:

```
    const simulation = d3
      .forceSimulation(nodes)
      .force('collide', bboxCollide(getBBox).strength(0.2))
      .force(
        'extent',
        forceExtent()
          .extent([[-40, 0], [width, height]])
          .bbox(d => [
            [-d.width / 2 - pad, -d.height / 2 - pad],
            [d.width / 2 + pad / 2, d.height / 2 + pad / 2]
          ])
      )

```

TODO:
* how to import lib locally
* failing in upper part

