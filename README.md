# Development process on Github

This document describes development process on github, issues assignment and changes management.


![development flow](http://g.gravizo.com/g?
  digraph G {
    aize ="4,4";
    start [shape=box];
    start -> issue_assigned;
    issue_assigned -> issue_in_progress;
    issue_in_progress -> issue_implemented;
    issue_implemented -> issue_code_review;
    issue_code_review -> issue_done [color=green];
    issue_code_review -> issue_in_progress [color=red,style=dotted,label="fix required"];
    issue_assigned [label="issue assigned to developer"];
    issue_in_progress [label="developer is working on issue:\\nset label state:in progress"];
    issue_implemented [label="task implemented:\\ncreate pull request\\nre-assigne issue\\PR to manager\\nset label state:ready4test"];
    issue_done [shape=box,label="DONE\\nissue is on manager\\nmanager will close issue"]
    issue_code_review [label="Code review \\nby other team member or by manager"];
  }
)
