# Football_score_prediction_model
This project tries to predict football matche's outcome based on machine learning through poisson distribution, KNN and MLP classifier

\documentclass{article}
\usepackage{amsmath}
\usepackage{color,pxfonts,fix-cm}
\usepackage{latexsym}
\usepackage[mathletters]{ucs}
\DeclareUnicodeCharacter{46}{\textperiodcentered}
\DeclareUnicodeCharacter{8242}{$\prime$}
\DeclareUnicodeCharacter{58}{$\colon$}
\DeclareUnicodeCharacter{8221}{\textquotedblright}
\DeclareUnicodeCharacter{955}{$\lambda$}
\DeclareUnicodeCharacter{8217}{\textquoteright}
\DeclareUnicodeCharacter{60}{\textless}
\DeclareUnicodeCharacter{62}{\textgreater}
\DeclareUnicodeCharacter{8230}{$\ldots$}
\DeclareUnicodeCharacter{32}{$\ $}
\usepackage[T1]{fontenc}
\usepackage[utf8x]{inputenc}
\usepackage{pict2e}
\usepackage{wasysym}
\usepackage[english]{babel}
\usepackage{tikz}
\pagestyle{empty}
\usepackage[margin=0in,paperwidth=612pt,paperheight=792pt]{geometry}
\begin{document}
\definecolor{color_29791}{rgb}{0,0,0}
\definecolor{color_37858}{rgb}{0.019608,0.388235,0.756863}
\definecolor{color_97849}{rgb}{0.266667,0.329412,0.415686}
\definecolor{color_283006}{rgb}{1,1,1}
\definecolor{color_63553}{rgb}{0.133333,0.133333,0.133333}
\begin{tikzpicture}[overlay]\path(0pt,0pt);\end{tikzpicture}
\begin{picture}(-5,0)(2.5,0)
\put(57.024,-743.096){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(177.85,-454.52){\includegraphics[width=269.35pt,height=391.67pt]{latexImage_915a2d3bbd4fdc68fee2efeec31644ba.png}}
\put(57.024,-80.73999){\fontsize{20.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(57.024,-113.5){\fontsize{20.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(57.024,-146.38){\fontsize{20.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(57.024,-179.14){\fontsize{20.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(57.024,-212.02){\fontsize{20.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(57.024,-244.81){\fontsize{20.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(57.024,-277.69){\fontsize{20.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(57.024,-310.45){\fontsize{20.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(57.024,-343.33){\fontsize{20.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(57.024,-376.09){\fontsize{20.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(57.024,-408.99){\fontsize{20.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(57.024,-441.75){\fontsize{20.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(57.024,-474.63){\fontsize{20.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(134.66,-507.39){\fontsize{20.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}Module: Applied Artificial Intelligence }
\put(291.05,-540.27){\fontsize{20.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(68.544,-573.03){\fontsize{20.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}Subject: International Football Match Prediction Model }
\put(291.05,-605.94){\fontsize{20.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(131.54,-638.7){\fontsize{20.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}Student Name: Moustapha Hadji Sidibe }
\put(291.05,-671.58){\fontsize{20.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(178.22,-704.336){\fontsize{20.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}Student Number: C3004427 }
\end{picture}
\newpage
\begin{tikzpicture}[overlay]\path(0pt,0pt);\end{tikzpicture}
\begin{picture}(-5,0)(2.5,0)
\put(57.024,-743.096){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(67.944,-75.34003){\fontsize{14.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}I. Introduction }
\end{picture}
\begin{tikzpicture}[overlay]
\path(0pt,0pt);
\filldraw[color_29791][even odd rule]
(111.02pt, -77.85999pt) -- (181.724pt, -77.85999pt)
 -- (181.724pt, -77.85999pt)
 -- (181.724pt, -76.89996pt)
 -- (181.724pt, -76.89996pt)
 -- (111.02pt, -76.89996pt) -- cycle
;
\end{tikzpicture}
\begin{picture}(-5,0)(2.5,0)
\put(57.024,-98.85999){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}Football, the most popular collective sport worldwide has gradually attracted more focus from scientists }
\put(57.024,-113.38){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}from different fields in the past few years. In this ever-evolving landscape of sports analytics [1] and }
\put(57.024,-127.9){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}statistics, the application of machine learning techniques [2] and probabilities has become increasingly }
\put(57.024,-142.42){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}prevalent. However, in such intensive and complicated sport confrontations, we might think there is a lot }
\put(57.024,-156.82){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}of randomness but with a closer look at the data, we could get some better understanding of the }
\put(57.024,-171.34){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}outcomes.  This project aims to leverage the power of the AI technics in combination with the Poisson }
\put(57.024,-185.86){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}distribution to predict the winners of international football matches. FIFA (Federation Internationale de }
\put(57.024,-200.38){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}Football Association), the main body in charge of maintaining, managing, and regularizing this sport has }
\put(57.024,-214.78){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}been doing a good job at keeping track of every event occurred in the past 100 years including game }
\put(57.024,-229.3){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}results, number of shots, corners, yellow and red cards, player lists, substitutions, managers, referees }
\put(57.024,-243.85){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}etc. Our objective is to find the correlation between these features and try to predict the winner of }
\put(57.024,-258.37){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}international football matches. }
\put(57.024,-280.81){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(64.464,-306.25){\fontsize{14.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}II. Literature review }
\end{picture}
\begin{tikzpicture}[overlay]
\path(0pt,0pt);
\filldraw[color_29791][even odd rule]
(111.02pt, -308.77pt) -- (207.764pt, -308.77pt)
 -- (207.764pt, -308.77pt)
 -- (207.764pt, -307.81pt)
 -- (207.764pt, -307.81pt)
 -- (111.02pt, -307.81pt) -- cycle
;
\end{tikzpicture}
\begin{picture}(-5,0)(2.5,0)
\put(57.024,-329.77){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(75.024,-352.21){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}1. Football }
\put(57.024,-374.77){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}In general, most team-based sports despite being different in the rules, regulations and intensity have }
\put(57.024,-389.17){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}the same objective: score the most points. A match of football [3], first, involves 11 players on each team }
\put(57.024,-403.69){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}and takes place on a 90m wide and 120m long pitch with a net on both sides. The team that gets the ball }
\put(57.024,-418.23){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}in the opposite net the greatest number of times wins the game. Each player on the field has a specific }
\put(57.024,-432.75){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}role, position, skillset, and follows instructions given by his coach. The performance of each player could }
\put(57.024,-447.27){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}have a big impact on the matches’ outcome but for this project, we shall ignore individual performances }
\put(57.024,-461.67){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}and focus more on team’s values based on their past results. }
\put(75.024,-484.23){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}2. Poisson distribution }
\put(57.024,-506.67){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}The Poisson distribution [4] is a probability distribution that expresses the likelihood of a given number }
\put(57.024,-521.19){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}of events occurring within a fixed interval. In the context of football, with all the data collected over the }
\put(57.024,-535.71){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}years, the Poisson distribution has proven to be a robust model for estimating diverse short time events }
\put(57.024,-550.11){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}one being goal-scoring probabilities. By considering historical data on goals scored by a team, the }
\put(57.024,-564.63){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}distribution provides a probabilistic framework for predicting the number of goals a team is likely to }
\put(57.024,-579.18){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}score in a future match. This could be more specific and accurate given the context of the rivalry with the }
\put(57.024,-593.7){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}opposite team, the tournament, the engagement of the stadium and the ambition of the players on }
\put(57.024,-608.1){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}stage.  The application of Poisson distribution is particularly relevant because here in football, scoring }
\put(57.024,-622.62){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}events are relatively rare and can significantly impact match outcomes. One of its benefits is the easy }
\put(57.024,-637.14){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}approach it offers. First, we gather the results of the team for the season and get the average goals }
\put(57.024,-651.66){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}scored. Then the Poisson distribution is calculated on the likelihood for the team to a certain range of }
\put(57.024,-666.06){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}goals and select the most likely one. This probability can then be associated with the one got from the }
\put(57.024,-680.58){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}opposite team and analyzed. }
\put(75.024,-703.136){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}3. K-nearest Neighbor }
\end{picture}
\newpage
\begin{tikzpicture}[overlay]\path(0pt,0pt);\end{tikzpicture}
\begin{picture}(-5,0)(2.5,0)
\put(57.024,-743.096){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(57.024,-72.44){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}KNN [5] is non-parametric machine learning algorithm that is particularly effective in sports prediction }
\put(57.024,-86.97998){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}tasks. Unlike other technics, it does not rely on weighted paradigm between the different features but }
\put(57.024,-101.5){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}mainly focuses on the direct relationship between them. KNN is also known as a classifier meaning that }
\put(57.024,-115.9){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}it gives out a binary answer (1 or 0), in our case: win or loss. Its simplicity and flexibility make it suitable }
\put(57.024,-130.42){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}for scenarios where the outcome is influenced by the proximity of similar instances. In the realm of }
\put(57.024,-144.94){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}football, KNN has found success in various applications, including predicting match outcomes based on }
\put(57.024,-159.46){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}historical data. The algorithm's ability to adapt to different types of data and capture underlying patterns }
\put(57.024,-173.86){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}has made it a valuable tool in sports analytics. The principle is simple: for each given request, the }
\put(57.024,-188.38){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}algorithm has to calculate its Euclidean distance relative to every data point in the training set. That }
\put(57.024,-202.9){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}allows is to make up a table of the “K” shortest ones called the K-Neighbors, K being an integer. Then, the }
\put(57.024,-217.42){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}result is represented by the most common data point’s outcome from the table. The subtility of this }
\put(57.024,-231.82){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}algorithm is to find the best K value that could fit the given training data.  }
\put(57.024,-254.41){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(75.024,-276.85){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}4. MLP Classifier }
\put(57.024,-299.41){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}The Multilayer Perceptron (MLP) classifier [6] is a type of artificial neural network (ANN) that falls under }
\put(57.024,-313.81){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}the broader category of supervised machine learning models. It is particularly effective for tasks such as }
\put(57.024,-328.33){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}classification and regression. The MLP consists of multiple layers of nodes (neurons), organized into an }
\put(57.024,-342.85){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}input layer, one or more hidden layers, and an output layer. }
\put(57.024,-365.29){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}In an MLP classifier, each connection between nodes has an associated weight, and each node applies an }
\put(57.024,-379.81){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}activation function to the weighted sum of its inputs. The network learns during training by adjusting }
\put(57.024,-394.33){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}these weights to minimize the difference between predicted and actual outputs. }
\put(57.024,-416.79){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}The MLP model learns to understand the relationships between the given features and the match }
\put(57.024,-431.31){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}outcomes, providing a more sophisticated and data-driven approach to predicting the results of football }
\put(57.024,-445.83){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}matches. This could be more beneficial than the other models as it is not based on linear relationships }
\put(57.024,-460.23){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}but mainly focuses on more complex dependencies in the data. }
\put(60.864,-485.79){\fontsize{14.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}III. Methodology }
\end{picture}
\begin{tikzpicture}[overlay]
\path(0pt,0pt);
\filldraw[color_29791][even odd rule]
(111.02pt, -488.31pt) -- (187.604pt, -488.31pt)
 -- (187.604pt, -488.31pt)
 -- (187.604pt, -487.35pt)
 -- (187.604pt, -487.35pt)
 -- (111.02pt, -487.35pt) -- cycle
