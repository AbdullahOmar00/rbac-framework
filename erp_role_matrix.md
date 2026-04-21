# ERP System — Role-Permission Matrix

**System:** Enterprise Resource Planning (Sample)  
**Last Updated:** January 2025  
**Owner:** IT Department  

## Roles

| Role | Description | Assigned To |
|------|-------------|-------------|
| ERP_Admin | Full system access, user management, configuration | IT team only |
| Finance_Manager | Approve transactions, view all finance reports | Finance department heads |
| Finance_Editor | Create and edit invoices, POs, journal entries | Finance staff |
| Finance_Viewer | Read-only access to finance reports | Cross-functional managers |
| HR_Editor | Manage employee records within HR module | HR staff |
| HR_Viewer | View employee directory (no salary data) | All departments |

## Permission Matrix

| Module | ERP_Admin | Finance_Manager | Finance_Editor | Finance_Viewer | HR_Editor | HR_Viewer |
|--------|-----------|-----------------|----------------|----------------|-----------|-----------|
| System Config | F | N | N | N | N | N |
| User Management | F | N | N | N | N | N |
| Invoices | F | A | W | R | N | N |
| Purchase Orders | F | A | W | R | N | N |
| Journal Entries | F | A | W | R | N | N |
| Finance Reports | F | R | R | R | N | N |
| Employee Records | F | N | N | N | W | N |
| Salary Data | F | N | N | N | W | N |
| Employee Directory | F | R | R | R | R | R |
| Audit Logs | F | N | N | N | N | N |

**F** = Full | **W** = Write | **R** = Read | **A** = Approve | **N** = No access

## Access Rules

1. Finance_Editor cannot approve their own transactions — must go through Finance_Manager
2. HR salary data is restricted to HR_Editor and ERP_Admin only
3. ERP_Admin access requires IT Manager approval and is reviewed monthly
4. Finance_Viewer is the default role for non-finance managers who need reporting access
