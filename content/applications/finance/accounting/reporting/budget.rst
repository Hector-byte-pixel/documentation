================
Analytic budgets
================

:guilabel:`Analytic Budgets` track and forecast specific activities, helping businesses make
informed decisions about internal operations. They allow for allocating and tracking income and
expenses in detail, breaking down costs and revenues by specific projects, departments, or
activities. Analytic budgets can be applied across various departments or projects to measure
profitability and performance. Odoo manages analytic budgets using
:doc:`analytic accounting <analytic_accounting>`.

.. note::
   :guilabel:`Financial budgets`, available in the :guilabel:`Profit and Loss` report, are linked to
   the general ledger and focus on the company’s overall economic position. They are structured
   around specific accounts and transactions for official financial reporting and compliance
   purposes.

.. _accounting/reporting/analytic-budget/configuration:

Configuration
=============

Go to :menuselection:`Accounting --> Configuration --> Settings`, and enable
:guilabel:`Budget Management` in the :guilabel:`Analytics` section.

.. _accounting/reporting/analytic-budget/analytic-accounting:

Analytic accounting
===================

Odoo structures budgets using :ref:`accounts <analytic_accounting/analytic_plans>` and
:ref:`accounts <accounting/analytic_accounting/analytic_accounts>`, which must be configured
*before* creating a budget.

.. _accounting/reporting/analytic-budget/budget:

Set a budget
============

To create a new budget, go to :menuselection:`Accounting --> Analytic Budgets` and click
:guilabel:`New`.
Make sure the following fields are appropriately completed: :guilabel:`Budget Name`,
:guilabel:`Period`, and :guilabel:`Budget Type`.

Click :guilabel:`Add a line` in the :guilabel:`Budget Lines` tab to structure the budget according
to the analytic plans and accounts previously created.
While the analytic plans correspond to the column names, select the analytic accounts to define the
budget lines and set the chosen amounts for each in the :guilabel:`Budgeted` column. Once all the
budget lines are settled, click :guilabel:`Open`.
If changes need to be done once the budget is in the :guilabel:`Open` status, there are two options:

- :guilabel:`Reset to Draft`: To overwrite the data, then reopen the budget.
- :guilabel:`Revise`: A new budget will be created. Once it is set to the :guilabel:`Open` status,
  Odoo will add a :guilabel:`Rev` reference to the :guilabel:`Budget name`. The original budget has
  then the :guilabel:`Revised` status.

.. _accounting/reporting/analytic-budget/budget-check:

Check a budget
==============

Once the budget is in the :guilabel:`Open` status, two additional columns are available:
:guilabel:`Committed` and :guilabel:`Achieved`. Their amounts are automatically calculated based on
the vendor bills/invoices and their related analytic distribution. They evolve when a new journal
entry linked to the analytic account is created. The :guilabel:`Achieved` amount reflects the
current result according to the expenses or income for the associated analytic account. In contrast,
the :guilabel:`Committed` amount displays what has already been purchased or sold, regardless of
whether it has been billed or invoiced.

.. note::
   For budgets in the :guilabel:`Open` status, when a purchase order created with the associated
   analytic distribution exceeds the amount budgeted, the related purchase order line turns red.

To reveal the :guilabel:`Theoretical` amount or percentage, use the :icon:`oi-settings-adjust`
(:guilabel:`settings adjust`) icon in the far right of the budget top row. The
:guilabel:`Theoretical` represents the amount of money that could theoretically have been spent or
should have been received based on the date.
To open the reporting view, click :guilabel:`Details` and filter the budget lines and columns of
the pivot table.

.. image:: budget/budget.png
   :alt: open budget with committed, achieved and theoretical amounts

.. note::
   Deletion of a budget is only allowed in the :guilabel:`Draft` and :guilabel:`Cancelled` stages.

To view all the different budget lines directly from the :guilabel:`Budgets` view, select the
:guilabel:`Budget Name` and click :guilabel:`Budget Lines`.

.. _accounting/reporting/analytic-budget/budget-generate:

Generate periodical budgets
---------------------------

The :guilabel:`Generate` option allows the creation of multiple budget periods. To do so, select the
budget and click :guilabel:`Generate` to open the :guilabel:`Generate Budget` window. Set the dates,
select the :guilabel:`Period` and the :guilabel:`Analytic Plans`, then click :guilabel:`Split`.

.. image:: budget/generate-budgets.png
   :alt: all the options to generate periodical budgets

.. _accounting/reporting/analytic-budget/budget-reporting:

Reporting
=========

To perform various reporting actions, go to :menuselection:`Accounting --> Reporting -->
Budget Report`, then:

- Track, analyze, and compare budget data.
- Filter and group Data using the :icon:`fa-plus-square` (:guilabel:`plus-square`) or
  :icon:`fa-minus-square` (:guilabel:`minus-square`) icon.
- Drill down into the report to see more detail on the actual amounts and transactions.
- Export for further analysis or reporting needs.
