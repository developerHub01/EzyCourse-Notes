- **Create:**
	- Do not have any special extra fields

- **Settings:**
	- **Phase management**
		- Phase ordering
		- Client Phase Switching
			- One time payment user always can switch
			- Other
				- **Yes - Allow clients to switch phases**
				- **No - Restrict clients to their selected phase** (Default)

	- **Premium content access control**
		- **Course Access & Billing Rules**
			- **One-Time Users:** Permanent access to everything. No restrictions.
			- **Subscribers:** Access depends on active payment dates and whether past-content access is toggled on.
			    - _Overlap:_ If a chapter touches an active paid window by even one day, it unlocks.
			    - _Gaps:_ If it falls entirely between unpaid dates, it locks (unless "Yes" is selected for past content).
		- **The Two Access Settings**
			- **Yes (Allow previous content):** Subscribers can view everything from their start date to today, skipping payment gaps.
			- **No (Strict paid periods):** Subscribers only see content matching active payment dates. (**Default**)
		- **Step-by-Step Chapter Calculations**

	- **Pregnancy Phase**
	    1. **Determine the Due Date:** Use one of three methods based on available data:
	        - _Last Period Date:_ Add **280** days (e.g., June 1 $\rightarrow$ March 8).
	        - _Conception Date:_ Add **266** days (e.g., July 15 $\rightarrow$ April 7).
	        - _Doctor's Prediction:_ Use the exact date provided.
	    2. **Calculate Remaining Time:** `Days remaining = Due date − Today's date`
	    3. **Calculate Progress & Chapter:**
	        - `Days pregnant = 280 − Days remaining`
	        - `Current chapter = Days pregnant ÷ 7` (always **round up**) 
	        - _Example:_ 273 days pregnant $\div$ 7 = Chapter 38.
	        
	- **Postpartum Phase**
	    1. **Calculate Elapsed Time:** `Days since birth = Today's date − Birth date`
	    2. **Calculate Chapter:** `Current chapter = Days since birth ÷ 7` (always **round up**)
	        - _Example:_ 15 days since birth $\div$ 7 = Chapter 3 (since 2.14 rounds up to 3).

	- **Other Phases (General Enrollment)**
	    1. **Calculate Elapsed Time:** `Days since enrollment = Today's date − Enrollment date`
	    2. **Calculate Chapter:** `Current chapter = Days since enrollment ÷ 7` (always **round up**)
	        - _Example:_ 20 days since enrollment $\div$ 7 = Chapter 3 (since 2.85 rounds up to 3).

	- **Task & Exercise Submissions**
		- **Task & Exercise Submission Policy Implementation**
			- **Yes:** Submit anytime for any past chapter (flexible, catch-up friendly).
			- **No:** Current chapter only, past chapters lock after moving forward (strict deadlines).

	- **Right side UI visibility control**
		- **Show right sidebar** - Toggle (Default: Enabled) 
		- Have preview

- **Clients:**
	- Here admin can search and filter based on
		- Name
		- Time
			- Today
			- Last Week
			- Last Month
			- Last Year
			- All Time
		- Phases
			- Phase 1
			- Phase 2 
			- All Phases
	- For each clients have
		- Notes
		- Enrollment Details
			- ![[Pasted image 20260911143310.png]]

- **Facts:**
	- 1 chapter = 7 days
		- Means each chapter is a lesson
		- And can only access current week chapters not future even if purchased. 
	- Lesson can be paid or free
		- Paid lesson only matter for subscription gap.
	- Can't move or clone any lesson
	- Each lesson have following options
		- Edit
		- Make Free/Premium
		- Disable discussion
		- Delete
	- On enroll and phase selection in pregnant
		- Based on pregnancy related info it calculate the current weeks and assign that week (chapter) as current.
		- So if in subscription for monthly even though 4 weeks fall in a months but student can't access future purchased weeks until that weeks start.
	- ![[Pasted image 20260911142719.png]]