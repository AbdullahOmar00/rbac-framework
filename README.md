[README.md](https://github.com/user-attachments/files/26930178/README.md)
# RBAC Framework

Templates and examples for designing role-based access control across enterprise systems. Built from real implementation experience managing access governance for 4 systems.

## What's inside

```
rbac-framework/
├── templates/
│   ├── role_matrix_template.md       # Blank role-permission matrix to fill per system
│   └── access_review_checklist.md    # Quarterly access review checklist
├── examples/
│   ├── erp_role_matrix.md            # Example: ERP system role definitions
│   └── least_privilege_policy.md     # Example: Least-privilege access policy
└── README.md
```

## How I use these

When onboarding a new system or running a quarterly access review, I start with the templates and adapt them to the specific platform. The role matrix maps every role to its exact permissions, which makes it easy to spot over-provisioned accounts.

## Key principles

1. **Least privilege** — Users get the minimum access needed for their job function
2. **Separation of duties** — No single role should have both request and approval rights
3. **Regular reviews** — Quarterly reviews catch dormant accounts and role drift
4. **Document everything** — Every access decision should be traceable to a business justification
