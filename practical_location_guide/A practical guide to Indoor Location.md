# A practical guide to Indoor Location

## Highlights

- To effectively utilize location data, it must be part of a packaged solution that provides insight beyond the “where.”
- With so many technologies available and on the horizon, all design considerations must be evaluated to achieve a successful solution.
- Ultra Wideband (UWB) is the industry general gold standard, providing consistent and accurate location.
- Many location systems may only require a proximity solution like a QR code or RFID.
- Existing WiFi systems can be improved to provide sufficiently accurate and consistent location for most applications at a lower cost.

## Introduction

![image.png](A%20practical%20guide%20to%20Indoor%20Location/image.png)

Location data answers the question of “where” and provides an extra dimension to analyze many different processes, exposing new insights that can radically optimize existing processes and have long standing impact within an organization. However, there are many options and considerations to be made when integrating location data into a product, and when implemented improperly, adds bloated, overwhelming, siloed data and quickly becomes a costly waste of time, energy and resources. With the ever increasing number of real time location services (RTLS) solutions and companies in the market, it’s important to address some fundamental questions about your use case before you embark on your location journey.

Purposeful location data enlightens customers to make impactful changes that directly affect their ROI; aimless location becomes an ornamental distraction. The first hurdle to address in the location journey is to find out why you need it, why it matters, and how it directly affects ROI. A workflow optimization solution can drastically increase efficiency and might only require knowledge of location within a zone, whereas loss prevention may require multiple redundant technologies to alert customers to lost equipment. Identifying how location data will create value is crucial to understanding your budget and accuracy needs. For some solutions, even just a QR code can provide enough context to improve efficiency and ROI for next to zero investment. Asking “What do I need my solution to provide that a QR code can’t?” is a good starting point for any location solution.

## Design Considerations

Accuracy, purpose and budget are great first steps to identifying the optimal location solution, but many other factors should be considered before making a decision.

### Location Needs

- **Accuracy:** Determining accuracy is the first step in picking an RTLS solution after identifying the use case as it impacts the project budget significantly.
    - **Region level accuracy:** Sufficient for supply chain transport tracking, region level accuracy can identify which buildings and campuses have been visited and might utilize traditional GPS technologies. Typically a low cost solution.
    - **Zone level accuracy:** With a range of approximately 5-30 meters, zone level accuracy can identify equipment within a section of a building, or when something enters or exits that zone. Typically a low cost solution.
    - **Room level accuracy:** Provides a range of 1-5 meters, or confirms the presence of equipment in a room. Can be implemented at a lower cost, but typically implemented at a moderate cost and requiring specialized location infrastructure.
    - **Sub-meter accuracy:** Useful for finding specific locations of equipment and allows for scope creep in the future using the same location architecture. A sweet spot for most location data applications, but is higher cost and requires significant amounts of specialized infrastructure.
    - **Precision tracking:** Used in specialized cases for precise positioning in automation or tracking specialized workflows. High cost and requires specialized, tuned infrastructure. Usually only useful in a small range.
- **Range:** After determining accuracy, range will determine how far away your RTLS solution will be able to track locations and how much infrastructure you’ll need in a given space. Zone level solutions may just need a few meters, while loss prevention may require a much longer range solution like GPS or LORaWAN.
- **Consistency:** While loss prevention solutions may require high levels of consistency, lots of process optimization workflows may not require perfect accuracy everywhere. Relaxing the consistency constraint can significantly reduce the cost of an RTLS solution.
- **Real-Time need:** Many solutions may not need to know where everything is all of the time. If location can be made available on demand, battery life can be improved significantly.
- **Infrastructure needs:** Some technologies rely on trilateration to resolve location, increasing the number and density of devices needed to reach a location, whereas solutions utilizing advanced location methods like time of flight (ToF), time and/or phase difference of arrival (TDoA/PDoA), and angle of arrival (AoA) may require less infrastructure by being able to determine location with fewer reference points.

### Environmental Needs

- **Indoors or Outdoors:** Knowing the environment your system will be operating in can help determine what systems might be relevant for you. For example, if your system is primarily outdoors, a GPS base station can improve GPS accuracy down to a centimeter scale for a relatively low cost.
- **Surrounding Materials:** Cement, metal and water significantly impact RF signals and can limit the accuracy of 2.4GHz solutions like Bluetooth and Wifi.
- **Hardiness:** What kind of wear and tear might your device be subjected to? IP67 enclosures are dust-tight and water resistant and can be used to protect location hardware from the environment.

### Support

- **Battery life:** How long should the solution last before batteries need to be replaced? If the tracking hardware is difficult to access after deployment, battery life becomes a chief concern and cost figure.
- **Upkeep:** What’s required to keep the system up and running while maintaining a consistent level of accuracy? Some infrastructure heavy solutions may require lots of tweaks to maintain performance.
- **Development/Integration Time:** How long will it take to integrate location data into your product? Many systems represent their data in custom Cartesian coordinates, adding complexity to data conversion between reference systems. Custom solutions may be tailored to your needs but also tie up development teams for years supporting just the location aspect of the product.
- **Cost Structure:** There are many costs in an RTLS system which affect system scalability and the overall bottom line, including:
    - **Tags:** devices that report location on some interval.
    - **Gateways:** Devices that communicate with the tags and the backend system to provide a grounded reference point and report locations to the backend.
    - **SaaS fees:** Many RTLS solutions include large SaaS fees to support the hardware.

