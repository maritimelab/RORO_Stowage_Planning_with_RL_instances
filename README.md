README: RORO Stowage Problem Data File

This document describes the structure and meaning of the data in the provided text-files for the RORO (Roll-on/Roll-off)
stowage planning problem.

General Parameters

    nRows: The number of rows in the stowage grid (e.g., 10).
    nCols: The number of columns in the stowage grid (e.g., 15).
    nCargoes: The total number of cargo units to be stowed (e.g., 217).
    nCargoTypes: The number of distinct types of cargo (e.g., 6).
    nPorts: The number of ports involved in the problem (e.g., 4).
    handlingtime: The time required to handle a single cargo unit (e.g., 5).
    noise_perc: The percentage of noise introduced in the forecasted arrival times (e.g., 0.0).
    nintervals: The number of time intervals considered in the problem (e.g., 20).

Port Information

    loadingPorts: A list indicating the loading port for each cargo unit. Each number corresponds to a port ID (e.g., 1, 2, 3).
    dischargePorts: A list indicating the discharge port for each cargo unit. Each number corresponds to a port ID (e.g., 3, 2, 4).

Stowage Grid Layout

    layout: A 2D representation of the stowage grid. Each cell contains a value:
        -2: Indicates restricted or unusable areas.
        -1: Indicates empty stowage position.

Connectivity Information

    adj with (zero index from python): An adjacency list representing the connectivity of cargo units in the grid. Each entry corresponds to a cargo unit,
    and the list contains IDs of other connected cargo units. The last item in the adjacency list contains the entry/exit node.

Time Information

    arrivals: A list of arrival times for each cargo unit. The times are represented as floating-point numbers.