;
\end{tikzpicture}
\begin{picture}(-5,0)(2.5,0)
\put(111.02,-501.27){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(75.024,-515.67){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}1. Dataset Overview }
\put(57.024,-538.23){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}The Dataset chosen for this project is the “International football results from 1872 to 2023” by MART }
\put(57.024,-552.75){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}JÜRISOO [6] available on www.kaggle.com. It is a set of football results between the national teams in }
\end{picture}
\begin{tikzpicture}[overlay]
\path(0pt,0pt);
\filldraw[color_37858][even odd rule]
(169.22pt, -554.67pt) -- (245.444pt, -554.67pt)
 -- (245.444pt, -554.67pt)
 -- (245.444pt, -553.95pt)
 -- (245.444pt, -553.95pt)
 -- (169.22pt, -553.95pt) -- cycle
;
\end{tikzpicture}
\begin{picture}(-5,0)(2.5,0)
\put(57.024,-567.15){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}the major international competitions since 1872 ordered by date. It includes over 45,000 matches with }
\put(57.024,-581.7){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}the following features: }
\put(75.024,-604.14){\fontsize{9.96}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}- Home and away team }
\put(75.024,-618.66){\fontsize{9.96}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}- Home and away scored goal }
\put(75.024,-633.18){\fontsize{9.96}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}- Tournament }
\put(75.024,-647.7){\fontsize{9.96}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}- Country and city where the game is taking place at }
\put(75.024,-662.1){\fontsize{9.96}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}- Neutral state of the game }
\put(75.024,-676.62){\fontsize{9.96}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}- date  }
\put(93.02,-691.136){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\end{picture}
\newpage
\begin{tikzpicture}[overlay]\path(0pt,0pt);\end{tikzpicture}
\begin{picture}(-5,0)(2.5,0)
\put(57.024,-743.096){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(561.1,-248.05){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(238.13,-265.81){\fontsize{9}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_97849}Figure 1: Raw Data Overview }
\put(93.02,-288.49){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(75.024,-303.01){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}2. Data analysis }
\put(57.024,-325.57){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}With such a large dataset, it is more than essential to analyze the quality of the features. The dataset }
\put(57.024,-339.97){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}quality can have a big impact on the overall machine learning model as it helps avoid biases in the }
\put(57.024,-354.49){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}training set. One of the big aspects of our project is based on the goals so it’s essential to be sure of the }
\put(57.024,-369.01){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}number of goals on each side of the field. }
\put(525.1,-511.95){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(198.17,-529.71){\fontsize{9}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_97849}Figure 2: Home and away team's goals comparison }
\put(57.024,-552.51){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}For both home and away teams, there is a big gap between the minimum and maximum goals scored, 31 }
\put(57.024,-566.91){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}for home and 21 for away teams.  }
\put(388.51,-621.42){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(206.09,-639.06){\fontsize{9}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_97849}Figure 3: Home and away team's highest goals }
\put(57.024,-661.86){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}However, the average number of goals is similar: 1.71 for home and 1.17 for away side. This comparison }
\put(57.024,-676.38){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}confirms the quality of the data as most of the scores are below 5 and knowing that most football }
\put(57.024,-690.896){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}m}
\put(93,-247.35){\includegraphics[width=468pt,height=185.35pt]{latexImage_f574c2da24da0a3bbac960cf56e0286f.png}}
\put(57,-511.89){\includegraphics[width=468pt,height=130.9pt]{latexImage_6046c01cd9046f3735b20ac0ecfa1ef6.png}}
\put(193.5,-621.27){\includegraphics[width=194.6pt,height=42.35pt]{latexImage_095d40bc8bee4824f2177fbbc0995ef9.png}}
\end{picture}
\newpage
\begin{tikzpicture}[overlay]\path(0pt,0pt);\end{tikzpicture}
\begin{picture}(-5,0)(2.5,0)
\put(57.024,-743.096){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(57.024,-72.44){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(75.024,-94.90002){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}3. Data pre-processing }
\put(57.024,-117.46){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}No matter how complete the dataset we have is, it is not suitable for any machine learning algorithm. As }
\put(57.024,-131.98){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}part of AI engineering, it’s crucial to make the dataset usable. It involves a series of operations aimed at }
\put(57.024,-146.38){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}cleaning, transforming, and organizing the data to enhance the performance and reliability of the }
\put(57.024,-160.9){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}machine learning model. For our project, that boils down to a few basic steps. }
\put(111.02,-183.46){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}a. Information classification }
\put(57.024,-205.9){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}This project aims to predict the outcome of a match only based on recent performance and home }
\put(57.024,-220.42){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}advantage. In this perspective, it is important to ignore some of the variables. First, we can drop the }
\put(57.024,-234.82){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}neutral and city columns assuming that every team is playing home if the game takes place in the team’s }
\put(57.024,-249.37){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}representative country. Then we get rid of all neutral games. For the sake of simplicity, unlike real life }
\put(57.024,-263.89){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}situations, there is a consequent gap between good and less competent teams, but we will consider }
\put(57.024,-278.41){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}them to be all equal and only the historical data make up their strength. }
\put(111.02,-300.85){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}b. Indexing  }
\put(57.024,-323.41){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}AI models can only deal with numerical values so it’s essential to replace all alphabetic variables by its }
\put(57.024,-337.81){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}corresponding index. At first, 317 different teams have been identified both for home and away side that }
\put(57.024,-352.33){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}can be ranged from 1 and 317. Following the same logic, 147 tournaments and 268 home stadiums were }
\put(57.024,-366.85){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}found and indexed in the dataset. }
\put(111.02,-389.29){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}c. Seasons identification }
\put(57.024,-411.87){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}International football teams have a different selection every year as the players are requested to play }
\put(57.024,-426.27){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}based on their season’s performance. Knowing that, to identify each selection, we have to separate the }
\put(57.024,-440.79){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}data by date hence by year. }
\put(111.02,-463.35){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}d. Winning side }
\put(57.024,-485.79){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}In the dataset, we have the home and away score. However, it might be unclear for the AI models what }
\put(57.024,-500.31){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}the target value is. First, we calculate the difference between the home and away score. That allows us }
\put(57.024,-514.83){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}to classify the outcomes of all the matches:  }
\put(75.024,-537.27){\fontsize{9.96}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}- Home win if difference > 0 }
\put(75.024,-551.79){\fontsize{9.96}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}- Away win if difference < 0 }
\put(75.024,-566.31){\fontsize{9.96}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}- Draw if difference = 0 }
\put(57.024,-588.78){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}This new column can now be added to the dataset as target value. }
\put(57.024,-611.22){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} e. Data normalization and  }
\put(57.024,-633.78){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}The cell values in the dataset are far apart and can be a downfall for the training step. To avoid that, we }
\put(57.024,-648.3){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}need to go through a normalization process that ensures that all the values are between 0 and 1. Then, }
\put(57.024,-662.7){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}the dataset we be separated in two parts: around 80\% as training set and 20\% for test purposes. }
\put(75.024,-685.256){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}4. AI models training }
\put(111.02,-699.656){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}a. Poisson Distribution }
\end{picture}
\newpage
\begin{tikzpicture}[overlay]\path(0pt,0pt);\end{tikzpicture}
\begin{picture}(-5,0)(2.5,0)
\put(57.024,-743.096){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(57.024,-72.44){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}Poisson Distribution is an easy-to-understand step-by-step approach. At first, let’s get the average }
\put(57.024,-86.97998){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}number of goals for each team per season per year. Then we can make calculate the Poisson distribution }
\put(57.024,-101.5){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}using the formula: }
\put(201.05,-128.98){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}Y = }
\put(216.89,-122.5){\fontsize{8.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}e}
\put(220.85,-119.5){\fontsize{6.48}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}−λ}
\put(228.77,-121.06){\fontsize{6.48}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}1}
\put(233.33,-122.5){\fontsize{8.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}.λ}
\put(238.97,-124.54){\fontsize{6.48}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}1}
\put(238.97,-119.26){\fontsize{6.48}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}푥}
\put(226.97,-134.5){\fontsize{8.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}x!}
\end{picture}
\begin{tikzpicture}[overlay]
\path(0pt,0pt);
\filldraw[color_29791][even odd rule]
(216.89pt, -126.22pt) -- (243.29pt, -126.22pt)
 -- (243.29pt, -126.22pt)
 -- (243.29pt, -125.5pt)
 -- (243.29pt, -125.5pt)
 -- (216.89pt, -125.5pt) -- cycle