## A Brief Summary of the RTLS Space

Basic Visual Comparison of RF Technologies

![](A%20practical%20guide%20to%20Indoor%20Location/image18.jpg)

There are many technologies available for providing location data, each with their own niche. A brief survey of the available technologies is provided below.

Table 1: Comparison of RF Location Technologies

| Type | Accuracy | Max Range | Cost | Infrastructure needs | Maturity |
| --- | --- | --- | --- | --- | --- |
| Ultra Wideband (UWB) | Sub-meter to Precision Level | 10-200 meters | High | Moderate | Early Adoption |
| Bluetooth Low Energy (BLE) | Zone to Room Level | 30-200 meters | Low to Medium | High | Developed |
| Wifi | Zone to Room Level | 50 meters | Low | Moderate | Developed |
| Passive RFID/NFC | Zone to Room Level | Proximity | Low | Moderate | Developed |
| Cellular 5G/mmWave | Zone to Precision | 1 kilometer | High | Low | Evangelist |
| LoRaWAN | Region to Zone Level | 1-5 km | Low | Low | Developed |
| Proprietary | Zone to Precision | 100 meters (varies) | Varies | Varies | Developed |

### RF Technologies

- **UWB:** The current gold standard for RTLS solutions, UWB provides precise, consistent accuracy and is more resistant to interference and multipath effects. It does what you expect it to do and is easily integrated into mobile workflows as UWB chips have been added to most current generation phones.
- **BLE:** BLE RTLS solutions have been leading the market for quite some time due to their versatility, low power consumption, and moderate accuracy. However, UWB does a lot of the things BLE does, just better. They also require a large amount of specialized infrastructure, which can be a hard sell, especially compared to WiFi solutions that provide a more general benefit and greater connectivity to all.
- **WiFi:** WiFi location can leave a lot to be desired, as access points are typically placed too far apart to provide good location fidelity. However, when combined with sensor fusion and fingerprinting techniques, room level accuracy can be achieved with a good amount of consistency without having to add any infrastructure. Even then, adding more WiFi access points tends to bring other benefits than just an accurate RTLS system and can be an easier sell.
- **RFID/NFC:** Passive RFID tags don't require a battery and can last a long time as a result. Range is dependent on the scanners, but is typically less than 1 meter. Proximity solutions might not be the best for every use case, but are a cheaper option when consistent real time data isn't needed.
- **Cellular 5G/mmWave:** While cellular 5G has been around for a while, Private 5G stands to disrupt the RTLS market in the near future, especially when combined with mmWave technology. As these signals can go through most non-metallic materials and have quite a long range, less location infrastructure is needed to provide precise centimeter level accuracy. 5G can also be useful in loss prevention scenarios when a connection is needed outside the typical device environment.
- **LoRaWAN:** LoRaWAN will typically have less accuracy than most other systems, but is a cheaper alternative to cellular when a solution needs to communicate over large distances and outside of the typical operating location of the device.
- **Proprietary technologies:** Catch all for various proprietary technologies created by different RTLS companies throughout the years with varying accuracy and range. They do exist, and some are even useful.

                                    Table 2: Comparison of Other Location Technologies

| Infrared (IR) | Room Level | Line of Sight (LOS) | Low | High | Developed |
| --- | --- | --- | --- | --- | --- |
| Ultrasound | Sub-meter to precision | 10-20m | High | High | Growing |
| Computer Vision/LiDAR | Sub-meter to precision | 100m | Moderate | Low/none | Developed |
| GPS/GNSS | Region to precision | Global, LOS to sky | Low | Low/none | Developed |
| Magnetic Fingerprint | Room level | Mapped region | Low | Low/none | Developed |

### Other Technologies

- **Infrared:** Infrared can provide room level accuracy with a high degree of certainty, and can be implemented at a lower cost than many other solutions. However, it is dependent on line of sight between a tag and a gateway.
- **Ultrasound:** Ultrasound provides remarkable precision with some systems achieving 1.5mm accuracy, smaller than the diameter of your typical ball point pen. However, these systems can be quite costly and require lots of infrastructure to realize that level of accuracy.
- **Computer Vision/LiDAR/SLAM:** Computer Vision methods can map the features of the building to determine their location and orientation with very precise location accuracy. However, these methods can be affected by occlusions, drift, dynamic environments and varied lighting, and require substantial computation and calibration.
- **GPS:** The gold standard for outdoor global location, GPS provides great accuracy for many systems and can be improved by adding a GPS base station as a reference point, improving accuracy to the centimeter level.Typically cheap and requires little infrastructure.
- **Magnetic Fingerprinting:** Magnetic fingerprinting identifies the magnetic signature in the mapped area to uniquely identify locations and can be done with a smartphone, eliminating any need for additional infrastructure. However, it can be easily affected by moving hardware, especially metal. Best when combined with sensor fusion and other fingerprinting methods.

