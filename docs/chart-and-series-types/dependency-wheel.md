Dependency wheel
===

A dependency wheel is a type of flow diagram, where nodes are laid out in a circle, and links are drawn between them. This width of the link and size of the nodes are proportional to the flow quantity or weight of each link.

The dependency wheel's use areas are similar to the [Sankey diagram](https://www.highcharts.com/docs/chart-and-series-types/sankey-diagram), but while the Sankey diagram supports multiple columns, and there is a clear direction of flow, the dependency wheel's nodes are laid out on the same level, indicating that the flow is multidirectional.

For more detailed samples and documentation, check the [API](https://api.highcharts.com/highcharts/plotOptions.series.dependencywheel).

<iframe style="width: 100%; height: 600px; border: none;" src=https://www.highcharts.com/samples/embed/highcharts/demo/dependency-wheel allow="fullscreen"></iframe>

The data structure, as well as the concept of nodes and links, is identical to those of the [Sankey diagram](https://www.highcharts.com/docs/chart-and-series-types/sankey-diagram).
 title: {
        text: 'Highcharts Dependency Wheel'
      },

      accessibility: {
        point: {
          valueDescriptionFormat: '{index}. From {point.from} to {point.to}: {point.weight}.'
        }
      },

      series: [{
          keys: ['from', 'to', 'weight'],
          data: [
            ['Cancer', 'AntiHIV', 3],
            ['Cancer', 'Antiviral', 5],
            ['Cancer', 'Antibiotic', 5],
            ['Cancer', 'schizophrenia', 1],
            ['Cancer', 'Antipsychotic', 2],
            ['Cancer', 'epilepsy', 2],
            ['Cancer', 'hpertension', 2],
            ['cancer', 'Lyme disease', 1],
            ['cancer', 'antiparasitic', 2],
            ['cancer', 'Inflammation', 5],
            ['Cancer', 'Rheumatoid arthritis', 1],
            ['Rheumatoid arthritis', 'cancer', 3],
            ['Multiple sclerosis', 'cancer', 1],
            ['Inflammation', 'cancer', 1],
            ['Malaria', 'cancer', 1],
            ['Dermatological', 'cancer', 2],
            ['PCOS', 'cancer', 3],
            ['Cancer', 'sleeping sickness', 1],
            ['Pakinsons, '
              cancer ', 2], ['cancer', 'precocious puberty', 1],
              ['cancer', 'Sickel cell disease', 1]
            ],
            type: 'dependencywheel',
            name: 'Dependency wheel series',
            dataLabels: {
              color: '#333',
              textPath: {
                enabled: true,
                attributes: {
                  dy: 5
                }
              },
              distance: 10
            },
            size: '95%'
          }]

      });