;
\end{tikzpicture}
\begin{picture}(-5,0)(2.5,0)
\put(243.29,-128.98){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(245.69,-122.5){\fontsize{8.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}e}
\put(249.65,-119.5){\fontsize{6.48}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}−λ}
\put(257.57,-121.06){\fontsize{6.48}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}2}
\put(262.13,-122.5){\fontsize{8.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}.λ}
\put(267.77,-124.54){\fontsize{6.48}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}2}
\put(267.77,-119.26){\fontsize{6.48}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}푥}
\put(255.65,-134.5){\fontsize{8.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}y!}
\end{picture}
\begin{tikzpicture}[overlay]
\path(0pt,0pt);
\filldraw[color_29791][even odd rule]
(245.69pt, -126.22pt) -- (272.09pt, -126.22pt)
 -- (272.09pt, -126.22pt)
 -- (272.09pt, -125.5pt)
 -- (272.09pt, -125.5pt)
 -- (245.69pt, -125.5pt) -- cycle
;
\end{tikzpicture}
\begin{picture}(-5,0)(2.5,0)
\put(272.09,-128.98){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(75.024,-155.74){\fontsize{9.96}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}- λ1 and λ2 respectively being the average goals score by home team and away team  }
\put(75.024,-170.26){\fontsize{9.96}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}- x and y are the respective number of goals potentially scored by home and away team }
\put(75.024,-184.78){\fontsize{9.96}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}- x and y range from 0 to 5 }
\put(57.024,-207.22){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}As we know that majority of goals are below 5, we need to get the Poisson distribution for every score }
\put(57.024,-221.74){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}value from 0 to 5 and select the most likely one. As we are using this as a classifier, we could ignore the }
\put(57.024,-236.26){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}draw results and only keep the rows where one team wins then calculate the distribution following these }
\put(57.024,-250.69){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}steps: }
\put(57.024,-273.25){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}- for each year, for each tournament, calculate the number of goals for each team }
\put(57.024,-295.69){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}- get the average goal for each team for every confrontation }
\put(140.3,-326.17){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}푙}
\put(143.78,-328.45){\fontsize{8.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}ℎ표푚푒}
\put(169.1,-326.17){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}=}
\put(187.25,-317.77){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}푛푢푚푏푒푟 표푓 ℎ표푚푒′푠 푔표푎푙푠 푝푒푟 푦푒푎푟 푝푒푟 푡표푢푟푛푎푚푒푛푡}
\put(180.29,-333.61){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}푛푢푚푏푒푟 표푓 ℎ표푚푒′푠 푚푎푡푐ℎ푒푠 푝푒푟 푦푒푎푟 푝푒푟 푡표푢푟푛푎푚푒푛푡}
\end{picture}
\begin{tikzpicture}[overlay]
\path(0pt,0pt);
\filldraw[color_29791][even odd rule]
(180.29pt, -323.41pt) -- (441.7pt, -323.41pt)
 -- (441.7pt, -323.41pt)
 -- (441.7pt, -322.69pt)
 -- (441.7pt, -322.69pt)
 -- (180.29pt, -322.69pt) -- cycle
