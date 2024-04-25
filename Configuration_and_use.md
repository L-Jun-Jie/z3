# Configuration and use

‍

# 1. Installation and Uninstallation

## 1.1 Installation

General Installation Method:

```bash
python3 scripts/mk_make.py
cd build
make
sudo make install
```

You can select the installation path:

```bash
python3 scripts/mk_make.py --prefix=/home/leo
cd build
make
make install
```

Installation can be done in `debug`​ mode.

```bash
python3 scripts/mk_make.py --debug --trace
cd build
make
sudo make install
```

See `mk_make.py`​ for optional commands:

​`python3 scripts/mk_make.py -h`​

## 1.2 Uninstallation

```bash
cd build
sudo make uninstall
```

Cleans up an environment that has been polluted by python scripts:

​`git clean -fx src`​

# 2. Optional trace options

```bash
    /* assumptions */
    Z3_enable_trace("assumptions");
    Z3_enable_trace("internalize_assertions");
    Z3_enable_trace("after_internalization");
    Z3_enable_trace("internalize_assertion");
    Z3_enable_trace("internalize_assertion_ll");
    Z3_enable_trace("generation");

    /* search */
    Z3_enable_trace("literal_occ");
    Z3_enable_trace("after_init_search");
    Z3_enable_trace("before_search");
    Z3_enable_trace("search");
    Z3_enable_trace("search_lite");
    Z3_enable_trace("search_detail");
    Z3_enable_trace("bounded_search");
    Z3_enable_trace("after_search");
    Z3_enable_trace("search_bug");

    /* decide */
    Z3_enable_trace("decide");
    Z3_enable_trace("decide_detail");
    Z3_enable_trace("random_split");

    /* assign */
    Z3_enable_trace("guessed_literals");
    Z3_enable_trace("assign_core");
    Z3_enable_trace("phase_selection");

    /* propagate */
    Z3_enable_trace("propagate");
    Z3_enable_trace("propagate_atoms");
    Z3_enable_trace("propagate_eqs");
    Z3_enable_trace("after_first_propagate");

    Z3_enable_trace("final_check_result");
    Z3_enable_trace("solver_na2as");
    Z3_enable_trace("set_conflict");
    Z3_enable_trace("theory_case_split");
    Z3_enable_trace("activity_profile");
    Z3_enable_trace("assigned_literals_per_lvl");
    Z3_enable_trace("guessed_literals");
```

‍
