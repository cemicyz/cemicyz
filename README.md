```java
package io.github.cemicyz;

import org.jetbrains.annotations.NotNull;

public final class cemicyz extends People {

    @NotNull
    String getName() {
        return "Cem";
    }

    boolean isStudent() {
        return true;
    }

    @NotNull
    String getInterests() {
        return "Java";
    }

    @NotNull
    String getWorkingOn() {
        return "@semicyz";
    }

    @NotNull
    String[] getMailAdresses() {
        return new String[] {"cemicyz@tuta.io", "cemicyz@pm.me"};
    }

    @NotNull
    String getSocialMediaAccount(@NotNull SocialMedia socialMedia) {
        switch (socialMedia) {
            case KEYBASE:
            case TWITTER:
            case STEAM:
            case INSTAGRAM:
                return "cemicyz";
                break;
            case DISCORD:
                return "cemicyz#3610";
				break;
            default:
                return "cemicyz";
				break;
        }
    }

    void onStar(@NotNull StarEvent e) {
        e.getStargazer().sendMessage("Thank You!");
    }
}
```