;
\end{tikzpicture}
\begin{picture}(-5,0)(2.5,0)
\put(441.82,-326.17){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(140.3,-363.25){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}푙}
\put(143.78,-365.53){\fontsize{8.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}푎푤푎푦}
\put(169.1,-363.25){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}=}
\put(188.81,-354.85){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}푛푢푚푏푒푟 표푓 푎푤푎푦′푠푔표푎푙푠 푝푒푟 푦푒푎푟 푝푒푟 푡표푢푟푛푎푚푒푛푡}
\put(180.41,-370.69){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}푛푢푚푏푒푟 표푓 푎푤푎푦′푠 푚푎푡푐ℎ푒푠 푝푒푟 푦푒푎푟 푝푒푟 푡표푢푟푛푎푚푒푛푡}
\end{picture}
\begin{tikzpicture}[overlay]
\path(0pt,0pt);
\filldraw[color_29791][even odd rule]
(180.41pt, -360.49pt) -- (441.82pt, -360.49pt)
 -- (441.82pt, -360.49pt)
 -- (441.82pt, -359.77pt)
 -- (441.82pt, -359.77pt)
 -- (180.41pt, -359.77pt) -- cycle
;
\end{tikzpicture}
\begin{picture}(-5,0)(2.5,0)
\put(441.7,-363.25){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(57.024,-392.53){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}Thees numbers are then used to calculate the Poisson distribution for each team: }
\put(57.024,-414.99){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}- for each match we calculate the probability for both home and away teams to score 0,1,2,…,k goals }
\put(57.024,-429.51){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}respectively. }
\put(57.024,-451.95){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}- after this first step, we have a k*k different score predictions, so we evaluate how many times each side }
\put(57.024,-466.47){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}gets the highest goals and pick the one with the highest number of wins }
\put(57.024,-488.91){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}- calculate the accuracy for different k values and keep the best k. In this case, for k-value < 5, the }
\put(57.024,-503.43){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}accuracy of our model increases gradually until it reaches 20\% and stop improving at k=10 staying at }
\put(57.024,-517.95){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}21\%.  }
\put(57.024,-540.39){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}The results got from the Poisson Distribution is very low and can be explained. In fact, the average }
\put(57.024,-554.91){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}results used for the predictions are not representative of the team’s performance and can be improved }
\put(57.024,-569.43){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}using this following technique. Instead of using a basic average per year, we could use the average goal }
\put(57.024,-583.98){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}of the team on just recent games and or based on the last confrontations of the two teams. However, }
\put(57.024,-598.38){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}the result we have got so far can be used as features for the next models. }
\put(93.02,-620.94){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}b. KNN }
\put(57.024,-643.38){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}The Poisson Distribution calculated earlier, serve as feature inputs for the KNN model. When predicting }
\put(57.024,-657.9){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}the outcome of a new match, the KNN algorithm identifies the k-nearest neighbors in the historical }
\put(57.024,-672.42){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}dataset based on the calculated Poisson features. The majority class (win, lose, or draw) within these }
\put(57.024,-686.936){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}neighbors determines the predicted outcome for the new match. The choice of 'k' (number of neighbors) }
\put(57.024,-701.336){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}is a crucial parameter for better performance and accuracy. This integration of Poisson distribution }
\end{picture}
\newpage
\begin{tikzpicture}[overlay]\path(0pt,0pt);\end{tikzpicture}
\begin{picture}(-5,0)(2.5,0)
\put(57.024,-743.096){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(57.024,-72.44){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}insights into the KNN framework allows a more probabilistic approach to predicting football match }
\put(57.024,-86.97998){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}outcomes instead of basic numbers. }
\put(399.07,-211.78){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(237.53,-229.54){\fontsize{9}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_97849}Figure 4: KNN K's comparison }
\put(408.79,-417.51){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(229.61,-435.15){\fontsize{9}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_97849}Figure 5: K's accuracy comparison }
\put(57.024,-457.95){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}The accuracy is best at k=7 and is equivalent to 70\%. That constitutes a huge improvement from the last }
\put(57.024,-472.35){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}model and knowing that we ignored many variables at first, this result could be enough to prove the }
\put(57.024,-486.87){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}utility of the model. }
\put(57.024,-509.31){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(93.02,-531.87){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}c. MLP classifier }
\put(57.024,-554.31){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}For this step, it is more convenient to use the probabilities as features to help the model perform better. }
\put(57.024,-568.83){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}The Poisson distribution provides a probabilistic framework for estimating goal-scoring probabilities, }
\put(57.024,-583.38){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}which, when integrated into the MLP, allows for a more nuanced understanding of team performance. }
\put(57.024,-597.9){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}Then, the network learns to discern patterns and dependencies between these features and match }
\put(57.024,-612.3){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}outcomes during training. The hidden layers of the MLP enable the model to capture deeper interactions }
\put(57.024,-626.82){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}and non-linear dependencies, potentially enhancing predictive accuracy. This combination of the Poisson }
\put(57.024,-641.34){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}distribution and MLP classifier offers a sophisticated and more realistic results. }
\put(57.024,-663.78){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}The structure of the model is as follows: }
\put(75.024,-686.336){\fontsize{9.96}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}- 4 hidden layers of 10 neurons long each }
\put(75.024,-700.736){\fontsize{9.96}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}-}
\put(183,-211.78){\includegraphics[width=216pt,height=112.8pt]{latexImage_d03ca7905c566fc26925807993ca612a.png}}
\put(173.25,-416.73){\includegraphics[width=235.2pt,height=174.9pt]{latexImage_f737da731f4c6b4dca99b9ae5b136ef3.png}}
\end{picture}
\newpage
\begin{tikzpicture}[overlay]\path(0pt,0pt);\end{tikzpicture}
\begin{picture}(-5,0)(2.5,0)
\put(57.024,-743.096){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(57.024,-72.44){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}After 160 epochs, the loss does not seem to decrease anymore so we assume that as the lowest. The }
\put(57.024,-86.97998){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}accuracy got from this training process is 69.6\%. }
\put(57.024,-109.42){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}As this result derive from the Poisson distribution, it could be more accurate with better probabilistic }
\put(57.024,-123.94){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}features. }
\put(75.024,-146.38){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}5. Result evaluation }
\put(57.024,-168.94){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}Each Machine learning technic used is this project has been beneficial to provide a metric for the better }
\put(57.024,-183.46){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}understanding of the impact of features on the prediction of football matches. It all boils down to the }
\put(57.024,-197.86){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}same underlying factor: the Poisson distribution. The probabilities can be determined in different ways. }
\put(57.024,-212.38){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}However, with the simple and easy step by step approach used here has been able to produce some }
\put(57.024,-226.9){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}good results. First of all, the Poisson distribution alone was 21\% accurate on the test set but more }
\put(57.024,-241.45){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}complex and robust models like KNN and MLP have produced 69 to 70\% score overall. }
\put(57.024,-263.89){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(60.024,-289.21){\fontsize{14.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}IV. Ethics }
\end{picture}
\begin{tikzpicture}[overlay]
\path(0pt,0pt);
\filldraw[color_29791][even odd rule]
(111.02pt, -291.73pt) -- (144.38pt, -291.73pt)
 -- (144.38pt, -291.73pt)
 -- (144.38pt, -290.77pt)
 -- (144.38pt, -290.77pt)
 -- (111.02pt, -290.77pt) -- cycle
;
\end{tikzpicture}
\begin{picture}(-5,0)(2.5,0)
\put(57.024,-312.85){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(57.024,-335.29){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}The ethical implications of football prediction using AI are controversial and demand careful }
\put(57.024,-349.81){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}consideration. On the positive side, AI technologies can enhance the sports experience for fans, }
\put(57.024,-364.33){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}providing insights, and analysis that contribute to a deeper understanding of the game. Furthermore, it }
\put(57.024,-378.73){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}helps the teams, players, and sponsors to better prepare for their future confrontations as a lot of money }
\put(57.024,-393.25){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}is involved in this industry with millions of fans around the world. However, ethical concerns arise, }
\put(57.024,-407.77){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}particularly in the context of sports betting. The use of AI for football prediction introduces the potential }
\put(57.024,-422.31){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}for exploitation, encouraging irresponsible gambling behaviors based on algorithmic prediction. This }
\put(57.024,-436.71){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}raises issues related to addiction, financial harm, and the need for responsible implementation of AI-}
\put(57.024,-451.23){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}driven prediction models. Furthermore, there's a risk of perpetuating inequalities within the sport, as }
\put(57.024,-465.75){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}teams with greater financial resources may leverage AI for a competitive advantage. }
\put(57.024,-488.19){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}On the other hand, many of these issues can be avoided. First, transparency in the development and }
\put(57.024,-502.71){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}deployment of prediction models, as well as safeguards to prevent unethical uses, is essential. }
\put(57.024,-517.23){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}Additionally, the privacy of athletes and the potential for match-fixing should be carefully addressed.  }
\put(57.024,-539.67){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(63.504,-565.11){\fontsize{14.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}V. Conclusion }
\end{picture}
\begin{tikzpicture}[overlay]
\path(0pt,0pt);
\filldraw[color_29791][even odd rule]
(111.02pt, -567.63pt) -- (173.18pt, -567.63pt)
 -- (173.18pt, -567.63pt)
 -- (173.18pt, -566.67pt)
 -- (173.18pt, -566.67pt)
 -- (111.02pt, -566.67pt) -- cycle
;
\end{tikzpicture}
\begin{picture}(-5,0)(2.5,0)
\put(57.024,-588.66){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}Machine Learning in general has proven to be useful in every sector of activity and sport is no exception. }
\put(57.024,-603.18){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}Football, the most popular collective sport is the world was a high concern for years in data analytics and }
\put(57.024,-617.7){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}probability. By using more sophisticated techniques such as KNN, Poisson Distribution and MLP, a big }
\put(57.024,-632.1){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}improvement can be made in predictive models. Despite having ethical concerns on this matter, we can }
\put(57.024,-646.62){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}still establish regulations and rules on its usage in the industry. However, no matter how accurate a }
\put(57.024,-661.14){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}model is, there could still be downfalls as football is not just a score game but also a mind game. The }
\put(57.024,-675.66){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}performance of each of the 22 players on the field cannot be defined in advance nor the coach’s }
\put(57.024,-690.056){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}decisions during the match. On the contrary, we are forced is to acknowledge the impact of data on }
\put(57.024,-704.576){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}every side of our day to day lives. It all depends on the data quantity and quality which, in this case, is }
\end{picture}
\newpage
\begin{tikzpicture}[overlay]\path(0pt,0pt);\end{tikzpicture}
\begin{picture}(-5,0)(2.5,0)
\put(57.024,-743.096){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(57.024,-72.44){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}monitored and maintained by FIFA that have been collecting every aspect of every game for years. }
\put(57.024,-86.97998){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}Nowadays, all the data is available for everyone and could be misused. In this perspective, we might }
\put(57.024,-101.5){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}wonder, what impact can such a model do to such a lucrative and popular industry such as Football? }
\put(57.024,-123.94){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(60.024,-149.38){\fontsize{14.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}VI. References }
\end{picture}
\begin{tikzpicture}[overlay]
\path(0pt,0pt);
\filldraw[color_29791][even odd rule]
(111.02pt, -151.9pt) -- (173.54pt, -151.9pt)
 -- (173.54pt, -151.9pt)
 -- (173.54pt, -150.94pt)
 -- (173.54pt, -150.94pt)
 -- (111.02pt, -150.94pt) -- cycle
;
\end{tikzpicture}
\begin{picture}(-5,0)(2.5,0)
\put(111.02,-167.86){\fontsize{14.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\end{picture}
\begin{tikzpicture}[overlay]
\path(0pt,0pt);
\filldraw[color_283006][even odd rule]
(93.02pt, -185.5pt) -- (520.41pt, -185.5pt)
 -- (520.41pt, -185.5pt)
 -- (520.41pt, -172.9pt)
 -- (520.41pt, -172.9pt)
 -- (93.02pt, -172.9pt) -- cycle
;
\end{tikzpicture}
\begin{picture}(-5,0)(2.5,0)
\put(75.024,-183.34){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}1. Memmert, D., \& Raabe, D. (2018). Data analytics in football: Positional data collection, modelling }
\end{picture}
\begin{tikzpicture}[overlay]
\path(0pt,0pt);
\filldraw[color_283006][even odd rule]
(93.02pt, -197.98pt) -- (202.6pt, -197.98pt)
 -- (202.6pt, -197.98pt)
 -- (202.6pt, -186.34pt)
 -- (202.6pt, -186.34pt)
 -- (93.02pt, -186.34pt) -- cycle
;
\end{tikzpicture}
\begin{picture}(-5,0)(2.5,0)
\put(93.02,-195.7){\fontsize{9.96}{1}\usefont{T1}{cmr}{m}{it}\selectfont\color{color_63553}and analysis. Routledge. }
\end{picture}
\begin{tikzpicture}[overlay]
\path(0pt,0pt);
\filldraw[color_283006][even odd rule]
(93.02pt, -211.42pt) -- (477.33pt, -211.42pt)
 -- (477.33pt, -211.42pt)
 -- (477.33pt, -198.82pt)
 -- (477.33pt, -198.82pt)
 -- (93.02pt, -198.82pt) -- cycle
;
\end{tikzpicture}
\begin{picture}(-5,0)(2.5,0)
\put(75.024,-209.26){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}2. Horvat, T., \& Job, J. (2020). The use of machine learning in sport outcome prediction: A }
\end{picture}
\begin{tikzpicture}[overlay]
\path(0pt,0pt);
\filldraw[color_283006][even odd rule]
(93.02pt, -223.9pt) -- (506.49pt, -223.9pt)
 -- (506.49pt, -223.9pt)
 -- (506.49pt, -212.26pt)
 -- (506.49pt, -212.26pt)
 -- (93.02pt, -212.26pt) -- cycle
;
\end{tikzpicture}
\begin{picture}(-5,0)(2.5,0)
\put(93.02,-221.62){\fontsize{9.96}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_63553}review. Wiley Interdisciplinary Reviews: Data Mining and Knowledge Discovery, 10(5), e1380. }
\end{picture}
\begin{tikzpicture}[overlay]
\path(0pt,0pt);
\filldraw[color_283006][even odd rule]
(93.02pt, -237.34pt) -- (524.01pt, -237.34pt)
 -- (524.01pt, -237.34pt)
 -- (524.01pt, -224.7401pt)
 -- (524.01pt, -224.7401pt)
 -- (93.02pt, -224.7401pt) -- cycle
