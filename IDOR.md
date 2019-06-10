# IDOR Tips
1. TRY HPP
2. Try URL Path Permutations

        * /api/users/user@email.com -> /api/users/..%2Fuser@email.com
        * /api/account/123/ -> /api/account/..%2F..%2F123
