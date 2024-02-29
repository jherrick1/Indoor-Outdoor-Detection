# Indoor-Outdoor-Detection

Python notebook that utilizes a CNN and LSTM to create a model that can predict whether a phone is indoors or outdoors based on various sensors.

## Data Source:
Bakirtzis, S., Qiu, K., Wassell, I., Fiore, M., and Zhang, J. (2022). Research data supporting “Deep Learning-based Multivariate Time Series Classification for Indoor Outdoor Detection”. Apollo - University of Cambridge Repository. https://www.repository.cam.ac.uk/items/7e5b7161-c3a9-465a-8595-c04cb356ecfa

## Reference Article:
S. Bakirtzis, K. Qiu, I. Wassell, M. Fiore and J. Zhang, "Deep-Learning-Based Multivariate Time-Series Classification for Indoor/Outdoor Detection," in IEEE Internet of Things Journal, vol. 9, no. 23, pp. 24529-24540, 1 Dec.1, 2022, https://ieeexplore.ieee.org/document/9828386

<table class="tg">
<thead>
  <tr>
    <th class="tg-baqh" colspan="3"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Data Description</span></th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-baqh"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Attribute Name</span></td>
    <td class="tg-baqh"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Description</span></td>
    <td class="tg-baqh"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Values</span></td>
  </tr>
  <tr>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">RSRP</span></td>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Reference Signal Received Power, metric used to quantify the strength of the received signal from the cell</span></td>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Continuous</span></td>
  </tr>
  <tr>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">RSRQ</span></td>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Reference Signal Received Quality, metric used to quantify the quality of the received signal from the cell</span></td>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Continuous</span></td>
  </tr>
  <tr>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Light</span></td>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Ambient light intensity</span></td>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Continuous</span></td>
  </tr>
  <tr>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Mag</span></td>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Total magnetic field intensity</span></td>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Continuous</span></td>
  </tr>
  <tr>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Acc</span></td>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Accelerometer measurement</span></td>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Continuous</span></td>
  </tr>
  <tr>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Sound</span></td>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Sound intensity of the area</span></td>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Continuous</span></td>
  </tr>
  <tr>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Proximity</span></td>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Whether the light sensor is blocked by an obstacle</span></td>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Binary</span></td>
  </tr>
  <tr>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Daytime</span></td>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Whether the recording was taken during daytime</span></td>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Binary</span></td>
  </tr>
  <tr>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">IO </span></td>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Target, indoor or outdoor</span></td>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Binary</span></td>
  </tr>
</tbody>
</table>
