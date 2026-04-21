# Role-Permission Matrix Template

**System Name:** [System Name]  
**Last Updated:** [Date]  
**Owner:** [System Owner Name]  

## Instructions

Fill in each cell with the permission level for that role. Use:
- **F** = Full access (create, read, update, delete)
- **R** = Read only
- **W** = Write (create + update, no delete)
- **N** = No access
- **A** = Approve only (no direct data access)

## Role Definitions

| Role | Description | Typical Department |
|------|-------------|-------------------|
| Admin | Full system configuration and user management | IT |
| Manager | Approve requests, view reports, manage team data | Department heads |
| Editor | Create and modify records within their scope | Operational staff |
| Viewer | Read-only access to reports and dashboards | Cross-functional |
| Auditor | Read-only access to all data + audit logs | Security / Compliance |

## Permission Matrix

| Module / Feature | Admin | Manager | Editor | Viewer | Auditor |
|-----------------|-------|---------|--------|--------|---------|
| User Management | F | N | N | N | R |
| System Configuration | F | N | N | N | R |
| Records — Own Department | F | F | W | R | R |
| Records — Other Departments | F | R | N | N | R |
| Reports & Dashboards | F | R | N | R | R |
| Audit Logs | F | N | N | N | R |
| Approval Workflows | F | A | N | N | R |
| Data Export | F | R | N | N | R |
| API Access | F | N | N | N | N |

## Notes

- Admin role should be limited to IT staff only
- Manager approval is required before granting Editor or higher access
- Auditor role is read-only by design — no write permissions under any circumstance
- Review this matrix quarterly and after any major system update