;
\end{tikzpicture}
\begin{picture}(-5,0)(2.5,0)
\put(75.024,-235.18){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}3. Reilly, T., \& Gilbourne, D. (2003). Science and football: a review of applied research in the football }
\end{picture}
\begin{tikzpicture}[overlay]
\path(0pt,0pt);
\filldraw[color_283006][even odd rule]
(93.02pt, -249.85pt) -- (314.95pt, -249.85pt)
 -- (314.95pt, -249.85pt)
 -- (314.95pt, -238.186pt)
 -- (314.95pt, -238.186pt)
 -- (93.02pt, -238.186pt) -- cycle
;
\end{tikzpicture}
\begin{picture}(-5,0)(2.5,0)
\put(93.02,-247.57){\fontsize{9.96}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_63553}codes. Journal of sports sciences, 21(9), 693-705. }
\end{picture}
\begin{tikzpicture}[overlay]
\path(0pt,0pt);
\filldraw[color_283006][even odd rule]
(93.02pt, -263.29pt) -- (519.09pt, -263.29pt)
 -- (519.09pt, -263.29pt)
 -- (519.09pt, -250.69pt)
 -- (519.09pt, -250.69pt)
 -- (93.02pt, -250.69pt) -- cycle
;
\end{tikzpicture}
\begin{picture}(-5,0)(2.5,0)
\put(75.024,-261.13){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}4. Greenhough, J., Birch, P. C., Chapman, S. C., \& Rowlands, G. (2002). Football goal distributions }
\end{picture}
\begin{tikzpicture}[overlay]
\path(0pt,0pt);
\filldraw[color_283006][even odd rule]
(93.02pt, -275.65pt) -- (517.65pt, -275.65pt)
 -- (517.65pt, -275.65pt)
 -- (517.65pt, -264.13pt)
 -- (517.65pt, -264.13pt)
 -- (93.02pt, -264.13pt) -- cycle
