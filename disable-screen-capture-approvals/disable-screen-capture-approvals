#!/bin/sh

PLIST_FILE="$HOME/Library/Group Containers/group.com.apple.replayd/ScreenCaptureApprovals.plist"

/usr/bin/xmllint  --xpath '//key/text()' "$PLIST_FILE" | while read -r key; do 

    /usr/libexec/PlistBuddy -c "Set ':$key' 'Mon Jan 01 12:34:56 2345'" "$PLIST_FILE"
    echo "Finished stopping '$key' reminder."

done
