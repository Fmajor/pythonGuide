# A python introduction

# homework1

* this homework is to test your skills to use basic python syntax and tools, so do **not** use packages like numpy or pandas to parse the file (we will use them in the next lecture)
* before doing this homework, you should
    * understand all the python syntax in lecture1
    * search google (or bing or baidu...) and learn to use the "time" and "timedate" package
    * search google (or bing or baidu...) and learn to use the "format" function, which is an method of Class String.
```
we have a datafile of one variabe star, the first few lines is the header (or meta data) of this file,
    which record the basic information of this variable star and the format of the latter data.

you need to:
    define a class named VariableStar, then use the data file name to init it and get a instance.
        like this:   someSpecificVariableStar = VariableStar("data1.txt")
        Tips: use string method "stripe", "split"

    parse all the information into properties of this class.
        For example, I want to use someSpecificVariableStar.name to get the name of this variable

    store all the data into one dict: self.data
        store V band magnitudes in to self.data["V"] and so on for other bands
            you should store the magnitudes in type float (not in string)

    make some magic function, so
        I can use someSpecificVariableStar["V"] to get a list of V band magnitude
        I can use len(someSpecificVariableStar) to get the length of the data

    define a function name "print"
        so i can use someSpecificVariableStar.print() to print all the data in format like:
            name: <name of the star>
            time                      U            V            B
            2014-11-23T10:23:10
            ......
        use "nan" in the print for missing data
        try to align your print in proper way

    write Docs

    write a Demo to show that all the requirements are satisfied
```
# homework2
* before doing this homework, you should
    * learn to use numpy and pandas to parse tables files
    * learn to use astropy

```
    modify your VariableStar, now you can use pandas to parse the file

    use matplotlib
    add function "plot" into class VariableStar, so
        I can use someSpecificVariableStar.plot() to get a beautiful plot of time v.s. all bands
        I need the sticks of the x axis to be in format of 2014-11-23T10:23:10

    use astropy
    add function "plotInMJD"
        make a plot the same as in function "plot", except that the x axis is MJD

    add function "getRaDec"
        return (ra, dec) of the star
    add function "getLB"
        return the galactic coordinates of the star

    add another function of your like...
        for example, you can write a function to get the median value of magnitude of all the bands

    write Docs

    write a Demo to show that all the requirements are satisfied
```
