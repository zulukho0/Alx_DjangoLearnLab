# Permissions and Groups Setup

- Custom permissions added to Book model: can_view, can_create, can_edit, can_delete
- Groups created:
  - Viewers: can_view
  - Editors: can_create, can_edit
  - Admins: all permissions
- Views protected using @permission_required
- Users assigned to groups via Django Admin or shell

# Security Best Practices

- DEBUG disabled in production
- CSRF and session cookies secured
- XSS and clickjacking protections via headers
- All forms include {% csrf_token %}
- ORM used for all queries; raw SQL avoided
- CSP headers configured via django-csp
