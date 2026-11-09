# Burger Shop Console App

## Overview

This C++ simulation follows a burger shop from both sides of the counter. A customer can browse the menu and place an order, while a manager can look up menu items and update prices, ratings, and records. An order queue models the handoff from customer to kitchen, and CSV files give the app a way to retain menu, customer, and chef data between runs.

## How it’s built

- **Console workflows.** [BurgerShop.cpp](BurgerShop.cpp) contains the customer and manager menus, along with input validation and menu actions.
- **Domain modeling.** Separate structures represent customers, chefs, and burgers. [QueueOrders.h](QueueOrders.h) models pending orders.
- **Persistence.** [CSVManip.h](CSVManip.h) uses the bundled rapidcsv library to load and update records.

## Run or explore locally

The project includes a CMake configuration and sample CSV files in `cmake-build-debug/`. Before building on another machine, update the original machine’s absolute paths in `CMakeLists.txt` and `CSVManip.h` to point to your local project and sample data.
