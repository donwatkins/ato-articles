# The case for open source solutions in HIPAA

Using an open source approach to find a balance between performance, compliance, and cost.

**By Don Watkins**  
**Published:** November 21, 2024  
**Source:** [https://allthingsopen.org/articles/the-case-for-open-source-solutions-in-hipaa](https://allthingsopen.org/articles/the-case-for-open-source-solutions-in-hipaa)

<figure class="featured">
<img src="https://allthingsopen.org/wp-content/uploads/2024/08/escalator-red-compliance-e1724864082881.jpg" class="featured" alt="Escalator with red lights" />
<figcaption>Image by <a href="https://pixabay.com/users/kaipilger-5841200/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=3010870">Kai Pilger</a> from <a href="https://pixabay.com//?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=3010870">Pixabay</a></figcaption>
</figure>

A recent task involved assisting a healthcare professional with upgrading their computer system. The goal was to provide a more robust solution that offers redundant backup, both onsite and in the cloud that is [HIPAA compliant](https://www.hhs.gov/hipaa/for-professionals/index.html) (HIPAA is a United States national standard that protects individual medical records and other health information.) The current system, a 2017 13-inch MacBook Air, needs this upgrade. Given Apple’s proprietary approach to computing platforms, the challenge is finding the best options within a budget.

Initially, I recommended a newer MacBook Air with a 512-gigabyte solid-state drive, Apple’s proprietary TimeMachine backup system for on-premise backup, and proprietary cloud solutions that are HIPAA-compliant, such as Microsoft OneDrive or Google Drive. It is noteworthy that iCloud is not HIPAA-compliant. Then, I began to think about this solution and had an epiphany. Why not open source?

## Using an open source approach

Based on my experience with open source systems, a new computer running any popular distribution could be a compelling choice for your upgraded system. If HIPAA compliant, such a system could offer a longer lifespan and better meet the project parameters. Options like a new Linux laptop from System76, Dell XPS developer edition, or a similarly configured machine running almost any version of Linux could provide a lifespan of up to ten years, ensuring the system’s relevance and efficiency for years to come.

Using such a system would provide the most optimal memory and storage solutions while maximizing the total cost of ownership. Eight to sixteen gigabytes of RAM with a 512 GB or 1 TB NVME drive, possibly connected to a dock and an external display, would be affordable and sufficient for most healthcare professionals’ needs.

## Finding a back-up solution

Combine this with an external USB drive with TimeShift, Cronopete, or another open source incremental backup solution would be ideal for additional data backup and security. These solutions work by creating regular, incremental backups of your data, ensuring that even if a file is lost or corrupted, you can quickly restore it from a previous backup.

Proprietary cloud solutions like OneDrive and Google Drive could be replaced by <a href="https://nextcloud.com/compliance/" target="_blank" rel="noreferrer noopener">NextCloud</a>, which is HIPAA compliant. Using these cost-efficient approaches for a back-up solution, ensures that your upgrade is not only high-performing, but also financially viable.

## Using open formats for long-term viability

My client is currently keeping client journal entries with Apple Pages. To transition to a more open format, it’s easy to convert those documents to LibreOffice Writer. Open the documents in LibreOffice Writer and then save them in open document format. This process ensures the long-term viability of the document and the information contained therein as it moves from a proprietary format to an open format, providing you with a secure and future-proof solution. This transition to an open format should reassure you about the data’s long-term viability.

## Conclusion

In conclusion, upgrading a healthcare professional’s computer system requires a thoughtful balance between performance, compliance, and cost. While Apple’s proprietary systems, such as the 15-inch MacBook Air, offer a solid performance, their limitations in terms of aftermarket upgrades and HIPAA compliance necessitate exploring alternative solutions.

The potential for a longer-lasting, more versatile setup with a Linux-based system provides an attractive option for both cost efficiency and system longevity. By integrating robust open source tools for backup and storage, such as NextCloud and incremental backup solutions, the system can meet HIPAA compliance requirements while ensuring data security and ease of access. This balanced approach instills confidence in the overall upgrade strategy.

Additionally, transitioning from proprietary formats to open ones, like converting Apple Pages documents to LibreOffice Writer, will safeguard the long-term usability and integrity of important client information. Overall, while the initial investment might be higher with Linux-based solutions and open source software, the benefits of flexibility, extended lifespan, and compliance make it a prudent choice for a healthcare setting.

Embracing these solutions enhances system reliability and aligns with best data management and security practices, ensuring a resilient and future-proof setup for the years to come.

</div>

---

<div class="cc-license">

<a href="https://creativecommons.org/licenses/by-sa/4.0/" rel="license"><img src="https://allthingsopen.org/wp-content/themes/ato-main-2024/img/cc/by-sa.png" title="This work is licensed under a Creative Commons Attribution-Share Alike 4.0 International License." alt="Creative Commons License" /></a>

This work is licensed under a Creative Commons Attribution-Share Alike 4.0 International License.

