# MIMWAL Change Log

All notable changes to MIMWAL project will be documented in this file. The "Unreleased" section at the top is for keeping track of important changes that might make it to upcoming releases.

## [Unreleased]

### Added

* Re-branded of FIMWAL "2" version 2.15.1016.0 as MIMWAL.
	* AICs are updated to a "WAL: " prefix instead of "FIMWAL: ".
	* The event log  ane changed from "FIMWAL" to "WAL".
* Added design time check for the Activity Execution Condition to be a boolean function expression.
	* If in FIMWAL "2" you were using an `IIF` function expression as an Activity Execution Condition, you'll need to wrap it around a `ConvertToBoolean` for UI validation to succeed when making any changes to the activity in future.
* Added support to break iteration loop in `UpdateResources` and `CreateResource` activities.
	* Reserved `$__BREAK_ITERATION__` for the name of the boolean variable that needs to be set to true to break the loop.
* Added support for cascaded queries lookup so that data from the first query can be used in the XPath search filter expression of the second query.

### Changed

* Updated `Add` and `Subtract` function to treat null input values as zero instead of throwing exception
* Made substitutions parameter optional in `NormalizeString` function.

### Removed

* Deleted compiled referenced DLLs and EXEs until LCA provides a split licence.
	* Build and Deployment Wiki documents how to gather these files for building the solution.

### Fixed

* There are no bug fixes in this release.