With the technology picked out, it becomes easier to focus on specific providers for a RTLS solution. Along with the considerations of the previous paragraph, be sure to consider responsibilities for deploying, supporting and maintaining the RTLS hardware, as different technologies and companies will have different preferences for each. More precise solutions such as ultrasound and UWB may require trained technicians to deploy whereas fingerprinting could be delegated to the customer as it’s less technically intensive.

## The Last Stretch: Integration and Data Strategy

After identifying the pains and gains alleviated by adding location data and picking the best technology for your use case, the hardest part still remains: making the data useful. Without context, even the most accurate location data isn’t helpful just on its own. Location data needs to be integrated with solutions customers regularly use with the context of the environment around it. In order to make the most of your system, consider the following steps in your integration.

### Data Exchange, Transformation, Storage and Analysis

- **Data Preparation**
    - **Environmental Context:** Locations of interest need to be enumerated and stored in a location format to give the data actionable context. For example, in a workflow solution, identifying a “dock” or “assembly line” feature could be used to create a trigger for a process automation. These features could be stored in the RTLS provider’s system or in a separate file such as a CAD or Indoor Mapping Data Format (IMDF) file.
    - **Location Normalization:** Many RTLS providers create their own abstract location coordinates which lack global context. This data needs to be transformed to a format to be interoperable with other systems if location data is being supplied from multiple sources.
- **Data Extraction & Storage**
    - **Real-Time vs. Batch Extraction:** Deciding whether location data needs to be delivered in real-time, routinely stored in batch cycles, delivered on demand or triggered by an event will constrain your data routing and architecture.
    - **Method:** Depending on the frequency of data delivery, there are multiple options for retrieving location data from your RTLS partner’s platform. APIs are generally useful for batch or event retrieval but can run into issues with rate or data limits, which can be common with location systems working with devices reporting frequently at scale. For real time applications, utilizing a lightweight message protocol like MQTT allows for subscription messaging, reducing API calls and creating a lightweight service for high throughput applications. CSV or JSON files can be used for longer term batch processes, where data is only collected infrequently and doesn’t require real-time analysis.
    - **Architecture:** Once extracted, data must be processed on the backend, either on the edge level with limited resources or by utilizing the cloud. This generally involves collecting the data, storing it in a database, and then making it accessible for analysis or presentation for users. For example, an MQTT solution hosted in AWS might have a message broker to host the channels, an AWS Kinesis stream for routing and real-time analysis of data, a function hosted in AWS Lambda to aggregate, condense or format data, and a Time-Series database (TSDB) like Amazon Timestream to allow for easier data querying when needed.

                                   Example IoT Cloud Architecture (provided by Amazon)

![](A%20practical%20guide%20to%20Indoor%20Location/image15.png)

- **Data Analysis and Presentation**
    - **Internal Analysis:** Real-time data can be analysed to provide quick insights into a product’s health and performance. While cloud monitoring services like Amazon Cloudwatch can provide alerts for backend problems, real-time analysis can alert teams to outages in the field, like a bad asset tag update or a power outage.
    - **Presentation:** If the product needs access to real-time data, optimizations may need to be made for efficiency and to ensure consistent data between all users. Adding an in-memory database like Redis to the data flow can ensure that all users are working from the same set of real-time data.
    - **External Analytics and Dashboards:** Location data can provide users with crucial, actionable context, typically when aggregated into reports and dashboards for easier consumption. Utilizing a time series database like Timestream can optimize retrieving reports over a period of time, making data analysis easier, quicker and less costly.

RTLS systems have a tendency to generate heaps of data as they take regular samples from large numbers of devices. Finding ways to handle, process and analyze that data is instrumental in providing meaningful, actionable insights to users and can be the make or break for a useful product that generates value to clients.

## Summary

Choosing the right location strategy is less about chasing the most advanced technology and more about aligning capabilities with business value. A QR code or RFID tag may solve a process bottleneck at negligible cost, while a high-fidelity UWB system may be essential for centimeter-level automation. The key is to match the minimum viable precision to your operational needs.

Organizations should start by clearly defining the “why” behind their location needs, whether it’s loss prevention, workflow optimization, safety compliance, or automation. From there, evaluate whether existing infrastructure can be leveraged to reduce cost and complexity. When real-time, granular tracking is needed, investing in UWB or hybrid solutions may yield strong long-term ROI, especially if designed with scalability and integration in mind.

Ultimately, a successful RTLS deployment is not just a technology choice, but a product, operations, and data strategy decision. Starting lean, validating early, and planning for integration at the outset are the best ways to ensure your location system evolves into a high-impact business asset rather than a costly side project.