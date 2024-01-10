step by step 

=> 1 => nano internsctl
=> 2 => isme apne according data change kr lena

cat << 'EOF' > internsctl
#!/bin/bash

# Function to add a new intern
add_intern() {
    echo "Adding a new intern: $1"
    # Logic to add the intern (e.g., create a new user, add to a database, etc.)
}

# Function to list existing interns
list_interns() {
    echo "List of interns:"
    # Logic to display a list of interns
}

# Function to remove an intern
remove_intern() {
    echo "Removing intern: $1"
    # Logic to remove the specified intern (e.g., delete user, remove from database, etc.)
}

# Function to display command usage/help
display_help() {
    echo "Usage: internsctl [add|list|remove] [intern_name]"
    echo "Options:"
    echo "  --help     Display this help message"
    echo "  --version  Display command version"
}

# Function to display command version
display_version() {
    echo "internsctl v0.1.0"
}

# Main script
if [[ "$1" == "--help" ]]; then
    display_help
    exit 0
elif [[ "$1" == "--version" ]]; then
    display_version
    exit 0
fi

case "$1" in
    add)
        add_intern "$2"
        ;;
    list)
        list_interns
        ;;
    remove)
        remove_intern "$2"
        ;;
    *)
        echo "Usage: internsctl [add|list|remove] [intern_name]"
        exit 1
        ;;
esac
EOF
 
 
=> 3 => chmod +x internsctl [give me all parmission]
=> 4 => sudo mv internsctl /usr/local/bin/
=> 5 => sudo mandb
=> Task - 1 => man internsctl
=> Task - 2 => internsctl --help
=> Task -2 => internsctl --version