;
\end{tikzpicture}
\begin{picture}(-5,0)(2.5,0)
\put(93.02,-273.49){\fontsize{9.96}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_63553}and extremal statistics. Physica A: Statistical Mechanics and its Applications, 316(1-4), 615-624. }
\end{picture}
\begin{tikzpicture}[overlay]
\path(0pt,0pt);
\filldraw[color_283006][even odd rule]
(93.02pt, -289.09pt) -- (511.41pt, -289.09pt)
 -- (511.41pt, -289.09pt)
 -- (511.41pt, -276.49pt)
 -- (511.41pt, -276.49pt)
 -- (93.02pt, -276.49pt) -- cycle
;
\end{tikzpicture}
\begin{picture}(-5,0)(2.5,0)
\put(75.024,-286.93){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}5. Rudin, P. (2016). Football result prediction using simple classification algorithms, a comparison }
\end{picture}
\begin{tikzpicture}[overlay]
\path(0pt,0pt);
\filldraw[color_283006][even odd rule]
(93.02pt, -301.57pt) -- (326.59pt, -301.57pt)
 -- (326.59pt, -301.57pt)
 -- (326.59pt, -290.05pt)
 -- (326.59pt, -290.05pt)
 -- (93.02pt, -290.05pt) -- cycle
;
\end{tikzpicture}
\begin{picture}(-5,0)(2.5,0)
\put(93.02,-299.41){\fontsize{9.96}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_63553}between k-Nearest Neighbor and Linear Regression. }
\end{picture}
\begin{tikzpicture}[overlay]
\path(0pt,0pt);
\filldraw[color_283006][even odd rule]
(93.02pt, -315.01pt) -- (519.93pt, -315.01pt)
 -- (519.93pt, -315.01pt)
 -- (519.93pt, -302.41pt)
 -- (519.93pt, -302.41pt)
 -- (93.02pt, -302.41pt) -- cycle
