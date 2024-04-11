# Hands-on Lab: Security Copilot with Microsoft Intune 
## Overview
In this lab, you will learn how to use Security Copilot, a feature of Microsoft Intune that helps you to assess and improve the security posture of your devices. You will use Security Copilot to view the security score of your devices, apply security recommendations, and monitor the impact of your actions.
## Prerequisites
To complete this lab, you will need:
- A Microsoft 365 E5 or Microsoft 365 Business Premium subscription with Intune enabled.
- A Windows 10 device enrolled in Intune.
- A device administrator account with the Intune role of Security administrator or Global administrator.
## Exercise 1: View the security score of your devices
In this exercise, you will use Security Copilot to view the security score of your devices and see how they compare to the industry average and the Microsoft recommended baseline.
1. Sign in to the Microsoft Endpoint Manager admin center at [URL].
2. In the navigation pane, select **Devices** > **Security Copilot**.
3. On the Security Copilot dashboard, you will see the following information:
- The **Security score** of your devices, which is calculated based on the security settings and configurations applied to them. The score ranges from 0 to 100, with higher scores indicating better security posture.
- The **Industry average** score, which is based on the aggregated data from other organizations that use Security Copilot.
- The **Microsoft recommended** score, which is based on the best practices and guidance from Microsoft.
- The **Security recommendations** that you can apply to improve your security score. Each recommendation has a description, an impact level, and a score increase value.
- The **Security score history** chart, which shows the trend of your security score over time.
- The **Device security groups** table, which shows the security score and the number of devices for each device group that you have created or assigned in Intune.
4. Review the information on the dashboard and note the following:
- How does your security score compare to the industry average and the Microsoft recommended score?
- Which security recommendations have the highest impact and score increase value?
- Which device groups have the lowest or highest security score?
## Exercise 2: Apply security recommendations
In this exercise, you will use Security Copilot to apply security recommendations to your devices and see how they affect your security score.
1. On the Security Copilot dashboard, select a security recommendation that you want to apply. For example, you can select **Require BitLocker** to encrypt the device drives.
2. On the recommendation details page, you will see the following information:
- The **Description** of the recommendation, which explains why it is important and how it works.
- The **Impact** level of the recommendation, which indicates how much it will affect the user experience and the device performance.
- The **Score increase** value of the recommendation, which shows how much it will improve your security score if you apply it to all devices.
- The **Affected devices** table, which shows the devices that are not compliant with the recommendation and their security score.
- The **Remediation steps** that you can follow to apply the recommendation to your devices. The steps may vary depending on the type of the recommendation and the device platform.
3. Follow the remediation steps to apply the recommendation to your devices. For example, if you selected **Require BitLocker**, you can do the following:
- In the remediation steps, select **Create a new policy**.
- On the Create a policy page, select **Windows 10 and later** as the platform and **Endpoint protection** as the profile type, and then select **Create**.
- On the Basics page, enter a name and a description for the policy, and then select **Next**.
- On the Configuration settings page, expand the **BitLocker** section and configure the settings as you want. For example, you can enable **Require device encryption** and **Enforce drive encryption type on operating system drives**.
- Select **Next** and then **Create** to create the policy.
- On the Assignments page, select the device groups that you want to apply the policy to, and then select **Next** and **Save** to assign the policy.
4. After you apply the recommendation, go back to the Security Copilot dashboard and refresh the page. You will see that your security score has increased and the recommendation status has changed to **In progress** or **Resolved** depending on the number of devices that are compliant with the recommendation.
5. Repeat steps 1 to 4 for other security recommendations that you want to apply to your devices.
## Exercise 3: Monitor the security score impact
In this exercise, you will use Security Copilot to monitor the impact of your actions on the security score of your devices and see how they affect the industry average and the Microsoft recommended score.
1. On the Security Copilot dashboard, select the **Security score history** chart.
2. On the Security score history page, you will see the following information:
- The **Security score history** chart, which shows the trend of your security score over time. You can select a time range from the drop-down list or use the slider to zoom in or out.
- The **Security score breakdown** table, which shows the security score and the number of recommendations for each category of security settings. You can select a category to see the details of the recommendations.
- The **Security score impact** table, which shows the security score and the number of devices for each action that you have taken to apply or remove a security recommendation. You can select an action to see the details of the recommendation and the affected devices.
3. Review the information on the page and note the following:
- How has your security score changed over time?
- Which categories of security settings have the most or least impact on your security score?
- Which actions have the most or least impact on your security score?
- How does your security score compare to the industry average and the Microsoft recommended score?
## Summary
In this lab, you have learned how to use Security Copilot to assess and improve the security posture of your devices. You have used Security Copilot to view the security score of your devices, apply security recommendations, and monitor the impact of your actions. You have also compared your security score to the industry average and the Microsoft recommended score. You can use Security Copilot to continuously monitor and enhance the security of your devices and protect them from threats.

