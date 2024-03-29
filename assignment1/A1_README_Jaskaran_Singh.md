# Assignment 1

* *Date Created*: 6 FEBRUARY 2024
* *Last Modification Date*: 7 FEBRUARY 2024
* *Assignment URL*: <https://main--feature-jaskaran-assignment1.netlify.app/>
* *Git URL*: <https://git.cs.dal.ca/singh16/csci-5709-assignments/-/tree/main/assignment1>

## Authors

* [Jaskaran Singh](js356337@dal.ca)

## Deployment

I created a mirror repository on github from gitlab and deployed on netlify. Configued the built settings of Netlify as required and the website is live on above URL.

## Built With

* [React](https://legacy.reactjs.org/docs/getting-started.html/) - The web framework used
* [npm](https://docs.npmjs.com//) - Dependency Management

## Sources Used

### budget-planner.js

*Lines 130 - 137*

```
    {/* Pie chart */}
        <PieChart
          series={[{ data: chartData }]}
          width={500}
          height={230}
          labelAccessor={({ dataEntry }) => `${dataEntry.value}%`}
        />
```

The code above was created by adapting the code in [Charts - Pie](https://mui.com/x/react-charts/pie/#basics) as shown below: 

```
import * as React from 'react';
import { PieChart } from '@mui/x-charts/PieChart';

export default function BasicPie() {
  return (
    <PieChart
      series={[
        {
          data: [
            { id: 0, value: 10, label: 'series A' },
            { id: 1, value: 15, label: 'series B' },
            { id: 2, value: 20, label: 'series C' },
          ],
        },
      ]}
      width={400}
      height={200}
    />
  );
}

```

*Lines 140 - 167*

```
    <Stack spacing={2}>
        <Box sx={{ display: "flex", flexWrap: "wrap" }}>
          {chartData.map((category, index) => (
            <Card
              key={category.id}
              style={{
                marginRight: "30px",
                marginBottom: "10px",
                width: "23%",
              }}
            >
              <CardContent>
                <Typography variant="h5">{category.label}</Typography>
                <Typography>
                  Budget: {category.value}% equals to $
                  {(category.value / 100) * monthlySalary}
                </Typography>
                <IconButton onClick={() => handleEdit(index)}>
                  <EditIcon />
                </IconButton>
                <IconButton onClick={() => handleDelete(index)}>
                  <DeleteIcon />
                </IconButton>
              </CardContent>
            </Card>
          ))}
        </Box>
      </Stack>
```

The code above was created by adapting the code in [Cards - Media](https://mui.com/material-ui/react-card/#basics) as shown below: 

```
import * as React from 'react';
import Card from '@mui/material/Card';
import CardActions from '@mui/material/CardActions';
import CardContent from '@mui/material/CardContent';
import CardMedia from '@mui/material/CardMedia';
import Button from '@mui/material/Button';
import Typography from '@mui/material/Typography';

export default function MediaCard() {
  return (
    <Card sx={{ maxWidth: 345 }}>
      <CardMedia
        sx={{ height: 140 }}
        image="/static/images/cards/contemplative-reptile.jpg"
        title="green iguana"
      />
      <CardContent>
        <Typography gutterBottom variant="h5" component="div">
          Lizard
        </Typography>
        <Typography variant="body2" color="text.secondary">
          Lizards are a widespread group of squamate reptiles, with over 6,000
          species, ranging across all continents except Antarctica
        </Typography>
      </CardContent>
      <CardActions>
        <Button size="small">Share</Button>
        <Button size="small">Learn More</Button>
      </CardActions>
    </Card>
  );
}

```



### navbar.js

*Lines 7 - 28*

```
    <AppBar position="static">
      {/* Toolbar for holding the content */}
      <Toolbar>
        {/* Stack to arrange elements horizontally with center alignment */}
        <Stack direction="row" alignItems="center" spacing={2} sx={{ flexGrow: 1 }}>
          {/* IconButton for the logo */}
          <IconButton size="large" edge="start" color="inherit" aria-label="logo">
            <AttachMoneyIcon />
          </IconButton>
          {/* Typography component for the title */}
          <Typography variant="h6" component="div">
            Fintastic
          </Typography>
        </Stack>
        {/* Stack to arrange elements horizontally */}
        <Stack direction="row" spacing={2}>
          {/* Button for features */}
          <Button color="inherit">Features</Button>
        </Stack>
      </Toolbar>
    </AppBar>

```

The code above was created by adapting the code from YouTube Channel - Codevolution (https://www.youtube.com/watch?v=y9iX6sfB40k&list=PLC3y8-rFHvwh-K9mDlrrcDywl7CeVL2rO&index=21&pp=iAQB)


## Acknowledgments

* I deeply appreciate the invaluable insights and dedication demonstrated through the provided code, which laid a solid foundation for comprehending its functionality and logic. Their commitment to their work is commendable.
* Their contribution offered profound insights and significantly impacted my learning journey, shaping my approach to understanding various techniques and approaches. I am genuinely grateful for their efforts and expertise.