;
\end{tikzpicture}
\begin{picture}(-5,0)(2.5,0)
\put(75.024,-312.85){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}6. Huang, K. Y., \& Chen, K. J. (2011). Multilayer perceptron for prediction of 2006 world cup football }
\end{picture}
\begin{tikzpicture}[overlay]
\path(0pt,0pt);
\filldraw[color_283006][even odd rule]
(93.02pt, -327.49pt) -- (318.79pt, -327.49pt)
 -- (318.79pt, -327.49pt)
 -- (318.79pt, -315.97pt)
 -- (318.79pt, -315.97pt)
 -- (93.02pt, -315.97pt) -- cycle
;
\end{tikzpicture}
\begin{picture}(-5,0)(2.5,0)
\put(93.02,-325.33){\fontsize{9.96}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_63553}game. Advances in Artificial Neural Systems, 2011. }
\put(75.024,-338.77){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791}7. https://www.kaggle.com/datasets/martj42/international-football-results-from-1872-to-2017 }
\end{picture}
\begin{tikzpicture}[overlay]
\path(0pt,0pt);
\filldraw[color_37858][even odd rule]
(93.02pt, -340.69pt) -- (506.49pt, -340.69pt)
 -- (506.49pt, -340.69pt)
 -- (506.49pt, -339.97pt)
 -- (506.49pt, -339.97pt)
 -- (93.02pt, -339.97pt) -- cycle
;
\end{tikzpicture}
\begin{picture}(-5,0)(2.5,0)
\put(93.02,-353.29){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\put(57.024,-375.85){\fontsize{11.04}{1}\usefont{T1}{cmr}{m}{n}\selectfont\color{color_29791} }
\end{picture}
\end{document}
