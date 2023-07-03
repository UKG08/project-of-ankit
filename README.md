-- phpMyAdmin SQL Dump
-- version 5.1.1
-- https://www.phpmyadmin.net/
--
-- Host: 127.0.0.1:3306
-- Generation Time: Mar 30, 2023 at 08:49 AM
-- Server version: 10.6.12-MariaDB-cll-lve
-- PHP Version: 7.2.34

SET SQL_MODE = "NO_AUTO_VALUE_ON_ZERO";
START TRANSACTION;
SET time_zone = "+00:00";


/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!40101 SET NAMES utf8mb4 */;

--
-- Database: `u914026094_color`
--

-- --------------------------------------------------------

--
-- Table structure for table `banner`
--

CREATE TABLE `banner` (
  `id` int(255) NOT NULL,
  `banner_title` varchar(500) NOT NULL,
  `material` varchar(255) NOT NULL,
  `status` smallint(11) NOT NULL
) ENGINE=MyISAM DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

-- --------------------------------------------------------

--
-- Table structure for table `child_menu`
--

CREATE TABLE `child_menu` (
  `id` int(11) NOT NULL,
  `p_id` varchar(255) NOT NULL,
  `child` varchar(255) NOT NULL,
  `url` varchar(255) NOT NULL,
  `status` smallint(11) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

--
-- Dumping data for table `child_menu`
--

INSERT INTO `child_menu` (`id`, `p_id`, `child`, `url`, `status`) VALUES
(1, '3', 'Manage Banner', 'manage_banner.php', 1),
(2, '4', 'Privacy Policy', 'privacy.php', 1),
(3, '4', 'Risk Disclosure Agreement', 'riskagreement.php', 1),
(4, '5', 'Manage Product', 'manage_product.php', 1),
(5, '2', 'Manage User', 'manage_adminuser.php', 1),
(6, '2', 'Manage Role', 'manage_role.php', 1),
(7, '2', 'Manage Task', 'manage_task.php', 1),
(8, '6', 'Manage User', 'manage_user.php', 1),
(9, '7', 'Withdrawal Request', 'manage_withdraw.php', 1),
(10, '7', 'Withdrawal Accept', 'manage_withdrawAccept.php', 1),
(11, '7', 'Withdrawal Reject', 'manage_withdrawReject.php', 1),
(12, '8', 'Manage Winner Result', 'manage_winresult.php', 1),
(13, '9', 'History For Parity', 'manage_parityhistory.php', 1),
(14, '9', 'History For Sapre', 'manage_saprehistory.php', 1),
(15, '9', 'History For Bcone', 'manage_bconehistory.php', 1),
(16, '9', 'History For Emerd', 'manage_emerdhistory.php', 1),
(17, '10', 'Manage Trade History', 'manage_tradehistory.php', 1),
(18, '11', 'Reward System', 'reward_system.php', 1),
(19, '12', 'Manage Amount', 'manage_amount.php', 1),
(20, '15', 'Manage Recharge', 'manage_recharge.php', 1),
(21, '16', 'Deposit Update', 'deposit update.php', 1);

-- --------------------------------------------------------

--
-- Table structure for table `content`
--

CREATE TABLE `content` (
  `id` int(10) NOT NULL DEFAULT 1,
  `riskagreement` text NOT NULL,
  `privacy` text NOT NULL,
  `rule` text NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

--
-- Dumping data for table `content`
--

INSERT INTO `content` (`id`, `riskagreement`, `privacy`, `rule`) VALUES
(1, '<p>Chapter 1.Booking/Collection Description\r\nPrepayment Booking/Recycling Customer should read and understand the business content carefully before making prepayment bookings (prepayment lock price, payment settlement and shipment) /recovery or repurchase (prepayment lock price, shipping payment) before making prepayment bookings to WinGo 2021:</p>\r\n\r\n<p>1. Before making an appointment/restoring the prepayment business, the customer should complete the real name authentication in the mall and ensure that the name, ID number, bank account number, delivery address and other information filled in are true, accurate and valid; Otherwise, the user will be liable for the consequences of false information.</p>\r\n\r\n<p>2. Customers can order gold and silver products in advance at the shopping centre. Orders can be cancelled by 01:30 a.m. on the same Saturday. When the customer pays the end payment, the mall receives the final payment and arranges the delivery.</p>\r\n\r\n<p>If the customer does not pay the final pick-up by 01:30 a.m. on Saturday, the customer is deemed to have made the last offer before the inventory and the booking is cancelled.</p>\r\n\r\n<p>3. Customers can make an appointment to recycle gold and silver products purchased at the gold point. Pre-purchase recovery requires a credit margin and confirmation of actual possession of gold and silver products purchased from the mall. Customers can cancel their reservation at any time before 01:30 on Saturday and the credit mark will be refunded after deducting the increase or decrease in the value of the goods within the corresponding time.</p>\r\n\r\n<p>If the customer fails to deliver the goods to a shopping mall or shopping center at the designated collection point by Saturday within the same week, or if the goods delivered do not meet the recycling standard test, the customer will be deemed to have cancelled the reservation recovery and will bear the logistics and testing costs.</p>\r\n\r\n<p>4. Counting time: Daily 01:30-05:30 for the mall warehouse inventory time. During the inventory period, the mall stops accepting advance payments for reservations/receipts.</p>\r\n\r\n<p>5. For further details, please refer to the Business Guidelines in the front page of the mall, Understanding WinGo2021.</p>\r\n\r\n\r\n<p>Chapter 2 Reveals the business model of WinGo2021</p>\r\n\r\n<p>Booking/repurchase orders, the business model for clearing balance shipments, uncertainties such as potential benefits and potential risks to the value of its merchandise due to real-time fluctuations in the gold and silver market, and the extent to which booking/repo risk stake is understood for customer booking/repo risk, Risk control ability and understanding of related products have high requirements. Customer selects pre-payment booking/repurchase, fully informed on behalf of the customer and understand the risks of prepayments/repurchase business and agree to and accept WinGo 2021 current and future relevant booking/repurchase business processes and management systems (collectively, the Process Systems) to develop, modify and publish. This Risk Disclosure (Disclosure) is intended to fully disclose to the Client the risk of the prepayment booking/repurchase business and is intended only to provide reference for the client to assess and determine its own risk tolerance. The risk disclosures described in this disclosure are for example only. All risk factors associated with WinGo 2021 Advance Booking/Repurchase are not detailed. Customers should also carefully understand and understand other possible risk factors before starting or participating in WinGo 2021 pre-payment booking/repurchase business. If the customer is not aware of or is not aware of this disclosure, they should consult WinGo 2021 Customer Service or the relevant regional service provider in a timely manner. If the Customer ultimately clicks on Risk Disclosure, it is deemed that the Customer fully agrees and accepts the full contents of this disclosure.</p>\r\n\r\n\r\n<p>Warm tips:-</p>\r\n<p>1.Minors under the age of 18 are not permitted to participate in The WinGo 2021 Advance Booking/Recycling.</p>\r\n<p>2.WinGo 2021 Advance Booking/Repo is only available to customers who meet all of the following criteria:</p>\r\n<p>* Natural persons with full civil capacity, legal persons of enterprises or other economic organizations registered in accordance with the law.</p>\r\n\r\n<p>* To fully understand all risks associated with WinGo 2021 Advance Booking/Repurchase business and have a certain risk tolerance.</p>\r\n\r\n<p>* Have a certain understanding of gold and silver and its products:</p>\r\n\r\n<p>A. Policy-related risk disclosure, such as changes in national laws, regulations and policies, contingency measures, implementation of appropriate regulatory measures, WinGo 2021 regulatory system and changes in management methods and regulations, etc., all risks that may affect customer bookings/repurchases, etc., the customer must bear the losses incurred.</p>\r\n\r\n<p>B. Price fluctuations, gold, silver and other precious metals and their accessories are affected by a variety of factors, such as the international economic situation, foreign exchange, related market trends, supply and demand, and political situation and energy prices. The pricing mechanism for gold, silver and other precious metals products is very complex, making it difficult for customers to fully grasp in practice, so decisions such as advance booking/buyback are possible Mistakes, if the risk cannot be effectively controlled, may suffer losses and the customer must bear all the losses incurred as a result.</p>\r\n\r\n<p>* WinGo 2021 has enabled the provision of services through electronic communication technology and Internet technology. Communication services and hardware and software services are provided by different vendors and may be at risk in terms of quality and stability. Interruptions or delays due to communication or network failures may affect customer prepayment bookings/repurchases. In addition, the customer\'s computer system may be attacked by viruses and/or cyber-hackers, resulting in the customer\'s advance payment booking/repurchase not being properly and/or timely.</p>\r\n\r\n<p>There is also a risk that the above uncertainties may affect the customer’s advance payment booking/repurchase.</p>\r\n<p>A. The price quoted by the WinGo 2021 Prepayment Booking/Repo System is based on the systems real-time trading price and may differ slightly from the commodity prices in other markets.\r\nWingo 2021 cannot guarantee that the above prepayment booking//repurchase price is fully consistent with other markets.</p>\r\n<p>B. At WinGo 2021;, once the customers pre-payment booking/repurchase application submitted through the online terminal is completed, it cannot be withdrawn and the customer must accept the risks associated with such a subscription.</p>\r\n<p>C. Wingo 2021 prohibits regional service providers and their staff from providing any profit guarantee to customers, from engaging in prepaid bookings/repurchases on behalf of customers, or from sharing profits or risks with customers. Customer should be aware that any profit guarantee or commitment that WinGo 2021 advance booking/repurchase does not have a loss, profit share or risk-sharing is impossible, unfounded, and incorrect.</p>\r\n<p>D. The customers pre-paid booking / repurchase application must be based on the customers own decision. WinGo 2021 and regional service providers and employees do not provide booking / buyback to the client, nor does it constitute any commitment if the client makes a booking / buyback decision accordingly.</p>\r\n<p>E. In advance booking / buyback process, there may be occasional apparent errors in the offer.</p>\r\n<p>* RISK-AGREEMENT</p>\r\n<p>Typhoons, floods, fires, wars, disturbances, rule revisions, changes or adjustments in government regulatory policies and regulatory requirements, and electricity, To ensure that you fully understand the relevant provisions and risks of booking / repurchase business, customers should be based on their own booking experience, booking / repurchase / purchase of commodities, read all the contents of the advance booking / repurchase notice carefully, and fully understand and agree to all the contents, I am willing to take all risks to start or participate in WinGo 2021. In case of above mentioned condition I shall be him-self liable to any financial as well as monitory loss. By accepting this I shall be no more eligible to claims any statutory legal benefits given to Indian citizen by Law of India.</p>\r\n\r\n\r\n<p>Note: I have carefully read all contents of this app including Privacy Statement, Risk Disclosure Agreement and Risk Agreement and I am agreed to continue with my own risk.</p>\r\n\r\n\r\n<p>Cancellation and refundable Policy\r\nIn case of any discrepancy we can cancel any of the orders placed by you. A few reasons for cancellation from our end usually include limitation of the product in the inventory, error in pricing, error in product information etc. We also have the right to check out for extra information for the purpose of accepting orders in a few cases. We make sure to notify you if in case your order is cancelled partially or completely or if in case any extra data is required for the purpose of accepting your order.</p>\r\n\r\n<p>Once you place the order, such order can be cancelled from your end before the shipping is undertaken to the destination. Once the request of cancellation for ready for shipping product is received by us, we make sure to refund the amount through the same mode of payment within 5 working days. Cancellation of the order of Gold coin(exchanged by integrals) shall not be accepted as under Company’s policies.</p>\r\n\r\n<p>We don’t accept Cancellation requests for Smart Buy orders or customized jewellery orders. In specific situations when the customer wants the money back or wants to exchange it with other products, making charges of the product and stone charges, if there is any stone on the product shall be deducted from the payment and balance will be refunded back to customer account within 5 working days.</p>\r\n\r\n<p>If in case the amount is deducted from your account and the transaction has failed, the same will be refunded back to your account within 72 hours.</p>\r\n', '<h3><strong><span style=\"color:red\">Privacy</span></strong><strong><span style=\"color:red\"> Policy</span></strong><strong><span style=\"color:red\"> for</span></strong><strong><span style=\"color:red\"> WinGo</span></strong></h3>  <p>This Privacy Policy describes Our policies and procedures on the collection, use and disclosure of Your information when You use the Service and tells You about Your privacy rights and how the law protects You.</p>  <p>Interpretation and Definitions</p> <p>Interpretation</p> <p>The words of which the initial letter is capitalized have meanings defined under the following conditions.</p>  <p>The following definitions shall have the same meaning regardless of whether they appear in singular or in plural.</p>  <p>Definitions</p> <p>For the purposes of this Privacy Policy:</p>  <p>You means the individual accessing or using the Service, or the company, or other legal entity on behalf of which such individual is accessing or using the Service, as applicable.</p>  <p>Company (referred to as either \"the Company\", \"We\", \"Us\" or \"Our\" in this Agreement) refers to Wingo 2021.</p>  <p>Affiliate means an entity that controls, is controlled by or is under common control with a party, where \"control\" means ownership of 50% or more of the shares, equity interest or other securities entitled to vote for election of directors or other managing authority.</p> <p>Account means a unique account created for You to access our Service or parts of our Service.</p> <p>Website refers to Wingo 2021, accessible from https://wingo2021.site.</p> <p>Service refers to the Website.</p> <p>Country refers to: Rajasthan, India</p> <p>Service Provider means any natural or legal person who processes the data on behalf of the Company. It refers to third-party companies or individuals employed by the Company to facilitate the Service, to provide the Service on behalf of the Company, to perform services related to the Service or to assist the Company in analyzing how the Service is used.</p>  <p>Third-party Social Media Service refers to any website or any social network website through which a User can log in or create an account to use the Service.</p> <p>Personal Data is any information that relates to an identified or identifiable individual.</p>  <p>Cookies are small files that are placed on Your computer, mobile device or any other device by a website, containing the details of Your browsing history on that website among its many uses.</p> <p>Device means any device that can access the Service such as a computer, a cellphone or a digital tablet.</p> <p>Usage Data refers to data collected automatically, either generated by the use of the Service or from the Service infrastructure itself (for example, the duration of a page visit).</p> <p>Collecting and Using Your Personal Data</p> <p>Types of Data Collected</p> <p>Personal Data</p> <p>While using Our Service, We may ask You to provide Us with certain personally identifiable information that can be used to contact or identify You. Personally identifiable information may include, but is not limited to:</p>  <p>Email address</p> <p>First name and last name</p> <p>Phone number</p> <p>Address, State, Province, ZIP/Postal code, City</p> <p>Usage Data</p> <p>Usage Data is collected automatically when using the Service.</p>  <p>Usage Data may include information such as Your Device\'s Internet Protocol address (e.g. IP address), browser type, browser version, the pages of our Service that You visit, the time and date of Your visit, the time spent on those pages, unique device identifiers and other diagnostic data.</p>  <p>When You access the Service by or through a mobile device, We may collect certain information automatically, including, but not limited to, the type of mobile device You use, Your mobile device unique ID, the IP address of Your mobile device, Your mobile operating system, the type of mobile Internet browser You use, unique device identifiers and other diagnostic data.</p>  <p>We may also collect information that Your browser sends whenever You visit our Service or when You access the Service by or through a mobile device.</p>  <p>Tracking Technologies and Cookies</p> <p>We use Cookies and similar tracking technologies to track the activity on Our Service and store certain information. Tracking technologies used are beacons, tags, and scripts to collect and track information and to improve and analyze Our Service.</p>  <p>You can instruct Your browser to refuse all Cookies or to indicate when a Cookie is being sent. However, if You do not accept Cookies, You may not be able to use some parts of our Service.</p>  <p>Cookies can be \"Persistent\" or \"Session\" Cookies. Persistent Cookies remain on your personal computer or mobile device when You go offline, while Session Cookies are deleted as soon as You close your web browser.</p>  <p>We use both session and persistent Cookies for the purposes set out below:</p>  <p>Necessary / Essential Cookies</p>  <p>Type: Session Cookies</p>  <p>Administered by: Us</p>  <p>Purpose: These Cookies are essential to provide You with services available through the Website and to enable You to use some of its features. They help to authenticate users and prevent fraudulent use of user accounts. Without these Cookies, the services that You have asked for cannot be provided, and We only use these Cookies to provide You with those services.</p>  <p>Cookies Policy / Notice Acceptance Cookies</p>  <p>Type: Persistent Cookies</p>  <p>Administered by: Us</p>  <p>Purpose: These Cookies identify if users have accepted the use of cookies on the Website.</p>  <p>Functionality Cookies</p>  <p>Type: Persistent Cookies</p>  <p>Administered by: Us</p>  <p>Purpose: These Cookies allow us to remember choices You make when You use the Website, such as remembering your login details or language preference. The purpose of these Cookies is to provide You with a more personal experience and to avoid You having to re-enter your preferences every time You use the Website.</p>  <p>For more information about the cookies we use and your choices regarding cookies, please visit our Cookies Policy.</p>  <p>Use of Your Personal Data</p> <p>The Company may use Personal Data for the following purposes:</p>  <p>To provide and maintain our Service, including to monitor the usage of our Service.</p> <p>To manage Your Account: to manage Your registration as a user of the Service. The Personal Data You provide can give You access to different functionalities of the Service that are available to You as a registered user.</p> <p>For the performance of a contract: the development, compliance and undertaking of the purchase contract for the products, items or services You have purchased or of any other contract with Us through the Service.</p> <p>To contact You: To contact You by email, telegram, SMS, or other equivalent forms of electronic communication, such as a mobile application\'s push notifications regarding updates or informative communications related to the functionalities, products or contracted services, including the security updates, when necessary or reasonable for their implementation.</p> <p>To provide You with news, special offers and general information about other goods, services and events which we offer that are similar to those that you have already purchased or enquired about unless You have opted not to receive such information.</p> <p>To manage Your requests: To attend and manage Your requests to Us.</p> <p>We may share your personal information in the following situations:</p>  <p>With Service Providers: We may share Your personal information with Service Providers to monitor and analyze the use of our Service, to contact You.</p> <p>For Business transfers: We may share or transfer Your personal information in connection with, or during negotiations of, any merger, sale of Company assets, financing, or acquisition of all or a portion of our business to another company.</p> <p>With Affiliates: We may share Your information with Our affiliates, in which case we will require those affiliates to honor this Privacy Policy. Affiliates include Our parent company and any other subsidiaries, joint venture partners or other companies that We control or that are under common control with Us.</p> <p>With Business partners: We may share Your information with Our business partners to offer You certain products, services or promotions.</p> <p>With other users: when You share personal information or otherwise interact in the public areas with other users, such information may be viewed by all users and may be publicly distributed outside.</p>  <p>If You interact with other users or register through a Third-Party Social Media Service, Your contacts on the Third-Party Social Media Service may see You name, profile, pictures and description of Your activity. Similarly, other users will be able to view descriptions of Your activity, communicate with You and view Your profile.</p> <p>Retention of Your Personal Data</p> <p>The Company will retain Your Personal Data only for as long as is necessary for the purposes set out in this Privacy Policy. We will retain and use Your Personal Data to the extent necessary to comply with our legal obligations (for example, if we are required to retain your data to comply with applicable laws), resolve disputes, and enforce our legal agreements and policies.</p>  <p>The Company will also retain Usage Data for internal analysis purposes. Usage Data is generally retained for a shorter period of time, except when this data is used to strengthen the security or to improve the functionality of Our Service, or We are legally obligated to retain this data for longer time periods.</p>  <p>Transfer of Your Personal Data</p> <p>Your information, including Personal Data, is processed at the Company\'s operating offices and in any other places where the parties involved in the processing are located. It means that this information may be transferred to — and maintained on — computers located outside of Your state, province, country or other governmental jurisdiction where the data protection laws may differ than those from Your jurisdiction.</p>  <p>Your consent to this Privacy Policy followed by Your submission of such information represents Your agreement to that transfer.</p>  <p>The Company will take all steps reasonably necessary to ensure that Your data is treated securely and in accordance with this Privacy Policy and no transfer of Your Personal Data will take place to an organization or a country unless there are adequate controls in place including the security of Your data and other personal information.</p>  <p>Disclosure of Your Personal Data</p> <p>Business Transactions</p> <p>If the Company is involved in a merger, acquisition or asset sale, Your Personal Data may be transferred. We will provide notice before Your Personal Data is transferred and becomes subject to a different Privacy Policy.</p>  <p>Law enforcement</p> <p>Under certain circumstances, the Company may be required to disclose Your Personal Data if required to do so by law or in response to valid requests by public authorities (e.g. a court or a government agency).</p>  <p>Other legal requirements</p> <p>The Company may disclose Your Personal Data in the good faith belief that such action is necessary to:</p>  <p>Comply with a legal obligation</p> <p>Protect and defend the rights or property of the Company</p> <p>Prevent or investigate possible wrongdoing in connection with the Service</p> <p>Protect the personal safety of Users of the Service or the public</p> <p>Protect against legal liability</p> <p>Security of Your Personal Data</p> <p>The security of Your Personal Data is important to Us, but remember that no method of transmission over the Internet, or method of electronic storage is 100% secure. While We strive to use commercially acceptable means to protect Your Personal Data, We cannot guarantee its absolute security.</p>  <p>Children\'s Privacy</p> <p>Our Service does not address anyone under the age of 13. We do not knowingly collect personally identifiable information from anyone under the age of 13. If You are a parent or guardian and You are aware that Your child has provided Us with Personal Data, please contact Us. If We become aware that We have collected Personal Data from anyone under the age of 13 without verification of parental consent, We take steps to remove that information from Our servers.</p>  <p>If We need to rely on consent as a legal basis for processing Your information and Your country requires consent from a parent, We may require Your parent\'s consent before We collect and use that information.</p>  <p>Links to Other Websites</p> <p>Our Service may contain links to other websites that are not operated by Us. If You click on a third party link, You will be directed to that third party\'s site. We strongly advise You to review the Privacy Policy of every site You visit.</p>  <p>We have no control over and assume no responsibility for the content, privacy policies or practices of any third party sites or services.</p>  <p>Changes to this Privacy Policy</p> <p>We may update our Privacy Policy from time to time. We will notify You of any changes by posting the new Privacy Policy on this page.</p>  <p>We will let You know via email and/or a prominent notice on Our Service, prior to the change becoming effective and update the \"Last updated\" date at the top of this Privacy Policy.</p>  <p>You are advised to review this Privacy Policy periodically for any changes. Changes to this Privacy Policy are effective when they are posted on this page.</p>  <p>Contact Us</p> <p>If you have any questions about this Privacy Policy, You can contact us:</p>  <p>By visiting this page on our website</p>', '<p style=\"font-size:15px\">2 minutes 1 issue, 1 minutes and 30 seconds to order, 30 seconds to show the lottery result. It opens all day. The total number of trade is 720 issues</p>\r\n\r\n<p style=\"font-size:15px\">If you spend 100 to trade, after deducting 2 service fee, your contract amount is 98</p>\r\n\r\n<p style=\"font-size:15px\">1. JOIN GREEN: if the result shows 1,3,7,9, you will get (98*2) 196</p>\r\n\r\n<p style=\"font-size:15px\">If the result shows 5, you will get (98*1.5) 147</p>\r\n\r\n<p style=\"font-size:15px\">2. JOIN RED: if the result shows 2,4,6,8, you will get (98*2) 196; If the result shows 0, you will get (98*1.5) 147</p>\r\n\r\n<p style=\"font-size:15px\">3. JOIN VIOLET: if the result shows 0 or 5, you will get (98*4.5) 441</p>\r\n\r\n<p style=\"font-size:15px\">4. SELECT NUMBER: if the result is the same as the number you selected, you will get (98*9) 882</p>');

-- --------------------------------------------------------

--
-- Table structure for table `deposits`
--

CREATE TABLE `deposits` (
  `id` int(11) NOT NULL,
  `ref_num` varchar(200) NOT NULL,
  `amount` varchar(200) NOT NULL,
  `email` varchar(200) NOT NULL,
  `status` varchar(200) NOT NULL,
  `uid` varchar(200) NOT NULL,
  `date` varchar(200) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

--
-- Dumping data for table `deposits`
--

INSERT INTO `deposits` (`id`, `ref_num`, `amount`, `email`, `status`, `uid`, `date`) VALUES
(1, '357952379', '99999', '9536852147', '2', '1', 'March 29, 2023, 4:48 pm'),
(2, '985632541256', '1000', '953874523', '2', '1', 'March 29, 2023, 4:52 pm'),
(3, '953652145874', '1000', '9658745214', '2', '2', 'March 29, 2023, 5:00 pm'),
(4, '965236541254', '1000', '9852147856', '2', '2', 'March 29, 2023, 5:08 pm'),
(5, '52486968', '50000', '9528741552', '2', '2', 'March 29, 2023, 5:12 pm'),
(6, '958741257874', '50000', '9587454870', '2', '2', 'March 29, 2023, 5:17 pm'),
(7, '2384367245', '99999', '96723848628', '2', '2', 'March 29, 2023, 5:29 pm'),
(8, '985632587456', '50000', '9586325478', '2', '1', 'March 29, 2023, 5:45 pm'),
(9, '46808532370', '10000', '8534790053', '2', '1', 'March 29, 2023, 6:05 pm'),
(10, '2589085237', '10000', '2580964147', '2', '1', 'March 29, 2023, 6:07 pm'),
(11, '36997533789', '1000', '468963379', '2', '2', 'March 29, 2023, 6:14 pm');

-- --------------------------------------------------------

--
-- Table structure for table `Red envlop`
--

CREATE TABLE `Red envlop` (
  `red envelop` int(1) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

-- --------------------------------------------------------

--
-- Table structure for table `role`
--

CREATE TABLE `role` (
  `id` int(11) NOT NULL,
  `role` varchar(255) NOT NULL,
  `created_date` timestamp NOT NULL DEFAULT current_timestamp(),
  `status` smallint(11) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

--
-- Dumping data for table `role`
--

INSERT INTO `role` (`id`, `role`, `created_date`, `status`) VALUES
(1, 'SuperAdmin', '2014-12-23 20:04:37', 1),
(2, 'Support', '2017-01-26 17:23:05', 1),
(13, 'serverRoot', '2021-10-09 12:49:15', 1),
(14, 'Assistant', '2022-01-26 19:57:56', 1),
(15, 'Agent', '2022-01-26 19:58:37', 1);

-- --------------------------------------------------------

--
-- Table structure for table `services`
--

CREATE TABLE `services` (
  `id` int(11) NOT NULL,
  `services` varchar(255) NOT NULL,
  `url` varchar(255) NOT NULL,
  `status` varchar(255) NOT NULL
) ENGINE=MyISAM DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

--
-- Dumping data for table `services`
--

INSERT INTO `services` (`id`, `services`, `url`, `status`) VALUES
(1, 'Dashboard', 'desktop.php', '1'),
(6, 'User Management', '#', '1'),
(7, 'Withdrawal Management ', '#', '1'),
(8, 'Wining Management', '#', '1'),
(11, 'Reward Management', '#', '1'),
(12, 'Amount Setup', '#', '1'),
(13, 'Recharge Management', '#', '1'),
(16, 'Deposit Update', 'deposit update.php', '1');

-- --------------------------------------------------------

--
-- Table structure for table `site_setting`
--

CREATE TABLE `site_setting` (
  `id` int(11) NOT NULL,
  `address` text NOT NULL,
  `email` varchar(255) NOT NULL,
  `mobile` varchar(255) NOT NULL,
  `fblink` text NOT NULL,
  `twlink` text NOT NULL,
  `ln` text NOT NULL,
  `insta` varchar(500) NOT NULL,
  `fbcount` varchar(100) NOT NULL,
  `twcount` varchar(100) NOT NULL,
  `youtubecount` varchar(100) NOT NULL,
  `instacount` varchar(100) NOT NULL,
  `status` smallint(11) NOT NULL,
  `updt_time` timestamp NOT NULL DEFAULT current_timestamp()
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

--
-- Dumping data for table `site_setting`
--

INSERT INTO `site_setting` (`id`, `address`, `email`, `mobile`, `fblink`, `twlink`, `ln`, `insta`, `fbcount`, `twcount`, `youtubecount`, `instacount`, `status`, `updt_time`) VALUES
(1, 'Stock Building, 125 Main Street 1st Lane, San Francisco, USA', 'info@gmail.com', '+91 9090909090', '#', '#', '#', '#', '985', '529', '888', '100', 1, '0000-00-00 00:00:00');

-- --------------------------------------------------------

--
-- Table structure for table `task`
--

CREATE TABLE `task` (
  `id` int(11) NOT NULL,
  `role_id` varchar(255) NOT NULL,
  `task` varchar(255) NOT NULL,
  `status` smallint(11) NOT NULL,
  `created_date` timestamp NOT NULL DEFAULT current_timestamp()
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

--
-- Dumping data for table `task`
--

INSERT INTO `task` (`id`, `role_id`, `task`, `status`, `created_date`) VALUES
(1, '1', '1,2,3,4,5,6,7,8,9,10,11,12,13', 1, '2021-09-25 10:51:32'),
(2, '2', '1,3,4,5,9,10', 1, '2019-09-18 07:17:58'),
(9, '13', '1,2,3,4,5,6,7,8,9,10,11,12,13,16', 1, '2021-10-09 12:49:50'),
(10, '15', '1,3,4,5,13', 1, '2022-01-26 20:01:28'),
(11, '14', '8', 1, '2022-01-26 20:02:33');

-- --------------------------------------------------------

--
-- Table structure for table `tbl_admin`
--

CREATE TABLE `tbl_admin` (
  `id` int(255) NOT NULL,
  `name` varchar(255) NOT NULL,
  `admin_name` varchar(255) NOT NULL,
  `password` varchar(255) NOT NULL,
  `role` varchar(255) NOT NULL,
  `expiry_date` varchar(255) NOT NULL,
  `status` smallint(11) NOT NULL,
  `date` datetime NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

--
-- Dumping data for table `tbl_admin`
--

INSERT INTO `tbl_admin` (`id`, `name`, `admin_name`, `password`, `role`, `expiry_date`, `status`, `date`) VALUES
(1, 'admin', 'admin', 'c6cab344b76165138cb0a40f5529796f', '13', 'no', 1, '0000-00-00 00:00:00');

-- --------------------------------------------------------

--
-- Table structure for table `tbl_bankdetail`
--

CREATE TABLE `tbl_bankdetail` (
  `id` int(11) NOT NULL,
  `userid` int(11) NOT NULL,
  `name` varchar(255) NOT NULL,
  `ifsc` varchar(255) NOT NULL,
  `bankname` varchar(255) NOT NULL,
  `account` varchar(255) NOT NULL,
  `mobile` varchar(300) NOT NULL,
  `email` varchar(300) NOT NULL,
  `type` varchar(50) NOT NULL,
  `status` smallint(11) NOT NULL
) ENGINE=MyISAM DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

--
-- Dumping data for table `tbl_bankdetail`
--

INSERT INTO `tbl_bankdetail` (`id`, `userid`, `name`, `ifsc`, `bankname`, `account`, `mobile`, `email`, `type`, `status`) VALUES
(1, 2, 'RajuKumar ', 'SBIN0065002', 'State Bank of India ', '35642578524', '9578641257', 'Ravindra53820153@ybl', 'bank', 1),
(2, 1, 'Ravi Kumar ', 'SBIN0032009', 'State Bank of India ', '658752365874', '6958236547', 'raviuukfevii@upi', 'bank', 1);

-- --------------------------------------------------------

--
-- Table structure for table `tbl_betting`
--

CREATE TABLE `tbl_betting` (
  `id` int(11) NOT NULL,
  `userid` int(11) NOT NULL,
  `periodid` varchar(255) NOT NULL,
  `type` varchar(100) NOT NULL,
  `value` varchar(100) NOT NULL,
  `amount` float NOT NULL,
  `tab` varchar(50) NOT NULL,
  `acceptrule` varchar(50) NOT NULL,
  `createdate` timestamp NOT NULL DEFAULT current_timestamp()
) ENGINE=MyISAM DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

--
-- Dumping data for table `tbl_betting`
--

INSERT INTO `tbl_betting` (`id`, `userid`, `periodid`, `type`, `value`, `amount`, `tab`, `acceptrule`, `createdate`) VALUES
(1, 1, '20230329540', 'button', 'Green', 10, 'parity', 'on', '2023-03-29 12:28:37'),
(2, 1, '20230329540', 'button', 'Red', 10, 'parity', 'on', '2023-03-29 12:28:40'),
(3, 1, '20230329540', 'button', '0', 10, 'parity', 'on', '2023-03-29 12:28:45'),
(4, 1, '20230329540', 'button', '1', 10, 'parity', 'on', '2023-03-29 12:28:47'),
(5, 1, '20230329540', 'button', '2', 10, 'parity', 'on', '2023-03-29 12:28:56'),
(6, 1, '20230329540', 'button', '3', 10, 'parity', 'on', '2023-03-29 12:28:58'),
(7, 1, '20230329540', 'button', '4', 10, 'parity', 'on', '2023-03-29 12:29:03'),
(8, 1, '20230329540', 'button', '5', 10, 'parity', 'on', '2023-03-29 12:29:08'),
(9, 1, '20230329540', 'button', '7', 10, 'parity', 'on', '2023-03-29 12:29:14'),
(10, 1, '20230329540', 'button', '8', 10, 'parity', 'on', '2023-03-29 12:29:16'),
(11, 1, '20230329540', 'button', '9', 10, 'parity', 'on', '2023-03-29 12:29:19'),
(12, 1, '20230329541', 'button', 'Green', 10, 'parity', 'on', '2023-03-29 12:30:29'),
(13, 1, '20230329541', 'button', 'Violet', 10, 'parity', 'on', '2023-03-29 12:30:32'),
(14, 1, '20230329541', 'button', 'Red', 10, 'parity', 'on', '2023-03-29 12:30:35'),
(15, 1, '20230329541', 'button', '0', 10, 'parity', 'on', '2023-03-29 12:30:38'),
(16, 1, '20230329541', 'button', '1', 10, 'parity', 'on', '2023-03-29 12:30:40'),
(17, 1, '20230329541', 'button', '2', 10, 'parity', 'on', '2023-03-29 12:30:49'),
(18, 1, '20230329541', 'button', '2', 10, 'parity', 'on', '2023-03-29 12:30:49'),
(19, 1, '20230329541', 'button', '2', 10, 'parity', 'on', '2023-03-29 12:30:49'),
(20, 1, '20230329541', 'button', '3', 10, 'parity', 'on', '2023-03-29 12:30:56'),
(21, 1, '20230329541', 'button', '4', 10, 'parity', 'on', '2023-03-29 12:31:02'),
(22, 1, '20230329541', 'button', '5', 10, 'parity', 'on', '2023-03-29 12:31:07'),
(23, 1, '20230329541', 'button', '6', 10, 'parity', 'on', '2023-03-29 12:31:14'),
(24, 1, '20230329541', 'button', '7', 10, 'parity', 'on', '2023-03-29 12:31:19'),
(25, 1, '20230329541', 'button', '8', 10, 'parity', 'on', '2023-03-29 12:31:26'),
(26, 1, '20230329545', 'button', '2', 10000, 'parity', 'on', '2023-03-29 12:39:10'),
(27, 1, '20230329546', 'button', '7', 10000, 'parity', 'on', '2023-03-29 12:40:40'),
(28, 1, '20230329546', 'button', '7', 10000, 'parity', 'on', '2023-03-29 12:40:56'),
(29, 1, '20230329546', 'button', '7', 10000, 'parity', 'on', '2023-03-29 12:41:00'),
(30, 1, '20230329546', 'button', '7', 10000, 'parity', 'on', '2023-03-29 12:41:05'),
(31, 1, '20230329547', 'button', '6', 10000, 'parity', 'on', '2023-03-29 12:42:21'),
(32, 1, '20230329547', 'button', '6', 10000, 'parity', 'on', '2023-03-29 12:42:31'),
(33, 1, '20230329547', 'button', '6', 10000, 'parity', 'on', '2023-03-29 12:42:34'),
(34, 1, '20230329547', 'button', '6', 10000, 'parity', 'on', '2023-03-29 12:42:38'),
(35, 2, '20230329549', 'button', 'Green', 1000, 'parity', 'on', '2023-03-29 12:46:28'),
(36, 1, '20230330187', 'button', '8', 10, 'parity', 'on', '2023-03-30 00:42:42'),
(37, 1, '20230330187', 'button', '8', 10, 'parity', 'on', '2023-03-30 00:42:42'),
(38, 1, '20230330190', 'button', '2', 40, 'parity', 'on', '2023-03-30 00:49:22'),
(39, 1, '20230330190', 'button', '2', 10000, 'parity', 'on', '2023-03-30 00:49:27'),
(40, 1, '20230330333', 'button', '6', 10000, 'parity', 'on', '2023-03-30 05:35:19');

-- --------------------------------------------------------

--
-- Table structure for table `tbl_bonus`
--

CREATE TABLE `tbl_bonus` (
  `id` int(11) NOT NULL,
  `userid` int(11) NOT NULL,
  `amount` varchar(300) NOT NULL,
  `level1` varchar(300) NOT NULL,
  `level2` varchar(300) NOT NULL
) ENGINE=MyISAM DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

-- --------------------------------------------------------

--
-- Table structure for table `tbl_bonussummery`
--

CREATE TABLE `tbl_bonussummery` (
  `id` int(11) NOT NULL,
  `userid` int(11) NOT NULL,
  `periodid` varchar(300) NOT NULL,
  `level1id` varchar(255) NOT NULL,
  `level2id` varchar(255) NOT NULL,
  `level1amount` varchar(255) NOT NULL,
  `level2amount` varchar(255) NOT NULL,
  `tradeamount` varchar(255) NOT NULL,
  `createdate` datetime NOT NULL
) ENGINE=MyISAM DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

--
-- Dumping data for table `tbl_bonussummery`
--

INSERT INTO `tbl_bonussummery` (`id`, `userid`, `periodid`, `level1id`, `level2id`, `level1amount`, `level2amount`, `tradeamount`, `createdate`) VALUES
(1, 1, '20230329540', '', '', '0.07', '0.05', '10', '2023-03-29 17:58:37'),
(2, 1, '20230329540', '', '', '0.07', '0.05', '10', '2023-03-29 17:58:40'),
(3, 1, '20230329540', '', '', '0.07', '0.05', '10', '2023-03-29 17:58:45'),
(4, 1, '20230329540', '', '', '0.07', '0.05', '10', '2023-03-29 17:58:47'),
(5, 1, '20230329540', '', '', '0.07', '0.05', '10', '2023-03-29 17:58:56'),
(6, 1, '20230329540', '', '', '0.07', '0.05', '10', '2023-03-29 17:58:58'),
(7, 1, '20230329540', '', '', '0.07', '0.05', '10', '2023-03-29 17:59:03'),
(8, 1, '20230329540', '', '', '0.07', '0.05', '10', '2023-03-29 17:59:08'),
(9, 1, '20230329540', '', '', '0.07', '0.05', '10', '2023-03-29 17:59:14'),
(10, 1, '20230329540', '', '', '0.07', '0.05', '10', '2023-03-29 17:59:16'),
(11, 1, '20230329540', '', '', '0.07', '0.05', '10', '2023-03-29 17:59:19'),
(12, 1, '20230329541', '', '', '0.07', '0.05', '10', '2023-03-29 18:00:29'),
(13, 1, '20230329541', '', '', '0.07', '0.05', '10', '2023-03-29 18:00:32'),
(14, 1, '20230329541', '', '', '0.07', '0.05', '10', '2023-03-29 18:00:35'),
(15, 1, '20230329541', '', '', '0.07', '0.05', '10', '2023-03-29 18:00:38'),
(16, 1, '20230329541', '', '', '0.07', '0.05', '10', '2023-03-29 18:00:40'),
(17, 1, '20230329541', '', '', '0.07', '0.05', '10', '2023-03-29 18:00:49'),
(18, 1, '20230329541', '', '', '0.07', '0.05', '10', '2023-03-29 18:00:49'),
(19, 1, '20230329541', '', '', '0.07', '0.05', '10', '2023-03-29 18:00:49'),
(20, 1, '20230329541', '', '', '0.07', '0.05', '10', '2023-03-29 18:00:56'),
(21, 1, '20230329541', '', '', '0.07', '0.05', '10', '2023-03-29 18:01:02'),
(22, 1, '20230329541', '', '', '0.07', '0.05', '10', '2023-03-29 18:01:07'),
(23, 1, '20230329541', '', '', '0.07', '0.05', '10', '2023-03-29 18:01:14'),
(24, 1, '20230329541', '', '', '0.07', '0.05', '10', '2023-03-29 18:01:19'),
(25, 1, '20230329541', '', '', '0.07', '0.05', '10', '2023-03-29 18:01:26'),
(26, 1, '20230329545', '', '', '70', '50', '10000', '2023-03-29 18:09:10'),
(27, 1, '20230329546', '', '', '70', '50', '10000', '2023-03-29 18:10:40'),
(28, 1, '20230329546', '', '', '70', '50', '10000', '2023-03-29 18:10:56'),
(29, 1, '20230329546', '', '', '70', '50', '10000', '2023-03-29 18:11:00'),
(30, 1, '20230329546', '', '', '70', '50', '10000', '2023-03-29 18:11:05'),
(31, 1, '20230329547', '', '', '70', '50', '10000', '2023-03-29 18:12:21'),
(32, 1, '20230329547', '', '', '70', '50', '10000', '2023-03-29 18:12:31'),
(33, 1, '20230329547', '', '', '70', '50', '10000', '2023-03-29 18:12:34'),
(34, 1, '20230329547', '', '', '70', '50', '10000', '2023-03-29 18:12:38'),
(35, 2, '20230329549', '1', '', '7', '5', '1000', '2023-03-29 18:16:28'),
(36, 1, '20230330187', '', '', '0.07', '0.05', '10', '2023-03-30 06:12:42'),
(37, 1, '20230330187', '', '', '0.07', '0.05', '10', '2023-03-30 06:12:42'),
(38, 1, '20230330190', '', '', '0.28', '0.2', '40', '2023-03-30 06:19:22'),
(39, 1, '20230330190', '', '', '70', '50', '10000', '2023-03-30 06:19:27'),
(40, 1, '20230330333', '', '', '70', '50', '10000', '2023-03-30 11:05:19');

-- --------------------------------------------------------

--
-- Table structure for table `tbl_bonuswithdrawal`
--

CREATE TABLE `tbl_bonuswithdrawal` (
  `id` int(11) NOT NULL,
  `userid` int(11) NOT NULL,
  `amount` varchar(255) NOT NULL,
  `createdate` datetime NOT NULL
) ENGINE=MyISAM DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

-- --------------------------------------------------------

--
-- Table structure for table `tbl_envelop`
--

CREATE TABLE `tbl_envelop` (
  `id` int(11) NOT NULL,
  `userid` int(11) NOT NULL,
  `name` varchar(300) NOT NULL,
  `email` varchar(300) NOT NULL,
  `mobile` varchar(300) NOT NULL,
  `amount` float NOT NULL,
  `status` smallint(11) NOT NULL,
  `rechargestatus` smallint(11) NOT NULL,
  `createdate` timestamp NOT NULL DEFAULT current_timestamp()
) ENGINE=MyISAM DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

-- --------------------------------------------------------

--
-- Table structure for table `tbl_gameid`
--

CREATE TABLE `tbl_gameid` (
  `id` int(11) NOT NULL,
  `gameid` varchar(500) NOT NULL,
  `createdate` timestamp NOT NULL DEFAULT current_timestamp()
) ENGINE=MyISAM DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

--
-- Dumping data for table `tbl_gameid`
--

INSERT INTO `tbl_gameid` (`id`, `gameid`, `createdate`) VALUES
(1, '20230330001', '2023-03-29 18:30:02'),
(2, '20230330002', '2023-03-29 18:32:02'),
(3, '20230330003', '2023-03-29 18:34:02'),
(4, '20230330004', '2023-03-29 18:36:02'),
(5, '20230330005', '2023-03-29 18:38:02'),
(6, '20230330006', '2023-03-29 18:40:02'),
(7, '20230330007', '2023-03-29 18:42:02'),
(8, '20230330008', '2023-03-29 18:44:02'),
(9, '20230330009', '2023-03-29 18:46:01'),
(10, '20230330010', '2023-03-29 18:48:03'),
(11, '20230330011', '2023-03-29 18:50:02'),
(12, '20230330012', '2023-03-29 18:52:01'),
(13, '20230330013', '2023-03-29 18:54:03'),
(14, '20230330014', '2023-03-29 18:56:01'),
(15, '20230330015', '2023-03-29 18:58:01'),
(16, '20230330016', '2023-03-29 19:00:02'),
(17, '20230330017', '2023-03-29 19:02:02'),
(18, '20230330018', '2023-03-29 19:04:01'),
(19, '20230330019', '2023-03-29 19:06:02'),
(20, '20230330020', '2023-03-29 19:08:01'),
(21, '20230330021', '2023-03-29 19:10:02'),
(22, '20230330022', '2023-03-29 19:12:02'),
(23, '20230330023', '2023-03-29 19:14:02'),
(24, '20230330024', '2023-03-29 19:16:01'),
(25, '20230330025', '2023-03-29 19:18:02'),
(26, '20230330026', '2023-03-29 19:20:02'),
(27, '20230330027', '2023-03-29 19:22:01'),
(28, '20230330028', '2023-03-29 19:24:01'),
(29, '20230330029', '2023-03-29 19:26:02'),
(30, '20230330030', '2023-03-29 19:28:02'),
(31, '20230330031', '2023-03-29 19:30:02'),
(32, '20230330032', '2023-03-29 19:32:02'),
(33, '20230330033', '2023-03-29 19:34:02'),
(34, '20230330034', '2023-03-29 19:36:02'),
(35, '20230330035', '2023-03-29 19:38:01'),
(36, '20230330036', '2023-03-29 19:40:01'),
(37, '20230330037', '2023-03-29 19:42:01'),
(38, '20230330038', '2023-03-29 19:44:01'),
(39, '20230330039', '2023-03-29 19:46:02'),
(40, '20230330040', '2023-03-29 19:48:02'),
(41, '20230330041', '2023-03-29 19:50:02'),
(42, '20230330042', '2023-03-29 19:52:02'),
(43, '20230330043', '2023-03-29 19:54:01'),
(44, '20230330044', '2023-03-29 19:56:02'),
(45, '20230330045', '2023-03-29 19:58:01'),
(46, '20230330046', '2023-03-29 20:00:02'),
(47, '20230330047', '2023-03-29 20:02:02'),
(48, '20230330048', '2023-03-29 20:04:02'),
(49, '20230330049', '2023-03-29 20:06:01'),
(50, '20230330050', '2023-03-29 20:08:01'),
(51, '20230330051', '2023-03-29 20:10:02'),
(52, '20230330052', '2023-03-29 20:12:02'),
(53, '20230330053', '2023-03-29 20:14:02'),
(54, '20230330054', '2023-03-29 20:16:02'),
(55, '20230330055', '2023-03-29 20:18:01'),
(56, '20230330056', '2023-03-29 20:20:02'),
(57, '20230330057', '2023-03-29 20:22:02'),
(58, '20230330058', '2023-03-29 20:24:02'),
(59, '20230330059', '2023-03-29 20:26:02'),
(60, '20230330060', '2023-03-29 20:28:01'),
(61, '20230330061', '2023-03-29 20:30:02'),
(62, '20230330062', '2023-03-29 20:32:01'),
(63, '20230330063', '2023-03-29 20:34:02'),
(64, '20230330064', '2023-03-29 20:36:02'),
(65, '20230330065', '2023-03-29 20:38:02'),
(66, '20230330066', '2023-03-29 20:40:02'),
(67, '20230330067', '2023-03-29 20:42:01'),
(68, '20230330068', '2023-03-29 20:44:02'),
(69, '20230330069', '2023-03-29 20:46:02'),
(70, '20230330070', '2023-03-29 20:48:02'),
(71, '20230330071', '2023-03-29 20:50:02'),
(72, '20230330072', '2023-03-29 20:52:01'),
(73, '20230330073', '2023-03-29 20:54:02'),
(74, '20230330074', '2023-03-29 20:56:01'),
(75, '20230330075', '2023-03-29 20:58:02'),
(76, '20230330076', '2023-03-29 21:00:02'),
(77, '20230330077', '2023-03-29 21:02:01'),
(78, '20230330078', '2023-03-29 21:04:02'),
(79, '20230330079', '2023-03-29 21:06:02'),
(80, '20230330080', '2023-03-29 21:08:02'),
(81, '20230330081', '2023-03-29 21:10:02'),
(82, '20230330082', '2023-03-29 21:12:02'),
(83, '20230330083', '2023-03-29 21:14:02'),
(84, '20230330084', '2023-03-29 21:16:02'),
(85, '20230330085', '2023-03-29 21:18:01'),
(86, '20230330086', '2023-03-29 21:20:02'),
(87, '20230330087', '2023-03-29 21:22:02'),
(88, '20230330088', '2023-03-29 21:24:02'),
(89, '20230330089', '2023-03-29 21:26:01'),
(90, '20230330090', '2023-03-29 21:28:01'),
(91, '20230330091', '2023-03-29 21:30:02'),
(92, '20230330092', '2023-03-29 21:32:02'),
(93, '20230330093', '2023-03-29 21:34:02'),
(94, '20230330094', '2023-03-29 21:36:01'),
(95, '20230330095', '2023-03-29 21:38:02'),
(96, '20230330096', '2023-03-29 21:40:02'),
(97, '20230330097', '2023-03-29 21:42:02'),
(98, '20230330098', '2023-03-29 21:44:01'),
(99, '20230330099', '2023-03-29 21:46:01'),
(100, '20230330100', '2023-03-29 21:48:01'),
(101, '20230330101', '2023-03-29 21:50:02'),
(102, '20230330102', '2023-03-29 21:52:02'),
(103, '20230330103', '2023-03-29 21:54:02'),
(104, '20230330104', '2023-03-29 21:56:02'),
(105, '20230330105', '2023-03-29 21:58:02'),
(106, '20230330106', '2023-03-29 22:00:02'),
(107, '20230330107', '2023-03-29 22:02:01'),
(108, '20230330108', '2023-03-29 22:04:02'),
(109, '20230330109', '2023-03-29 22:06:02'),
(110, '20230330110', '2023-03-29 22:08:01'),
(111, '20230330111', '2023-03-29 22:10:02'),
(112, '20230330112', '2023-03-29 22:12:02'),
(113, '20230330113', '2023-03-29 22:14:01'),
(114, '20230330114', '2023-03-29 22:16:02'),
(115, '20230330115', '2023-03-29 22:18:01'),
(116, '20230330116', '2023-03-29 22:20:01'),
(117, '20230330117', '2023-03-29 22:22:02'),
(118, '20230330118', '2023-03-29 22:24:02'),
(119, '20230330119', '2023-03-29 22:26:01'),
(120, '20230330120', '2023-03-29 22:28:01'),
(121, '20230330121', '2023-03-29 22:30:02'),
(122, '20230330122', '2023-03-29 22:32:02'),
(123, '20230330123', '2023-03-29 22:34:01'),
(124, '20230330124', '2023-03-29 22:36:02'),
(125, '20230330125', '2023-03-29 22:38:02'),
(126, '20230330126', '2023-03-29 22:40:02'),
(127, '20230330127', '2023-03-29 22:42:01'),
(128, '20230330128', '2023-03-29 22:44:01'),
(129, '20230330129', '2023-03-29 22:46:02'),
(130, '20230330130', '2023-03-29 22:48:02'),
(131, '20230330131', '2023-03-29 22:50:02'),
(132, '20230330132', '2023-03-29 22:52:02'),
(133, '20230330133', '2023-03-29 22:54:02'),
(134, '20230330134', '2023-03-29 22:56:02'),
(135, '20230330135', '2023-03-29 22:58:01'),
(136, '20230330136', '2023-03-29 23:00:02'),
(137, '20230330137', '2023-03-29 23:02:02'),
(138, '20230330138', '2023-03-29 23:04:01'),
(139, '20230330139', '2023-03-29 23:06:02'),
(140, '20230330140', '2023-03-29 23:08:01'),
(141, '20230330141', '2023-03-29 23:10:02'),
(142, '20230330142', '2023-03-29 23:12:02'),
(143, '20230330143', '2023-03-29 23:14:02'),
(144, '20230330144', '2023-03-29 23:16:02'),
(145, '20230330145', '2023-03-29 23:18:02'),
(146, '20230330146', '2023-03-29 23:20:02'),
(147, '20230330147', '2023-03-29 23:22:01'),
(148, '20230330148', '2023-03-29 23:24:02'),
(149, '20230330149', '2023-03-29 23:26:01'),
(150, '20230330150', '2023-03-29 23:28:02'),
(151, '20230330151', '2023-03-29 23:30:02'),
(152, '20230330152', '2023-03-29 23:32:02'),
(153, '20230330153', '2023-03-29 23:34:02'),
(154, '20230330154', '2023-03-29 23:36:02'),
(155, '20230330155', '2023-03-29 23:38:01'),
(156, '20230330156', '2023-03-29 23:40:02'),
(157, '20230330157', '2023-03-29 23:42:02'),
(158, '20230330158', '2023-03-29 23:44:02'),
(159, '20230330159', '2023-03-29 23:46:01'),
(160, '20230330160', '2023-03-29 23:48:01'),
(161, '20230330161', '2023-03-29 23:50:02'),
(162, '20230330162', '2023-03-29 23:52:02'),
(163, '20230330163', '2023-03-29 23:54:02'),
(164, '20230330164', '2023-03-29 23:56:02'),
(165, '20230330165', '2023-03-29 23:58:01'),
(166, '20230330166', '2023-03-30 00:00:03'),
(167, '20230330167', '2023-03-30 00:02:02'),
(168, '20230330168', '2023-03-30 00:04:01'),
(169, '20230330169', '2023-03-30 00:06:01'),
(170, '20230330170', '2023-03-30 00:08:02'),
(171, '20230330171', '2023-03-30 00:10:02'),
(172, '20230330172', '2023-03-30 00:12:01'),
(173, '20230330173', '2023-03-30 00:14:01'),
(174, '20230330174', '2023-03-30 00:16:01'),
(175, '20230330175', '2023-03-30 00:18:02'),
(176, '20230330176', '2023-03-30 00:20:02'),
(177, '20230330177', '2023-03-30 00:22:02'),
(178, '20230330178', '2023-03-30 00:24:02'),
(179, '20230330179', '2023-03-30 00:26:02'),
(180, '20230330180', '2023-03-30 00:28:01'),
(181, '20230330181', '2023-03-30 00:30:02'),
(182, '20230330182', '2023-03-30 00:32:02'),
(183, '20230330183', '2023-03-30 00:34:02'),
(184, '20230330184', '2023-03-30 00:36:02'),
(185, '20230330185', '2023-03-30 00:38:01'),
(186, '20230330186', '2023-03-30 00:40:02'),
(187, '20230330187', '2023-03-30 00:42:02'),
(188, '20230330188', '2023-03-30 00:44:02'),
(189, '20230330189', '2023-03-30 00:46:02'),
(190, '20230330190', '2023-03-30 00:48:01'),
(191, '20230330191', '2023-03-30 00:50:01'),
(192, '20230330192', '2023-03-30 00:52:01'),
(193, '20230330193', '2023-03-30 00:54:02'),
(194, '20230330194', '2023-03-30 00:56:01'),
(195, '20230330195', '2023-03-30 00:58:02'),
(196, '20230330196', '2023-03-30 01:00:02'),
(197, '20230330197', '2023-03-30 01:02:01'),
(198, '20230330198', '2023-03-30 01:04:01'),
(199, '20230330199', '2023-03-30 01:06:01'),
(200, '20230330200', '2023-03-30 01:08:02'),
(201, '20230330201', '2023-03-30 01:10:02'),
(202, '20230330202', '2023-03-30 01:12:01'),
(203, '20230330203', '2023-03-30 01:14:02'),
(204, '20230330204', '2023-03-30 01:16:01'),
(205, '20230330205', '2023-03-30 01:18:01'),
(206, '20230330206', '2023-03-30 01:20:02'),
(207, '20230330207', '2023-03-30 01:22:01'),
(208, '20230330208', '2023-03-30 01:24:02'),
(209, '20230330209', '2023-03-30 01:26:01'),
(210, '20230330210', '2023-03-30 01:28:02'),
(211, '20230330211', '2023-03-30 01:30:02'),
(212, '20230330212', '2023-03-30 01:32:01'),
(213, '20230330213', '2023-03-30 01:34:02'),
(214, '20230330214', '2023-03-30 01:36:01'),
(215, '20230330215', '2023-03-30 01:38:01'),
(216, '20230330216', '2023-03-30 01:40:01'),
(217, '20230330217', '2023-03-30 01:42:02'),
(218, '20230330218', '2023-03-30 01:44:02'),
(219, '20230330219', '2023-03-30 01:46:01'),
(220, '20230330220', '2023-03-30 01:48:02'),
(221, '20230330221', '2023-03-30 01:50:02'),
(222, '20230330222', '2023-03-30 01:52:01'),
(223, '20230330223', '2023-03-30 01:54:02'),
(224, '20230330224', '2023-03-30 01:56:02'),
(225, '20230330225', '2023-03-30 01:58:01'),
(226, '20230330226', '2023-03-30 02:00:02'),
(227, '20230330227', '2023-03-30 02:02:01'),
(228, '20230330228', '2023-03-30 02:04:02'),
(229, '20230330229', '2023-03-30 02:06:01'),
(230, '20230330230', '2023-03-30 02:08:01'),
(231, '20230330231', '2023-03-30 02:10:02'),
(232, '20230330232', '2023-03-30 02:12:02'),
(233, '20230330233', '2023-03-30 02:14:02'),
(234, '20230330234', '2023-03-30 02:16:01'),
(235, '20230330235', '2023-03-30 02:18:01'),
(236, '20230330236', '2023-03-30 02:20:02'),
(237, '20230330237', '2023-03-30 02:22:01'),
(238, '20230330238', '2023-03-30 02:24:02'),
(239, '20230330239', '2023-03-30 02:26:02'),
(240, '20230330240', '2023-03-30 02:28:02'),
(241, '20230330241', '2023-03-30 02:30:02'),
(242, '20230330242', '2023-03-30 02:32:01'),
(243, '20230330243', '2023-03-30 02:34:01'),
(244, '20230330244', '2023-03-30 02:36:01'),
(245, '20230330245', '2023-03-30 02:38:01'),
(246, '20230330246', '2023-03-30 02:40:02'),
(247, '20230330247', '2023-03-30 02:42:02'),
(248, '20230330248', '2023-03-30 02:44:02'),
(249, '20230330249', '2023-03-30 02:46:01'),
(250, '20230330250', '2023-03-30 02:48:01'),
(251, '20230330251', '2023-03-30 02:50:02'),
(252, '20230330252', '2023-03-30 02:52:02'),
(253, '20230330253', '2023-03-30 02:54:02'),
(254, '20230330254', '2023-03-30 02:56:02'),
(255, '20230330255', '2023-03-30 02:58:02'),
(256, '20230330256', '2023-03-30 03:00:02'),
(257, '20230330257', '2023-03-30 03:02:01'),
(258, '20230330258', '2023-03-30 03:04:01'),
(259, '20230330259', '2023-03-30 03:06:02'),
(260, '20230330260', '2023-03-30 03:08:01'),
(261, '20230330261', '2023-03-30 03:10:02'),
(262, '20230330262', '2023-03-30 03:12:02'),
(263, '20230330263', '2023-03-30 03:14:02'),
(264, '20230330264', '2023-03-30 03:16:02'),
(265, '20230330265', '2023-03-30 03:18:02'),
(266, '20230330266', '2023-03-30 03:20:02'),
(267, '20230330267', '2023-03-30 03:22:01'),
(268, '20230330268', '2023-03-30 03:24:01'),
(269, '20230330269', '2023-03-30 03:26:01'),
(270, '20230330270', '2023-03-30 03:28:02'),
(271, '20230330271', '2023-03-30 03:30:01'),
(272, '20230330272', '2023-03-30 03:32:02'),
(273, '20230330273', '2023-03-30 03:34:01'),
(274, '20230330274', '2023-03-30 03:36:01'),
(275, '20230330275', '2023-03-30 03:38:02'),
(276, '20230330276', '2023-03-30 03:40:02'),
(277, '20230330277', '2023-03-30 03:42:01'),
(278, '20230330278', '2023-03-30 03:44:01'),
(279, '20230330279', '2023-03-30 03:46:01'),
(280, '20230330280', '2023-03-30 03:48:02'),
(281, '20230330281', '2023-03-30 03:50:02'),
(282, '20230330282', '2023-03-30 03:52:02'),
(283, '20230330283', '2023-03-30 03:54:01'),
(284, '20230330284', '2023-03-30 03:56:02'),
(285, '20230330285', '2023-03-30 03:58:02'),
(286, '20230330286', '2023-03-30 04:00:02'),
(287, '20230330287', '2023-03-30 04:02:01'),
(288, '20230330288', '2023-03-30 04:04:02'),
(289, '20230330289', '2023-03-30 04:06:02'),
(290, '20230330290', '2023-03-30 04:08:01'),
(291, '20230330291', '2023-03-30 04:10:02'),
(292, '20230330292', '2023-03-30 04:12:02'),
(293, '20230330293', '2023-03-30 04:14:02'),
(294, '20230330294', '2023-03-30 04:16:01'),
(295, '20230330295', '2023-03-30 04:18:01'),
(296, '20230330296', '2023-03-30 04:20:02'),
(297, '20230330297', '2023-03-30 04:22:02'),
(298, '20230330298', '2023-03-30 04:24:02'),
(299, '20230330299', '2023-03-30 04:26:02'),
(300, '20230330300', '2023-03-30 04:28:02'),
(301, '20230330301', '2023-03-30 04:30:03'),
(302, '20230330302', '2023-03-30 04:32:01'),
(303, '20230330303', '2023-03-30 04:34:02'),
(304, '20230330304', '2023-03-30 04:36:02'),
(305, '20230330305', '2023-03-30 04:38:02'),
(306, '20230330306', '2023-03-30 04:40:01'),
(307, '20230330307', '2023-03-30 04:42:02'),
(308, '20230330308', '2023-03-30 04:44:02'),
(309, '20230330309', '2023-03-30 04:46:02'),
(310, '20230330310', '2023-03-30 04:48:01'),
(311, '20230330311', '2023-03-30 04:50:02'),
(312, '20230330312', '2023-03-30 04:52:01'),
(313, '20230330313', '2023-03-30 04:54:01'),
(314, '20230330314', '2023-03-30 04:56:01'),
(315, '20230330315', '2023-03-30 04:58:02'),
(316, '20230330316', '2023-03-30 05:00:03'),
(317, '20230330317', '2023-03-30 05:02:01'),
(318, '20230330318', '2023-03-30 05:04:02'),
(319, '20230330319', '2023-03-30 05:06:02'),
(320, '20230330320', '2023-03-30 05:08:01'),
(321, '20230330321', '2023-03-30 05:10:02'),
(322, '20230330322', '2023-03-30 05:12:02'),
(323, '20230330323', '2023-03-30 05:14:02'),
(324, '20230330324', '2023-03-30 05:16:02'),
(325, '20230330325', '2023-03-30 05:18:02'),
(326, '20230330326', '2023-03-30 05:20:02'),
(327, '20230330327', '2023-03-30 05:22:02'),
(328, '20230330328', '2023-03-30 05:24:01'),
(329, '20230330329', '2023-03-30 05:26:02'),
(330, '20230330330', '2023-03-30 05:28:01'),
(331, '20230330331', '2023-03-30 05:30:02'),
(332, '20230330332', '2023-03-30 05:32:01'),
(333, '20230330333', '2023-03-30 05:34:01'),
(334, '20230330334', '2023-03-30 05:36:01'),
(335, '20230330335', '2023-03-30 05:38:01'),
(336, '20230330336', '2023-03-30 05:40:02'),
(337, '20230330337', '2023-03-30 05:42:01'),
(338, '20230330338', '2023-03-30 05:44:02'),
(339, '20230330339', '2023-03-30 05:46:01'),
(340, '20230330340', '2023-03-30 05:48:01'),
(341, '20230330341', '2023-03-30 05:50:02'),
(342, '20230330342', '2023-03-30 05:52:01'),
(343, '20230330343', '2023-03-30 05:54:01'),
(344, '20230330344', '2023-03-30 05:56:02'),
(345, '20230330345', '2023-03-30 05:58:02'),
(346, '20230330346', '2023-03-30 06:00:02'),
(347, '20230330347', '2023-03-30 06:02:01'),
(348, '20230330348', '2023-03-30 06:04:02'),
(349, '20230330349', '2023-03-30 06:06:01'),
(350, '20230330350', '2023-03-30 06:08:01'),
(351, '20230330351', '2023-03-30 06:10:02'),
(352, '20230330352', '2023-03-30 06:12:02'),
(353, '20230330353', '2023-03-30 06:14:02'),
(354, '20230330354', '2023-03-30 06:16:01'),
(355, '20230330355', '2023-03-30 06:18:02'),
(356, '20230330356', '2023-03-30 06:20:02'),
(357, '20230330357', '2023-03-30 06:22:01'),
(358, '20230330358', '2023-03-30 06:24:01'),
(359, '20230330359', '2023-03-30 06:26:01'),
(360, '20230330360', '2023-03-30 06:28:01'),
(361, '20230330361', '2023-03-30 06:30:02'),
(362, '20230330362', '2023-03-30 06:32:01'),
(363, '20230330363', '2023-03-30 06:34:02'),
(364, '20230330364', '2023-03-30 06:36:02'),
(365, '20230330365', '2023-03-30 06:38:02'),
(366, '20230330366', '2023-03-30 06:40:02'),
(367, '20230330367', '2023-03-30 06:42:02'),
(368, '20230330368', '2023-03-30 06:44:02'),
(369, '20230330369', '2023-03-30 06:46:01'),
(370, '20230330370', '2023-03-30 06:48:01'),
(371, '20230330371', '2023-03-30 06:50:02'),
(372, '20230330372', '2023-03-30 06:52:01'),
(373, '20230330373', '2023-03-30 06:54:01'),
(374, '20230330374', '2023-03-30 06:56:02'),
(375, '20230330375', '2023-03-30 06:58:01'),
(376, '20230330376', '2023-03-30 07:00:02'),
(377, '20230330377', '2023-03-30 07:02:01'),
(378, '20230330378', '2023-03-30 07:04:01'),
(379, '20230330379', '2023-03-30 07:06:02'),
(380, '20230330380', '2023-03-30 07:08:02'),
(381, '20230330381', '2023-03-30 07:10:02'),
(382, '20230330382', '2023-03-30 07:12:01'),
(383, '20230330383', '2023-03-30 07:14:01'),
(384, '20230330384', '2023-03-30 07:16:02'),
(385, '20230330385', '2023-03-30 07:18:02'),
(386, '20230330386', '2023-03-30 07:20:01'),
(387, '20230330387', '2023-03-30 07:22:02'),
(388, '20230330388', '2023-03-30 07:24:02'),
(389, '20230330389', '2023-03-30 07:26:02'),
(390, '20230330390', '2023-03-30 07:28:02'),
(391, '20230330391', '2023-03-30 07:30:02'),
(392, '20230330392', '2023-03-30 07:32:02'),
(393, '20230330393', '2023-03-30 07:34:01'),
(394, '20230330394', '2023-03-30 07:36:01'),
(395, '20230330395', '2023-03-30 07:38:02'),
(396, '20230330396', '2023-03-30 07:40:01'),
(397, '20230330397', '2023-03-30 07:42:01'),
(398, '20230330398', '2023-03-30 07:44:01'),
(399, '20230330399', '2023-03-30 07:46:02'),
(400, '20230330400', '2023-03-30 07:48:01'),
(401, '20230330401', '2023-03-30 07:50:02'),
(402, '20230330402', '2023-03-30 07:52:01'),
(403, '20230330403', '2023-03-30 07:54:02'),
(404, '20230330404', '2023-03-30 07:56:01'),
(405, '20230330405', '2023-03-30 07:58:02'),
(406, '20230330406', '2023-03-30 08:00:03'),
(407, '20230330407', '2023-03-30 08:02:01'),
(408, '20230330408', '2023-03-30 08:04:02'),
(409, '20230330409', '2023-03-30 08:06:01'),
(410, '20230330410', '2023-03-30 08:08:01'),
(411, '20230330411', '2023-03-30 08:10:02'),
(412, '20230330412', '2023-03-30 08:12:01'),
(413, '20230330413', '2023-03-30 08:14:01'),
(414, '20230330414', '2023-03-30 08:16:02'),
(415, '20230330415', '2023-03-30 08:18:01'),
(416, '20230330416', '2023-03-30 08:20:02'),
(417, '20230330417', '2023-03-30 08:22:02'),
(418, '20230330418', '2023-03-30 08:24:02'),
(419, '20230330419', '2023-03-30 08:26:01'),
(420, '20230330420', '2023-03-30 08:28:01'),
(421, '20230330421', '2023-03-30 08:30:02'),
(422, '20230330422', '2023-03-30 08:32:01'),
(423, '20230330423', '2023-03-30 08:34:01'),
(424, '20230330424', '2023-03-30 08:36:01'),
(425, '20230330425', '2023-03-30 08:38:02'),
(426, '20230330426', '2023-03-30 08:40:02'),
(427, '20230330427', '2023-03-30 08:42:01'),
(428, '20230330428', '2023-03-30 08:44:01'),
(429, '20230330429', '2023-03-30 08:46:01'),
(430, '20230330430', '2023-03-30 08:48:02');

-- --------------------------------------------------------

--
-- Table structure for table `tbl_gamesettings`
--

CREATE TABLE `tbl_gamesettings` (
  `id` int(11) NOT NULL,
  `settingtype` varchar(255) NOT NULL,
  `createdate` datetime NOT NULL
) ENGINE=MyISAM DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

--
-- Dumping data for table `tbl_gamesettings`
--

INSERT INTO `tbl_gamesettings` (`id`, `settingtype`, `createdate`) VALUES
(1, 'low', '2021-05-28 15:29:42');

-- --------------------------------------------------------

--
-- Table structure for table `tbl_manualresult`
--

CREATE TABLE `tbl_manualresult` (
  `id` int(11) NOT NULL,
  `color` varchar(300) NOT NULL,
  `value` varchar(300) NOT NULL,
  `number` int(11) NOT NULL,
  `status` smallint(11) NOT NULL,
  `createdate` datetime NOT NULL
) ENGINE=MyISAM DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

--
-- Dumping data for table `tbl_manualresult`
--

INSERT INTO `tbl_manualresult` (`id`, `color`, `value`, `number`, `status`, `createdate`) VALUES
(1, '<span style=\"color:#f00;\">Red</span> + <span style=\"color:#C71585;\">Violet</span>', 'red+violet', 0, 0, '2021-02-01 00:00:00'),
(2, '<span style=\"color:#090;\">Green</span>', 'green', 1, 0, '2021-02-01 00:00:00'),
(3, '<span style=\"color:#f00;\">Red</span>', 'red', 2, 0, '2021-02-01 00:00:00'),
(4, '<span style=\"color:#090;\">Green</span>', 'green', 3, 0, '2021-02-01 00:00:00'),
(5, '<span style=\"color:#f00;\">Red</span>', 'red', 4, 0, '2021-02-01 00:00:00'),
(6, '<span style=\"color:#090;\">Green</span> + <span style=\"color:#C71585;\">Violet</span>', 'green+violet', 5, 0, '2021-02-01 00:00:00'),
(7, '<span style=\"color:#f00;\">Red</span>', 'red', 6, 0, '2021-02-01 00:00:00'),
(8, '<span style=\"color:#090;\">Green</span>', 'green', 7, 0, '2021-02-01 00:00:00'),
(9, '<span style=\"color:#f00;\">Red</span>', 'red', 8, 0, '2021-02-01 00:00:00'),
(10, '<span style=\"color:#090;\">Green</span>', 'green', 9, 0, '2021-02-01 00:00:00');

-- --------------------------------------------------------

--
-- Table structure for table `tbl_manualresultswitch`
--

CREATE TABLE `tbl_manualresultswitch` (
  `id` int(11) NOT NULL,
  `switch` varchar(50) NOT NULL,
  `tab` varchar(50) NOT NULL,
  `createdate` datetime NOT NULL
) ENGINE=MyISAM DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

--
-- Dumping data for table `tbl_manualresultswitch`
--

INSERT INTO `tbl_manualresultswitch` (`id`, `switch`, `tab`, `createdate`) VALUES
(1, 'no', '', '2023-03-30 13:32:07');

-- --------------------------------------------------------

--
-- Table structure for table `tbl_order`
--

CREATE TABLE `tbl_order` (
  `id` int(11) NOT NULL,
  `userid` int(11) NOT NULL,
  `transactionid` varchar(300) NOT NULL,
  `amount` varchar(300) NOT NULL,
  `status` smallint(11) NOT NULL,
  `createdate` timestamp NOT NULL DEFAULT current_timestamp()
) ENGINE=MyISAM DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

--
-- Dumping data for table `tbl_order`
--

INSERT INTO `tbl_order` (`id`, `userid`, `transactionid`, `amount`, `status`, `createdate`) VALUES
(1, 1, '20230329540', '10', 1, '2023-03-29 12:28:37'),
(2, 1, '20230329540', '10', 1, '2023-03-29 12:28:40'),
(3, 1, '20230329540', '10', 1, '2023-03-29 12:28:45'),
(4, 1, '20230329540', '10', 1, '2023-03-29 12:28:47'),
(5, 1, '20230329540', '10', 1, '2023-03-29 12:28:56'),
(6, 1, '20230329540', '10', 1, '2023-03-29 12:28:58'),
(7, 1, '20230329540', '10', 1, '2023-03-29 12:29:03'),
(8, 1, '20230329540', '10', 1, '2023-03-29 12:29:08'),
(9, 1, '20230329540', '10', 1, '2023-03-29 12:29:14'),
(10, 1, '20230329540', '10', 1, '2023-03-29 12:29:16'),
(11, 1, '20230329540', '10', 1, '2023-03-29 12:29:19'),
(12, 1, '20230329540', '19.6', 1, '2023-03-29 18:00:03'),
(13, 1, '20230329540', '88.2', 1, '2023-03-29 18:00:03'),
(14, 1, '20230329541', '10', 1, '2023-03-29 12:30:29'),
(15, 1, '20230329541', '10', 1, '2023-03-29 12:30:32'),
(16, 1, '20230329541', '10', 1, '2023-03-29 12:30:35'),
(17, 1, '20230329541', '10', 1, '2023-03-29 12:30:38'),
(18, 1, '20230329541', '10', 1, '2023-03-29 12:30:40'),
(19, 1, '20230329541', '10', 1, '2023-03-29 12:30:49'),
(20, 1, '20230329541', '10', 1, '2023-03-29 12:30:49'),
(21, 1, '20230329541', '10', 1, '2023-03-29 12:30:49'),
(22, 1, '20230329541', '10', 1, '2023-03-29 12:30:56'),
(23, 1, '20230329541', '10', 1, '2023-03-29 12:31:02'),
(24, 1, '20230329541', '10', 1, '2023-03-29 12:31:07'),
(25, 1, '20230329541', '10', 1, '2023-03-29 12:31:14'),
(26, 1, '20230329541', '10', 1, '2023-03-29 12:31:19'),
(27, 1, '20230329541', '10', 1, '2023-03-29 12:31:26'),
(28, 1, '20230329541', '19.6', 1, '2023-03-29 18:02:02'),
(29, 1, '20230329541', '88.2', 1, '2023-03-29 18:02:02'),
(30, 1, '20230329541', '88.2', 1, '2023-03-29 18:02:02'),
(31, 1, '20230329541', '88.2', 1, '2023-03-29 18:02:02'),
(32, 1, 'reward', '2000', 1, '2023-03-29 12:32:17'),
(33, 1, 'reward', '20000000000', 1, '2023-03-29 12:32:37'),
(34, 1, '20230329545', '10000', 1, '2023-03-29 12:39:10'),
(35, 1, '20230329546', '10000', 1, '2023-03-29 12:40:40'),
(36, 1, '20230329546', '10000', 1, '2023-03-29 12:40:56'),
(37, 1, '20230329546', '10000', 1, '2023-03-29 12:41:00'),
(38, 1, '20230329546', '10000', 1, '2023-03-29 12:41:05'),
(39, 1, '20230329546', '88200', 1, '2023-03-29 18:12:01'),
(40, 1, '20230329546', '88200', 1, '2023-03-29 18:12:01'),
(41, 1, '20230329546', '88200', 1, '2023-03-29 18:12:01'),
(42, 1, '20230329546', '88200', 1, '2023-03-29 18:12:01'),
(43, 1, '20230329547', '10000', 1, '2023-03-29 12:42:21'),
(44, 1, '20230329547', '10000', 1, '2023-03-29 12:42:31'),
(45, 1, '20230329547', '10000', 1, '2023-03-29 12:42:34'),
(46, 1, '20230329547', '10000', 1, '2023-03-29 12:42:38'),
(47, 1, '20230329547', '88200', 1, '2023-03-29 18:14:02'),
(48, 1, '20230329547', '88200', 1, '2023-03-29 18:14:02'),
(49, 1, '20230329547', '88200', 1, '2023-03-29 18:14:02'),
(50, 1, '20230329547', '88200', 1, '2023-03-29 18:14:02'),
(51, 2, '20230329549', '1000', 1, '2023-03-29 12:46:28'),
(52, 2, '20230329549', '1960', 1, '2023-03-29 18:18:02'),
(53, 1, 'withdraw', '2000', 1, '2023-03-29 14:11:02'),
(54, 1, 'withdraw', '50000', 1, '2023-03-29 14:42:03'),
(55, 1, 'withdraw', '5000', 1, '2023-03-29 14:59:44'),
(56, 1, 'withdraw', '20000', 1, '2023-03-29 15:43:14'),
(57, 1, '20230330187', '10', 1, '2023-03-30 00:42:42'),
(58, 1, '20230330187', '10', 1, '2023-03-30 00:42:42'),
(59, 1, '20230330190', '40', 1, '2023-03-30 00:49:22'),
(60, 1, '20230330190', '10000', 1, '2023-03-30 00:49:27'),
(61, 1, '20230330190', '352.8', 1, '2023-03-30 06:20:01'),
(62, 1, '20230330190', '88200', 1, '2023-03-30 06:20:01'),
(63, 1, '20230330333', '10000', 1, '2023-03-30 05:35:19'),
(64, 1, '20230330333', '88200', 1, '2023-03-30 11:06:01');

-- --------------------------------------------------------

--
-- Table structure for table `tbl_paymentsetting`
--

CREATE TABLE `tbl_paymentsetting` (
  `id` int(11) NOT NULL,
  `rechargeamount` varchar(500) NOT NULL,
  `withdrawalamount` varchar(500) NOT NULL,
  `bonusamount` varchar(500) NOT NULL,
  `rechargebonus` varchar(500) NOT NULL COMMENT 'in%age',
  `level1` varchar(300) NOT NULL COMMENT 'In%age',
  `level2` varchar(300) NOT NULL COMMENT 'In%age'
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

--
-- Dumping data for table `tbl_paymentsetting`
--

INSERT INTO `tbl_paymentsetting` (`id`, `rechargeamount`, `withdrawalamount`, `bonusamount`, `rechargebonus`, `level1`, `level2`) VALUES
(1, '1000', '300', '198', '10', '00.7', '00.5');

-- --------------------------------------------------------

--
-- Table structure for table `tbl_product`
--

CREATE TABLE `tbl_product` (
  `id` int(11) NOT NULL,
  `name` text NOT NULL,
  `price` varchar(255) NOT NULL,
  `images` varchar(300) NOT NULL,
  `status` smallint(11) NOT NULL
) ENGINE=MyISAM DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

--
-- Dumping data for table `tbl_product`
--

INSERT INTO `tbl_product` (`id`, `name`, `price`, `images`, `status`) VALUES
(1, 'Rose Gold Plated Ring With Diamond Leaves and beautiful design For Girls & Women', '29580.00', 'p3.png', 1),
(2, 'Rose Gold Plated Ring With Diamond Crystal on the Top For Girls & Women', '35590.00', 'p1.png', 1),
(3, 'Rose Gold Plated Watch With Diamonds ands classic design For Girls & Women', '92590.00', 'p2.png', 1),
(4, 'Rose Gold Plated Watch With Diamonds ands classic design For Boys & Men', '78510.00', 'p4.png', 1);

-- --------------------------------------------------------

--
-- Table structure for table `tbl_productfeature`
--

CREATE TABLE `tbl_productfeature` (
  `id` int(11) NOT NULL,
  `productid` int(11) NOT NULL,
  `title` varchar(500) NOT NULL,
  `feature` varchar(500) NOT NULL,
  `status` smallint(11) NOT NULL
) ENGINE=MyISAM DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

--
-- Dumping data for table `tbl_productfeature`
--

INSERT INTO `tbl_productfeature` (`id`, `productid`, `title`, `feature`, `status`) VALUES
(1, 1, 'Stone', 'American Diamond', 1),
(8, 2, 'Packaging', 'Elegant Jewellery Box/ Jewellery Pouch', 1),
(7, 2, 'Material', 'Rose Gold Plated', 1),
(2, 1, 'Material', 'Rose Gold Plated', 1),
(3, 1, 'Packaging', 'Elegant Jewellery Box/ Jewellery Pouch', 1),
(4, 1, 'Ring Size', 'Free Size', 1),
(5, 1, 'Warranty Type', 'Seller', 1),
(6, 2, 'Stone', 'American Diamond', 1),
(9, 2, 'Ring Size', 'Free Size', 1),
(10, 2, 'Warranty Type', 'Seller', 1),
(11, 3, 'Stone', 'American Diamond', 1),
(12, 3, 'Material', 'Rose Gold Plated', 1),
(13, 3, 'Packaging', 'Elegant Jewellery Box/ Jewellery Pouch', 1),
(14, 3, 'Wrist Size', 'Free Size', 1),
(15, 3, 'Warranty Type', 'Seller', 1),
(16, 4, 'Stone', 'American Diamond', 1),
(17, 4, 'Material', 'Rose Gold Plated', 1),
(18, 4, 'Packaging', 'Elegant Jewellery Box/ Jewellery Pouch', 1),
(19, 4, 'Wrist Size', 'Free Size', 1),
(20, 4, 'Warranty Type', 'Seller', 1);

-- --------------------------------------------------------

--
-- Table structure for table `tbl_randomdata`
--

CREATE TABLE `tbl_randomdata` (
  `id` int(11) NOT NULL,
  `price` float NOT NULL,
  `result` int(11) NOT NULL,
  `color` varchar(100) NOT NULL,
  `timer` int(11) NOT NULL,
  `dayofweek` varchar(100) NOT NULL
) ENGINE=MyISAM DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

--
-- Dumping data for table `tbl_randomdata`
--

INSERT INTO `tbl_randomdata` (`id`, `price`, `result`, `color`, `timer`, `dayofweek`) VALUES
(1, 31069, 9, 'GREEN', 1, 'Day 1'),
(2, 31041, 1, 'GREEN', 2, 'Day 1'),
(3, 31026, 6, 'RED', 3, 'Day 1'),
(4, 30937, 7, 'GREEN', 4, 'Day 1'),
(5, 31024, 4, 'RED', 5, 'Day 1'),
(6, 30952, 2, 'RED', 6, 'Day 1'),
(7, 30863, 3, 'GREEN', 7, 'Day 1'),
(8, 30808, 8, 'RED', 8, 'Day 1'),
(9, 30795, 5, 'GREEN & VIOLET', 9, 'Day 1'),
(10, 30710, 0, 'RED & VIOLET', 10, 'Day 1'),
(11, 30706, 6, 'RED', 11, 'Day 1'),
(12, 30702, 2, 'RED', 12, 'Day 1'),
(13, 30769, 9, 'GREEN', 13, 'Day 1'),
(14, 30809, 9, 'GREEN', 14, 'Day 1'),
(15, 30782, 2, 'RED', 15, 'Day 1'),
(16, 30879, 9, 'GREEN', 16, 'Day 1'),
(17, 30810, 0, 'RED & VIOLET', 17, 'Day 1'),
(18, 30891, 1, 'GREEN', 18, 'Day 1'),
(19, 30973, 3, 'GREEN', 19, 'Day 1'),
(20, 30871, 1, 'GREEN', 20, 'Day 1'),
(21, 30846, 6, 'RED', 21, 'Day 1'),
(22, 30885, 5, 'GREEN & VIOLET', 22, 'Day 1'),
(23, 30951, 1, 'GREEN', 23, 'Day 1'),
(24, 31000, 0, 'RED & VIOLET', 24, 'Day 1'),
(25, 31011, 1, 'GREEN', 25, 'Day 1'),
(26, 30922, 2, 'RED', 26, 'Day 1'),
(27, 30967, 7, 'GREEN', 27, 'Day 1'),
(28, 30881, 1, 'GREEN', 28, 'Day 1'),
(29, 30857, 7, 'GREEN', 29, 'Day 1'),
(30, 30786, 6, 'RED', 30, 'Day 1'),
(31, 30761, 1, 'GREEN', 31, 'Day 1'),
(32, 30724, 4, 'RED', 32, 'Day 1'),
(33, 30778, 8, 'RED', 33, 'Day 1'),
(34, 30863, 3, 'GREEN', 34, 'Day 1'),
(35, 30940, 0, 'RED & VIOLET', 35, 'Day 1'),
(36, 30844, 4, 'RED', 36, 'Day 1'),
(37, 30803, 3, 'GREEN', 37, 'Day 1'),
(38, 30852, 2, 'RED', 38, 'Day 1'),
(39, 30945, 5, 'GREEN & VIOLET', 39, 'Day 1'),
(40, 30882, 2, 'RED', 40, 'Day 1'),
(41, 30853, 3, 'GREEN', 41, 'Day 1'),
(42, 30931, 1, 'GREEN', 42, 'Day 1'),
(43, 30901, 1, 'GREEN', 43, 'Day 1'),
(44, 30821, 1, 'GREEN', 44, 'Day 1'),
(45, 30784, 4, 'RED', 45, 'Day 1'),
(46, 30754, 4, 'RED', 46, 'Day 1'),
(47, 30816, 6, 'RED', 47, 'Day 1'),
(48, 30912, 2, 'RED', 48, 'Day 1'),
(49, 30836, 6, 'RED', 49, 'Day 1'),
(50, 30807, 7, 'GREEN', 50, 'Day 1'),
(51, 30800, 0, 'RED & VIOLET', 51, 'Day 1'),
(52, 30811, 1, 'GREEN', 52, 'Day 1'),
(53, 30859, 9, 'GREEN', 53, 'Day 1'),
(54, 30840, 0, 'RED & VIOLET', 54, 'Day 1'),
(55, 30934, 4, 'RED', 55, 'Day 1'),
(56, 30853, 3, 'GREEN', 56, 'Day 1'),
(57, 30802, 2, 'RED', 57, 'Day 1'),
(58, 30812, 2, 'RED', 58, 'Day 1'),
(59, 30845, 5, 'GREEN & VIOLET', 59, 'Day 1'),
(60, 30873, 3, 'GREEN', 60, 'Day 1'),
(61, 30799, 9, 'GREEN', 61, 'Day 1'),
(62, 30803, 3, 'GREEN', 62, 'Day 1'),
(63, 30858, 8, 'RED', 63, 'Day 1'),
(64, 30903, 3, 'GREEN', 64, 'Day 1'),
(65, 30872, 2, 'RED', 65, 'Day 1'),
(66, 30774, 4, 'RED', 66, 'Day 1'),
(67, 30856, 6, 'RED', 67, 'Day 1'),
(68, 30823, 3, 'GREEN', 68, 'Day 1'),
(69, 30826, 6, 'RED', 69, 'Day 1'),
(70, 30789, 9, 'GREEN', 70, 'Day 1'),
(71, 30748, 8, 'RED', 71, 'Day 1'),
(72, 30834, 4, 'RED', 72, 'Day 1'),
(73, 30785, 5, 'GREEN & VIOLET', 73, 'Day 1'),
(74, 30830, 0, 'RED & VIOLET', 74, 'Day 1'),
(75, 30792, 2, 'RED', 75, 'Day 1'),
(76, 30792, 2, 'RED', 76, 'Day 1'),
(77, 30874, 4, 'RED', 77, 'Day 1'),
(78, 30817, 7, 'GREEN', 78, 'Day 1'),
(79, 30776, 6, 'RED', 79, 'Day 1'),
(80, 30873, 3, 'GREEN', 80, 'Day 1'),
(81, 30905, 5, 'GREEN & VIOLET', 81, 'Day 1'),
(82, 31001, 1, 'GREEN', 82, 'Day 1'),
(83, 31032, 2, 'RED', 83, 'Day 1'),
(84, 31071, 1, 'GREEN', 84, 'Day 1'),
(85, 31067, 7, 'GREEN', 85, 'Day 1'),
(86, 31072, 2, 'RED', 86, 'Day 1'),
(87, 31157, 7, 'GREEN', 87, 'Day 1'),
(88, 31197, 7, 'GREEN', 88, 'Day 1'),
(89, 31200, 0, 'RED & VIOLET', 89, 'Day 1'),
(90, 31113, 3, 'GREEN', 90, 'Day 1'),
(91, 31112, 2, 'RED', 91, 'Day 1'),
(92, 31198, 8, 'RED', 92, 'Day 1'),
(93, 31130, 0, 'RED & VIOLET', 93, 'Day 1'),
(94, 31109, 9, 'GREEN', 94, 'Day 1'),
(95, 31142, 2, 'RED', 95, 'Day 1'),
(96, 31223, 3, 'GREEN', 96, 'Day 1'),
(97, 31270, 0, 'RED & VIOLET', 97, 'Day 1'),
(98, 31297, 7, 'GREEN', 98, 'Day 1'),
(99, 31208, 8, 'RED', 99, 'Day 1'),
(100, 31152, 2, 'RED', 100, 'Day 1'),
(101, 31232, 2, 'RED', 101, 'Day 1'),
(102, 31299, 9, 'GREEN', 102, 'Day 1'),
(103, 31388, 8, 'RED', 103, 'Day 1'),
(104, 31337, 7, 'GREEN', 104, 'Day 1'),
(105, 31360, 0, 'RED & VIOLET', 105, 'Day 1'),
(106, 31417, 7, 'GREEN', 106, 'Day 1'),
(107, 31394, 4, 'RED', 107, 'Day 1'),
(108, 31486, 6, 'RED', 108, 'Day 1'),
(109, 31450, 0, 'RED & VIOLET', 109, 'Day 1'),
(110, 31482, 2, 'RED', 110, 'Day 1'),
(111, 31512, 2, 'RED', 111, 'Day 1'),
(112, 31483, 3, 'GREEN', 112, 'Day 1'),
(113, 31532, 2, 'RED', 113, 'Day 1'),
(114, 31549, 9, 'GREEN', 114, 'Day 1'),
(115, 31458, 8, 'RED', 115, 'Day 1'),
(116, 31528, 8, 'RED', 116, 'Day 1'),
(117, 31612, 2, 'RED', 117, 'Day 1'),
(118, 31553, 3, 'GREEN', 118, 'Day 1'),
(119, 31553, 3, 'GREEN', 119, 'Day 1'),
(120, 31514, 4, 'RED', 120, 'Day 1'),
(121, 31551, 1, 'GREEN', 121, 'Day 1'),
(122, 31568, 8, 'RED', 122, 'Day 1'),
(123, 31577, 7, 'GREEN', 123, 'Day 1'),
(124, 31486, 6, 'RED', 124, 'Day 1'),
(125, 31498, 8, 'RED', 125, 'Day 1'),
(126, 31457, 7, 'GREEN', 126, 'Day 1'),
(127, 31394, 4, 'RED', 127, 'Day 1'),
(128, 31416, 6, 'RED', 128, 'Day 1'),
(129, 31426, 6, 'RED', 129, 'Day 1'),
(130, 31480, 0, 'RED & VIOLET', 130, 'Day 1'),
(131, 31424, 4, 'RED', 131, 'Day 1'),
(132, 31414, 4, 'RED', 132, 'Day 1'),
(133, 31398, 8, 'RED', 133, 'Day 1'),
(134, 31417, 7, 'GREEN', 134, 'Day 1'),
(135, 31443, 3, 'GREEN', 135, 'Day 1'),
(136, 31483, 3, 'GREEN', 136, 'Day 1'),
(137, 31551, 1, 'GREEN', 137, 'Day 1'),
(138, 31466, 6, 'RED', 138, 'Day 1'),
(139, 31371, 1, 'GREEN', 139, 'Day 1'),
(140, 31447, 7, 'GREEN', 140, 'Day 1'),
(141, 31449, 9, 'GREEN', 141, 'Day 1'),
(142, 31499, 9, 'GREEN', 142, 'Day 1'),
(143, 31574, 4, 'RED', 143, 'Day 1'),
(144, 31610, 0, 'RED & VIOLET', 144, 'Day 1'),
(145, 31616, 6, 'RED', 145, 'Day 1'),
(146, 31689, 9, 'GREEN', 146, 'Day 1'),
(147, 31630, 0, 'RED & VIOLET', 147, 'Day 1'),
(148, 31636, 6, 'RED', 148, 'Day 1'),
(149, 31630, 0, 'RED & VIOLET', 149, 'Day 1'),
(150, 31657, 7, 'GREEN', 150, 'Day 1'),
(151, 31745, 5, 'GREEN & VIOLET', 151, 'Day 1'),
(152, 31821, 1, 'GREEN', 152, 'Day 1'),
(153, 31763, 3, 'GREEN', 153, 'Day 1'),
(154, 31680, 0, 'RED & VIOLET', 154, 'Day 1'),
(155, 31668, 8, 'RED', 155, 'Day 1'),
(156, 31638, 8, 'RED', 156, 'Day 1'),
(157, 31641, 1, 'GREEN', 157, 'Day 1'),
(158, 31709, 9, 'GREEN', 158, 'Day 1'),
(159, 31701, 1, 'GREEN', 159, 'Day 1'),
(160, 31646, 6, 'RED', 160, 'Day 1'),
(161, 31647, 7, 'GREEN', 161, 'Day 1'),
(162, 31713, 3, 'GREEN', 162, 'Day 1'),
(163, 31770, 0, 'RED & VIOLET', 163, 'Day 1'),
(164, 31866, 6, 'RED', 164, 'Day 1'),
(165, 31812, 2, 'RED', 165, 'Day 1'),
(166, 31863, 3, 'GREEN', 166, 'Day 1'),
(167, 31802, 2, 'RED', 167, 'Day 1'),
(168, 31893, 3, 'GREEN', 168, 'Day 1'),
(169, 31970, 0, 'RED & VIOLET', 169, 'Day 1'),
(170, 31921, 1, 'GREEN', 170, 'Day 1'),
(171, 31983, 3, 'GREEN', 171, 'Day 1'),
(172, 31887, 7, 'GREEN', 172, 'Day 1'),
(173, 31841, 1, 'GREEN', 173, 'Day 1'),
(174, 31910, 0, 'RED & VIOLET', 174, 'Day 1'),
(175, 31817, 7, 'GREEN', 175, 'Day 1'),
(176, 31734, 4, 'RED', 176, 'Day 1'),
(177, 31749, 9, 'GREEN', 177, 'Day 1'),
(178, 31812, 2, 'RED', 178, 'Day 1'),
(179, 31827, 7, 'GREEN', 179, 'Day 1'),
(180, 31857, 7, 'GREEN', 180, 'Day 1'),
(181, 31769, 9, 'GREEN', 181, 'Day 1'),
(182, 31863, 3, 'GREEN', 182, 'Day 1'),
(183, 31794, 4, 'RED', 183, 'Day 1'),
(184, 31695, 5, 'GREEN & VIOLET', 184, 'Day 1'),
(185, 31766, 6, 'RED', 185, 'Day 1'),
(186, 31741, 1, 'GREEN', 186, 'Day 1'),
(187, 31676, 6, 'RED', 187, 'Day 1'),
(188, 31745, 5, 'GREEN & VIOLET', 188, 'Day 1'),
(189, 31838, 8, 'RED', 189, 'Day 1'),
(190, 31879, 9, 'GREEN', 190, 'Day 1'),
(191, 31935, 5, 'GREEN & VIOLET', 191, 'Day 1'),
(192, 31982, 2, 'RED', 192, 'Day 1'),
(193, 32034, 4, 'RED', 193, 'Day 1'),
(194, 31957, 7, 'GREEN', 194, 'Day 1'),
(195, 32053, 3, 'GREEN', 195, 'Day 1'),
(196, 32056, 6, 'RED', 196, 'Day 1'),
(197, 32087, 7, 'GREEN', 197, 'Day 1'),
(198, 31995, 5, 'GREEN & VIOLET', 198, 'Day 1'),
(199, 32008, 8, 'RED', 199, 'Day 1'),
(200, 31917, 7, 'GREEN', 200, 'Day 1'),
(201, 31835, 5, 'GREEN & VIOLET', 201, 'Day 1'),
(202, 31759, 9, 'GREEN', 202, 'Day 1'),
(203, 31817, 7, 'GREEN', 203, 'Day 1'),
(204, 31883, 3, 'GREEN', 204, 'Day 1'),
(205, 31972, 2, 'RED', 205, 'Day 1'),
(206, 31900, 0, 'RED & VIOLET', 206, 'Day 1'),
(207, 31891, 1, 'GREEN', 207, 'Day 1'),
(208, 31941, 1, 'GREEN', 208, 'Day 1'),
(209, 31927, 7, 'GREEN', 209, 'Day 1'),
(210, 31931, 1, 'GREEN', 210, 'Day 1'),
(211, 31969, 9, 'GREEN', 211, 'Day 1'),
(212, 31979, 9, 'GREEN', 212, 'Day 1'),
(213, 31919, 9, 'GREEN', 213, 'Day 1'),
(214, 31962, 2, 'RED', 214, 'Day 1'),
(215, 31897, 7, 'GREEN', 215, 'Day 1'),
(216, 31873, 3, 'GREEN', 216, 'Day 1'),
(217, 31863, 3, 'GREEN', 217, 'Day 1'),
(218, 31889, 9, 'GREEN', 218, 'Day 1'),
(219, 31800, 0, 'RED & VIOLET', 219, 'Day 1'),
(220, 31832, 2, 'RED', 220, 'Day 1'),
(221, 31793, 3, 'GREEN', 221, 'Day 1'),
(222, 31704, 4, 'RED', 222, 'Day 1'),
(223, 31623, 3, 'GREEN', 223, 'Day 1'),
(224, 31579, 9, 'GREEN', 224, 'Day 1'),
(225, 31546, 6, 'RED', 225, 'Day 1'),
(226, 31550, 0, 'RED & VIOLET', 226, 'Day 1'),
(227, 31586, 6, 'RED', 227, 'Day 1'),
(228, 31539, 9, 'GREEN', 228, 'Day 1'),
(229, 31550, 0, 'RED & VIOLET', 229, 'Day 1'),
(230, 31564, 4, 'RED', 230, 'Day 1'),
(231, 31476, 6, 'RED', 231, 'Day 1'),
(232, 31528, 8, 'RED', 232, 'Day 1'),
(233, 31556, 6, 'RED', 233, 'Day 1'),
(234, 31609, 9, 'GREEN', 234, 'Day 1'),
(235, 31644, 4, 'RED', 235, 'Day 1'),
(236, 31574, 4, 'RED', 236, 'Day 1'),
(237, 31566, 6, 'RED', 237, 'Day 1'),
(238, 31614, 4, 'RED', 238, 'Day 1'),
(239, 31578, 8, 'RED', 239, 'Day 1'),
(240, 31668, 8, 'RED', 240, 'Day 1'),
(241, 31736, 6, 'RED', 241, 'Day 1'),
(242, 31642, 2, 'RED', 242, 'Day 1'),
(243, 31634, 4, 'RED', 243, 'Day 1'),
(244, 31572, 2, 'RED', 244, 'Day 1'),
(245, 31586, 6, 'RED', 245, 'Day 1'),
(246, 31672, 2, 'RED', 246, 'Day 1'),
(247, 31676, 6, 'RED', 247, 'Day 1'),
(248, 31699, 9, 'GREEN', 248, 'Day 1'),
(249, 31604, 4, 'RED', 249, 'Day 1'),
(250, 31555, 5, 'GREEN & VIOLET', 250, 'Day 1'),
(251, 31487, 7, 'GREEN', 251, 'Day 1'),
(252, 31439, 9, 'GREEN', 252, 'Day 1'),
(253, 31423, 3, 'GREEN', 253, 'Day 1'),
(254, 31353, 3, 'GREEN', 254, 'Day 1'),
(255, 31261, 1, 'GREEN', 255, 'Day 1'),
(256, 31233, 3, 'GREEN', 256, 'Day 1'),
(257, 31225, 5, 'GREEN & VIOLET', 257, 'Day 1'),
(258, 31251, 1, 'GREEN', 258, 'Day 1'),
(259, 31204, 4, 'RED', 259, 'Day 1'),
(260, 31193, 3, 'GREEN', 260, 'Day 1'),
(261, 31216, 6, 'RED', 261, 'Day 1'),
(262, 31182, 2, 'RED', 262, 'Day 1'),
(263, 31237, 7, 'GREEN', 263, 'Day 1'),
(264, 31169, 9, 'GREEN', 264, 'Day 1'),
(265, 31188, 8, 'RED', 265, 'Day 1'),
(266, 31105, 5, 'GREEN & VIOLET', 266, 'Day 1'),
(267, 31091, 1, 'GREEN', 267, 'Day 1'),
(268, 31181, 1, 'GREEN', 268, 'Day 1'),
(269, 31090, 0, 'RED & VIOLET', 269, 'Day 1'),
(270, 31026, 6, 'RED', 270, 'Day 1'),
(271, 30940, 0, 'RED & VIOLET', 271, 'Day 1'),
(272, 31006, 6, 'RED', 272, 'Day 1'),
(273, 31026, 6, 'RED', 273, 'Day 1'),
(274, 31017, 7, 'GREEN', 274, 'Day 1'),
(275, 31004, 4, 'RED', 275, 'Day 1'),
(276, 30919, 9, 'GREEN', 276, 'Day 1'),
(277, 31013, 3, 'GREEN', 277, 'Day 1'),
(278, 30967, 7, 'GREEN', 278, 'Day 1'),
(279, 31067, 7, 'GREEN', 279, 'Day 1'),
(280, 31123, 3, 'GREEN', 280, 'Day 1'),
(281, 31145, 5, 'GREEN & VIOLET', 281, 'Day 1'),
(282, 31060, 0, 'RED & VIOLET', 282, 'Day 1'),
(283, 31113, 3, 'GREEN', 283, 'Day 1'),
(284, 31181, 1, 'GREEN', 284, 'Day 1'),
(285, 31217, 7, 'GREEN', 285, 'Day 1'),
(286, 31314, 4, 'RED', 286, 'Day 1'),
(287, 31350, 0, 'RED & VIOLET', 287, 'Day 1'),
(288, 31377, 7, 'GREEN', 288, 'Day 1'),
(289, 31409, 9, 'GREEN', 289, 'Day 1'),
(290, 31504, 4, 'RED', 290, 'Day 1'),
(291, 31467, 7, 'GREEN', 291, 'Day 1'),
(292, 31514, 4, 'RED', 292, 'Day 1'),
(293, 31445, 5, 'GREEN & VIOLET', 293, 'Day 1'),
(294, 31506, 6, 'RED', 294, 'Day 1'),
(295, 31415, 5, 'GREEN & VIOLET', 295, 'Day 1'),
(296, 31410, 0, 'RED & VIOLET', 296, 'Day 1'),
(297, 31445, 5, 'GREEN & VIOLET', 297, 'Day 1'),
(298, 31489, 9, 'GREEN', 298, 'Day 1'),
(299, 31575, 5, 'GREEN & VIOLET', 299, 'Day 1'),
(300, 31677, 7, 'GREEN', 300, 'Day 1'),
(301, 31724, 4, 'RED', 301, 'Day 1'),
(302, 31685, 5, 'GREEN & VIOLET', 302, 'Day 1'),
(303, 31610, 0, 'RED & VIOLET', 303, 'Day 1'),
(304, 31679, 9, 'GREEN', 304, 'Day 1'),
(305, 31609, 9, 'GREEN', 305, 'Day 1'),
(306, 31640, 0, 'RED & VIOLET', 306, 'Day 1'),
(307, 31611, 1, 'GREEN', 307, 'Day 1'),
(308, 31618, 8, 'RED', 308, 'Day 1'),
(309, 31684, 4, 'RED', 309, 'Day 1'),
(310, 31614, 4, 'RED', 310, 'Day 1'),
(311, 31587, 7, 'GREEN', 311, 'Day 1'),
(312, 31561, 1, 'GREEN', 312, 'Day 1'),
(313, 31574, 4, 'RED', 313, 'Day 1'),
(314, 31614, 4, 'RED', 314, 'Day 1'),
(315, 31637, 7, 'GREEN', 315, 'Day 1'),
(316, 31716, 6, 'RED', 316, 'Day 1'),
(317, 31662, 2, 'RED', 317, 'Day 1'),
(318, 31723, 3, 'GREEN', 318, 'Day 1'),
(319, 31754, 4, 'RED', 319, 'Day 1'),
(320, 31707, 7, 'GREEN', 320, 'Day 1'),
(321, 31615, 5, 'GREEN & VIOLET', 321, 'Day 1'),
(322, 31571, 1, 'GREEN', 322, 'Day 1'),
(323, 31638, 8, 'RED', 323, 'Day 1'),
(324, 31629, 9, 'GREEN', 324, 'Day 1'),
(325, 31608, 8, 'RED', 325, 'Day 1'),
(326, 31530, 0, 'RED & VIOLET', 326, 'Day 1'),
(327, 31481, 1, 'GREEN', 327, 'Day 1'),
(328, 31395, 5, 'GREEN & VIOLET', 328, 'Day 1'),
(329, 31477, 7, 'GREEN', 329, 'Day 1'),
(330, 31470, 0, 'RED & VIOLET', 330, 'Day 1'),
(331, 31427, 7, 'GREEN', 331, 'Day 1'),
(332, 31478, 8, 'RED', 332, 'Day 1'),
(333, 31440, 0, 'RED & VIOLET', 333, 'Day 1'),
(334, 31438, 8, 'RED', 334, 'Day 1'),
(335, 31400, 0, 'RED & VIOLET', 335, 'Day 1'),
(336, 31322, 2, 'RED', 336, 'Day 1'),
(337, 31386, 6, 'RED', 337, 'Day 1'),
(338, 31337, 7, 'GREEN', 338, 'Day 1'),
(339, 31284, 4, 'RED', 339, 'Day 1'),
(340, 31277, 7, 'GREEN', 340, 'Day 1'),
(341, 31206, 6, 'RED', 341, 'Day 1'),
(342, 31156, 6, 'RED', 342, 'Day 1'),
(343, 31204, 4, 'RED', 343, 'Day 1'),
(344, 31214, 4, 'RED', 344, 'Day 1'),
(345, 31283, 3, 'GREEN', 345, 'Day 1'),
(346, 31376, 6, 'RED', 346, 'Day 1'),
(347, 31473, 3, 'GREEN', 347, 'Day 1'),
(348, 31431, 1, 'GREEN', 348, 'Day 1'),
(349, 31398, 8, 'RED', 349, 'Day 1'),
(350, 31360, 0, 'RED & VIOLET', 350, 'Day 1'),
(351, 31312, 2, 'RED', 351, 'Day 1'),
(352, 31419, 9, 'GREEN', 352, 'Day 1'),
(353, 31467, 7, 'GREEN', 353, 'Day 1'),
(354, 31414, 4, 'RED', 354, 'Day 1'),
(355, 31350, 0, 'RED & VIOLET', 355, 'Day 1'),
(356, 31290, 0, 'RED & VIOLET', 356, 'Day 1'),
(357, 31362, 2, 'RED', 357, 'Day 1'),
(358, 31368, 8, 'RED', 358, 'Day 1'),
(359, 31398, 8, 'RED', 359, 'Day 1'),
(360, 31477, 7, 'GREEN', 360, 'Day 1'),
(361, 31429, 9, 'GREEN', 361, 'Day 1'),
(362, 31367, 7, 'GREEN', 362, 'Day 1'),
(363, 31379, 9, 'GREEN', 363, 'Day 1'),
(364, 31324, 4, 'RED', 364, 'Day 1'),
(365, 31346, 6, 'RED', 365, 'Day 1'),
(366, 31281, 1, 'GREEN', 366, 'Day 1'),
(367, 31344, 4, 'RED', 367, 'Day 1'),
(368, 31431, 1, 'GREEN', 368, 'Day 1'),
(369, 31467, 7, 'GREEN', 369, 'Day 1'),
(370, 31540, 0, 'RED & VIOLET', 370, 'Day 1'),
(371, 31567, 7, 'GREEN', 371, 'Day 1'),
(372, 31554, 4, 'RED', 372, 'Day 1'),
(373, 31600, 0, 'RED & VIOLET', 373, 'Day 1'),
(374, 31589, 9, 'GREEN', 374, 'Day 1'),
(375, 31644, 4, 'RED', 375, 'Day 1'),
(376, 31708, 8, 'RED', 376, 'Day 1'),
(377, 31682, 2, 'RED', 377, 'Day 1'),
(378, 31671, 1, 'GREEN', 378, 'Day 1'),
(379, 31575, 5, 'GREEN & VIOLET', 379, 'Day 1'),
(380, 31625, 5, 'GREEN & VIOLET', 380, 'Day 1'),
(381, 31536, 6, 'RED', 381, 'Day 1'),
(382, 31567, 7, 'GREEN', 382, 'Day 1'),
(383, 31541, 1, 'GREEN', 383, 'Day 1'),
(384, 31543, 3, 'GREEN', 384, 'Day 1'),
(385, 31498, 8, 'RED', 385, 'Day 1'),
(386, 31424, 4, 'RED', 386, 'Day 1'),
(387, 31331, 1, 'GREEN', 387, 'Day 1'),
(388, 31284, 4, 'RED', 388, 'Day 1'),
(389, 31183, 3, 'GREEN', 389, 'Day 1'),
(390, 31270, 0, 'RED & VIOLET', 390, 'Day 1'),
(391, 31185, 5, 'GREEN & VIOLET', 391, 'Day 1'),
(392, 31227, 7, 'GREEN', 392, 'Day 1'),
(393, 31171, 1, 'GREEN', 393, 'Day 1'),
(394, 31115, 5, 'GREEN & VIOLET', 394, 'Day 1'),
(395, 31177, 7, 'GREEN', 395, 'Day 1'),
(396, 31277, 7, 'GREEN', 396, 'Day 1'),
(397, 31185, 5, 'GREEN & VIOLET', 397, 'Day 1'),
(398, 31189, 9, 'GREEN', 398, 'Day 1'),
(399, 31137, 7, 'GREEN', 399, 'Day 1'),
(400, 31086, 6, 'RED', 400, 'Day 1'),
(401, 31176, 6, 'RED', 401, 'Day 1'),
(402, 31129, 9, 'GREEN', 402, 'Day 1'),
(403, 31136, 6, 'RED', 403, 'Day 1'),
(404, 31167, 7, 'GREEN', 404, 'Day 1'),
(405, 31156, 6, 'RED', 405, 'Day 1'),
(406, 31222, 2, 'RED', 406, 'Day 1'),
(407, 31262, 2, 'RED', 407, 'Day 1'),
(408, 31326, 6, 'RED', 408, 'Day 1'),
(409, 31388, 8, 'RED', 409, 'Day 1'),
(410, 31489, 9, 'GREEN', 410, 'Day 1'),
(411, 31576, 6, 'RED', 411, 'Day 1'),
(412, 31583, 3, 'GREEN', 412, 'Day 1'),
(413, 31633, 3, 'GREEN', 413, 'Day 1'),
(414, 31721, 1, 'GREEN', 414, 'Day 1'),
(415, 31757, 7, 'GREEN', 415, 'Day 1'),
(416, 31731, 1, 'GREEN', 416, 'Day 1'),
(417, 31721, 1, 'GREEN', 417, 'Day 1'),
(418, 31633, 3, 'GREEN', 418, 'Day 1'),
(419, 31640, 0, 'RED & VIOLET', 419, 'Day 1'),
(420, 31582, 2, 'RED', 420, 'Day 1'),
(421, 31508, 8, 'RED', 421, 'Day 1'),
(422, 31557, 7, 'GREEN', 422, 'Day 1'),
(423, 31514, 4, 'RED', 423, 'Day 1'),
(424, 31435, 5, 'GREEN & VIOLET', 424, 'Day 1'),
(425, 31345, 5, 'GREEN & VIOLET', 425, 'Day 1'),
(426, 31347, 7, 'GREEN', 426, 'Day 1'),
(427, 31316, 6, 'RED', 427, 'Day 1'),
(428, 31287, 7, 'GREEN', 428, 'Day 1'),
(429, 31194, 4, 'RED', 429, 'Day 1'),
(430, 31193, 3, 'GREEN', 430, 'Day 1'),
(431, 31178, 8, 'RED', 431, 'Day 1'),
(432, 31112, 2, 'RED', 432, 'Day 1'),
(433, 31129, 9, 'GREEN', 433, 'Day 1'),
(434, 31163, 3, 'GREEN', 434, 'Day 1'),
(435, 31220, 0, 'RED & VIOLET', 435, 'Day 1'),
(436, 31223, 3, 'GREEN', 436, 'Day 1'),
(437, 31208, 8, 'RED', 437, 'Day 1'),
(438, 31211, 1, 'GREEN', 438, 'Day 1'),
(439, 31160, 0, 'RED & VIOLET', 439, 'Day 1'),
(440, 31235, 5, 'GREEN & VIOLET', 440, 'Day 1'),
(441, 31173, 3, 'GREEN', 441, 'Day 1'),
(442, 31239, 9, 'GREEN', 442, 'Day 1'),
(443, 31146, 6, 'RED', 443, 'Day 1'),
(444, 31117, 7, 'GREEN', 444, 'Day 1'),
(445, 31116, 6, 'RED', 445, 'Day 1'),
(446, 31133, 3, 'GREEN', 446, 'Day 1'),
(447, 31131, 1, 'GREEN', 447, 'Day 1'),
(448, 31169, 9, 'GREEN', 448, 'Day 1'),
(449, 31129, 9, 'GREEN', 449, 'Day 1'),
(450, 31053, 3, 'GREEN', 450, 'Day 1'),
(451, 31122, 2, 'RED', 451, 'Day 1'),
(452, 31198, 8, 'RED', 452, 'Day 1'),
(453, 31175, 5, 'GREEN & VIOLET', 453, 'Day 1'),
(454, 31236, 6, 'RED', 454, 'Day 1'),
(455, 31301, 1, 'GREEN', 455, 'Day 1'),
(456, 31293, 3, 'GREEN', 456, 'Day 1'),
(457, 31269, 9, 'GREEN', 457, 'Day 1'),
(458, 31185, 5, 'GREEN & VIOLET', 458, 'Day 1'),
(459, 31121, 1, 'GREEN', 459, 'Day 1'),
(460, 31108, 8, 'RED', 460, 'Day 1'),
(461, 31127, 7, 'GREEN', 461, 'Day 1'),
(462, 31119, 9, 'GREEN', 462, 'Day 1'),
(463, 31071, 1, 'GREEN', 463, 'Day 1'),
(464, 31131, 1, 'GREEN', 464, 'Day 1'),
(465, 31223, 3, 'GREEN', 465, 'Day 1'),
(466, 31280, 0, 'RED & VIOLET', 466, 'Day 1'),
(467, 31229, 9, 'GREEN', 467, 'Day 1'),
(468, 31261, 1, 'GREEN', 468, 'Day 1'),
(469, 31203, 3, 'GREEN', 469, 'Day 1'),
(470, 31185, 5, 'GREEN & VIOLET', 470, 'Day 1'),
(471, 31164, 4, 'RED', 471, 'Day 1'),
(472, 31254, 4, 'RED', 472, 'Day 1'),
(473, 31274, 4, 'RED', 473, 'Day 1'),
(474, 31211, 1, 'GREEN', 474, 'Day 1'),
(475, 31144, 4, 'RED', 475, 'Day 1'),
(476, 31123, 3, 'GREEN', 476, 'Day 1'),
(477, 31079, 9, 'GREEN', 477, 'Day 1'),
(478, 31162, 2, 'RED', 478, 'Day 1'),
(479, 31219, 9, 'GREEN', 479, 'Day 1'),
(480, 29691, 1, 'GREEN', 480, 'Day 1');

-- --------------------------------------------------------

--
-- Table structure for table `tbl_result`
--

CREATE TABLE `tbl_result` (
  `id` int(11) NOT NULL,
  `periodid` varchar(300) NOT NULL,
  `price` float NOT NULL,
  `randomprice` float NOT NULL,
  `result` int(11) NOT NULL,
  `randomresult` int(11) NOT NULL,
  `color` varchar(100) NOT NULL,
  `randomcolor` varchar(100) NOT NULL,
  `resulttype` varchar(50) NOT NULL,
  `tabtype` varchar(50) NOT NULL,
  `createdate` timestamp NOT NULL DEFAULT current_timestamp()
) ENGINE=MyISAM DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

--
-- Dumping data for table `tbl_result`
--

INSERT INTO `tbl_result` (`id`, `periodid`, `price`, `randomprice`, `result`, `randomresult`, `color`, `randomcolor`, `resulttype`, `tabtype`, `createdate`) VALUES
(1, '20230330001', 0, 31371, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 00:02:02'),
(2, '20230330001', 0, 31439, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 00:02:02'),
(3, '20230330001', 0, 31131, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 00:02:02'),
(4, '20230330001', 0, 31261, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 00:02:02'),
(5, '20230330002', 0, 31723, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 00:04:02'),
(6, '20230330002', 0, 31699, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 00:04:02'),
(7, '20230330002', 0, 31041, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 00:04:02'),
(8, '20230330002', 0, 31211, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 00:04:02'),
(9, '20230330003', 0, 31821, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 00:06:02'),
(10, '20230330003', 0, 31429, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 00:06:02'),
(11, '20230330003', 0, 31551, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 00:06:02'),
(12, '20230330003', 0, 31564, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 00:06:02'),
(13, '20230330004', 0, 30919, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 00:08:02'),
(14, '20230330004', 0, 31350, 0, 0, '', 'red++violet', 'random', 'sapre', '2023-03-30 00:08:02'),
(15, '20230330004', 0, 31917, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 00:08:02'),
(16, '20230330004', 0, 31123, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 00:08:02'),
(17, '20230330005', 0, 31473, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 00:10:02'),
(18, '20230330005', 0, 31211, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 00:10:02'),
(19, '20230330005', 0, 31204, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 00:10:02'),
(20, '20230330005', 0, 31424, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 00:10:02'),
(21, '20230330006', 0, 30778, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 00:12:02'),
(22, '20230330006', 0, 31741, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 00:12:02'),
(23, '20230330006', 0, 31185, 0, 5, '', 'green++violet', 'random', 'bcone', '2023-03-30 00:12:02'),
(24, '20230330006', 0, 31157, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 00:12:02'),
(25, '20230330007', 0, 31173, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 00:14:02'),
(26, '20230330007', 0, 31486, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 00:14:02'),
(27, '20230330007', 0, 31889, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 00:14:02'),
(28, '20230330007', 0, 31970, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 00:14:02'),
(29, '20230330008', 0, 31353, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 00:16:01'),
(30, '20230330008', 0, 31270, 0, 0, '', 'red++violet', 'random', 'sapre', '2023-03-30 00:16:01'),
(31, '20230330008', 0, 31331, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 00:16:01'),
(32, '20230330008', 0, 31927, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 00:16:01'),
(33, '20230330009', 0, 31316, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 00:18:03'),
(34, '20230330009', 0, 31887, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 00:18:03'),
(35, '20230330009', 0, 31067, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 00:18:03'),
(36, '20230330009', 0, 31676, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 00:18:03'),
(37, '20230330010', 0, 31090, 0, 0, '', 'red++violet', 'random', 'parity', '2023-03-30 00:20:02'),
(38, '20230330010', 0, 30800, 0, 0, '', 'red++violet', 'random', 'sapre', '2023-03-30 00:20:02'),
(39, '20230330010', 0, 31376, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 00:20:02'),
(40, '20230330010', 0, 31466, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 00:20:02'),
(41, '20230330011', 0, 31347, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 00:22:01'),
(42, '20230330011', 0, 31415, 0, 5, '', 'green++violet', 'random', 'sapre', '2023-03-30 00:22:01'),
(43, '20230330011', 0, 31838, 0, 8, '', 'red', 'random', 'bcone', '2023-03-30 00:22:01'),
(44, '20230330011', 0, 31723, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 00:22:01'),
(45, '20230330012', 0, 30945, 0, 5, '', 'green++violet', 'random', 'parity', '2023-03-30 00:24:03'),
(46, '20230330012', 0, 31489, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 00:24:03'),
(47, '20230330012', 0, 31350, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 00:24:03'),
(48, '20230330012', 0, 30931, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 00:24:03'),
(49, '20230330013', 0, 31638, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 00:26:01'),
(50, '20230330013', 0, 31935, 0, 5, '', 'green++violet', 'random', 'sapre', '2023-03-30 00:26:01'),
(51, '20230330013', 0, 31489, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 00:26:01'),
(52, '20230330013', 0, 31171, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 00:26:01'),
(53, '20230330014', 0, 31274, 0, 4, '', 'red', 'random', 'parity', '2023-03-30 00:28:01'),
(54, '20230330014', 0, 31388, 0, 8, '', 'red', 'random', 'sapre', '2023-03-30 00:28:01'),
(55, '20230330014', 0, 31481, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 00:28:01'),
(56, '20230330014', 0, 31514, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 00:28:01'),
(57, '20230330015', 0, 31564, 0, 4, '', 'red', 'random', 'parity', '2023-03-30 00:30:02'),
(58, '20230330015', 0, 31467, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 00:30:02'),
(59, '20230330015', 0, 31157, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 00:30:02'),
(60, '20230330015', 0, 31414, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 00:30:02'),
(61, '20230330016', 0, 31287, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 00:32:02'),
(62, '20230330016', 0, 30748, 0, 8, '', 'red', 'random', 'sapre', '2023-03-30 00:32:02'),
(63, '20230330016', 0, 31487, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 00:32:02'),
(64, '20230330016', 0, 30799, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 00:32:02'),
(65, '20230330017', 0, 31269, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 00:34:01'),
(66, '20230330017', 0, 31431, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 00:34:01'),
(67, '20230330017', 0, 31482, 0, 2, '', 'red', 'random', 'bcone', '2023-03-30 00:34:01'),
(68, '20230330017', 0, 31431, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 00:34:01'),
(69, '20230330018', 0, 31105, 0, 5, '', 'green++violet', 'random', 'parity', '2023-03-30 00:36:02'),
(70, '20230330018', 0, 31657, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 00:36:02'),
(71, '20230330018', 0, 31156, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 00:36:02'),
(72, '20230330018', 0, 31657, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 00:36:02'),
(73, '20230330019', 0, 31447, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 00:38:01'),
(74, '20230330019', 0, 31734, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 00:38:01'),
(75, '20230330019', 0, 31438, 0, 8, '', 'red', 'random', 'bcone', '2023-03-30 00:38:01'),
(76, '20230330019', 0, 30905, 0, 5, '', 'green++violet', 'random', 'emerd', '2023-03-30 00:38:01'),
(77, '20230330020', 0, 31006, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 00:40:02'),
(78, '20230330020', 0, 31439, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 00:40:02'),
(79, '20230330020', 0, 31556, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 00:40:02'),
(80, '20230330020', 0, 31935, 0, 5, '', 'green++violet', 'random', 'emerd', '2023-03-30 00:40:02'),
(81, '20230330021', 0, 30873, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 00:42:02'),
(82, '20230330021', 0, 31173, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 00:42:02'),
(83, '20230330021', 0, 30859, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 00:42:02'),
(84, '20230330021', 0, 31707, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 00:42:02'),
(85, '20230330022', 0, 31745, 0, 5, '', 'green++violet', 'random', 'parity', '2023-03-30 00:44:02'),
(86, '20230330022', 0, 30792, 0, 2, '', 'red', 'random', 'sapre', '2023-03-30 00:44:02'),
(87, '20230330022', 0, 31499, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 00:44:02'),
(88, '20230330022', 0, 31185, 0, 5, '', 'green++violet', 'random', 'emerd', '2023-03-30 00:44:02'),
(89, '20230330023', 0, 31206, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 00:46:01'),
(90, '20230330023', 0, 31489, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 00:46:01'),
(91, '20230330023', 0, 30844, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 00:46:01'),
(92, '20230330023', 0, 31540, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 00:46:01'),
(93, '20230330024', 0, 31353, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 00:48:02'),
(94, '20230330024', 0, 31528, 0, 8, '', 'red', 'random', 'sapre', '2023-03-30 00:48:02'),
(95, '20230330024', 0, 31477, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 00:48:02'),
(96, '20230330024', 0, 31802, 0, 2, '', 'red', 'random', 'emerd', '2023-03-30 00:48:02'),
(97, '20230330025', 0, 31208, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 00:50:02'),
(98, '20230330025', 0, 31577, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 00:50:02'),
(99, '20230330025', 0, 31589, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 00:50:02'),
(100, '20230330025', 0, 31610, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 00:50:02'),
(101, '20230330026', 0, 30761, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 00:52:01'),
(102, '20230330026', 0, 31766, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 00:52:01'),
(103, '20230330026', 0, 31982, 0, 2, '', 'red', 'random', 'bcone', '2023-03-30 00:52:01'),
(104, '20230330026', 0, 31398, 0, 8, '', 'red', 'random', 'emerd', '2023-03-30 00:52:01'),
(105, '20230330027', 0, 31216, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 00:54:01'),
(106, '20230330027', 0, 31982, 0, 2, '', 'red', 'random', 'sapre', '2023-03-30 00:54:01'),
(107, '20230330027', 0, 31979, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 00:54:01'),
(108, '20230330027', 0, 31113, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 00:54:01'),
(109, '20230330028', 0, 31216, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 00:56:02'),
(110, '20230330028', 0, 31347, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 00:56:02'),
(111, '20230330028', 0, 30937, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 00:56:02'),
(112, '20230330028', 0, 30891, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 00:56:02'),
(113, '20230330029', 0, 31367, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 00:58:02'),
(114, '20230330029', 0, 31682, 0, 2, '', 'red', 'random', 'sapre', '2023-03-30 00:58:02'),
(115, '20230330029', 0, 31793, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 00:58:02'),
(116, '20230330029', 0, 31219, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 00:58:02'),
(117, '20230330030', 0, 31347, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 01:00:02'),
(118, '20230330030', 0, 31514, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 01:00:02'),
(119, '20230330030', 0, 31144, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 01:00:02'),
(120, '20230330030', 0, 31541, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 01:00:02'),
(121, '20230330031', 0, 30922, 0, 2, '', 'red', 'random', 'parity', '2023-03-30 01:02:02'),
(122, '20230330031', 0, 30830, 0, 0, '', 'red++violet', 'random', 'sapre', '2023-03-30 01:02:02'),
(123, '20230330031', 0, 31873, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 01:02:02'),
(124, '20230330031', 0, 30799, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 01:02:02'),
(125, '20230330032', 0, 31067, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 01:04:02'),
(126, '20230330032', 0, 31604, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 01:04:02'),
(127, '20230330032', 0, 31219, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 01:04:02'),
(128, '20230330032', 0, 31117, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 01:04:02'),
(129, '20230330033', 0, 31716, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 01:06:02'),
(130, '20230330033', 0, 31254, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 01:06:02'),
(131, '20230330033', 0, 31679, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 01:06:02'),
(132, '20230330033', 0, 30881, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 01:06:02'),
(133, '20230330034', 0, 31181, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 01:08:01'),
(134, '20230330034', 0, 31229, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 01:08:01'),
(135, '20230330034', 0, 31394, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 01:08:01'),
(136, '20230330034', 0, 31424, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 01:08:01'),
(137, '20230330035', 0, 31239, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 01:10:01'),
(138, '20230330035', 0, 31109, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 01:10:01'),
(139, '20230330035', 0, 31067, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 01:10:01'),
(140, '20230330035', 0, 30945, 0, 5, '', 'green++violet', 'random', 'emerd', '2023-03-30 01:10:01'),
(141, '20230330036', 0, 32008, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 01:12:01'),
(142, '20230330036', 0, 31458, 0, 8, '', 'red', 'random', 'sapre', '2023-03-30 01:12:01'),
(143, '20230330036', 0, 31577, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 01:12:01'),
(144, '20230330036', 0, 31671, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 01:12:01'),
(145, '20230330037', 0, 31223, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 01:14:01'),
(146, '20230330037', 0, 31724, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 01:14:01'),
(147, '20230330037', 0, 31123, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 01:14:01'),
(148, '20230330037', 0, 31157, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 01:14:01'),
(149, '20230330038', 0, 30810, 0, 0, '', 'red++violet', 'random', 'parity', '2023-03-30 01:16:02'),
(150, '20230330038', 0, 31223, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 01:16:02'),
(151, '20230330038', 0, 31204, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 01:16:02'),
(152, '20230330038', 0, 31557, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 01:16:02'),
(153, '20230330039', 0, 30769, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 01:18:02'),
(154, '20230330039', 0, 31644, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 01:18:02'),
(155, '20230330039', 0, 31146, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 01:18:02'),
(156, '20230330039', 0, 31071, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 01:18:02'),
(157, '20230330040', 0, 31117, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 01:20:02'),
(158, '20230330040', 0, 31931, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 01:20:02'),
(159, '20230330040', 0, 31350, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 01:20:02'),
(160, '20230330040', 0, 31026, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 01:20:02'),
(161, '20230330041', 0, 31644, 0, 4, '', 'red', 'random', 'parity', '2023-03-30 01:22:02'),
(162, '20230330041', 0, 31970, 0, 0, '', 'red++violet', 'random', 'sapre', '2023-03-30 01:22:02'),
(163, '20230330041', 0, 31644, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 01:22:02'),
(164, '20230330041', 0, 31217, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 01:22:02'),
(165, '20230330042', 0, 31481, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 01:24:01'),
(166, '20230330042', 0, 30844, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 01:24:01'),
(167, '20230330042', 0, 31001, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 01:24:01'),
(168, '20230330042', 0, 31152, 0, 2, '', 'red', 'random', 'emerd', '2023-03-30 01:24:01'),
(169, '20230330043', 0, 30769, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 01:26:02'),
(170, '20230330043', 0, 31290, 0, 0, '', 'red++violet', 'random', 'sapre', '2023-03-30 01:26:02'),
(171, '20230330043', 0, 31026, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 01:26:02'),
(172, '20230330043', 0, 31169, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 01:26:02'),
(173, '20230330044', 0, 30826, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 01:28:01'),
(174, '20230330044', 0, 31812, 0, 2, '', 'red', 'random', 'sapre', '2023-03-30 01:28:01'),
(175, '20230330044', 0, 31193, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 01:28:01'),
(176, '20230330044', 0, 31662, 0, 2, '', 'red', 'random', 'emerd', '2023-03-30 01:28:01'),
(177, '20230330045', 0, 31324, 0, 4, '', 'red', 'random', 'parity', '2023-03-30 01:30:02'),
(178, '20230330045', 0, 31812, 0, 2, '', 'red', 'random', 'sapre', '2023-03-30 01:30:02'),
(179, '20230330045', 0, 31863, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 01:30:02'),
(180, '20230330045', 0, 31623, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 01:30:02'),
(181, '20230330046', 0, 31217, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 01:32:02'),
(182, '20230330046', 0, 31832, 0, 2, '', 'red', 'random', 'sapre', '2023-03-30 01:32:02'),
(183, '20230330046', 0, 31638, 0, 8, '', 'red', 'random', 'bcone', '2023-03-30 01:32:02'),
(184, '20230330046', 0, 31185, 0, 5, '', 'green++violet', 'random', 'emerd', '2023-03-30 01:32:02'),
(185, '20230330047', 0, 31910, 0, 0, '', 'red++violet', 'random', 'parity', '2023-03-30 01:34:02'),
(186, '20230330047', 0, 31281, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 01:34:02'),
(187, '20230330047', 0, 31261, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 01:34:02'),
(188, '20230330047', 0, 31498, 0, 8, '', 'red', 'random', 'emerd', '2023-03-30 01:34:02'),
(189, '20230330048', 0, 31004, 0, 4, '', 'red', 'random', 'parity', '2023-03-30 01:36:01'),
(190, '20230330048', 0, 30857, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 01:36:01'),
(191, '20230330048', 0, 31299, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 01:36:01'),
(192, '20230330048', 0, 31214, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 01:36:01'),
(193, '20230330049', 0, 31682, 0, 2, '', 'red', 'random', 'parity', '2023-03-30 01:38:01'),
(194, '20230330049', 0, 30863, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 01:38:01'),
(195, '20230330049', 0, 31362, 0, 2, '', 'red', 'random', 'bcone', '2023-03-30 01:38:01'),
(196, '20230330049', 0, 31827, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 01:38:01'),
(197, '20230330050', 0, 31745, 0, 5, '', 'green++violet', 'random', 'parity', '2023-03-30 01:40:02'),
(198, '20230330050', 0, 31261, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 01:40:02'),
(199, '20230330050', 0, 31280, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 01:40:02'),
(200, '20230330050', 0, 31917, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 01:40:02'),
(201, '20230330051', 0, 31227, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 01:42:02'),
(202, '20230330051', 0, 30799, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 01:42:02'),
(203, '20230330051', 0, 30863, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 01:42:02'),
(204, '20230330051', 0, 30853, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 01:42:02'),
(205, '20230330052', 0, 31508, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 01:44:02'),
(206, '20230330052', 0, 30812, 0, 2, '', 'red', 'random', 'sapre', '2023-03-30 01:44:02'),
(207, '20230330052', 0, 31222, 0, 2, '', 'red', 'random', 'bcone', '2023-03-30 01:44:02'),
(208, '20230330052', 0, 31121, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 01:44:02'),
(209, '20230330053', 0, 31116, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 01:46:02'),
(210, '20230330053', 0, 31969, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 01:46:02'),
(211, '20230330053', 0, 31136, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 01:46:02'),
(212, '20230330053', 0, 31586, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 01:46:02'),
(213, '20230330054', 0, 31026, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 01:48:01'),
(214, '20230330054', 0, 31284, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 01:48:01'),
(215, '20230330054', 0, 31400, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 01:48:01'),
(216, '20230330054', 0, 31817, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 01:48:01'),
(217, '20230330055', 0, 31763, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 01:50:02'),
(218, '20230330055', 0, 31067, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 01:50:02'),
(219, '20230330055', 0, 31171, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 01:50:02'),
(220, '20230330055', 0, 31388, 0, 8, '', 'red', 'random', 'emerd', '2023-03-30 01:50:02'),
(221, '20230330056', 0, 31417, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 01:52:02'),
(222, '20230330056', 0, 30919, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 01:52:02'),
(223, '20230330056', 0, 31183, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 01:52:02'),
(224, '20230330056', 0, 31969, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 01:52:02'),
(225, '20230330057', 0, 31794, 0, 4, '', 'red', 'random', 'parity', '2023-03-30 01:54:02'),
(226, '20230330057', 0, 31623, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 01:54:02'),
(227, '20230330057', 0, 31123, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 01:54:02'),
(228, '20230330057', 0, 31208, 0, 8, '', 'red', 'random', 'emerd', '2023-03-30 01:54:02'),
(229, '20230330058', 0, 31838, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 01:56:02'),
(230, '20230330058', 0, 31575, 0, 5, '', 'green++violet', 'random', 'sapre', '2023-03-30 01:56:02'),
(231, '20230330058', 0, 32056, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 01:56:02'),
(232, '20230330058', 0, 31414, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 01:56:02'),
(233, '20230330059', 0, 31554, 0, 4, '', 'red', 'random', 'parity', '2023-03-30 01:58:01'),
(234, '20230330059', 0, 31178, 0, 8, '', 'red', 'random', 'sapre', '2023-03-30 01:58:01'),
(235, '20230330059', 0, 31424, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 01:58:01'),
(236, '20230330059', 0, 31574, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 01:58:01'),
(237, '20230330060', 0, 30973, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 02:00:02'),
(238, '20230330060', 0, 31883, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 02:00:02'),
(239, '20230330060', 0, 31482, 0, 2, '', 'red', 'random', 'bcone', '2023-03-30 02:00:02'),
(240, '20230330060', 0, 31447, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 02:00:02'),
(241, '20230330061', 0, 31144, 0, 4, '', 'red', 'random', 'parity', '2023-03-30 02:02:01'),
(242, '20230330061', 0, 31504, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 02:02:01'),
(243, '20230330061', 0, 31032, 0, 2, '', 'red', 'random', 'bcone', '2023-03-30 02:02:01'),
(244, '20230330061', 0, 31337, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 02:02:01'),
(245, '20230330062', 0, 31614, 0, 4, '', 'red', 'random', 'parity', '2023-03-30 02:04:02'),
(246, '20230330062', 0, 31222, 0, 2, '', 'red', 'random', 'sapre', '2023-03-30 02:04:02'),
(247, '20230330062', 0, 31583, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 02:04:02'),
(248, '20230330062', 0, 30940, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 02:04:02'),
(249, '20230330063', 0, 31574, 0, 4, '', 'red', 'random', 'parity', '2023-03-30 02:06:02'),
(250, '20230330063', 0, 30874, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 02:06:02'),
(251, '20230330063', 0, 31571, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 02:06:02'),
(252, '20230330063', 0, 31006, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 02:06:02'),
(253, '20230330064', 0, 30881, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 02:08:02'),
(254, '20230330064', 0, 31754, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 02:08:02'),
(255, '20230330064', 0, 31731, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 02:08:02'),
(256, '20230330064', 0, 31604, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 02:08:02'),
(257, '20230330065', 0, 31553, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 02:10:02'),
(258, '20230330065', 0, 31185, 0, 5, '', 'green++violet', 'random', 'sapre', '2023-03-30 02:10:02'),
(259, '20230330065', 0, 30774, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 02:10:02'),
(260, '20230330065', 0, 31112, 0, 2, '', 'red', 'random', 'emerd', '2023-03-30 02:10:02'),
(261, '20230330066', 0, 31564, 0, 4, '', 'red', 'random', 'parity', '2023-03-30 02:12:01'),
(262, '20230330066', 0, 30901, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 02:12:01'),
(263, '20230330066', 0, 31935, 0, 5, '', 'green++violet', 'random', 'bcone', '2023-03-30 02:12:01'),
(264, '20230330066', 0, 32053, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 02:12:01'),
(265, '20230330067', 0, 31499, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 02:14:02'),
(266, '20230330067', 0, 31644, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 02:14:02'),
(267, '20230330067', 0, 31721, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 02:14:02'),
(268, '20230330067', 0, 31553, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 02:14:02'),
(269, '20230330068', 0, 31745, 0, 5, '', 'green++violet', 'random', 'parity', '2023-03-30 02:16:02'),
(270, '20230330068', 0, 31614, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 02:16:02'),
(271, '20230330068', 0, 31090, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 02:16:02'),
(272, '20230330068', 0, 31731, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 02:16:02'),
(273, '20230330069', 0, 31634, 0, 4, '', 'red', 'random', 'parity', '2023-03-30 02:18:02'),
(274, '20230330069', 0, 31360, 0, 0, '', 'red++violet', 'random', 'sapre', '2023-03-30 02:18:02'),
(275, '20230330069', 0, 31466, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 02:18:02'),
(276, '20230330069', 0, 31637, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 02:18:02'),
(277, '20230330070', 0, 30967, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 02:20:02'),
(278, '20230330070', 0, 31677, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 02:20:02'),
(279, '20230330070', 0, 31486, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 02:20:02'),
(280, '20230330070', 0, 31445, 0, 5, '', 'green++violet', 'random', 'emerd', '2023-03-30 02:20:02'),
(281, '20230330071', 0, 31541, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 02:22:01'),
(282, '20230330071', 0, 31229, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 02:22:01'),
(283, '20230330071', 0, 31145, 0, 5, '', 'green++violet', 'random', 'bcone', '2023-03-30 02:22:01'),
(284, '20230330071', 0, 30803, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 02:22:01'),
(285, '20230330072', 0, 31866, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 02:24:02'),
(286, '20230330072', 0, 31112, 0, 2, '', 'red', 'random', 'sapre', '2023-03-30 02:24:02'),
(287, '20230330072', 0, 31129, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 02:24:02'),
(288, '20230330072', 0, 31676, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 02:24:02'),
(289, '20230330073', 0, 30761, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 02:26:01'),
(290, '20230330073', 0, 31512, 0, 2, '', 'red', 'random', 'sapre', '2023-03-30 02:26:01'),
(291, '20230330073', 0, 31467, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 02:26:01'),
(292, '20230330073', 0, 31757, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 02:26:01'),
(293, '20230330074', 0, 31344, 0, 4, '', 'red', 'random', 'parity', '2023-03-30 02:28:02'),
(294, '20230330074', 0, 31156, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 02:28:02'),
(295, '20230330074', 0, 31684, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 02:28:02'),
(296, '20230330074', 0, 31000, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 02:28:02'),
(297, '20230330075', 0, 31232, 0, 2, '', 'red', 'random', 'parity', '2023-03-30 02:30:02'),
(298, '20230330075', 0, 31962, 0, 2, '', 'red', 'random', 'sapre', '2023-03-30 02:30:02'),
(299, '20230330075', 0, 31677, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 02:30:02'),
(300, '20230330075', 0, 31167, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 02:30:02'),
(301, '20230330076', 0, 31360, 0, 0, '', 'red++violet', 'random', 'parity', '2023-03-30 02:32:01'),
(302, '20230330076', 0, 31347, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 02:32:01'),
(303, '20230330076', 0, 31695, 0, 5, '', 'green++violet', 'random', 'bcone', '2023-03-30 02:32:01'),
(304, '20230330076', 0, 32056, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 02:32:01'),
(305, '20230330077', 0, 31770, 0, 0, '', 'red++violet', 'random', 'parity', '2023-03-30 02:34:02'),
(306, '20230330077', 0, 30823, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 02:34:02'),
(307, '20230330077', 0, 31416, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 02:34:02'),
(308, '20230330077', 0, 31642, 0, 2, '', 'red', 'random', 'emerd', '2023-03-30 02:34:02'),
(309, '20230330078', 0, 30885, 0, 5, '', 'green++violet', 'random', 'parity', '2023-03-30 02:36:02'),
(310, '20230330078', 0, 31657, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 02:36:02'),
(311, '20230330078', 0, 31640, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 02:36:02'),
(312, '20230330078', 0, 32087, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 02:36:02'),
(313, '20230330079', 0, 31198, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 02:38:02'),
(314, '20230330079', 0, 31182, 0, 2, '', 'red', 'random', 'sapre', '2023-03-30 02:38:02'),
(315, '20230330079', 0, 31863, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 02:38:02'),
(316, '20230330079', 0, 31041, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 02:38:02'),
(317, '20230330080', 0, 32087, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 02:40:02'),
(318, '20230330080', 0, 31173, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 02:40:02'),
(319, '20230330080', 0, 31467, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 02:40:02'),
(320, '20230330080', 0, 30934, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 02:40:02'),
(321, '20230330081', 0, 31188, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 02:42:02'),
(322, '20230330081', 0, 31486, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 02:42:02'),
(323, '20230330081', 0, 30934, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 02:42:02'),
(324, '20230330081', 0, 30789, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 02:42:02'),
(325, '20230330082', 0, 31438, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 02:44:02'),
(326, '20230330082', 0, 32008, 0, 8, '', 'red', 'random', 'sapre', '2023-03-30 02:44:02'),
(327, '20230330082', 0, 31314, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 02:44:02'),
(328, '20230330082', 0, 30706, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 02:44:02'),
(329, '20230330083', 0, 31131, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 02:46:02'),
(330, '20230330083', 0, 30873, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 02:46:02'),
(331, '20230330083', 0, 31142, 0, 2, '', 'red', 'random', 'bcone', '2023-03-30 02:46:02'),
(332, '20230330083', 0, 31337, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 02:46:02'),
(333, '20230330084', 0, 31609, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 02:48:01'),
(334, '20230330084', 0, 30799, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 02:48:01'),
(335, '20230330084', 0, 31427, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 02:48:01'),
(336, '20230330084', 0, 31749, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 02:48:01'),
(337, '20230330085', 0, 31540, 0, 0, '', 'red++violet', 'random', 'parity', '2023-03-30 02:50:02'),
(338, '20230330085', 0, 31662, 0, 2, '', 'red', 'random', 'sapre', '2023-03-30 02:50:02'),
(339, '20230330085', 0, 31561, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 02:50:02'),
(340, '20230330085', 0, 31067, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 02:50:02'),
(341, '20230330086', 0, 31173, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 02:52:02'),
(342, '20230330086', 0, 31129, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 02:52:02'),
(343, '20230330086', 0, 31466, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 02:52:02'),
(344, '20230330086', 0, 31108, 0, 8, '', 'red', 'random', 'emerd', '2023-03-30 02:52:02'),
(345, '20230330087', 0, 31668, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 02:54:02'),
(346, '20230330087', 0, 31171, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 02:54:02'),
(347, '20230330087', 0, 31671, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 02:54:02'),
(348, '20230330087', 0, 31067, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 02:54:02'),
(349, '20230330088', 0, 31917, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 02:56:01'),
(350, '20230330088', 0, 31557, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 02:56:01'),
(351, '20230330088', 0, 31721, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 02:56:01'),
(352, '20230330088', 0, 31079, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 02:56:01'),
(353, '20230330089', 0, 31032, 0, 2, '', 'red', 'random', 'parity', '2023-03-30 02:58:01'),
(354, '20230330089', 0, 31024, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 02:58:01'),
(355, '20230330089', 0, 31467, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 02:58:01'),
(356, '20230330089', 0, 31609, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 02:58:01'),
(357, '20230330090', 0, 31169, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 03:00:02'),
(358, '20230330090', 0, 31173, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 03:00:02'),
(359, '20230330090', 0, 31129, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 03:00:02'),
(360, '20230330090', 0, 30967, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 03:00:02'),
(361, '20230330091', 0, 31701, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 03:02:02'),
(362, '20230330091', 0, 31386, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 03:02:02'),
(363, '20230330091', 0, 31668, 0, 8, '', 'red', 'random', 'bcone', '2023-03-30 03:02:02'),
(364, '20230330091', 0, 31979, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 03:02:02'),
(365, '20230330092', 0, 31677, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 03:04:02'),
(366, '20230330092', 0, 31204, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 03:04:02'),
(367, '20230330092', 0, 31032, 0, 2, '', 'red', 'random', 'bcone', '2023-03-30 03:04:02'),
(368, '20230330092', 0, 31766, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 03:04:02'),
(369, '20230330093', 0, 31610, 0, 0, '', 'red++violet', 'random', 'parity', '2023-03-30 03:06:01'),
(370, '20230330093', 0, 31724, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 03:06:01'),
(371, '20230330093', 0, 31236, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 03:06:01'),
(372, '20230330093', 0, 31684, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 03:06:01'),
(373, '20230330094', 0, 31470, 0, 0, '', 'red++violet', 'random', 'parity', '2023-03-30 03:08:02'),
(374, '20230330094', 0, 30853, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 03:08:02'),
(375, '20230330094', 0, 31817, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 03:08:02'),
(376, '20230330094', 0, 31299, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 03:08:02'),
(377, '20230330095', 0, 31119, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 03:10:02'),
(378, '20230330095', 0, 31554, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 03:10:02'),
(379, '20230330095', 0, 31032, 0, 2, '', 'red', 'random', 'bcone', '2023-03-30 03:10:02'),
(380, '20230330095', 0, 31482, 0, 2, '', 'red', 'random', 'emerd', '2023-03-30 03:10:02'),
(381, '20230330096', 0, 32053, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 03:12:02'),
(382, '20230330096', 0, 31129, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 03:12:02'),
(383, '20230330096', 0, 31026, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 03:12:02'),
(384, '20230330096', 0, 31440, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 03:12:02'),
(385, '20230330097', 0, 31069, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 03:14:01'),
(386, '20230330097', 0, 31555, 0, 5, '', 'green++violet', 'random', 'sapre', '2023-03-30 03:14:01'),
(387, '20230330097', 0, 31634, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 03:14:01'),
(388, '20230330097', 0, 31812, 0, 2, '', 'red', 'random', 'emerd', '2023-03-30 03:14:01'),
(389, '20230330098', 0, 31630, 0, 0, '', 'red++violet', 'random', 'parity', '2023-03-30 03:16:01'),
(390, '20230330098', 0, 31424, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 03:16:01'),
(391, '20230330098', 0, 31672, 0, 2, '', 'red', 'random', 'bcone', '2023-03-30 03:16:01'),
(392, '20230330098', 0, 31316, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 03:16:01'),
(393, '20230330099', 0, 31579, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 03:18:01'),
(394, '20230330099', 0, 31741, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 03:18:01'),
(395, '20230330099', 0, 31604, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 03:18:01'),
(396, '20230330099', 0, 31117, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 03:18:01'),
(397, '20230330100', 0, 31450, 0, 0, '', 'red++violet', 'random', 'parity', '2023-03-30 03:20:02'),
(398, '20230330100', 0, 31414, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 03:20:02'),
(399, '20230330100', 0, 30940, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 03:20:02'),
(400, '20230330100', 0, 30761, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 03:20:02'),
(401, '20230330101', 0, 30863, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 03:22:02'),
(402, '20230330101', 0, 31146, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 03:22:02'),
(403, '20230330101', 0, 30836, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 03:22:02'),
(404, '20230330101', 0, 30882, 0, 2, '', 'red', 'random', 'emerd', '2023-03-30 03:22:02'),
(405, '20230330102', 0, 31142, 0, 2, '', 'red', 'random', 'parity', '2023-03-30 03:24:02'),
(406, '20230330102', 0, 30931, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 03:24:02'),
(407, '20230330102', 0, 31713, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 03:24:02'),
(408, '20230330102', 0, 31145, 0, 5, '', 'green++violet', 'random', 'emerd', '2023-03-30 03:24:02'),
(409, '20230330103', 0, 31704, 0, 4, '', 'red', 'random', 'parity', '2023-03-30 03:26:02'),
(410, '20230330103', 0, 30821, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 03:26:02'),
(411, '20230330103', 0, 31182, 0, 2, '', 'red', 'random', 'bcone', '2023-03-30 03:26:02'),
(412, '20230330103', 0, 31482, 0, 2, '', 'red', 'random', 'emerd', '2023-03-30 03:26:02'),
(413, '20230330104', 0, 31793, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 03:28:02'),
(414, '20230330104', 0, 31137, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 03:28:02'),
(415, '20230330104', 0, 31736, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 03:28:02'),
(416, '20230330104', 0, 31131, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 03:28:02'),
(417, '20230330105', 0, 31821, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 03:30:02'),
(418, '20230330105', 0, 31410, 0, 0, '', 'red++violet', 'random', 'sapre', '2023-03-30 03:30:02'),
(419, '20230330105', 0, 31498, 0, 8, '', 'red', 'random', 'bcone', '2023-03-30 03:30:02'),
(420, '20230330105', 0, 31800, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 03:30:02'),
(421, '20230330106', 0, 31208, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 03:32:01'),
(422, '20230330106', 0, 31641, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 03:32:01'),
(423, '20230330106', 0, 31371, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 03:32:01'),
(424, '20230330106', 0, 31550, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 03:32:01'),
(425, '20230330107', 0, 31350, 0, 0, '', 'red++violet', 'random', 'parity', '2023-03-30 03:34:02'),
(426, '20230330107', 0, 31483, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 03:34:02'),
(427, '20230330107', 0, 31704, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 03:34:02'),
(428, '20230330107', 0, 31198, 0, 8, '', 'red', 'random', 'emerd', '2023-03-30 03:34:02'),
(429, '20230330108', 0, 31142, 0, 2, '', 'red', 'random', 'parity', '2023-03-30 03:36:02'),
(430, '20230330108', 0, 31270, 0, 0, '', 'red++violet', 'random', 'sapre', '2023-03-30 03:36:02'),
(431, '20230330108', 0, 31553, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 03:36:02'),
(432, '20230330108', 0, 31183, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 03:36:02'),
(433, '20230330109', 0, 31130, 0, 0, '', 'red++violet', 'random', 'parity', '2023-03-30 03:38:01'),
(434, '20230330109', 0, 31499, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 03:38:01'),
(435, '20230330109', 0, 30812, 0, 2, '', 'red', 'random', 'bcone', '2023-03-30 03:38:01'),
(436, '20230330109', 0, 31610, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 03:38:01'),
(437, '20230330110', 0, 31841, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 03:40:02'),
(438, '20230330110', 0, 31536, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 03:40:02'),
(439, '20230330110', 0, 31647, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 03:40:02'),
(440, '20230330110', 0, 31770, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 03:40:02'),
(441, '20230330111', 0, 31499, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 03:42:02'),
(442, '20230330111', 0, 31684, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 03:42:02'),
(443, '20230330111', 0, 30782, 0, 2, '', 'red', 'random', 'bcone', '2023-03-30 03:42:02'),
(444, '20230330111', 0, 31280, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 03:42:02'),
(445, '20230330112', 0, 31424, 0, 4, '', 'red', 'random', 'parity', '2023-03-30 03:44:01'),
(446, '20230330112', 0, 31115, 0, 5, '', 'green++violet', 'random', 'sapre', '2023-03-30 03:44:01'),
(447, '20230330112', 0, 31556, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 03:44:01'),
(448, '20230330112', 0, 31957, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 03:44:01'),
(449, '20230330113', 0, 31445, 0, 5, '', 'green++violet', 'random', 'parity', '2023-03-30 03:46:02'),
(450, '20230330113', 0, 30830, 0, 0, '', 'red++violet', 'random', 'sapre', '2023-03-30 03:46:02'),
(451, '20230330113', 0, 31540, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 03:46:02'),
(452, '20230330113', 0, 31571, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 03:46:02'),
(453, '20230330114', 0, 30811, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 03:48:01'),
(454, '20230330114', 0, 31113, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 03:48:01'),
(455, '20230330114', 0, 31684, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 03:48:01'),
(456, '20230330114', 0, 31129, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 03:48:01'),
(457, '20230330115', 0, 31857, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 03:50:01'),
(458, '20230330115', 0, 30903, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 03:50:01'),
(459, '20230330115', 0, 31587, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 03:50:01'),
(460, '20230330115', 0, 31921, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 03:50:01'),
(461, '20230330116', 0, 31398, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 03:52:02'),
(462, '20230330116', 0, 31386, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 03:52:02'),
(463, '20230330116', 0, 31640, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 03:52:02'),
(464, '20230330116', 0, 31431, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 03:52:02'),
(465, '20230330117', 0, 31477, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 03:54:02'),
(466, '20230330117', 0, 31575, 0, 5, '', 'green++violet', 'random', 'sapre', '2023-03-30 03:54:02'),
(467, '20230330117', 0, 30807, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 03:54:02'),
(468, '20230330117', 0, 31757, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 03:54:02'),
(469, '20230330118', 0, 31324, 0, 4, '', 'red', 'random', 'parity', '2023-03-30 03:56:01'),
(470, '20230330118', 0, 31676, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 03:56:01'),
(471, '20230330118', 0, 31637, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 03:56:01'),
(472, '20230330118', 0, 31024, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 03:56:01'),
(473, '20230330119', 0, 31614, 0, 4, '', 'red', 'random', 'parity', '2023-03-30 03:58:01'),
(474, '20230330119', 0, 31759, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 03:58:01'),
(475, '20230330119', 0, 30882, 0, 2, '', 'red', 'random', 'bcone', '2023-03-30 03:58:01'),
(476, '20230330119', 0, 30859, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 03:58:01'),
(477, '20230330120', 0, 31957, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 04:00:02'),
(478, '20230330120', 0, 31011, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 04:00:02'),
(479, '20230330120', 0, 31290, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 04:00:02'),
(480, '20230330120', 0, 31734, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 04:00:02'),
(481, '20230330121', 0, 30836, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 04:02:02'),
(482, '20230330121', 0, 31123, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 04:02:02'),
(483, '20230330121', 0, 31550, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 04:02:02'),
(484, '20230330121', 0, 31398, 0, 8, '', 'red', 'random', 'emerd', '2023-03-30 04:02:02'),
(485, '20230330122', 0, 31145, 0, 5, '', 'green++violet', 'random', 'parity', '2023-03-30 04:04:01'),
(486, '20230330122', 0, 31414, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 04:04:01'),
(487, '20230330122', 0, 31508, 0, 8, '', 'red', 'random', 'bcone', '2023-03-30 04:04:01'),
(488, '20230330122', 0, 31112, 0, 2, '', 'red', 'random', 'emerd', '2023-03-30 04:04:01'),
(489, '20230330123', 0, 31203, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 04:06:02'),
(490, '20230330123', 0, 31483, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 04:06:02'),
(491, '20230330123', 0, 31721, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 04:06:02'),
(492, '20230330123', 0, 31299, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 04:06:02'),
(493, '20230330124', 0, 31112, 0, 2, '', 'red', 'random', 'parity', '2023-03-30 04:08:02'),
(494, '20230330124', 0, 31394, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 04:08:02'),
(495, '20230330124', 0, 31480, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 04:08:02'),
(496, '20230330124', 0, 31239, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 04:08:02'),
(497, '20230330125', 0, 31160, 0, 0, '', 'red++violet', 'random', 'parity', '2023-03-30 04:10:02'),
(498, '20230330125', 0, 30816, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 04:10:02'),
(499, '20230330125', 0, 31724, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 04:10:02'),
(500, '20230330125', 0, 31071, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 04:10:02'),
(501, '20230330126', 0, 30748, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 04:12:01'),
(502, '20230330126', 0, 31198, 0, 8, '', 'red', 'random', 'sapre', '2023-03-30 04:12:01'),
(503, '20230330126', 0, 31229, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 04:12:01'),
(504, '20230330126', 0, 31188, 0, 8, '', 'red', 'random', 'emerd', '2023-03-30 04:12:01'),
(505, '20230330127', 0, 30845, 0, 5, '', 'green++violet', 'random', 'parity', '2023-03-30 04:14:01'),
(506, '20230330127', 0, 31499, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 04:14:01'),
(507, '20230330127', 0, 31293, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 04:14:01'),
(508, '20230330127', 0, 30799, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 04:14:01'),
(509, '20230330128', 0, 31609, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 04:16:02'),
(510, '20230330128', 0, 31745, 0, 5, '', 'green++violet', 'random', 'sapre', '2023-03-30 04:16:02'),
(511, '20230330128', 0, 31478, 0, 8, '', 'red', 'random', 'bcone', '2023-03-30 04:16:02'),
(512, '20230330128', 0, 31086, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 04:16:02'),
(513, '20230330129', 0, 31024, 0, 4, '', 'red', 'random', 'parity', '2023-03-30 04:18:02'),
(514, '20230330129', 0, 31657, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 04:18:02'),
(515, '20230330129', 0, 31032, 0, 2, '', 'red', 'random', 'bcone', '2023-03-30 04:18:02'),
(516, '20230330129', 0, 31331, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 04:18:02'),
(517, '20230330130', 0, 31379, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 04:20:02'),
(518, '20230330130', 0, 30769, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 04:20:02'),
(519, '20230330130', 0, 31223, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 04:20:02'),
(520, '20230330130', 0, 31634, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 04:20:02'),
(521, '20230330131', 0, 31983, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 04:22:02'),
(522, '20230330131', 0, 31189, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 04:22:02'),
(523, '20230330131', 0, 31188, 0, 8, '', 'red', 'random', 'bcone', '2023-03-30 04:22:02'),
(524, '20230330131', 0, 30710, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 04:22:02'),
(525, '20230330132', 0, 31053, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 04:24:02'),
(526, '20230330132', 0, 30812, 0, 2, '', 'red', 'random', 'sapre', '2023-03-30 04:24:02'),
(527, '20230330132', 0, 30826, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 04:24:02'),
(528, '20230330132', 0, 31672, 0, 2, '', 'red', 'random', 'emerd', '2023-03-30 04:24:02'),
(529, '20230330133', 0, 31970, 0, 0, '', 'red++violet', 'random', 'parity', '2023-03-30 04:26:02'),
(530, '20230330133', 0, 31443, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 04:26:02'),
(531, '20230330133', 0, 31863, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 04:26:02'),
(532, '20230330133', 0, 31467, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 04:26:02'),
(533, '20230330134', 0, 31208, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 04:28:01'),
(534, '20230330134', 0, 31024, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 04:28:01'),
(535, '20230330134', 0, 31146, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 04:28:01'),
(536, '20230330134', 0, 31817, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 04:28:01'),
(537, '20230330135', 0, 31086, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 04:30:02'),
(538, '20230330135', 0, 31211, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 04:30:02'),
(539, '20230330135', 0, 31214, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 04:30:02'),
(540, '20230330135', 0, 31891, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 04:30:02'),
(541, '20230330136', 0, 31608, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 04:32:02'),
(542, '20230330136', 0, 30873, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 04:32:02'),
(543, '20230330136', 0, 31398, 0, 8, '', 'red', 'random', 'bcone', '2023-03-30 04:32:02'),
(544, '20230330136', 0, 31736, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 04:32:02'),
(545, '20230330137', 0, 31477, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 04:34:01'),
(546, '20230330137', 0, 31394, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 04:34:01');
INSERT INTO `tbl_result` (`id`, `periodid`, `price`, `randomprice`, `result`, `randomresult`, `color`, `randomcolor`, `resulttype`, `tabtype`, `createdate`) VALUES
(547, '20230330137', 0, 31223, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 04:34:01'),
(548, '20230330137', 0, 31630, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 04:34:01'),
(549, '20230330138', 0, 30873, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 04:36:02'),
(550, '20230330138', 0, 31979, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 04:36:02'),
(551, '20230330138', 0, 31528, 0, 8, '', 'red', 'random', 'bcone', '2023-03-30 04:36:02'),
(552, '20230330138', 0, 31398, 0, 8, '', 'red', 'random', 'emerd', '2023-03-30 04:36:02'),
(553, '20230330139', 0, 30922, 0, 2, '', 'red', 'random', 'parity', '2023-03-30 04:38:01'),
(554, '20230330139', 0, 31123, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 04:38:01'),
(555, '20230330139', 0, 31962, 0, 2, '', 'red', 'random', 'bcone', '2023-03-30 04:38:01'),
(556, '20230330139', 0, 30761, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 04:38:01'),
(557, '20230330140', 0, 31447, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 04:40:02'),
(558, '20230330140', 0, 31514, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 04:40:02'),
(559, '20230330140', 0, 31802, 0, 2, '', 'red', 'random', 'bcone', '2023-03-30 04:40:02'),
(560, '20230330140', 0, 31398, 0, 8, '', 'red', 'random', 'emerd', '2023-03-30 04:40:02'),
(561, '20230330141', 0, 31203, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 04:42:02'),
(562, '20230330141', 0, 31682, 0, 2, '', 'red', 'random', 'sapre', '2023-03-30 04:42:02'),
(563, '20230330141', 0, 31541, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 04:42:02'),
(564, '20230330141', 0, 31770, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 04:42:02'),
(565, '20230330142', 0, 31283, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 04:44:02'),
(566, '20230330142', 0, 31618, 0, 8, '', 'red', 'random', 'sapre', '2023-03-30 04:44:02'),
(567, '20230330142', 0, 31301, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 04:44:02'),
(568, '20230330142', 0, 31575, 0, 5, '', 'green++violet', 'random', 'emerd', '2023-03-30 04:44:02'),
(569, '20230330143', 0, 31183, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 04:46:02'),
(570, '20230330143', 0, 31261, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 04:46:02'),
(571, '20230330143', 0, 31131, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 04:46:02'),
(572, '20230330143', 0, 31283, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 04:46:02'),
(573, '20230330144', 0, 31489, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 04:48:02'),
(574, '20230330144', 0, 31546, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 04:48:02'),
(575, '20230330144', 0, 30919, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 04:48:02'),
(576, '20230330144', 0, 30873, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 04:48:02'),
(577, '20230330145', 0, 31724, 0, 4, '', 'red', 'random', 'parity', '2023-03-30 04:50:02'),
(578, '20230330145', 0, 31178, 0, 8, '', 'red', 'random', 'sapre', '2023-03-30 04:50:02'),
(579, '20230330145', 0, 31574, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 04:50:02'),
(580, '20230330145', 0, 31477, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 04:50:02'),
(581, '20230330146', 0, 31754, 0, 4, '', 'red', 'random', 'parity', '2023-03-30 04:52:01'),
(582, '20230330146', 0, 30872, 0, 2, '', 'red', 'random', 'sapre', '2023-03-30 04:52:01'),
(583, '20230330146', 0, 30769, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 04:52:01'),
(584, '20230330146', 0, 31567, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 04:52:01'),
(585, '20230330147', 0, 31219, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 04:54:02'),
(586, '20230330147', 0, 31577, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 04:54:02'),
(587, '20230330147', 0, 31053, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 04:54:02'),
(588, '20230330147', 0, 31707, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 04:54:02'),
(589, '20230330148', 0, 31371, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 04:56:01'),
(590, '20230330148', 0, 31417, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 04:56:01'),
(591, '20230330148', 0, 31388, 0, 8, '', 'red', 'random', 'bcone', '2023-03-30 04:56:01'),
(592, '20230330148', 0, 31638, 0, 8, '', 'red', 'random', 'emerd', '2023-03-30 04:56:01'),
(593, '20230330149', 0, 30879, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 04:58:02'),
(594, '20230330149', 0, 31487, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 04:58:02'),
(595, '20230330149', 0, 31817, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 04:58:02'),
(596, '20230330149', 0, 31662, 0, 2, '', 'red', 'random', 'emerd', '2023-03-30 04:58:02'),
(597, '20230330150', 0, 31208, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 05:00:02'),
(598, '20230330150', 0, 31026, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 05:00:02'),
(599, '20230330150', 0, 31417, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 05:00:02'),
(600, '20230330150', 0, 31236, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 05:00:02'),
(601, '20230330151', 0, 31614, 0, 4, '', 'red', 'random', 'parity', '2023-03-30 05:02:02'),
(602, '20230330151', 0, 31000, 0, 0, '', 'red++violet', 'random', 'sapre', '2023-03-30 05:02:02'),
(603, '20230330151', 0, 31586, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 05:02:02'),
(604, '20230330151', 0, 31757, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 05:02:02'),
(605, '20230330152', 0, 31175, 0, 5, '', 'green++violet', 'random', 'parity', '2023-03-30 05:04:02'),
(606, '20230330152', 0, 31414, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 05:04:02'),
(607, '20230330152', 0, 30912, 0, 2, '', 'red', 'random', 'bcone', '2023-03-30 05:04:02'),
(608, '20230330152', 0, 31211, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 05:04:02'),
(609, '20230330153', 0, 31647, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 05:06:02'),
(610, '20230330153', 0, 31863, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 05:06:02'),
(611, '20230330153', 0, 31350, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 05:06:02'),
(612, '20230330153', 0, 31280, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 05:06:02'),
(613, '20230330154', 0, 30952, 0, 2, '', 'red', 'random', 'parity', '2023-03-30 05:08:01'),
(614, '20230330154', 0, 31982, 0, 2, '', 'red', 'random', 'sapre', '2023-03-30 05:08:01'),
(615, '20230330154', 0, 31167, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 05:08:01'),
(616, '20230330154', 0, 31866, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 05:08:01'),
(617, '20230330155', 0, 31679, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 05:10:02'),
(618, '20230330155', 0, 31136, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 05:10:02'),
(619, '20230330155', 0, 31557, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 05:10:02'),
(620, '20230330155', 0, 30967, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 05:10:02'),
(621, '20230330156', 0, 31817, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 05:12:02'),
(622, '20230330156', 0, 31419, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 05:12:02'),
(623, '20230330156', 0, 30826, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 05:12:02'),
(624, '20230330156', 0, 31129, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 05:12:02'),
(625, '20230330157', 0, 30872, 0, 2, '', 'red', 'random', 'parity', '2023-03-30 05:14:02'),
(626, '20230330157', 0, 31794, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 05:14:02'),
(627, '20230330157', 0, 31721, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 05:14:02'),
(628, '20230330157', 0, 31171, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 05:14:02'),
(629, '20230330158', 0, 31528, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 05:16:01'),
(630, '20230330158', 0, 31766, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 05:16:01'),
(631, '20230330158', 0, 31079, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 05:16:01'),
(632, '20230330158', 0, 31324, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 05:16:01'),
(633, '20230330159', 0, 30967, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 05:18:01'),
(634, '20230330159', 0, 31604, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 05:18:01'),
(635, '20230330159', 0, 31508, 0, 8, '', 'red', 'random', 'bcone', '2023-03-30 05:18:01'),
(636, '20230330159', 0, 31498, 0, 8, '', 'red', 'random', 'emerd', '2023-03-30 05:18:01'),
(637, '20230330160', 0, 31438, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 05:20:02'),
(638, '20230330160', 0, 31793, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 05:20:02'),
(639, '20230330160', 0, 31647, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 05:20:02'),
(640, '20230330160', 0, 31431, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 05:20:02'),
(641, '20230330161', 0, 31277, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 05:22:02'),
(642, '20230330161', 0, 31582, 0, 2, '', 'red', 'random', 'sapre', '2023-03-30 05:22:02'),
(643, '20230330161', 0, 31551, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 05:22:02'),
(644, '20230330161', 0, 31235, 0, 5, '', 'green++violet', 'random', 'emerd', '2023-03-30 05:22:02'),
(645, '20230330162', 0, 31208, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 05:24:02'),
(646, '20230330162', 0, 31233, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 05:24:02'),
(647, '20230330162', 0, 31630, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 05:24:02'),
(648, '20230330162', 0, 31699, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 05:24:02'),
(649, '20230330163', 0, 31633, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 05:26:02'),
(650, '20230330163', 0, 31470, 0, 0, '', 'red++violet', 'random', 'sapre', '2023-03-30 05:26:02'),
(651, '20230330163', 0, 31684, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 05:26:02'),
(652, '20230330163', 0, 31957, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 05:26:02'),
(653, '20230330164', 0, 31232, 0, 2, '', 'red', 'random', 'parity', '2023-03-30 05:28:01'),
(654, '20230330164', 0, 30774, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 05:28:01'),
(655, '20230330164', 0, 31129, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 05:28:01'),
(656, '20230330164', 0, 31388, 0, 8, '', 'red', 'random', 'emerd', '2023-03-30 05:28:01'),
(657, '20230330165', 0, 31540, 0, 0, '', 'red++violet', 'random', 'parity', '2023-03-30 05:30:03'),
(658, '20230330165', 0, 31623, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 05:30:03'),
(659, '20230330165', 0, 31630, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 05:30:03'),
(660, '20230330165', 0, 31704, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 05:30:03'),
(661, '20230330166', 0, 31741, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 05:32:02'),
(662, '20230330166', 0, 31371, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 05:32:02'),
(663, '20230330166', 0, 31129, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 05:32:02'),
(664, '20230330166', 0, 31376, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 05:32:02'),
(665, '20230330167', 0, 31458, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 05:34:01'),
(666, '20230330167', 0, 31887, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 05:34:01'),
(667, '20230330167', 0, 31476, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 05:34:01'),
(668, '20230330167', 0, 31108, 0, 8, '', 'red', 'random', 'emerd', '2023-03-30 05:34:01'),
(669, '20230330168', 0, 31676, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 05:36:01'),
(670, '20230330168', 0, 31567, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 05:36:01'),
(671, '20230330168', 0, 31026, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 05:36:01'),
(672, '20230330168', 0, 31129, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 05:36:01'),
(673, '20230330169', 0, 30872, 0, 2, '', 'red', 'random', 'parity', '2023-03-30 05:38:02'),
(674, '20230330169', 0, 31586, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 05:38:02'),
(675, '20230330169', 0, 31676, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 05:38:02'),
(676, '20230330169', 0, 31763, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 05:38:02'),
(677, '20230330170', 0, 31969, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 05:40:02'),
(678, '20230330170', 0, 31169, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 05:40:02'),
(679, '20230330170', 0, 31556, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 05:40:02'),
(680, '20230330170', 0, 31759, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 05:40:02'),
(681, '20230330171', 0, 31821, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 05:42:01'),
(682, '20230330171', 0, 31041, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 05:42:01'),
(683, '20230330171', 0, 31112, 0, 2, '', 'red', 'random', 'bcone', '2023-03-30 05:42:01'),
(684, '20230330171', 0, 31274, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 05:42:01'),
(685, '20230330172', 0, 31616, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 05:44:01'),
(686, '20230330172', 0, 31283, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 05:44:01'),
(687, '20230330172', 0, 30873, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 05:44:01'),
(688, '20230330172', 0, 31941, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 05:44:01'),
(689, '20230330173', 0, 31208, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 05:46:01'),
(690, '20230330173', 0, 31105, 0, 5, '', 'green++violet', 'random', 'sapre', '2023-03-30 05:46:01'),
(691, '20230330173', 0, 31394, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 05:46:01'),
(692, '20230330173', 0, 31817, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 05:46:01'),
(693, '20230330174', 0, 31131, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 05:48:02'),
(694, '20230330174', 0, 31211, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 05:48:02'),
(695, '20230330174', 0, 31211, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 05:48:02'),
(696, '20230330174', 0, 31193, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 05:48:02'),
(697, '20230330175', 0, 31293, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 05:50:02'),
(698, '20230330175', 0, 31090, 0, 0, '', 'red++violet', 'random', 'sapre', '2023-03-30 05:50:02'),
(699, '20230330175', 0, 31731, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 05:50:02'),
(700, '20230330175', 0, 31616, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 05:50:02'),
(701, '20230330176', 0, 31211, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 05:52:02'),
(702, '20230330176', 0, 31817, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 05:52:02'),
(703, '20230330176', 0, 31281, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 05:52:02'),
(704, '20230330176', 0, 31561, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 05:52:02'),
(705, '20230330177', 0, 31579, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 05:54:02'),
(706, '20230330177', 0, 30952, 0, 2, '', 'red', 'random', 'sapre', '2023-03-30 05:54:02'),
(707, '20230330177', 0, 31578, 0, 8, '', 'red', 'random', 'bcone', '2023-03-30 05:54:02'),
(708, '20230330177', 0, 31185, 0, 5, '', 'green++violet', 'random', 'emerd', '2023-03-30 05:54:02'),
(709, '20230330178', 0, 31618, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 05:56:02'),
(710, '20230330178', 0, 31137, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 05:56:02'),
(711, '20230330178', 0, 31394, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 05:56:02'),
(712, '20230330178', 0, 30901, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 05:56:02'),
(713, '20230330179', 0, 31277, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 05:58:01'),
(714, '20230330179', 0, 31578, 0, 8, '', 'red', 'random', 'sapre', '2023-03-30 05:58:01'),
(715, '20230330179', 0, 31409, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 05:58:01'),
(716, '20230330179', 0, 31185, 0, 5, '', 'green++violet', 'random', 'emerd', '2023-03-30 05:58:01'),
(717, '20230330180', 0, 30857, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 06:00:02'),
(718, '20230330180', 0, 31969, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 06:00:02'),
(719, '20230330180', 0, 31498, 0, 8, '', 'red', 'random', 'bcone', '2023-03-30 06:00:02'),
(720, '20230330180', 0, 31189, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 06:00:02'),
(721, '20230330181', 0, 31011, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 06:02:02'),
(722, '20230330181', 0, 31345, 0, 5, '', 'green++violet', 'random', 'sapre', '2023-03-30 06:02:02'),
(723, '20230330181', 0, 31741, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 06:02:02'),
(724, '20230330181', 0, 31157, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 06:02:02'),
(725, '20230330182', 0, 31866, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 06:04:02'),
(726, '20230330182', 0, 30945, 0, 5, '', 'green++violet', 'random', 'sapre', '2023-03-30 06:04:02'),
(727, '20230330182', 0, 31211, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 06:04:02'),
(728, '20230330182', 0, 31578, 0, 8, '', 'red', 'random', 'emerd', '2023-03-30 06:04:02'),
(729, '20230330183', 0, 31026, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 06:06:02'),
(730, '20230330183', 0, 31766, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 06:06:02'),
(731, '20230330183', 0, 31322, 0, 2, '', 'red', 'random', 'bcone', '2023-03-30 06:06:02'),
(732, '20230330183', 0, 31486, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 06:06:02'),
(733, '20230330184', 0, 31676, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 06:08:01'),
(734, '20230330184', 0, 31017, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 06:08:01'),
(735, '20230330184', 0, 31235, 0, 5, '', 'green++violet', 'random', 'bcone', '2023-03-30 06:08:01'),
(736, '20230330184', 0, 30891, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 06:08:01'),
(737, '20230330185', 0, 31572, 0, 2, '', 'red', 'random', 'parity', '2023-03-30 06:10:02'),
(738, '20230330185', 0, 31217, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 06:10:02'),
(739, '20230330185', 0, 31440, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 06:10:02'),
(740, '20230330185', 0, 31668, 0, 8, '', 'red', 'random', 'emerd', '2023-03-30 06:10:02'),
(741, '20230330186', 0, 31900, 0, 0, '', 'red++violet', 'random', 'parity', '2023-03-30 06:12:02'),
(742, '20230330186', 0, 31550, 0, 0, '', 'red++violet', 'random', 'sapre', '2023-03-30 06:12:02'),
(743, '20230330186', 0, 30846, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 06:12:02'),
(744, '20230330186', 0, 31353, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 06:12:02'),
(745, '20230330187', 20, 31112, 0, 2, 'red+violet', 'RED', 'real', 'parity', '2023-03-30 06:14:02'),
(746, '20230330187', 0, 31969, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 06:14:02'),
(747, '20230330187', 0, 31608, 0, 8, '', 'red', 'random', 'bcone', '2023-03-30 06:14:02'),
(748, '20230330187', 0, 31443, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 06:14:02'),
(749, '20230330188', 0, 30853, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 06:16:02'),
(750, '20230330188', 0, 31817, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 06:16:02'),
(751, '20230330188', 0, 31721, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 06:16:02'),
(752, '20230330188', 0, 30853, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 06:16:02'),
(753, '20230330189', 0, 31879, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 06:18:01'),
(754, '20230330189', 0, 31416, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 06:18:01'),
(755, '20230330189', 0, 31473, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 06:18:01'),
(756, '20230330189', 0, 31866, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 06:18:01'),
(757, '20230330190', -78512.8, 31176, 2, 6, 'red', 'RED', 'real', 'parity', '2023-03-30 06:20:01'),
(758, '20230330190', 0, 31685, 0, 5, '', 'green++violet', 'random', 'sapre', '2023-03-30 06:20:01'),
(759, '20230330190', 0, 30702, 0, 2, '', 'red', 'random', 'bcone', '2023-03-30 06:20:01'),
(760, '20230330190', 0, 30812, 0, 2, '', 'red', 'random', 'emerd', '2023-03-30 06:20:01'),
(761, '20230330191', 0, 31489, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 06:22:01'),
(762, '20230330191', 0, 31609, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 06:22:01'),
(763, '20230330191', 0, 31144, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 06:22:01'),
(764, '20230330191', 0, 30795, 0, 5, '', 'green++violet', 'random', 'emerd', '2023-03-30 06:22:01'),
(765, '20230330192', 0, 31350, 0, 0, '', 'red++violet', 'random', 'parity', '2023-03-30 06:24:02'),
(766, '20230330192', 0, 32053, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 06:24:02'),
(767, '20230330192', 0, 31995, 0, 5, '', 'green++violet', 'random', 'bcone', '2023-03-30 06:24:02'),
(768, '20230330192', 0, 31551, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 06:24:02'),
(769, '20230330193', 0, 31109, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 06:26:01'),
(770, '20230330193', 0, 31883, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 06:26:01'),
(771, '20230330193', 0, 31684, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 06:26:01'),
(772, '20230330193', 0, 31931, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 06:26:01'),
(773, '20230330194', 0, 31615, 0, 5, '', 'green++violet', 'random', 'parity', '2023-03-30 06:28:02'),
(774, '20230330194', 0, 31122, 0, 2, '', 'red', 'random', 'sapre', '2023-03-30 06:28:02'),
(775, '20230330194', 0, 31731, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 06:28:02'),
(776, '20230330194', 0, 31188, 0, 8, '', 'red', 'random', 'emerd', '2023-03-30 06:28:02'),
(777, '20230330195', 0, 31419, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 06:30:02'),
(778, '20230330195', 0, 30885, 0, 5, '', 'green++violet', 'random', 'sapre', '2023-03-30 06:30:02'),
(779, '20230330195', 0, 31891, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 06:30:02'),
(780, '20230330195', 0, 30809, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 06:30:02'),
(781, '20230330196', 0, 31219, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 06:32:01'),
(782, '20230330196', 0, 31123, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 06:32:01'),
(783, '20230330196', 0, 31395, 0, 5, '', 'green++violet', 'random', 'bcone', '2023-03-30 06:32:01'),
(784, '20230330196', 0, 30951, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 06:32:01'),
(785, '20230330197', 0, 31616, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 06:34:01'),
(786, '20230330197', 0, 31644, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 06:34:01'),
(787, '20230330197', 0, 31353, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 06:34:01'),
(788, '20230330197', 0, 31745, 0, 5, '', 'green++violet', 'random', 'emerd', '2023-03-30 06:34:01'),
(789, '20230330198', 0, 31450, 0, 0, '', 'red++violet', 'random', 'parity', '2023-03-30 06:36:01'),
(790, '20230330198', 0, 31013, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 06:36:01'),
(791, '20230330198', 0, 30919, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 06:36:01'),
(792, '20230330198', 0, 31450, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 06:36:01'),
(793, '20230330199', 0, 30901, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 06:38:02'),
(794, '20230330199', 0, 31637, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 06:38:02'),
(795, '20230330199', 0, 31467, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 06:38:02'),
(796, '20230330199', 0, 31194, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 06:38:02'),
(797, '20230330200', 0, 31026, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 06:40:02'),
(798, '20230330200', 0, 31487, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 06:40:02'),
(799, '20230330200', 0, 31109, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 06:40:02'),
(800, '20230330200', 0, 31137, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 06:40:02'),
(801, '20230330201', 0, 31572, 0, 2, '', 'red', 'random', 'parity', '2023-03-30 06:42:01'),
(802, '20230330201', 0, 31032, 0, 2, '', 'red', 'random', 'sapre', '2023-03-30 06:42:01'),
(803, '20230330201', 0, 31395, 0, 5, '', 'green++violet', 'random', 'bcone', '2023-03-30 06:42:01'),
(804, '20230330201', 0, 31530, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 06:42:01'),
(805, '20230330202', 0, 31388, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 06:44:02'),
(806, '20230330202', 0, 31439, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 06:44:02'),
(807, '20230330202', 0, 31551, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 06:44:02'),
(808, '20230330202', 0, 30945, 0, 5, '', 'green++violet', 'random', 'emerd', '2023-03-30 06:44:02'),
(809, '20230330203', 0, 31467, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 06:46:01'),
(810, '20230330203', 0, 31353, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 06:46:01'),
(811, '20230330203', 0, 31090, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 06:46:01'),
(812, '20230330203', 0, 31157, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 06:46:01'),
(813, '20230330204', 0, 31935, 0, 5, '', 'green++violet', 'random', 'parity', '2023-03-30 06:48:01'),
(814, '20230330204', 0, 31579, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 06:48:01'),
(815, '20230330204', 0, 31419, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 06:48:01'),
(816, '20230330204', 0, 31625, 0, 5, '', 'green++violet', 'random', 'emerd', '2023-03-30 06:48:01'),
(817, '20230330205', 0, 31122, 0, 2, '', 'red', 'random', 'parity', '2023-03-30 06:50:02'),
(818, '20230330205', 0, 30769, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 06:50:02'),
(819, '20230330205', 0, 31219, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 06:50:02'),
(820, '20230330205', 0, 31450, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 06:50:02'),
(821, '20230330206', 0, 31119, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 06:52:01'),
(822, '20230330206', 0, 30823, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 06:52:01'),
(823, '20230330206', 0, 31616, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 06:52:01'),
(824, '20230330206', 0, 31636, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 06:52:01'),
(825, '20230330207', 0, 31957, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 06:54:02'),
(826, '20230330207', 0, 30891, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 06:54:02'),
(827, '20230330207', 0, 31893, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 06:54:02'),
(828, '20230330207', 0, 31024, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 06:54:02'),
(829, '20230330208', 0, 31589, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 06:56:01'),
(830, '20230330208', 0, 31482, 0, 2, '', 'red', 'random', 'sapre', '2023-03-30 06:56:01'),
(831, '20230330208', 0, 31721, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 06:56:01'),
(832, '20230330208', 0, 31400, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 06:56:01'),
(833, '20230330209', 0, 31568, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 06:58:02'),
(834, '20230330209', 0, 31156, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 06:58:02'),
(835, '20230330209', 0, 30792, 0, 2, '', 'red', 'random', 'bcone', '2023-03-30 06:58:02'),
(836, '20230330209', 0, 31641, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 06:58:02'),
(837, '20230330210', 0, 31662, 0, 2, '', 'red', 'random', 'parity', '2023-03-30 07:00:01'),
(838, '20230330210', 0, 30856, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 07:00:01'),
(839, '20230330210', 0, 30803, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 07:00:01'),
(840, '20230330210', 0, 31800, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 07:00:01'),
(841, '20230330211', 0, 31575, 0, 5, '', 'green++violet', 'random', 'parity', '2023-03-30 07:02:01'),
(842, '20230330211', 0, 31553, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 07:02:01'),
(843, '20230330211', 0, 31006, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 07:02:01'),
(844, '20230330211', 0, 31514, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 07:02:01'),
(845, '20230330212', 0, 30881, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 07:04:02'),
(846, '20230330212', 0, 30919, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 07:04:02'),
(847, '20230330212', 0, 31347, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 07:04:02'),
(848, '20230330212', 0, 31713, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 07:04:02'),
(849, '20230330213', 0, 30769, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 07:06:01'),
(850, '20230330213', 0, 30807, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 07:06:01'),
(851, '20230330213', 0, 31182, 0, 2, '', 'red', 'random', 'bcone', '2023-03-30 07:06:01'),
(852, '20230330213', 0, 31017, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 07:06:01'),
(853, '20230330214', 0, 31567, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 07:08:01'),
(854, '20230330214', 0, 31176, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 07:08:01'),
(855, '20230330214', 0, 31553, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 07:08:01'),
(856, '20230330214', 0, 31483, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 07:08:01'),
(857, '20230330215', 0, 31410, 0, 0, '', 'red++violet', 'random', 'parity', '2023-03-30 07:10:01'),
(858, '20230330215', 0, 30937, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 07:10:01'),
(859, '20230330215', 0, 31417, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 07:10:01'),
(860, '20230330215', 0, 31431, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 07:10:01'),
(861, '20230330216', 0, 31633, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 07:12:02'),
(862, '20230330216', 0, 30940, 0, 0, '', 'red++violet', 'random', 'sapre', '2023-03-30 07:12:02'),
(863, '20230330216', 0, 31835, 0, 5, '', 'green++violet', 'random', 'bcone', '2023-03-30 07:12:02'),
(864, '20230330216', 0, 31817, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 07:12:02'),
(865, '20230330217', 0, 30803, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 07:14:02'),
(866, '20230330217', 0, 31549, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 07:14:02'),
(867, '20230330217', 0, 31575, 0, 5, '', 'green++violet', 'random', 'bcone', '2023-03-30 07:14:02'),
(868, '20230330217', 0, 30846, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 07:14:02'),
(869, '20230330218', 0, 31415, 0, 5, '', 'green++violet', 'random', 'parity', '2023-03-30 07:16:01'),
(870, '20230330218', 0, 31129, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 07:16:01'),
(871, '20230330218', 0, 31543, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 07:16:01'),
(872, '20230330218', 0, 31395, 0, 5, '', 'green++violet', 'random', 'emerd', '2023-03-30 07:16:01'),
(873, '20230330219', 0, 31647, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 07:18:02'),
(874, '20230330219', 0, 31827, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 07:18:02'),
(875, '20230330219', 0, 31704, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 07:18:02'),
(876, '20230330219', 0, 31156, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 07:18:02'),
(877, '20230330220', 0, 31188, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 07:20:02'),
(878, '20230330220', 0, 31863, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 07:20:02'),
(879, '20230330220', 0, 31217, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 07:20:02'),
(880, '20230330220', 0, 30872, 0, 2, '', 'red', 'random', 'emerd', '2023-03-30 07:20:02'),
(881, '20230330221', 0, 30891, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 07:22:01'),
(882, '20230330221', 0, 31636, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 07:22:01'),
(883, '20230330221', 0, 31575, 0, 5, '', 'green++violet', 'random', 'bcone', '2023-03-30 07:22:01'),
(884, '20230330221', 0, 30784, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 07:22:01'),
(885, '20230330222', 0, 31578, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 07:24:02'),
(886, '20230330222', 0, 31957, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 07:24:02'),
(887, '20230330222', 0, 30905, 0, 5, '', 'green++violet', 'random', 'bcone', '2023-03-30 07:24:02'),
(888, '20230330222', 0, 31555, 0, 5, '', 'green++violet', 'random', 'emerd', '2023-03-30 07:24:02'),
(889, '20230330223', 0, 31026, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 07:26:02'),
(890, '20230330223', 0, 31757, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 07:26:02'),
(891, '20230330223', 0, 30800, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 07:26:02'),
(892, '20230330223', 0, 31206, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 07:26:02'),
(893, '20230330224', 0, 31251, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 07:28:01'),
(894, '20230330224', 0, 31921, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 07:28:01'),
(895, '20230330224', 0, 31344, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 07:28:01'),
(896, '20230330224', 0, 31006, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 07:28:01'),
(897, '20230330225', 0, 30967, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 07:30:02'),
(898, '20230330225', 0, 31344, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 07:30:02'),
(899, '20230330225', 0, 30905, 0, 5, '', 'green++violet', 'random', 'bcone', '2023-03-30 07:30:02'),
(900, '20230330225', 0, 31079, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 07:30:02'),
(901, '20230330226', 0, 30951, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 07:32:01'),
(902, '20230330226', 0, 31583, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 07:32:01'),
(903, '20230330226', 0, 31629, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 07:32:01'),
(904, '20230330226', 0, 31013, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 07:32:01'),
(905, '20230330227', 0, 31185, 0, 5, '', 'green++violet', 'random', 'parity', '2023-03-30 07:34:01'),
(906, '20230330227', 0, 31137, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 07:34:01'),
(907, '20230330227', 0, 31251, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 07:34:01'),
(908, '20230330227', 0, 31229, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 07:34:01'),
(909, '20230330228', 0, 31188, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 07:36:01'),
(910, '20230330228', 0, 31668, 0, 8, '', 'red', 'random', 'sapre', '2023-03-30 07:36:01'),
(911, '20230330228', 0, 31540, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 07:36:01'),
(912, '20230330228', 0, 31431, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 07:36:01'),
(913, '20230330229', 0, 31721, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 07:38:01'),
(914, '20230330229', 0, 30853, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 07:38:01'),
(915, '20230330229', 0, 30724, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 07:38:01'),
(916, '20230330229', 0, 31770, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 07:38:01'),
(917, '20230330230', 0, 31423, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 07:40:02'),
(918, '20230330230', 0, 31156, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 07:40:02'),
(919, '20230330230', 0, 31133, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 07:40:02'),
(920, '20230330230', 0, 30826, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 07:40:02'),
(921, '20230330231', 0, 31071, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 07:42:02'),
(922, '20230330231', 0, 31314, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 07:42:02'),
(923, '20230330231', 0, 31123, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 07:42:02'),
(924, '20230330231', 0, 31802, 0, 2, '', 'red', 'random', 'emerd', '2023-03-30 07:42:02'),
(925, '20230330232', 0, 31566, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 07:44:02'),
(926, '20230330232', 0, 31090, 0, 0, '', 'red++violet', 'random', 'sapre', '2023-03-30 07:44:02'),
(927, '20230330232', 0, 30903, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 07:44:02'),
(928, '20230330232', 0, 31935, 0, 5, '', 'green++violet', 'random', 'emerd', '2023-03-30 07:44:02'),
(929, '20230330233', 0, 31640, 0, 0, '', 'red++violet', 'random', 'parity', '2023-03-30 07:46:01'),
(930, '20230330233', 0, 31483, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 07:46:01'),
(931, '20230330233', 0, 31376, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 07:46:01'),
(932, '20230330233', 0, 31969, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 07:46:01'),
(933, '20230330234', 0, 32008, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 07:48:01'),
(934, '20230330234', 0, 31324, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 07:48:01'),
(935, '20230330234', 0, 31682, 0, 2, '', 'red', 'random', 'bcone', '2023-03-30 07:48:01'),
(936, '20230330234', 0, 31367, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 07:48:01'),
(937, '20230330235', 0, 30859, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 07:50:02'),
(938, '20230330235', 0, 31866, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 07:50:02'),
(939, '20230330235', 0, 31431, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 07:50:02'),
(940, '20230330235', 0, 30871, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 07:50:02'),
(941, '20230330236', 0, 30830, 0, 0, '', 'red++violet', 'random', 'parity', '2023-03-30 07:52:01'),
(942, '20230330236', 0, 31274, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 07:52:01'),
(943, '20230330236', 0, 31435, 0, 5, '', 'green++violet', 'random', 'bcone', '2023-03-30 07:52:01'),
(944, '20230330236', 0, 31458, 0, 8, '', 'red', 'random', 'emerd', '2023-03-30 07:52:01'),
(945, '20230330237', 0, 31431, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 07:54:02'),
(946, '20230330237', 0, 31439, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 07:54:02'),
(947, '20230330237', 0, 30919, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 07:54:02'),
(948, '20230330237', 0, 31394, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 07:54:02'),
(949, '20230330238', 0, 31223, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 07:56:02'),
(950, '20230330238', 0, 30891, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 07:56:02'),
(951, '20230330238', 0, 31630, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 07:56:02'),
(952, '20230330238', 0, 31707, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 07:56:02'),
(953, '20230330239', 0, 31556, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 07:58:02'),
(954, '20230330239', 0, 31957, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 07:58:02'),
(955, '20230330239', 0, 31891, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 07:58:02'),
(956, '20230330239', 0, 31129, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 07:58:02'),
(957, '20230330240', 0, 31185, 0, 5, '', 'green++violet', 'random', 'parity', '2023-03-30 08:00:02'),
(958, '20230330240', 0, 31156, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 08:00:02'),
(959, '20230330240', 0, 31638, 0, 8, '', 'red', 'random', 'bcone', '2023-03-30 08:00:02'),
(960, '20230330240', 0, 31142, 0, 2, '', 'red', 'random', 'emerd', '2023-03-30 08:00:02'),
(961, '20230330241', 0, 30872, 0, 2, '', 'red', 'random', 'parity', '2023-03-30 08:02:01'),
(962, '20230330241', 0, 31130, 0, 0, '', 'red++violet', 'random', 'sapre', '2023-03-30 08:02:01'),
(963, '20230330241', 0, 30823, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 08:02:01'),
(964, '20230330241', 0, 30852, 0, 2, '', 'red', 'random', 'emerd', '2023-03-30 08:02:01'),
(965, '20230330242', 0, 30836, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 08:04:01'),
(966, '20230330242', 0, 30724, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 08:04:01'),
(967, '20230330242', 0, 31011, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 08:04:01'),
(968, '20230330242', 0, 31499, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 08:04:01'),
(969, '20230330243', 0, 30706, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 08:06:01'),
(970, '20230330243', 0, 31633, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 08:06:01'),
(971, '20230330243', 0, 31574, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 08:06:01'),
(972, '20230330243', 0, 31431, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 08:06:01'),
(973, '20230330244', 0, 31223, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 08:08:01'),
(974, '20230330244', 0, 31539, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 08:08:01'),
(975, '20230330244', 0, 31609, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 08:08:01'),
(976, '20230330244', 0, 31540, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 08:08:01'),
(977, '20230330245', 0, 31583, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 08:10:02'),
(978, '20230330245', 0, 31117, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 08:10:02'),
(979, '20230330245', 0, 31345, 0, 5, '', 'green++violet', 'random', 'bcone', '2023-03-30 08:10:02'),
(980, '20230330245', 0, 31668, 0, 8, '', 'red', 'random', 'emerd', '2023-03-30 08:10:02'),
(981, '20230330246', 0, 31127, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 08:12:02'),
(982, '20230330246', 0, 30786, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 08:12:02'),
(983, '20230330246', 0, 31388, 0, 8, '', 'red', 'random', 'bcone', '2023-03-30 08:12:02'),
(984, '20230330246', 0, 31754, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 08:12:02'),
(985, '20230330247', 0, 31204, 0, 4, '', 'red', 'random', 'parity', '2023-03-30 08:14:02'),
(986, '20230330247', 0, 31000, 0, 0, '', 'red++violet', 'random', 'sapre', '2023-03-30 08:14:02'),
(987, '20230330247', 0, 30810, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 08:14:02'),
(988, '20230330247', 0, 31540, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 08:14:02'),
(989, '20230330248', 0, 31435, 0, 5, '', 'green++violet', 'random', 'parity', '2023-03-30 08:16:01'),
(990, '20230330248', 0, 30905, 0, 5, '', 'green++violet', 'random', 'sapre', '2023-03-30 08:16:01'),
(991, '20230330248', 0, 31122, 0, 2, '', 'red', 'random', 'bcone', '2023-03-30 08:16:01'),
(992, '20230330248', 0, 31198, 0, 8, '', 'red', 'random', 'emerd', '2023-03-30 08:16:01'),
(993, '20230330249', 0, 31458, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 08:18:01'),
(994, '20230330249', 0, 31198, 0, 8, '', 'red', 'random', 'sapre', '2023-03-30 08:18:01'),
(995, '20230330249', 0, 31625, 0, 5, '', 'green++violet', 'random', 'bcone', '2023-03-30 08:18:01'),
(996, '20230330249', 0, 31551, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 08:18:01'),
(997, '20230330250', 0, 31582, 0, 2, '', 'red', 'random', 'parity', '2023-03-30 08:20:02'),
(998, '20230330250', 0, 30795, 0, 5, '', 'green++violet', 'random', 'sapre', '2023-03-30 08:20:02'),
(999, '20230330250', 0, 30724, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 08:20:02'),
(1000, '20230330250', 0, 31350, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 08:20:02'),
(1001, '20230330251', 0, 31921, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 08:22:02'),
(1002, '20230330251', 0, 31269, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 08:22:02'),
(1003, '20230330251', 0, 30811, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 08:22:02'),
(1004, '20230330251', 0, 30800, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 08:22:02'),
(1005, '20230330252', 0, 31644, 0, 4, '', 'red', 'random', 'parity', '2023-03-30 08:24:02'),
(1006, '20230330252', 0, 30951, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 08:24:02'),
(1007, '20230330252', 0, 30934, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 08:24:02'),
(1008, '20230330252', 0, 31203, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 08:24:02'),
(1009, '20230330253', 0, 31144, 0, 4, '', 'red', 'random', 'parity', '2023-03-30 08:26:02'),
(1010, '20230330253', 0, 30761, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 08:26:02'),
(1011, '20230330253', 0, 31211, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 08:26:02'),
(1012, '20230330253', 0, 31314, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 08:26:02'),
(1013, '20230330254', 0, 31130, 0, 0, '', 'red++violet', 'random', 'parity', '2023-03-30 08:28:02'),
(1014, '20230330254', 0, 31269, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 08:28:02'),
(1015, '20230330254', 0, 31129, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 08:28:02'),
(1016, '20230330254', 0, 31115, 0, 5, '', 'green++violet', 'random', 'emerd', '2023-03-30 08:28:02'),
(1017, '20230330255', 0, 31477, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 08:30:02'),
(1018, '20230330255', 0, 31640, 0, 0, '', 'red++violet', 'random', 'sapre', '2023-03-30 08:30:02'),
(1019, '20230330255', 0, 31745, 0, 5, '', 'green++violet', 'random', 'bcone', '2023-03-30 08:30:02'),
(1020, '20230330255', 0, 31838, 0, 8, '', 'red', 'random', 'emerd', '2023-03-30 08:30:02'),
(1021, '20230330256', 0, 31763, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 08:32:01'),
(1022, '20230330256', 0, 29691, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 08:32:01'),
(1023, '20230330256', 0, 31695, 0, 5, '', 'green++violet', 'random', 'bcone', '2023-03-30 08:32:01'),
(1024, '20230330256', 0, 31299, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 08:32:01'),
(1025, '20230330257', 0, 31121, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 08:34:01'),
(1026, '20230330257', 0, 31668, 0, 8, '', 'red', 'random', 'sapre', '2023-03-30 08:34:01'),
(1027, '20230330257', 0, 30940, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 08:34:01'),
(1028, '20230330257', 0, 30973, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 08:34:01'),
(1029, '20230330258', 0, 30973, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 08:36:02'),
(1030, '20230330258', 0, 31122, 0, 2, '', 'red', 'random', 'sapre', '2023-03-30 08:36:02'),
(1031, '20230330258', 0, 32087, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 08:36:02'),
(1032, '20230330258', 0, 31457, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 08:36:02'),
(1033, '20230330259', 0, 31794, 0, 4, '', 'red', 'random', 'parity', '2023-03-30 08:38:01'),
(1034, '20230330259', 0, 31086, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 08:38:01'),
(1035, '20230330259', 0, 31466, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 08:38:01'),
(1036, '20230330259', 0, 31481, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 08:38:01'),
(1037, '20230330260', 0, 31476, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 08:40:02'),
(1038, '20230330260', 0, 30967, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 08:40:02'),
(1039, '20230330260', 0, 31269, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 08:40:02'),
(1040, '20230330260', 0, 31709, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 08:40:02'),
(1041, '20230330261', 0, 30834, 0, 4, '', 'red', 'random', 'parity', '2023-03-30 08:42:02'),
(1042, '20230330261', 0, 30844, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 08:42:02'),
(1043, '20230330261', 0, 31377, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 08:42:02'),
(1044, '20230330261', 0, 31181, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 08:42:02'),
(1045, '20230330262', 0, 31388, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 08:44:02'),
(1046, '20230330262', 0, 31367, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 08:44:02'),
(1047, '20230330262', 0, 31130, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 08:44:02'),
(1048, '20230330262', 0, 30761, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 08:44:02'),
(1049, '20230330263', 0, 30789, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 08:46:02'),
(1050, '20230330263', 0, 30853, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 08:46:02'),
(1051, '20230330263', 0, 31419, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 08:46:02'),
(1052, '20230330263', 0, 30891, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 08:46:02'),
(1053, '20230330264', 0, 31419, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 08:48:02'),
(1054, '20230330264', 0, 30812, 0, 2, '', 'red', 'random', 'sapre', '2023-03-30 08:48:02'),
(1055, '20230330264', 0, 31450, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 08:48:02'),
(1056, '20230330264', 0, 31970, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 08:48:02'),
(1057, '20230330265', 0, 31919, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 08:50:02'),
(1058, '20230330265', 0, 31270, 0, 0, '', 'red++violet', 'random', 'sapre', '2023-03-30 08:50:02'),
(1059, '20230330265', 0, 30803, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 08:50:02'),
(1060, '20230330265', 0, 31193, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 08:50:02'),
(1061, '20230330266', 0, 31129, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 08:52:01'),
(1062, '20230330266', 0, 31181, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 08:52:01'),
(1063, '20230330266', 0, 31388, 0, 8, '', 'red', 'random', 'bcone', '2023-03-30 08:52:01'),
(1064, '20230330266', 0, 30774, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 08:52:01'),
(1065, '20230330267', 0, 31235, 0, 5, '', 'green++violet', 'random', 'parity', '2023-03-30 08:54:01'),
(1066, '20230330267', 0, 31567, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 08:54:01'),
(1067, '20230330267', 0, 30800, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 08:54:01'),
(1068, '20230330267', 0, 31708, 0, 8, '', 'red', 'random', 'emerd', '2023-03-30 08:54:01'),
(1069, '20230330268', 0, 30724, 0, 4, '', 'red', 'random', 'parity', '2023-03-30 08:56:01'),
(1070, '20230330268', 0, 30952, 0, 2, '', 'red', 'random', 'sapre', '2023-03-30 08:56:01'),
(1071, '20230330268', 0, 31072, 0, 2, '', 'red', 'random', 'bcone', '2023-03-30 08:56:01'),
(1072, '20230330268', 0, 31568, 0, 8, '', 'red', 'random', 'emerd', '2023-03-30 08:56:01'),
(1073, '20230330269', 0, 31223, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 08:58:02'),
(1074, '20230330269', 0, 31982, 0, 2, '', 'red', 'random', 'sapre', '2023-03-30 08:58:02'),
(1075, '20230330269', 0, 30830, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 08:58:02'),
(1076, '20230330269', 0, 31477, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 08:58:02'),
(1077, '20230330270', 0, 31941, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 09:00:01'),
(1078, '20230330270', 0, 30778, 0, 8, '', 'red', 'random', 'sapre', '2023-03-30 09:00:01'),
(1079, '20230330270', 0, 31254, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 09:00:01'),
(1080, '20230330270', 0, 31633, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 09:00:01'),
(1081, '20230330271', 0, 31041, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 09:02:02'),
(1082, '20230330271', 0, 31251, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 09:02:02'),
(1083, '20230330271', 0, 31556, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 09:02:02'),
(1084, '20230330271', 0, 31169, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 09:02:02'),
(1085, '20230330272', 0, 31587, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 09:04:01'),
(1086, '20230330272', 0, 31633, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 09:04:01'),
(1087, '20230330272', 0, 31616, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 09:04:01'),
(1088, '20230330272', 0, 30774, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 09:04:01');
INSERT INTO `tbl_result` (`id`, `periodid`, `price`, `randomprice`, `result`, `randomresult`, `color`, `randomcolor`, `resulttype`, `tabtype`, `createdate`) VALUES
(1089, '20230330273', 0, 31026, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 09:06:01'),
(1090, '20230330273', 0, 31642, 0, 2, '', 'red', 'random', 'sapre', '2023-03-30 09:06:01'),
(1091, '20230330273', 0, 31540, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 09:06:01'),
(1092, '20230330273', 0, 31921, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 09:06:01'),
(1093, '20230330274', 0, 31499, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 09:08:02'),
(1094, '20230330274', 0, 31863, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 09:08:02'),
(1095, '20230330274', 0, 31129, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 09:08:02'),
(1096, '20230330274', 0, 31235, 0, 5, '', 'green++violet', 'random', 'emerd', '2023-03-30 09:08:02'),
(1097, '20230330275', 0, 31156, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 09:10:02'),
(1098, '20230330275', 0, 30823, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 09:10:02'),
(1099, '20230330275', 0, 31091, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 09:10:02'),
(1100, '20230330275', 0, 31229, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 09:10:02'),
(1101, '20230330276', 0, 31415, 0, 5, '', 'green++violet', 'random', 'parity', '2023-03-30 09:12:01'),
(1102, '20230330276', 0, 31477, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 09:12:01'),
(1103, '20230330276', 0, 31812, 0, 2, '', 'red', 'random', 'bcone', '2023-03-30 09:12:01'),
(1104, '20230330276', 0, 31006, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 09:12:01'),
(1105, '20230330277', 0, 31447, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 09:14:01'),
(1106, '20230330277', 0, 31129, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 09:14:01'),
(1107, '20230330277', 0, 31227, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 09:14:01'),
(1108, '20230330277', 0, 31483, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 09:14:01'),
(1109, '20230330278', 0, 31677, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 09:16:01'),
(1110, '20230330278', 0, 30858, 0, 8, '', 'red', 'random', 'sapre', '2023-03-30 09:16:01'),
(1111, '20230330278', 0, 30859, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 09:16:01'),
(1112, '20230330278', 0, 31575, 0, 5, '', 'green++violet', 'random', 'emerd', '2023-03-30 09:16:01'),
(1113, '20230330279', 0, 31672, 0, 2, '', 'red', 'random', 'parity', '2023-03-30 09:18:02'),
(1114, '20230330279', 0, 31528, 0, 8, '', 'red', 'random', 'sapre', '2023-03-30 09:18:02'),
(1115, '20230330279', 0, 31745, 0, 5, '', 'green++violet', 'random', 'bcone', '2023-03-30 09:18:02'),
(1116, '20230330279', 0, 31957, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 09:18:02'),
(1117, '20230330280', 0, 31233, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 09:20:02'),
(1118, '20230330280', 0, 30881, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 09:20:02'),
(1119, '20230330280', 0, 31499, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 09:20:02'),
(1120, '20230330280', 0, 31707, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 09:20:02'),
(1121, '20230330281', 0, 31398, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 09:22:02'),
(1122, '20230330281', 0, 31419, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 09:22:02'),
(1123, '20230330281', 0, 32008, 0, 8, '', 'red', 'random', 'bcone', '2023-03-30 09:22:02'),
(1124, '20230330281', 0, 31549, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 09:22:02'),
(1125, '20230330282', 0, 31206, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 09:24:01'),
(1126, '20230330282', 0, 31957, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 09:24:01'),
(1127, '20230330282', 0, 31759, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 09:24:01'),
(1128, '20230330282', 0, 31026, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 09:24:01'),
(1129, '20230330283', 0, 31917, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 09:26:02'),
(1130, '20230330283', 0, 31716, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 09:26:02'),
(1131, '20230330283', 0, 31167, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 09:26:02'),
(1132, '20230330283', 0, 30803, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 09:26:02'),
(1133, '20230330284', 0, 31682, 0, 2, '', 'red', 'random', 'parity', '2023-03-30 09:28:02'),
(1134, '20230330284', 0, 31467, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 09:28:02'),
(1135, '20230330284', 0, 31610, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 09:28:02'),
(1136, '20230330284', 0, 31185, 0, 5, '', 'green++violet', 'random', 'emerd', '2023-03-30 09:28:02'),
(1137, '20230330285', 0, 31395, 0, 5, '', 'green++violet', 'random', 'parity', '2023-03-30 09:30:02'),
(1138, '20230330285', 0, 31637, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 09:30:02'),
(1139, '20230330285', 0, 32087, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 09:30:02'),
(1140, '20230330285', 0, 31557, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 09:30:02'),
(1141, '20230330286', 0, 31274, 0, 4, '', 'red', 'random', 'parity', '2023-03-30 09:32:01'),
(1142, '20230330286', 0, 30857, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 09:32:01'),
(1143, '20230330286', 0, 31438, 0, 8, '', 'red', 'random', 'bcone', '2023-03-30 09:32:01'),
(1144, '20230330286', 0, 31183, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 09:32:01'),
(1145, '20230330287', 0, 30931, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 09:34:02'),
(1146, '20230330287', 0, 31216, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 09:34:02'),
(1147, '20230330287', 0, 31557, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 09:34:02'),
(1148, '20230330287', 0, 31277, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 09:34:02'),
(1149, '20230330288', 0, 31270, 0, 0, '', 'red++violet', 'random', 'parity', '2023-03-30 09:36:02'),
(1150, '20230330288', 0, 31561, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 09:36:02'),
(1151, '20230330288', 0, 31557, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 09:36:02'),
(1152, '20230330288', 0, 31506, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 09:36:02'),
(1153, '20230330289', 0, 31713, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 09:38:01'),
(1154, '20230330289', 0, 30840, 0, 0, '', 'red++violet', 'random', 'sapre', '2023-03-30 09:38:01'),
(1155, '20230330289', 0, 31614, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 09:38:01'),
(1156, '20230330289', 0, 31130, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 09:38:01'),
(1157, '20230330290', 0, 31233, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 09:40:01'),
(1158, '20230330290', 0, 31579, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 09:40:01'),
(1159, '20230330290', 0, 31931, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 09:40:01'),
(1160, '20230330290', 0, 31614, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 09:40:01'),
(1161, '20230330291', 0, 31129, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 09:42:02'),
(1162, '20230330291', 0, 30857, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 09:42:02'),
(1163, '20230330291', 0, 31483, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 09:42:02'),
(1164, '20230330291', 0, 31467, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 09:42:02'),
(1165, '20230330292', 0, 31640, 0, 0, '', 'red++violet', 'random', 'parity', '2023-03-30 09:44:02'),
(1166, '20230330292', 0, 31211, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 09:44:02'),
(1167, '20230330292', 0, 31129, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 09:44:02'),
(1168, '20230330292', 0, 31636, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 09:44:02'),
(1169, '20230330293', 0, 31225, 0, 5, '', 'green++violet', 'random', 'parity', '2023-03-30 09:46:01'),
(1170, '20230330293', 0, 31345, 0, 5, '', 'green++violet', 'random', 'sapre', '2023-03-30 09:46:01'),
(1171, '20230330293', 0, 31185, 0, 5, '', 'green++violet', 'random', 'bcone', '2023-03-30 09:46:01'),
(1172, '20230330293', 0, 31284, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 09:46:01'),
(1173, '20230330294', 0, 30803, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 09:48:01'),
(1174, '20230330294', 0, 31395, 0, 5, '', 'green++violet', 'random', 'sapre', '2023-03-30 09:48:01'),
(1175, '20230330294', 0, 30873, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 09:48:01'),
(1176, '20230330294', 0, 31817, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 09:48:01'),
(1177, '20230330295', 0, 31549, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 09:50:02'),
(1178, '20230330295', 0, 31857, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 09:50:02'),
(1179, '20230330295', 0, 31326, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 09:50:02'),
(1180, '20230330295', 0, 30810, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 09:50:02'),
(1181, '20230330296', 0, 31935, 0, 5, '', 'green++violet', 'random', 'parity', '2023-03-30 09:52:02'),
(1182, '20230330296', 0, 31614, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 09:52:02'),
(1183, '20230330296', 0, 30811, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 09:52:02'),
(1184, '20230330296', 0, 31609, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 09:52:02'),
(1185, '20230330297', 0, 30931, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 09:54:02'),
(1186, '20230330297', 0, 31251, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 09:54:02'),
(1187, '20230330297', 0, 31586, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 09:54:02'),
(1188, '20230330297', 0, 30846, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 09:54:02'),
(1189, '20230330298', 0, 31481, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 09:56:02'),
(1190, '20230330298', 0, 31745, 0, 5, '', 'green++violet', 'random', 'sapre', '2023-03-30 09:56:02'),
(1191, '20230330298', 0, 30873, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 09:56:02'),
(1192, '20230330298', 0, 31508, 0, 8, '', 'red', 'random', 'emerd', '2023-03-30 09:56:02'),
(1193, '20230330299', 0, 31004, 0, 4, '', 'red', 'random', 'parity', '2023-03-30 09:58:02'),
(1194, '20230330299', 0, 31600, 0, 0, '', 'red++violet', 'random', 'sapre', '2023-03-30 09:58:02'),
(1195, '20230330299', 0, 30967, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 09:58:02'),
(1196, '20230330299', 0, 30857, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 09:58:02'),
(1197, '20230330300', 0, 31476, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 10:00:03'),
(1198, '20230330300', 0, 31575, 0, 5, '', 'green++violet', 'random', 'sapre', '2023-03-30 10:00:03'),
(1199, '20230330300', 0, 31060, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 10:00:03'),
(1200, '20230330300', 0, 31431, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 10:00:03'),
(1201, '20230330301', 0, 31219, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 10:02:01'),
(1202, '20230330301', 0, 31345, 0, 5, '', 'green++violet', 'random', 'sapre', '2023-03-30 10:02:01'),
(1203, '20230330301', 0, 31586, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 10:02:01'),
(1204, '20230330301', 0, 31633, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 10:02:01'),
(1205, '20230330302', 0, 31026, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 10:04:02'),
(1206, '20230330302', 0, 31360, 0, 0, '', 'red++violet', 'random', 'sapre', '2023-03-30 10:04:02'),
(1207, '20230330302', 0, 31439, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 10:04:02'),
(1208, '20230330302', 0, 31817, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 10:04:02'),
(1209, '20230330303', 0, 31866, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 10:06:02'),
(1210, '20230330303', 0, 31203, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 10:06:02'),
(1211, '20230330303', 0, 31568, 0, 8, '', 'red', 'random', 'bcone', '2023-03-30 10:06:02'),
(1212, '20230330303', 0, 30808, 0, 8, '', 'red', 'random', 'emerd', '2023-03-30 10:06:02'),
(1213, '20230330304', 0, 31708, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 10:08:02'),
(1214, '20230330304', 0, 31614, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 10:08:02'),
(1215, '20230330304', 0, 30873, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 10:08:02'),
(1216, '20230330304', 0, 31891, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 10:08:02'),
(1217, '20230330305', 0, 31489, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 10:10:01'),
(1218, '20230330305', 0, 31604, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 10:10:01'),
(1219, '20230330305', 0, 31251, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 10:10:01'),
(1220, '20230330305', 0, 31440, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 10:10:01'),
(1221, '20230330306', 0, 31676, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 10:12:02'),
(1222, '20230330306', 0, 31685, 0, 5, '', 'green++violet', 'random', 'sapre', '2023-03-30 10:12:02'),
(1223, '20230330306', 0, 31229, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 10:12:02'),
(1224, '20230330306', 0, 31477, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 10:12:02'),
(1225, '20230330307', 0, 31917, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 10:14:02'),
(1226, '20230330307', 0, 31723, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 10:14:02'),
(1227, '20230330307', 0, 31162, 0, 2, '', 'red', 'random', 'bcone', '2023-03-30 10:14:02'),
(1228, '20230330307', 0, 31736, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 10:14:02'),
(1229, '20230330308', 0, 30858, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 10:16:02'),
(1230, '20230330308', 0, 31672, 0, 2, '', 'red', 'random', 'sapre', '2023-03-30 10:16:02'),
(1231, '20230330308', 0, 31699, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 10:16:02'),
(1232, '20230330308', 0, 31800, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 10:16:02'),
(1233, '20230330309', 0, 31060, 0, 0, '', 'red++violet', 'random', 'parity', '2023-03-30 10:18:01'),
(1234, '20230330309', 0, 31173, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 10:18:01'),
(1235, '20230330309', 0, 31587, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 10:18:01'),
(1236, '20230330309', 0, 31677, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 10:18:01'),
(1237, '20230330310', 0, 31489, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 10:20:02'),
(1238, '20230330310', 0, 31530, 0, 0, '', 'red++violet', 'random', 'sapre', '2023-03-30 10:20:02'),
(1239, '20230330310', 0, 31117, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 10:20:02'),
(1240, '20230330310', 0, 31112, 0, 2, '', 'red', 'random', 'emerd', '2023-03-30 10:20:02'),
(1241, '20230330311', 0, 31582, 0, 2, '', 'red', 'random', 'parity', '2023-03-30 10:22:01'),
(1242, '20230330311', 0, 31281, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 10:22:01'),
(1243, '20230330311', 0, 31608, 0, 8, '', 'red', 'random', 'bcone', '2023-03-30 10:22:01'),
(1244, '20230330311', 0, 31555, 0, 5, '', 'green++violet', 'random', 'emerd', '2023-03-30 10:22:01'),
(1245, '20230330312', 0, 31568, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 10:24:01'),
(1246, '20230330312', 0, 31331, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 10:24:01'),
(1247, '20230330312', 0, 31142, 0, 2, '', 'red', 'random', 'bcone', '2023-03-30 10:24:01'),
(1248, '20230330312', 0, 31162, 0, 2, '', 'red', 'random', 'emerd', '2023-03-30 10:24:01'),
(1249, '20230330313', 0, 31326, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 10:26:01'),
(1250, '20230330313', 0, 30789, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 10:26:01'),
(1251, '20230330313', 0, 31514, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 10:26:01'),
(1252, '20230330313', 0, 30967, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 10:26:01'),
(1253, '20230330314', 0, 31208, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 10:28:02'),
(1254, '20230330314', 0, 31724, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 10:28:02'),
(1255, '20230330314', 0, 31193, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 10:28:02'),
(1256, '20230330314', 0, 31414, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 10:28:02'),
(1257, '20230330315', 0, 31431, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 10:30:03'),
(1258, '20230330315', 0, 31575, 0, 5, '', 'green++violet', 'random', 'sapre', '2023-03-30 10:30:03'),
(1259, '20230330315', 0, 31386, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 10:30:03'),
(1260, '20230330315', 0, 31270, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 10:30:03'),
(1261, '20230330316', 0, 31556, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 10:32:01'),
(1262, '20230330316', 0, 30724, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 10:32:01'),
(1263, '20230330316', 0, 31270, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 10:32:01'),
(1264, '20230330316', 0, 31676, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 10:32:01'),
(1265, '20230330317', 0, 31216, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 10:34:02'),
(1266, '20230330317', 0, 31415, 0, 5, '', 'green++violet', 'random', 'sapre', '2023-03-30 10:34:02'),
(1267, '20230330317', 0, 31486, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 10:34:02'),
(1268, '20230330317', 0, 31640, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 10:34:02'),
(1269, '20230330318', 0, 30934, 0, 4, '', 'red', 'random', 'parity', '2023-03-30 10:36:02'),
(1270, '20230330318', 0, 31445, 0, 5, '', 'green++violet', 'random', 'sapre', '2023-03-30 10:36:02'),
(1271, '20230330318', 0, 31121, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 10:36:02'),
(1272, '20230330318', 0, 31123, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 10:36:02'),
(1273, '20230330319', 0, 31211, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 10:38:01'),
(1274, '20230330319', 0, 31171, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 10:38:01'),
(1275, '20230330319', 0, 30857, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 10:38:01'),
(1276, '20230330319', 0, 30836, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 10:38:01'),
(1277, '20230330320', 0, 30782, 0, 2, '', 'red', 'random', 'parity', '2023-03-30 10:40:02'),
(1278, '20230330320', 0, 31112, 0, 2, '', 'red', 'random', 'sapre', '2023-03-30 10:40:02'),
(1279, '20230330320', 0, 31239, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 10:40:02'),
(1280, '20230330320', 0, 31551, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 10:40:02'),
(1281, '20230330321', 0, 31429, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 10:42:02'),
(1282, '20230330321', 0, 31440, 0, 0, '', 'red++violet', 'random', 'sapre', '2023-03-30 10:42:02'),
(1283, '20230330321', 0, 31232, 0, 2, '', 'red', 'random', 'bcone', '2023-03-30 10:42:02'),
(1284, '20230330321', 0, 31424, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 10:42:02'),
(1285, '20230330322', 0, 31398, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 10:44:02'),
(1286, '20230330322', 0, 30795, 0, 5, '', 'green++violet', 'random', 'sapre', '2023-03-30 10:44:02'),
(1287, '20230330322', 0, 30871, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 10:44:02'),
(1288, '20230330322', 0, 31793, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 10:44:02'),
(1289, '20230330323', 0, 30881, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 10:46:02'),
(1290, '20230330323', 0, 31431, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 10:46:02'),
(1291, '20230330323', 0, 31193, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 10:46:02'),
(1292, '20230330323', 0, 31360, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 10:46:02'),
(1293, '20230330324', 0, 31337, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 10:48:02'),
(1294, '20230330324', 0, 31072, 0, 2, '', 'red', 'random', 'sapre', '2023-03-30 10:48:02'),
(1295, '20230330324', 0, 31185, 0, 5, '', 'green++violet', 'random', 'bcone', '2023-03-30 10:48:02'),
(1296, '20230330324', 0, 31817, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 10:48:02'),
(1297, '20230330325', 0, 31970, 0, 0, '', 'red++violet', 'random', 'parity', '2023-03-30 10:50:02'),
(1298, '20230330325', 0, 30774, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 10:50:02'),
(1299, '20230330325', 0, 31611, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 10:50:02'),
(1300, '20230330325', 0, 31024, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 10:50:02'),
(1301, '20230330326', 0, 31398, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 10:52:02'),
(1302, '20230330326', 0, 31589, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 10:52:02'),
(1303, '20230330326', 0, 31574, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 10:52:02'),
(1304, '20230330326', 0, 31554, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 10:52:02'),
(1305, '20230330327', 0, 31142, 0, 2, '', 'red', 'random', 'parity', '2023-03-30 10:54:01'),
(1306, '20230330327', 0, 31281, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 10:54:01'),
(1307, '20230330327', 0, 31979, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 10:54:01'),
(1308, '20230330327', 0, 31116, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 10:54:01'),
(1309, '20230330328', 0, 31972, 0, 2, '', 'red', 'random', 'parity', '2023-03-30 10:56:02'),
(1310, '20230330328', 0, 31157, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 10:56:02'),
(1311, '20230330328', 0, 31567, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 10:56:02'),
(1312, '20230330328', 0, 31409, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 10:56:02'),
(1313, '20230330329', 0, 30702, 0, 2, '', 'red', 'random', 'parity', '2023-03-30 10:58:01'),
(1314, '20230330329', 0, 31556, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 10:58:01'),
(1315, '20230330329', 0, 31337, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 10:58:01'),
(1316, '20230330329', 0, 31131, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 10:58:01'),
(1317, '20230330330', 0, 31577, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 11:00:02'),
(1318, '20230330330', 0, 31312, 0, 2, '', 'red', 'random', 'sapre', '2023-03-30 11:00:02'),
(1319, '20230330330', 0, 31360, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 11:00:02'),
(1320, '20230330330', 0, 31721, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 11:00:02'),
(1321, '20230330331', 0, 31609, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 11:02:01'),
(1322, '20230330331', 0, 30952, 0, 2, '', 'red', 'random', 'sapre', '2023-03-30 11:02:01'),
(1323, '20230330331', 0, 32034, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 11:02:01'),
(1324, '20230330331', 0, 31181, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 11:02:01'),
(1325, '20230330332', 0, 31069, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 11:04:01'),
(1326, '20230330332', 0, 31398, 0, 8, '', 'red', 'random', 'sapre', '2023-03-30 11:04:01'),
(1327, '20230330332', 0, 31793, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 11:04:01'),
(1328, '20230330332', 0, 31429, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 11:04:01'),
(1329, '20230330333', -78200, 31616, 6, 6, 'red', 'RED', 'real', 'parity', '2023-03-30 11:06:01'),
(1330, '20230330333', 0, 30905, 0, 5, '', 'green++violet', 'random', 'sapre', '2023-03-30 11:06:01'),
(1331, '20230330333', 0, 31817, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 11:06:01'),
(1332, '20230330333', 0, 30846, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 11:06:01'),
(1333, '20230330334', 0, 30885, 0, 5, '', 'green++violet', 'random', 'parity', '2023-03-30 11:08:01'),
(1334, '20230330334', 0, 31723, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 11:08:01'),
(1335, '20230330334', 0, 30873, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 11:08:01'),
(1336, '20230330334', 0, 30803, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 11:08:01'),
(1337, '20230330335', 0, 31431, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 11:10:02'),
(1338, '20230330335', 0, 31514, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 11:10:02'),
(1339, '20230330335', 0, 31072, 0, 2, '', 'red', 'random', 'bcone', '2023-03-30 11:10:02'),
(1340, '20230330335', 0, 31770, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 11:10:02'),
(1341, '20230330336', 0, 31386, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 11:12:01'),
(1342, '20230330336', 0, 31424, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 11:12:01'),
(1343, '20230330336', 0, 31388, 0, 8, '', 'red', 'random', 'bcone', '2023-03-30 11:12:01'),
(1344, '20230330336', 0, 30809, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 11:12:01'),
(1345, '20230330337', 0, 31353, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 11:14:02'),
(1346, '20230330337', 0, 31879, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 11:14:02'),
(1347, '20230330337', 0, 31759, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 11:14:02'),
(1348, '20230330337', 0, 31682, 0, 2, '', 'red', 'random', 'emerd', '2023-03-30 11:14:02'),
(1349, '20230330338', 0, 31156, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 11:16:01'),
(1350, '20230330338', 0, 30856, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 11:16:01'),
(1351, '20230330338', 0, 30784, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 11:16:01'),
(1352, '20230330338', 0, 31763, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 11:16:01'),
(1353, '20230330339', 0, 31893, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 11:18:01'),
(1354, '20230330339', 0, 31324, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 11:18:01'),
(1355, '20230330339', 0, 31112, 0, 2, '', 'red', 'random', 'bcone', '2023-03-30 11:18:01'),
(1356, '20230330339', 0, 31644, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 11:18:01'),
(1357, '20230330340', 0, 31553, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 11:20:02'),
(1358, '20230330340', 0, 30845, 0, 5, '', 'green++violet', 'random', 'sapre', '2023-03-30 11:20:02'),
(1359, '20230330340', 0, 31611, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 11:20:02'),
(1360, '20230330340', 0, 31972, 0, 2, '', 'red', 'random', 'emerd', '2023-03-30 11:20:02'),
(1361, '20230330341', 0, 31473, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 11:22:01'),
(1362, '20230330341', 0, 31416, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 11:22:01'),
(1363, '20230330341', 0, 31480, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 11:22:01'),
(1364, '20230330341', 0, 32056, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 11:22:01'),
(1365, '20230330342', 0, 31426, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 11:24:01'),
(1366, '20230330342', 0, 31145, 0, 5, '', 'green++violet', 'random', 'sapre', '2023-03-30 11:24:01'),
(1367, '20230330342', 0, 30754, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 11:24:01'),
(1368, '20230330342', 0, 31910, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 11:24:01'),
(1369, '20230330343', 0, 31188, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 11:26:02'),
(1370, '20230330343', 0, 31838, 0, 8, '', 'red', 'random', 'sapre', '2023-03-30 11:26:02'),
(1371, '20230330343', 0, 31071, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 11:26:02'),
(1372, '20230330343', 0, 30863, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 11:26:02'),
(1373, '20230330344', 0, 31793, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 11:28:02'),
(1374, '20230330344', 0, 31970, 0, 0, '', 'red++violet', 'random', 'sapre', '2023-03-30 11:28:02'),
(1375, '20230330344', 0, 31208, 0, 8, '', 'red', 'random', 'bcone', '2023-03-30 11:28:02'),
(1376, '20230330344', 0, 31223, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 11:28:02'),
(1377, '20230330345', 0, 31283, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 11:30:02'),
(1378, '20230330345', 0, 31467, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 11:30:02'),
(1379, '20230330345', 0, 31571, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 11:30:02'),
(1380, '20230330345', 0, 31793, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 11:30:02'),
(1381, '20230330346', 0, 31931, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 11:32:01'),
(1382, '20230330346', 0, 30952, 0, 2, '', 'red', 'random', 'sapre', '2023-03-30 11:32:01'),
(1383, '20230330346', 0, 31301, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 11:32:01'),
(1384, '20230330346', 0, 31866, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 11:32:01'),
(1385, '20230330347', 0, 31091, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 11:34:02'),
(1386, '20230330347', 0, 31893, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 11:34:02'),
(1387, '20230330347', 0, 31133, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 11:34:02'),
(1388, '20230330347', 0, 30710, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 11:34:02'),
(1389, '20230330348', 0, 31699, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 11:36:01'),
(1390, '20230330348', 0, 30710, 0, 0, '', 'red++violet', 'random', 'sapre', '2023-03-30 11:36:01'),
(1391, '20230330348', 0, 31376, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 11:36:01'),
(1392, '20230330348', 0, 31566, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 11:36:01'),
(1393, '20230330349', 0, 31467, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 11:38:01'),
(1394, '20230330349', 0, 30940, 0, 0, '', 'red++violet', 'random', 'sapre', '2023-03-30 11:38:01'),
(1395, '20230330349', 0, 31467, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 11:38:01'),
(1396, '20230330349', 0, 31487, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 11:38:01'),
(1397, '20230330350', 0, 31644, 0, 4, '', 'red', 'random', 'parity', '2023-03-30 11:40:02'),
(1398, '20230330350', 0, 31897, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 11:40:02'),
(1399, '20230330350', 0, 31429, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 11:40:02'),
(1400, '20230330350', 0, 31223, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 11:40:02'),
(1401, '20230330351', 0, 30830, 0, 0, '', 'red++violet', 'random', 'parity', '2023-03-30 11:42:02'),
(1402, '20230330351', 0, 30830, 0, 0, '', 'red++violet', 'random', 'sapre', '2023-03-30 11:42:02'),
(1403, '20230330351', 0, 31090, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 11:42:02'),
(1404, '20230330351', 0, 31449, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 11:42:02'),
(1405, '20230330352', 0, 30879, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 11:44:02'),
(1406, '20230330352', 0, 30807, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 11:44:02'),
(1407, '20230330352', 0, 31917, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 11:44:02'),
(1408, '20230330352', 0, 31301, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 11:44:02'),
(1409, '20230330353', 0, 31600, 0, 0, '', 'red++violet', 'random', 'parity', '2023-03-30 11:46:01'),
(1410, '20230330353', 0, 31157, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 11:46:01'),
(1411, '20230330353', 0, 31550, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 11:46:01'),
(1412, '20230330353', 0, 31812, 0, 2, '', 'red', 'random', 'emerd', '2023-03-30 11:46:01'),
(1413, '20230330354', 0, 31891, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 11:48:02'),
(1414, '20230330354', 0, 31817, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 11:48:02'),
(1415, '20230330354', 0, 31337, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 11:48:02'),
(1416, '20230330354', 0, 31572, 0, 2, '', 'red', 'random', 'emerd', '2023-03-30 11:48:02'),
(1417, '20230330355', 0, 30873, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 11:50:02'),
(1418, '20230330355', 0, 31897, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 11:50:02'),
(1419, '20230330355', 0, 31013, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 11:50:02'),
(1420, '20230330355', 0, 31575, 0, 5, '', 'green++violet', 'random', 'emerd', '2023-03-30 11:50:02'),
(1421, '20230330356', 0, 31802, 0, 2, '', 'red', 'random', 'parity', '2023-03-30 11:52:01'),
(1422, '20230330356', 0, 31301, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 11:52:01'),
(1423, '20230330356', 0, 31439, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 11:52:01'),
(1424, '20230330356', 0, 31368, 0, 8, '', 'red', 'random', 'emerd', '2023-03-30 11:52:01'),
(1425, '20230330357', 0, 31130, 0, 0, '', 'red++violet', 'random', 'parity', '2023-03-30 11:54:01'),
(1426, '20230330357', 0, 31183, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 11:54:01'),
(1427, '20230330357', 0, 31812, 0, 2, '', 'red', 'random', 'bcone', '2023-03-30 11:54:01'),
(1428, '20230330357', 0, 31498, 0, 8, '', 'red', 'random', 'emerd', '2023-03-30 11:54:01'),
(1429, '20230330358', 0, 31284, 0, 4, '', 'red', 'random', 'parity', '2023-03-30 11:56:01'),
(1430, '20230330358', 0, 30931, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 11:56:01'),
(1431, '20230330358', 0, 31817, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 11:56:01'),
(1432, '20230330358', 0, 31026, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 11:56:01'),
(1433, '20230330359', 0, 31935, 0, 5, '', 'green++violet', 'random', 'parity', '2023-03-30 11:58:01'),
(1434, '20230330359', 0, 31350, 0, 0, '', 'red++violet', 'random', 'sapre', '2023-03-30 11:58:01'),
(1435, '20230330359', 0, 31204, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 11:58:01'),
(1436, '20230330359', 0, 30882, 0, 2, '', 'red', 'random', 'emerd', '2023-03-30 11:58:01'),
(1437, '20230330360', 0, 31185, 0, 5, '', 'green++violet', 'random', 'parity', '2023-03-30 12:00:02'),
(1438, '20230330360', 0, 31676, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 12:00:02'),
(1439, '20230330360', 0, 31204, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 12:00:02'),
(1440, '20230330360', 0, 31123, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 12:00:02'),
(1441, '20230330361', 0, 31935, 0, 5, '', 'green++violet', 'random', 'parity', '2023-03-30 12:02:01'),
(1442, '20230330361', 0, 31185, 0, 5, '', 'green++violet', 'random', 'sapre', '2023-03-30 12:02:01'),
(1443, '20230330361', 0, 31410, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 12:02:01'),
(1444, '20230330361', 0, 31197, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 12:02:01'),
(1445, '20230330362', 0, 30940, 0, 0, '', 'red++violet', 'random', 'parity', '2023-03-30 12:04:02'),
(1446, '20230330362', 0, 30811, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 12:04:02'),
(1447, '20230330362', 0, 31297, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 12:04:02'),
(1448, '20230330362', 0, 31530, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 12:04:02'),
(1449, '20230330363', 0, 31142, 0, 2, '', 'red', 'random', 'parity', '2023-03-30 12:06:02'),
(1450, '20230330363', 0, 31554, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 12:06:02'),
(1451, '20230330363', 0, 31423, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 12:06:02'),
(1452, '20230330363', 0, 30952, 0, 2, '', 'red', 'random', 'emerd', '2023-03-30 12:06:02'),
(1453, '20230330364', 0, 31182, 0, 2, '', 'red', 'random', 'parity', '2023-03-30 12:08:02'),
(1454, '20230330364', 0, 31615, 0, 5, '', 'green++violet', 'random', 'sapre', '2023-03-30 12:08:02'),
(1455, '20230330364', 0, 31360, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 12:08:02'),
(1456, '20230330364', 0, 31108, 0, 8, '', 'red', 'random', 'emerd', '2023-03-30 12:08:02'),
(1457, '20230330365', 0, 31032, 0, 2, '', 'red', 'random', 'parity', '2023-03-30 12:10:02'),
(1458, '20230330365', 0, 31541, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 12:10:02'),
(1459, '20230330365', 0, 30903, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 12:10:02'),
(1460, '20230330365', 0, 31206, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 12:10:02'),
(1461, '20230330366', 0, 32056, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 12:12:02'),
(1462, '20230330366', 0, 31129, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 12:12:02'),
(1463, '20230330366', 0, 31716, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 12:12:02'),
(1464, '20230330366', 0, 31644, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 12:12:02'),
(1465, '20230330367', 0, 30817, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 12:14:02'),
(1466, '20230330367', 0, 31873, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 12:14:02'),
(1467, '20230330367', 0, 30891, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 12:14:02'),
(1468, '20230330367', 0, 30778, 0, 8, '', 'red', 'random', 'emerd', '2023-03-30 12:14:02'),
(1469, '20230330368', 0, 31131, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 12:16:01'),
(1470, '20230330368', 0, 31897, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 12:16:01'),
(1471, '20230330368', 0, 30857, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 12:16:01'),
(1472, '20230330368', 0, 31564, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 12:16:01'),
(1473, '20230330369', 0, 30803, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 12:18:01'),
(1474, '20230330369', 0, 31067, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 12:18:01'),
(1475, '20230330369', 0, 30769, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 12:18:01'),
(1476, '20230330369', 0, 31112, 0, 2, '', 'red', 'random', 'emerd', '2023-03-30 12:18:01'),
(1477, '20230330370', 0, 31345, 0, 5, '', 'green++violet', 'random', 'parity', '2023-03-30 12:20:02'),
(1478, '20230330370', 0, 31176, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 12:20:02'),
(1479, '20230330370', 0, 31614, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 12:20:02'),
(1480, '20230330370', 0, 30873, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 12:20:02'),
(1481, '20230330371', 0, 31629, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 12:22:01'),
(1482, '20230330371', 0, 31551, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 12:22:01'),
(1483, '20230330371', 0, 31478, 0, 8, '', 'red', 'random', 'bcone', '2023-03-30 12:22:01'),
(1484, '20230330371', 0, 31608, 0, 8, '', 'red', 'random', 'emerd', '2023-03-30 12:22:01'),
(1485, '20230330372', 0, 31866, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 12:24:01'),
(1486, '20230330372', 0, 31394, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 12:24:01'),
(1487, '20230330372', 0, 30940, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 12:24:01'),
(1488, '20230330372', 0, 31477, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 12:24:01'),
(1489, '20230330373', 0, 31873, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 12:26:02'),
(1490, '20230330373', 0, 31927, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 12:26:02'),
(1491, '20230330373', 0, 31067, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 12:26:02'),
(1492, '20230330373', 0, 31144, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 12:26:02'),
(1493, '20230330374', 0, 31347, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 12:28:01'),
(1494, '20230330374', 0, 31261, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 12:28:01'),
(1495, '20230330374', 0, 31483, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 12:28:01'),
(1496, '20230330374', 0, 31647, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 12:28:01'),
(1497, '20230330375', 0, 31736, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 12:30:02'),
(1498, '20230330375', 0, 31970, 0, 0, '', 'red++violet', 'random', 'sapre', '2023-03-30 12:30:02'),
(1499, '20230330375', 0, 31067, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 12:30:02'),
(1500, '20230330375', 0, 30754, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 12:30:02'),
(1501, '20230330376', 0, 31644, 0, 4, '', 'red', 'random', 'parity', '2023-03-30 12:32:01'),
(1502, '20230330376', 0, 31470, 0, 0, '', 'red++violet', 'random', 'sapre', '2023-03-30 12:32:01'),
(1503, '20230330376', 0, 31026, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 12:32:01'),
(1504, '20230330376', 0, 31312, 0, 2, '', 'red', 'random', 'emerd', '2023-03-30 12:32:01'),
(1505, '20230330377', 0, 31657, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 12:34:01'),
(1506, '20230330377', 0, 31564, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 12:34:01'),
(1507, '20230330377', 0, 31449, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 12:34:01'),
(1508, '20230330377', 0, 31685, 0, 5, '', 'green++violet', 'random', 'emerd', '2023-03-30 12:34:01'),
(1509, '20230330378', 0, 31499, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 12:36:02'),
(1510, '20230330378', 0, 30844, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 12:36:02'),
(1511, '20230330378', 0, 31609, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 12:36:02'),
(1512, '20230330378', 0, 30903, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 12:36:02'),
(1513, '20230330379', 0, 31759, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 12:38:02'),
(1514, '20230330379', 0, 31685, 0, 5, '', 'green++violet', 'random', 'sapre', '2023-03-30 12:38:02'),
(1515, '20230330379', 0, 31277, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 12:38:02'),
(1516, '20230330379', 0, 30858, 0, 8, '', 'red', 'random', 'emerd', '2023-03-30 12:38:02'),
(1517, '20230330380', 0, 31508, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 12:40:02'),
(1518, '20230330380', 0, 31551, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 12:40:02'),
(1519, '20230330380', 0, 31156, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 12:40:02'),
(1520, '20230330380', 0, 31458, 0, 8, '', 'red', 'random', 'emerd', '2023-03-30 12:40:02'),
(1521, '20230330381', 0, 31630, 0, 0, '', 'red++violet', 'random', 'parity', '2023-03-30 12:42:01'),
(1522, '20230330381', 0, 31344, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 12:42:01'),
(1523, '20230330381', 0, 30858, 0, 8, '', 'red', 'random', 'bcone', '2023-03-30 12:42:01'),
(1524, '20230330381', 0, 31684, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 12:42:01'),
(1525, '20230330382', 0, 31567, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 12:44:01'),
(1526, '20230330382', 0, 31506, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 12:44:01'),
(1527, '20230330382', 0, 31724, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 12:44:01'),
(1528, '20230330382', 0, 31676, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 12:44:01'),
(1529, '20230330383', 0, 31893, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 12:46:02'),
(1530, '20230330383', 0, 31863, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 12:46:02'),
(1531, '20230330383', 0, 31116, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 12:46:02'),
(1532, '20230330383', 0, 31770, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 12:46:02'),
(1533, '20230330384', 0, 30803, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 12:48:02'),
(1534, '20230330384', 0, 31483, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 12:48:02'),
(1535, '20230330384', 0, 31745, 0, 5, '', 'green++violet', 'random', 'bcone', '2023-03-30 12:48:02'),
(1536, '20230330384', 0, 31640, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 12:48:02'),
(1537, '20230330385', 0, 31482, 0, 2, '', 'red', 'random', 'parity', '2023-03-30 12:50:01'),
(1538, '20230330385', 0, 30922, 0, 2, '', 'red', 'random', 'sapre', '2023-03-30 12:50:01'),
(1539, '20230330385', 0, 31680, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 12:50:01'),
(1540, '20230330385', 0, 31721, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 12:50:01'),
(1541, '20230330386', 0, 31577, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 12:52:02'),
(1542, '20230330386', 0, 31072, 0, 2, '', 'red', 'random', 'sapre', '2023-03-30 12:52:02'),
(1543, '20230330386', 0, 31935, 0, 5, '', 'green++violet', 'random', 'bcone', '2023-03-30 12:52:02'),
(1544, '20230330386', 0, 31480, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 12:52:02'),
(1545, '20230330387', 0, 31157, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 12:54:02'),
(1546, '20230330387', 0, 30792, 0, 2, '', 'red', 'random', 'sapre', '2023-03-30 12:54:02'),
(1547, '20230330387', 0, 30859, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 12:54:02'),
(1548, '20230330387', 0, 31586, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 12:54:02'),
(1549, '20230330388', 0, 31429, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 12:56:02'),
(1550, '20230330388', 0, 31360, 0, 0, '', 'red++violet', 'random', 'sapre', '2023-03-30 12:56:02'),
(1551, '20230330388', 0, 31883, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 12:56:02'),
(1552, '20230330388', 0, 30905, 0, 5, '', 'green++violet', 'random', 'emerd', '2023-03-30 12:56:02'),
(1553, '20230330389', 0, 31467, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 12:58:02'),
(1554, '20230330389', 0, 31337, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 12:58:02'),
(1555, '20230330389', 0, 31821, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 12:58:02'),
(1556, '20230330389', 0, 31290, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 12:58:02'),
(1557, '20230330390', 0, 31129, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 13:00:02'),
(1558, '20230330390', 0, 31633, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 13:00:02'),
(1559, '20230330390', 0, 31214, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 13:00:02'),
(1560, '20230330390', 0, 31793, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 13:00:02'),
(1561, '20230330391', 0, 30905, 0, 5, '', 'green++violet', 'random', 'parity', '2023-03-30 13:02:02'),
(1562, '20230330391', 0, 31609, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 13:02:02'),
(1563, '20230330391', 0, 31467, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 13:02:02'),
(1564, '20230330391', 0, 31695, 0, 5, '', 'green++violet', 'random', 'emerd', '2023-03-30 13:02:02'),
(1565, '20230330392', 0, 31013, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 13:04:01'),
(1566, '20230330392', 0, 31536, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 13:04:01'),
(1567, '20230330392', 0, 31982, 0, 2, '', 'red', 'random', 'bcone', '2023-03-30 13:04:01'),
(1568, '20230330392', 0, 31041, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 13:04:01'),
(1569, '20230330393', 0, 31754, 0, 4, '', 'red', 'random', 'parity', '2023-03-30 13:06:01'),
(1570, '20230330393', 0, 30863, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 13:06:01'),
(1571, '20230330393', 0, 30706, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 13:06:01'),
(1572, '20230330393', 0, 31024, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 13:06:01'),
(1573, '20230330394', 0, 31164, 0, 4, '', 'red', 'random', 'parity', '2023-03-30 13:08:02'),
(1574, '20230330394', 0, 30808, 0, 8, '', 'red', 'random', 'sapre', '2023-03-30 13:08:02'),
(1575, '20230330394', 0, 31489, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 13:08:02'),
(1576, '20230330394', 0, 31546, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 13:08:02'),
(1577, '20230330395', 0, 31467, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 13:10:01'),
(1578, '20230330395', 0, 31156, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 13:10:01'),
(1579, '20230330395', 0, 31262, 0, 2, '', 'red', 'random', 'bcone', '2023-03-30 13:10:01'),
(1580, '20230330395', 0, 30706, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 13:10:01'),
(1581, '20230330396', 0, 31769, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 13:12:01'),
(1582, '20230330396', 0, 30785, 0, 5, '', 'green++violet', 'random', 'sapre', '2023-03-30 13:12:01'),
(1583, '20230330396', 0, 31004, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 13:12:01'),
(1584, '20230330396', 0, 31277, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 13:12:01'),
(1585, '20230330397', 0, 30844, 0, 4, '', 'red', 'random', 'parity', '2023-03-30 13:14:01'),
(1586, '20230330397', 0, 31821, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 13:14:01'),
(1587, '20230330397', 0, 31610, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 13:14:01'),
(1588, '20230330397', 0, 30937, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 13:14:01'),
(1589, '20230330398', 0, 31608, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 13:16:02'),
(1590, '20230330398', 0, 30885, 0, 5, '', 'green++violet', 'random', 'sapre', '2023-03-30 13:16:02'),
(1591, '20230330398', 0, 31646, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 13:16:02'),
(1592, '20230330398', 0, 31817, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 13:16:02'),
(1593, '20230330399', 0, 31299, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 13:18:01'),
(1594, '20230330399', 0, 31543, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 13:18:01'),
(1595, '20230330399', 0, 31571, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 13:18:01'),
(1596, '20230330399', 0, 31424, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 13:18:01'),
(1597, '20230330400', 0, 31299, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 13:20:02'),
(1598, '20230330400', 0, 31060, 0, 0, '', 'red++violet', 'random', 'sapre', '2023-03-30 13:20:02'),
(1599, '20230330400', 0, 31415, 0, 5, '', 'green++violet', 'random', 'bcone', '2023-03-30 13:20:02'),
(1600, '20230330400', 0, 32053, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 13:20:02'),
(1601, '20230330401', 0, 31301, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 13:22:01'),
(1602, '20230330401', 0, 31571, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 13:22:01'),
(1603, '20230330401', 0, 31467, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 13:22:01'),
(1604, '20230330401', 0, 31069, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 13:22:01'),
(1605, '20230330402', 0, 31353, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 13:24:02'),
(1606, '20230330402', 0, 31367, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 13:24:02'),
(1607, '20230330402', 0, 31636, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 13:24:02'),
(1608, '20230330402', 0, 30919, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 13:24:02'),
(1609, '20230330403', 0, 31188, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 13:26:01'),
(1610, '20230330403', 0, 31721, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 13:26:01'),
(1611, '20230330403', 0, 31423, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 13:26:01'),
(1612, '20230330403', 0, 31962, 0, 2, '', 'red', 'random', 'emerd', '2023-03-30 13:26:01'),
(1613, '20230330404', 0, 31642, 0, 2, '', 'red', 'random', 'parity', '2023-03-30 13:28:02'),
(1614, '20230330404', 0, 31398, 0, 8, '', 'red', 'random', 'sapre', '2023-03-30 13:28:02'),
(1615, '20230330404', 0, 31682, 0, 2, '', 'red', 'random', 'bcone', '2023-03-30 13:28:02'),
(1616, '20230330404', 0, 31679, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 13:28:02'),
(1617, '20230330405', 0, 30952, 0, 2, '', 'red', 'random', 'parity', '2023-03-30 13:30:03'),
(1618, '20230330405', 0, 31156, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 13:30:03'),
(1619, '20230330405', 0, 31254, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 13:30:03'),
(1620, '20230330405', 0, 31270, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 13:30:03'),
(1621, '20230330406', 0, 31644, 0, 4, '', 'red', 'random', 'parity', '2023-03-30 13:32:01'),
(1622, '20230330406', 0, 31473, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 13:32:01'),
(1623, '20230330406', 0, 30859, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 13:32:01'),
(1624, '20230330406', 0, 31105, 0, 5, '', 'green++violet', 'random', 'emerd', '2023-03-30 13:32:01'),
(1625, '20230330407', 0, 31582, 0, 2, '', 'red', 'random', 'parity', '2023-03-30 13:34:02');
INSERT INTO `tbl_result` (`id`, `periodid`, `price`, `randomprice`, `result`, `randomresult`, `color`, `randomcolor`, `resulttype`, `tabtype`, `createdate`) VALUES
(1626, '20230330407', 0, 31701, 0, 1, '', 'green', 'random', 'sapre', '2023-03-30 13:34:02'),
(1627, '20230330407', 0, 30802, 0, 2, '', 'red', 'random', 'bcone', '2023-03-30 13:34:02'),
(1628, '20230330407', 0, 31770, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 13:34:02'),
(1629, '20230330408', 0, 31458, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 13:36:01'),
(1630, '20230330408', 0, 31277, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 13:36:01'),
(1631, '20230330408', 0, 31175, 0, 5, '', 'green++violet', 'random', 'bcone', '2023-03-30 13:36:01'),
(1632, '20230330408', 0, 31478, 0, 8, '', 'red', 'random', 'emerd', '2023-03-30 13:36:01'),
(1633, '20230330409', 0, 30702, 0, 2, '', 'red', 'random', 'parity', '2023-03-30 13:38:01'),
(1634, '20230330409', 0, 30800, 0, 0, '', 'red++violet', 'random', 'sapre', '2023-03-30 13:38:01'),
(1635, '20230330409', 0, 31419, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 13:38:01'),
(1636, '20230330409', 0, 31086, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 13:38:01'),
(1637, '20230330410', 0, 31112, 0, 2, '', 'red', 'random', 'parity', '2023-03-30 13:40:02'),
(1638, '20230330410', 0, 31466, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 13:40:02'),
(1639, '20230330410', 0, 31657, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 13:40:02'),
(1640, '20230330410', 0, 31713, 0, 3, '', 'green', 'random', 'emerd', '2023-03-30 13:40:02'),
(1641, '20230330411', 0, 30856, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 13:42:01'),
(1642, '20230330411', 0, 31636, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 13:42:01'),
(1643, '20230330411', 0, 31229, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 13:42:01'),
(1644, '20230330411', 0, 31067, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 13:42:01'),
(1645, '20230330412', 0, 31414, 0, 4, '', 'red', 'random', 'parity', '2023-03-30 13:44:01'),
(1646, '20230330412', 0, 31679, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 13:44:01'),
(1647, '20230330412', 0, 31183, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 13:44:01'),
(1648, '20230330412', 0, 31185, 0, 5, '', 'green++violet', 'random', 'emerd', '2023-03-30 13:44:01'),
(1649, '20230330413', 0, 31532, 0, 2, '', 'red', 'random', 'parity', '2023-03-30 13:46:02'),
(1650, '20230330413', 0, 30863, 0, 3, '', 'green', 'random', 'sapre', '2023-03-30 13:46:02'),
(1651, '20230330413', 0, 30774, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 13:46:02'),
(1652, '20230330413', 0, 31568, 0, 8, '', 'red', 'random', 'emerd', '2023-03-30 13:46:02'),
(1653, '20230330414', 0, 31229, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 13:48:01'),
(1654, '20230330414', 0, 31857, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 13:48:01'),
(1655, '20230330414', 0, 31274, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 13:48:01'),
(1656, '20230330414', 0, 30706, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 13:48:01'),
(1657, '20230330415', 0, 31530, 0, 0, '', 'red++violet', 'random', 'parity', '2023-03-30 13:50:02'),
(1658, '20230330415', 0, 31379, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 13:50:02'),
(1659, '20230330415', 0, 31417, 0, 7, '', 'green', 'random', 'bcone', '2023-03-30 13:50:02'),
(1660, '20230330415', 0, 31704, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 13:50:02'),
(1661, '20230330416', 0, 31863, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 13:52:02'),
(1662, '20230330416', 0, 31568, 0, 8, '', 'red', 'random', 'sapre', '2023-03-30 13:52:02'),
(1663, '20230330416', 0, 31614, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 13:52:02'),
(1664, '20230330416', 0, 30919, 0, 9, '', 'green', 'random', 'emerd', '2023-03-30 13:52:02'),
(1665, '20230330417', 0, 31575, 0, 5, '', 'green++violet', 'random', 'parity', '2023-03-30 13:54:02'),
(1666, '20230330417', 0, 30840, 0, 0, '', 'red++violet', 'random', 'sapre', '2023-03-30 13:54:02'),
(1667, '20230330417', 0, 31219, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 13:54:02'),
(1668, '20230330417', 0, 31071, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 13:54:02'),
(1669, '20230330418', 0, 31427, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 13:56:01'),
(1670, '20230330418', 0, 30919, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 13:56:01'),
(1671, '20230330418', 0, 31284, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 13:56:01'),
(1672, '20230330418', 0, 31630, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 13:56:01'),
(1673, '20230330419', 0, 31736, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 13:58:01'),
(1674, '20230330419', 0, 31897, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 13:58:01'),
(1675, '20230330419', 0, 31931, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 13:58:01'),
(1676, '20230330419', 0, 30840, 0, 0, '', 'red++violet', 'random', 'emerd', '2023-03-30 13:58:01'),
(1677, '20230330420', 0, 31239, 0, 9, '', 'green', 'random', 'parity', '2023-03-30 14:00:02'),
(1678, '20230330420', 0, 31757, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 14:00:02'),
(1679, '20230330420', 0, 31299, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 14:00:02'),
(1680, '20230330420', 0, 31766, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 14:00:02'),
(1681, '20230330421', 0, 31277, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 14:02:01'),
(1682, '20230330421', 0, 31162, 0, 2, '', 'red', 'random', 'sapre', '2023-03-30 14:02:01'),
(1683, '20230330421', 0, 31982, 0, 2, '', 'red', 'random', 'bcone', '2023-03-30 14:02:01'),
(1684, '20230330421', 0, 31431, 0, 1, '', 'green', 'random', 'emerd', '2023-03-30 14:02:01'),
(1685, '20230330422', 0, 31640, 0, 0, '', 'red++violet', 'random', 'parity', '2023-03-30 14:04:01'),
(1686, '20230330422', 0, 30937, 0, 7, '', 'green', 'random', 'sapre', '2023-03-30 14:04:01'),
(1687, '20230330422', 0, 31169, 0, 9, '', 'green', 'random', 'bcone', '2023-03-30 14:04:01'),
(1688, '20230330422', 0, 31684, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 14:04:01'),
(1689, '20230330423', 0, 30951, 0, 1, '', 'green', 'random', 'parity', '2023-03-30 14:06:01'),
(1690, '20230330423', 0, 31229, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 14:06:01'),
(1691, '20230330423', 0, 31293, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 14:06:01'),
(1692, '20230330423', 0, 31644, 0, 4, '', 'red', 'random', 'emerd', '2023-03-30 14:06:01'),
(1693, '20230330424', 0, 31163, 0, 3, '', 'green', 'random', 'parity', '2023-03-30 14:08:02'),
(1694, '20230330424', 0, 31280, 0, 0, '', 'red++violet', 'random', 'sapre', '2023-03-30 14:08:02'),
(1695, '20230330424', 0, 31470, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 14:08:02'),
(1696, '20230330424', 0, 31575, 0, 5, '', 'green++violet', 'random', 'emerd', '2023-03-30 14:08:02'),
(1697, '20230330425', 0, 31636, 0, 6, '', 'red', 'random', 'parity', '2023-03-30 14:10:02'),
(1698, '20230330425', 0, 30724, 0, 4, '', 'red', 'random', 'sapre', '2023-03-30 14:10:02'),
(1699, '20230330425', 0, 31766, 0, 6, '', 'red', 'random', 'bcone', '2023-03-30 14:10:02'),
(1700, '20230330425', 0, 31567, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 14:10:02'),
(1701, '20230330426', 0, 31188, 0, 8, '', 'red', 'random', 'parity', '2023-03-30 14:12:01'),
(1702, '20230330426', 0, 31395, 0, 5, '', 'green++violet', 'random', 'sapre', '2023-03-30 14:12:01'),
(1703, '20230330426', 0, 31680, 0, 0, '', 'red++violet', 'random', 'bcone', '2023-03-30 14:12:01'),
(1704, '20230330426', 0, 31086, 0, 6, '', 'red', 'random', 'emerd', '2023-03-30 14:12:01'),
(1705, '20230330427', 0, 31410, 0, 0, '', 'red++violet', 'random', 'parity', '2023-03-30 14:14:01'),
(1706, '20230330427', 0, 31109, 0, 9, '', 'green', 'random', 'sapre', '2023-03-30 14:14:01'),
(1707, '20230330427', 0, 31394, 0, 4, '', 'red', 'random', 'bcone', '2023-03-30 14:14:01'),
(1708, '20230330427', 0, 31137, 0, 7, '', 'green', 'random', 'emerd', '2023-03-30 14:14:01'),
(1709, '20230330428', 0, 31477, 0, 7, '', 'green', 'random', 'parity', '2023-03-30 14:16:01'),
(1710, '20230330428', 0, 31176, 0, 6, '', 'red', 'random', 'sapre', '2023-03-30 14:16:01'),
(1711, '20230330428', 0, 31133, 0, 3, '', 'green', 'random', 'bcone', '2023-03-30 14:16:01'),
(1712, '20230330428', 0, 31638, 0, 8, '', 'red', 'random', 'emerd', '2023-03-30 14:16:01'),
(1713, '20230330429', 0, 31194, 0, 4, '', 'red', 'random', 'parity', '2023-03-30 14:18:02'),
(1714, '20230330429', 0, 30812, 0, 2, '', 'red', 'random', 'sapre', '2023-03-30 14:18:02'),
(1715, '20230330429', 0, 30951, 0, 1, '', 'green', 'random', 'bcone', '2023-03-30 14:18:02'),
(1716, '20230330429', 0, 30845, 0, 5, '', 'green++violet', 'random', 'emerd', '2023-03-30 14:18:02');

-- --------------------------------------------------------

--
-- Table structure for table `tbl_reward`
--

CREATE TABLE `tbl_reward` (
  `id` int(11) NOT NULL,
  `userid` int(11) NOT NULL,
  `amount` float NOT NULL,
  `createdate` timestamp NOT NULL DEFAULT current_timestamp()
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

--
-- Dumping data for table `tbl_reward`
--

INSERT INTO `tbl_reward` (`id`, `userid`, `amount`, `createdate`) VALUES
(4, 4, 100000, '2022-01-06 16:50:12'),
(5, 8, 110, '2022-01-16 05:18:18'),
(6, 4, 100, '2022-01-16 05:31:28'),
(7, 8, 121, '2022-01-16 06:56:41'),
(8, 121, 121, '2022-01-16 14:09:10'),
(9, 8, 121, '2022-01-17 11:36:52'),
(10, 8, 121, '2022-01-18 08:30:33'),
(11, 87, 530, '2022-01-18 17:35:50'),
(12, 191, 330, '2022-01-19 05:36:21'),
(13, 148, 330, '2022-01-19 05:44:30'),
(14, 46, 121, '2022-01-19 06:41:21'),
(15, 4, 5000, '2022-01-19 06:41:44'),
(16, 114, 121, '2022-01-19 07:02:35'),
(17, 195, 330, '2022-01-19 08:00:52'),
(18, 193, 330, '2022-01-19 08:17:05'),
(19, 191, 121, '2022-01-19 08:18:45'),
(20, 46, 121, '2022-01-19 08:22:15'),
(21, 8, 150, '2022-01-19 16:46:55'),
(22, 106, 100, '2022-01-19 17:21:04'),
(23, 81, 500, '2022-01-20 05:00:48'),
(24, 186, 1100, '2022-01-20 07:00:44'),
(25, 167, 121, '2022-01-20 07:03:09'),
(26, 114, 330, '2022-01-20 10:33:06'),
(27, 81, 5000, '2022-01-20 15:48:10'),
(28, 4, 50000, '2022-01-21 09:54:17'),
(29, 74, 2000, '2022-01-22 04:25:50'),
(30, 229, 2000, '2022-01-22 05:54:45'),
(31, 114, 40, '2022-01-22 07:12:18'),
(32, 74, 100, '2022-01-22 07:20:31'),
(33, 8, 20, '2022-01-22 08:12:44'),
(34, 46, 100, '2022-01-22 09:03:43'),
(35, 193, 120, '2022-01-22 09:15:01'),
(36, 186, 1500, '2022-01-22 10:58:11'),
(37, 234, 330, '2022-01-22 14:32:32'),
(38, 74, 12900, '2022-01-22 14:35:05'),
(39, 74, 4, '2022-01-22 14:36:13'),
(40, 74, 4000, '2022-01-22 14:36:38'),
(41, 74, 1000, '2022-01-22 14:38:28'),
(42, 96, 6000, '2022-01-22 15:29:05'),
(43, 81, 11000, '2022-01-23 05:37:17'),
(44, 52, 121, '2022-01-23 06:52:37'),
(45, 240, 330, '2022-01-23 06:56:42'),
(46, 234, 121, '2022-01-23 07:02:46'),
(47, 246, 330, '2022-01-23 09:44:37'),
(48, 234, 121, '2022-01-23 09:47:16'),
(49, 245, 330, '2022-01-23 11:20:35'),
(50, 193, 121, '2022-01-23 11:23:38'),
(51, 247, 330, '2022-01-23 11:30:20'),
(52, 245, 121, '2022-01-23 11:31:49'),
(53, 204, 550, '2022-01-23 12:04:50'),
(54, 81, 121, '2022-01-23 12:06:20'),
(55, 74, 3500, '2022-01-23 13:06:50'),
(56, 245, 300, '2022-01-24 04:46:13'),
(57, 247, 330, '2022-01-24 04:54:47'),
(58, 220, 1100, '2022-01-24 13:07:39'),
(59, 203, 121, '2022-01-24 13:08:58'),
(60, 250, 500, '2022-01-24 16:20:49'),
(61, 250, 500, '2022-01-25 05:17:37'),
(62, 265, 200, '2022-01-25 19:10:35'),
(63, 272, 330, '2022-01-26 11:53:03'),
(64, 74, 121, '2022-01-26 11:54:15'),
(65, 96, 20000, '2022-01-26 13:52:30'),
(66, 96, 10000, '2022-01-26 13:52:45'),
(67, 295, 1000, '2022-01-27 04:51:39'),
(68, 265, 121, '2022-01-27 04:52:40'),
(69, 300, 30, '2022-01-27 09:10:09'),
(70, 8, 121, '2022-01-27 17:03:47'),
(71, 265, 340, '2022-01-27 17:34:22'),
(72, 293, 121, '2022-01-28 05:52:15'),
(73, 186, 1000, '2022-01-28 09:50:51'),
(74, 327, 330, '2022-01-28 15:53:08'),
(75, 8, 121, '2022-01-29 09:17:37'),
(76, 347, 121, '2022-01-30 03:39:21'),
(77, 348, 100, '2022-01-30 04:25:58'),
(78, 347, 121, '2022-01-30 04:28:08'),
(79, 347, 121, '2022-01-30 04:28:18'),
(80, 8, 121, '2022-01-30 16:48:12'),
(81, 329, 500, '2022-01-31 05:35:11'),
(82, 329, 50, '2022-01-31 05:37:07'),
(83, 252, 50, '2022-01-31 11:15:45'),
(84, 8, 121, '2022-01-31 11:16:43'),
(85, 8, 121, '2022-01-31 14:15:36'),
(86, 8, 121, '2022-02-02 05:46:29'),
(87, 258, 50, '2022-02-02 07:38:16'),
(88, 8, 121, '2022-02-02 07:41:21'),
(89, 542, 100, '2022-02-03 09:33:43'),
(90, 8, 121, '2022-02-03 09:36:34'),
(91, 96, 14000, '2022-02-03 17:42:47'),
(92, 96, 500, '2022-02-03 17:53:41'),
(93, 730, 310, '2022-02-04 06:29:24'),
(94, 499, 30, '2022-02-04 07:42:46'),
(95, 382, 121, '2022-02-04 07:43:41'),
(96, 330, 30, '2022-02-04 08:04:03'),
(97, 395, 30, '2022-02-04 10:59:56'),
(98, 369, 121, '2022-02-04 11:00:57'),
(99, 742, 50, '2022-02-04 16:32:10'),
(100, 358, 121, '2022-02-04 16:33:11'),
(101, 746, 50, '2022-02-05 05:55:25'),
(102, 351, 121, '2022-02-05 05:56:31'),
(103, 4, 500000, '2022-02-05 17:46:29'),
(104, 761, 30, '2022-02-07 04:27:14'),
(105, 759, 121, '2022-02-07 05:10:57'),
(106, 358, 100, '2022-02-08 05:18:26'),
(107, 352, 121, '2022-02-08 05:20:18'),
(108, 8, 3200, '2022-02-08 05:56:12'),
(109, 8, 1100, '2022-02-08 06:08:39'),
(110, 787, 30, '2022-02-08 06:36:15'),
(111, 4, 121, '2022-02-08 06:37:07'),
(112, 5, 121, '2022-02-08 09:18:53'),
(113, 716, 30, '2022-02-08 09:19:58'),
(114, 786, 30, '2022-02-09 17:57:51'),
(115, 223, 100, '2022-02-11 12:36:15'),
(116, 223, 1000, '2022-02-11 12:49:53'),
(117, 807, 50, '2022-02-12 04:38:46'),
(118, 5, 121, '2022-02-12 06:10:19'),
(119, 8, 121, '2022-02-13 04:46:33'),
(120, 824, 200, '2022-02-26 05:18:54'),
(121, 5, 121, '2022-02-26 05:20:19'),
(122, 1, 2000, '2023-03-29 12:32:17'),
(123, 1, 20000000000, '2023-03-29 12:32:37');

-- --------------------------------------------------------

--
-- Table structure for table `tbl_tempwinner`
--

CREATE TABLE `tbl_tempwinner` (
  `id` int(11) NOT NULL,
  `periodid` varchar(300) NOT NULL,
  `number` int(11) NOT NULL,
  `color` varchar(100) NOT NULL,
  `total` float NOT NULL,
  `type` varchar(50) NOT NULL
) ENGINE=MyISAM DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

-- --------------------------------------------------------

--
-- Table structure for table `tbl_test`
--

CREATE TABLE `tbl_test` (
  `id` int(11) NOT NULL,
  `test` varchar(200) NOT NULL,
  `date` timestamp NOT NULL DEFAULT current_timestamp()
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

-- --------------------------------------------------------

--
-- Table structure for table `tbl_user`
--

CREATE TABLE `tbl_user` (
  `id` int(11) NOT NULL,
  `mobile` varchar(500) NOT NULL,
  `email` varchar(500) NOT NULL,
  `password` varchar(300) NOT NULL,
  `code` varchar(255) NOT NULL,
  `owncode` varchar(255) NOT NULL,
  `privacy` varchar(50) NOT NULL,
  `status` smallint(11) NOT NULL,
  `createdate` timestamp NOT NULL DEFAULT current_timestamp()
) ENGINE=MyISAM DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

--
-- Dumping data for table `tbl_user`
--

INSERT INTO `tbl_user` (`id`, `mobile`, `email`, `password`, `code`, `owncode`, `privacy`, `status`, `createdate`) VALUES
(1, '9530120053', 'asdfghjkl45@gmail.com', 'c6cab344b76165138cb0a40f5529796f', '83723777', '83858738', 'on', 1, '2023-03-28 06:07:13'),
(2, '6378746367', 'rabifjkugdc@gmail.com', 'de204bfa510238af713fb5d185e4f36c', '83858738', '83858739', 'on', 1, '2023-03-29 10:02:04');

-- --------------------------------------------------------

--
-- Table structure for table `tbl_userresult`
--

CREATE TABLE `tbl_userresult` (
  `id` int(11) NOT NULL,
  `userid` int(11) NOT NULL,
  `periodid` varchar(300) NOT NULL,
  `type` varchar(100) NOT NULL,
  `value` varchar(100) NOT NULL,
  `amount` float NOT NULL,
  `openprice` float NOT NULL,
  `tab` varchar(50) NOT NULL,
  `paidamount` float NOT NULL,
  `fee` float NOT NULL,
  `status` varchar(50) NOT NULL,
  `createdate` datetime NOT NULL
) ENGINE=MyISAM DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

--
-- Dumping data for table `tbl_userresult`
--

INSERT INTO `tbl_userresult` (`id`, `userid`, `periodid`, `type`, `value`, `amount`, `openprice`, `tab`, `paidamount`, `fee`, `status`, `createdate`) VALUES
(1, 1, '20230329540', 'button', 'Green', 10, 31368, 'parity', 19.6, 0.2, 'success', '2023-03-29 18:00:03'),
(2, 1, '20230329540', 'button', 'Red', 10, 31368, 'parity', 9.8, 0.2, 'fail', '2023-03-29 18:00:03'),
(3, 1, '20230329540', 'button', '0', 10, 31368, 'parity', 9.8, 0.2, 'fail', '2023-03-29 18:00:03'),
(4, 1, '20230329540', 'button', '1', 10, 31368, 'parity', 88.2, 0.2, 'success', '2023-03-29 18:00:03'),
(5, 1, '20230329540', 'button', '2', 10, 31368, 'parity', 9.8, 0.2, 'fail', '2023-03-29 18:00:03'),
(6, 1, '20230329540', 'button', '3', 10, 31368, 'parity', 9.8, 0.2, 'fail', '2023-03-29 18:00:03'),
(7, 1, '20230329540', 'button', '4', 10, 31368, 'parity', 9.8, 0.2, 'fail', '2023-03-29 18:00:03'),
(8, 1, '20230329540', 'button', '5', 10, 31368, 'parity', 9.8, 0.2, 'fail', '2023-03-29 18:00:03'),
(9, 1, '20230329540', 'button', '7', 10, 31368, 'parity', 9.8, 0.2, 'fail', '2023-03-29 18:00:03'),
(10, 1, '20230329540', 'button', '8', 10, 31368, 'parity', 9.8, 0.2, 'fail', '2023-03-29 18:00:03'),
(11, 1, '20230329540', 'button', '9', 10, 31368, 'parity', 9.8, 0.2, 'fail', '2023-03-29 18:00:03'),
(12, 1, '20230329541', 'button', 'Green', 10, 31642, 'parity', 9.8, 0.2, 'fail', '2023-03-29 18:02:02'),
(13, 1, '20230329541', 'button', 'Violet', 10, 31642, 'parity', 9.8, 0.2, 'fail', '2023-03-29 18:02:02'),
(14, 1, '20230329541', 'button', 'Red', 10, 31642, 'parity', 19.6, 0.2, 'success', '2023-03-29 18:02:02'),
(15, 1, '20230329541', 'button', '0', 10, 31642, 'parity', 9.8, 0.2, 'fail', '2023-03-29 18:02:02'),
(16, 1, '20230329541', 'button', '1', 10, 31642, 'parity', 9.8, 0.2, 'fail', '2023-03-29 18:02:02'),
(17, 1, '20230329541', 'button', '2', 10, 31642, 'parity', 88.2, 0.2, 'success', '2023-03-29 18:02:02'),
(18, 1, '20230329541', 'button', '2', 10, 31642, 'parity', 88.2, 0.2, 'success', '2023-03-29 18:02:02'),
(19, 1, '20230329541', 'button', '2', 10, 31642, 'parity', 88.2, 0.2, 'success', '2023-03-29 18:02:02'),
(20, 1, '20230329541', 'button', '3', 10, 31642, 'parity', 9.8, 0.2, 'fail', '2023-03-29 18:02:02'),
(21, 1, '20230329541', 'button', '4', 10, 31642, 'parity', 9.8, 0.2, 'fail', '2023-03-29 18:02:02'),
(22, 1, '20230329541', 'button', '5', 10, 31642, 'parity', 9.8, 0.2, 'fail', '2023-03-29 18:02:02'),
(23, 1, '20230329541', 'button', '6', 10, 31642, 'parity', 9.8, 0.2, 'fail', '2023-03-29 18:02:02'),
(24, 1, '20230329541', 'button', '7', 10, 31642, 'parity', 9.8, 0.2, 'fail', '2023-03-29 18:02:02'),
(25, 1, '20230329541', 'button', '8', 10, 31642, 'parity', 9.8, 0.2, 'fail', '2023-03-29 18:02:02'),
(26, 1, '20230329545', 'button', '2', 10000, 31467, 'parity', 9800, 200, 'fail', '2023-03-29 18:10:02'),
(27, 1, '20230329546', 'button', '7', 10000, 31995, 'parity', 88200, 200, 'success', '2023-03-29 18:12:01'),
(28, 1, '20230329546', 'button', '7', 10000, 31995, 'parity', 88200, 200, 'success', '2023-03-29 18:12:01'),
(29, 1, '20230329546', 'button', '7', 10000, 31995, 'parity', 88200, 200, 'success', '2023-03-29 18:12:01'),
(30, 1, '20230329546', 'button', '7', 10000, 31995, 'parity', 88200, 200, 'success', '2023-03-29 18:12:01'),
(31, 1, '20230329547', 'button', '6', 10000, 31322, 'parity', 88200, 200, 'success', '2023-03-29 18:14:02'),
(32, 1, '20230329547', 'button', '6', 10000, 31322, 'parity', 88200, 200, 'success', '2023-03-29 18:14:02'),
(33, 1, '20230329547', 'button', '6', 10000, 31322, 'parity', 88200, 200, 'success', '2023-03-29 18:14:02'),
(34, 1, '20230329547', 'button', '6', 10000, 31322, 'parity', 88200, 200, 'success', '2023-03-29 18:14:02'),
(35, 2, '20230329549', 'button', 'Green', 1000, 31634, 'parity', 1960, 20, 'success', '2023-03-29 18:18:02'),
(36, 1, '20230330187', 'button', '8', 10, 31112, 'parity', 9.8, 0.2, 'fail', '2023-03-30 06:14:02'),
(37, 1, '20230330187', 'button', '8', 10, 31112, 'parity', 9.8, 0.2, 'fail', '2023-03-30 06:14:02'),
(38, 1, '20230330190', 'button', '2', 40, 31176, 'parity', 352.8, 0.8, 'success', '2023-03-30 06:20:01'),
(39, 1, '20230330190', 'button', '2', 10000, 31176, 'parity', 88200, 200, 'success', '2023-03-30 06:20:01'),
(40, 1, '20230330333', 'button', '6', 10000, 31616, 'parity', 88200, 200, 'success', '2023-03-30 11:06:01');

-- --------------------------------------------------------

--
-- Table structure for table `tbl_wallet`
--

CREATE TABLE `tbl_wallet` (
  `id` int(11) NOT NULL,
  `userid` int(11) NOT NULL,
  `amount` varchar(500) NOT NULL,
  `envelopestatus` smallint(11) NOT NULL,
  `createdate` timestamp NOT NULL DEFAULT current_timestamp()
) ENGINE=MyISAM DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

--
-- Dumping data for table `tbl_wallet`
--

INSERT INTO `tbl_wallet` (`id`, `userid`, `amount`, `envelopestatus`, `createdate`) VALUES
(1, 1, '656692.8', 0, '2023-03-29 12:26:39'),
(2, 2, '2960', 0, '2023-03-29 12:39:46');

-- --------------------------------------------------------

--
-- Table structure for table `tbl_walletsummery`
--

CREATE TABLE `tbl_walletsummery` (
  `id` int(11) NOT NULL,
  `userid` int(11) NOT NULL,
  `orderid` int(11) NOT NULL,
  `amount` float NOT NULL,
  `type` varchar(50) NOT NULL,
  `actiontype` varchar(50) NOT NULL,
  `createdate` timestamp NOT NULL DEFAULT current_timestamp()
) ENGINE=MyISAM DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

--
-- Dumping data for table `tbl_walletsummery`
--

INSERT INTO `tbl_walletsummery` (`id`, `userid`, `orderid`, `amount`, `type`, `actiontype`, `createdate`) VALUES
(1, 1, 1, 10, 'debit', 'recharge', '2023-03-29 12:28:37'),
(2, 1, 2, 10, 'debit', 'join', '2023-03-29 12:28:40'),
(3, 1, 3, 10, 'debit', 'join', '2023-03-29 12:28:45'),
(4, 1, 4, 10, 'debit', 'join', '2023-03-29 12:28:47'),
(5, 1, 5, 10, 'debit', 'join', '2023-03-29 12:28:56'),
(6, 1, 6, 10, 'debit', 'join', '2023-03-29 12:28:58'),
(7, 1, 7, 10, 'debit', 'join', '2023-03-29 12:29:03'),
(8, 1, 8, 10, 'debit', 'join', '2023-03-29 12:29:08'),
(9, 1, 9, 10, 'debit', 'join', '2023-03-29 12:29:14'),
(10, 1, 10, 10, 'debit', 'join', '2023-03-29 12:29:16'),
(11, 1, 11, 10, 'debit', 'join', '2023-03-29 12:29:19'),
(12, 1, 12, 19.6, 'credit', 'win', '2023-03-29 18:00:03'),
(13, 1, 13, 88.2, 'credit', 'win', '2023-03-29 18:00:03'),
(14, 1, 14, 10, 'debit', 'join', '2023-03-29 12:30:29'),
(15, 1, 15, 10, 'debit', 'join', '2023-03-29 12:30:32'),
(16, 1, 16, 10, 'debit', 'join', '2023-03-29 12:30:35'),
(17, 1, 17, 10, 'debit', 'join', '2023-03-29 12:30:38'),
(18, 1, 18, 10, 'debit', 'join', '2023-03-29 12:30:40'),
(19, 1, 19, 10, 'debit', 'join', '2023-03-29 12:30:49'),
(20, 1, 20, 10, 'debit', 'join', '2023-03-29 12:30:49'),
(21, 1, 21, 10, 'debit', 'join', '2023-03-29 12:30:49'),
(22, 1, 22, 10, 'debit', 'join', '2023-03-29 12:30:56'),
(23, 1, 23, 10, 'debit', 'join', '2023-03-29 12:31:02'),
(24, 1, 24, 10, 'debit', 'join', '2023-03-29 12:31:07'),
(25, 1, 25, 10, 'debit', 'join', '2023-03-29 12:31:14'),
(26, 1, 26, 10, 'debit', 'join', '2023-03-29 12:31:19'),
(27, 1, 27, 10, 'debit', 'join', '2023-03-29 12:31:26'),
(28, 1, 28, 19.6, 'credit', 'win', '2023-03-29 18:02:02'),
(29, 1, 29, 88.2, 'credit', 'win', '2023-03-29 18:02:02'),
(30, 1, 30, 88.2, 'credit', 'win', '2023-03-29 18:02:02'),
(31, 1, 31, 88.2, 'credit', 'win', '2023-03-29 18:02:02'),
(32, 1, 32, 2000, 'credit', 'reward', '2023-03-29 18:02:17'),
(33, 1, 33, 20000000000, 'credit', 'reward', '2023-03-29 18:02:37'),
(34, 1, 34, 10000, 'debit', 'join', '2023-03-29 12:39:10'),
(35, 1, 35, 10000, 'debit', 'join', '2023-03-29 12:40:40'),
(36, 1, 36, 10000, 'debit', 'join', '2023-03-29 12:40:56'),
(37, 1, 37, 10000, 'debit', 'join', '2023-03-29 12:41:00'),
(38, 1, 38, 10000, 'debit', 'join', '2023-03-29 12:41:05'),
(39, 1, 39, 88200, 'credit', 'win', '2023-03-29 18:12:01'),
(40, 1, 40, 88200, 'credit', 'win', '2023-03-29 18:12:01'),
(41, 1, 41, 88200, 'credit', 'win', '2023-03-29 18:12:01'),
(42, 1, 42, 88200, 'credit', 'win', '2023-03-29 18:12:01'),
(43, 1, 43, 10000, 'debit', 'join', '2023-03-29 12:42:21'),
(44, 1, 44, 10000, 'debit', 'join', '2023-03-29 12:42:31'),
(45, 1, 45, 10000, 'debit', 'join', '2023-03-29 12:42:34'),
(46, 1, 46, 10000, 'debit', 'join', '2023-03-29 12:42:38'),
(47, 1, 47, 88200, 'credit', 'win', '2023-03-29 18:14:02'),
(48, 1, 48, 88200, 'credit', 'win', '2023-03-29 18:14:02'),
(49, 1, 49, 88200, 'credit', 'win', '2023-03-29 18:14:02'),
(50, 1, 50, 88200, 'credit', 'win', '2023-03-29 18:14:02'),
(51, 1, 51, 1000, 'credit', 'recharge~2', '2023-03-29 12:46:28'),
(52, 2, 52, 1960, 'credit', 'recharge', '2023-03-29 18:18:02'),
(53, 1, 53, 2000, 'debit', 'withdraw~1', '2023-03-29 19:41:59'),
(54, 1, 54, 50000, 'debit', 'withdraw~2', '2023-03-29 20:12:32'),
(55, 1, 55, 5000, 'debit', 'withdraw~3', '2023-03-29 14:59:44'),
(56, 1, 56, 20000, 'debit', 'withdraw~4', '2023-03-29 15:43:14'),
(57, 1, 57, 10, 'debit', 'join', '2023-03-30 00:42:42'),
(58, 1, 58, 10, 'debit', 'join', '2023-03-30 00:42:42'),
(59, 1, 59, 40, 'debit', 'join', '2023-03-30 00:49:22'),
(60, 1, 60, 10000, 'debit', 'join', '2023-03-30 00:49:27'),
(61, 1, 61, 352.8, 'credit', 'win', '2023-03-30 06:20:01'),
(62, 1, 62, 88200, 'credit', 'win', '2023-03-30 06:20:01'),
(63, 1, 63, 10000, 'debit', 'join', '2023-03-30 05:35:19'),
(64, 1, 64, 88200, 'credit', 'win', '2023-03-30 11:06:01');

-- --------------------------------------------------------

--
-- Table structure for table `tbl_withdrawal`
--

CREATE TABLE `tbl_withdrawal` (
  `id` int(11) NOT NULL,
  `userid` int(11) NOT NULL,
  `amount` float NOT NULL,
  `payout` varchar(50) NOT NULL,
  `payid` int(11) NOT NULL,
  `status` smallint(11) NOT NULL,
  `createdate` datetime NOT NULL
) ENGINE=MyISAM DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

--
-- Dumping data for table `tbl_withdrawal`
--

INSERT INTO `tbl_withdrawal` (`id`, `userid`, `amount`, `payout`, `payid`, `status`, `createdate`) VALUES
(1, 1, 2000, 'bank', 2, 0, '2023-03-29 19:41:59'),
(2, 1, 50000, 'bank', 2, 0, '2023-03-29 20:12:32'),
(3, 1, 5000, 'bank', 2, 2, '2023-03-29 20:30:31'),
(4, 1, 20000, 'bank', 2, 1, '2023-03-29 21:13:14');

-- --------------------------------------------------------

--
-- Table structure for table `wager_amount`
--

CREATE TABLE `wager_amount` (
  `id` int(11) NOT NULL,
  `tot_deposit` varchar(200) CHARACTER SET utf8mb3 COLLATE utf8mb3_general_ci NOT NULL,
  `wager_amt` varchar(200) CHARACTER SET utf8mb3 COLLATE utf8mb3_general_ci NOT NULL,
  `uid` varchar(200) CHARACTER SET utf8mb3 COLLATE utf8mb3_general_ci NOT NULL,
  `date` varchar(200) CHARACTER SET utf8mb3 COLLATE utf8mb3_general_ci NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

--
-- Dumping data for table `wager_amount`
--

INSERT INTO `wager_amount` (`id`, `tot_deposit`, `wager_amt`, `uid`, `date`) VALUES
(1, '99999', '99999', '1', 'March 29, 2023, 4:48 pm'),
(2, '99999', '99999', '1', 'March 29, 2023, 4:49 pm'),
(3, '1000', '1000', '1', 'March 29, 2023, 4:53 pm'),
(4, '1000', '1000', '2', 'March 29, 2023, 5:00 pm'),
(5, '1000', '1000', '2', 'March 29, 2023, 5:00 pm'),
(6, '1000', '1000', '2', 'March 29, 2023, 5:08 pm'),
(7, '50000', '50000', '2', 'March 29, 2023, 5:12 pm'),
(8, '50000', '50000', '2', 'March 29, 2023, 5:13 pm'),
(9, '50000', '50000', '2', 'March 29, 2023, 5:17 pm'),
(10, '50000', '50000', '2', 'March 29, 2023, 5:22 pm'),
(11, '99999', '99999', '2', 'March 29, 2023, 5:30 pm'),
(12, '50000', '50000', '1', 'March 29, 2023, 5:45 pm'),
(13, '10000', '10000', '1', 'March 29, 2023, 6:05 pm'),
(14, '10000', '10000', '1', 'March 29, 2023, 6:05 pm'),
(15, '10000', '10000', '1', 'March 29, 2023, 6:06 pm'),
(16, '10000', '10000', '1', 'March 29, 2023, 6:06 pm'),
(17, '10000', '10000', '1', 'March 29, 2023, 6:08 pm'),
(18, '1000', '1000', '2', 'March 29, 2023, 6:15 pm');

-- --------------------------------------------------------

--
-- Table structure for table `wallet`
--

CREATE TABLE `wallet` (
  `id` int(11) NOT NULL,
  `uid` varchar(100) CHARACTER SET utf8mb3 COLLATE utf8mb3_general_ci NOT NULL,
  `amount` varchar(255) CHARACTER SET utf8mb3 COLLATE utf8mb3_general_ci NOT NULL,
  `updated_at` timestamp NOT NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  `created_at` timestamp NOT NULL DEFAULT current_timestamp()
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

--
-- Dumping data for table `wallet`
--

INSERT INTO `wallet` (`id`, `uid`, `amount`, `updated_at`, `created_at`) VALUES
(1, '1', '200000000', '2023-03-29 12:26:07', '2023-03-29 12:25:28'),
(2, '2', '200000000', '2023-03-29 12:39:07', '2023-03-29 12:25:42');

--
-- Indexes for dumped tables
--

--
-- Indexes for table `banner`
--
ALTER TABLE `banner`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `child_menu`
--
ALTER TABLE `child_menu`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `content`
--
ALTER TABLE `content`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `deposits`
--
ALTER TABLE `deposits`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `Red envlop`
--
ALTER TABLE `Red envlop`
  ADD PRIMARY KEY (`red envelop`);

--
-- Indexes for table `role`
--
ALTER TABLE `role`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `services`
--
ALTER TABLE `services`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `site_setting`
--
ALTER TABLE `site_setting`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `task`
--
ALTER TABLE `task`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `tbl_admin`
--
ALTER TABLE `tbl_admin`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `tbl_bankdetail`
--
ALTER TABLE `tbl_bankdetail`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `tbl_betting`
--
ALTER TABLE `tbl_betting`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `tbl_bonus`
--
ALTER TABLE `tbl_bonus`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `tbl_bonussummery`
--
ALTER TABLE `tbl_bonussummery`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `tbl_bonuswithdrawal`
--
ALTER TABLE `tbl_bonuswithdrawal`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `tbl_envelop`
--
ALTER TABLE `tbl_envelop`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `tbl_gameid`
--
ALTER TABLE `tbl_gameid`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `tbl_gamesettings`
--
ALTER TABLE `tbl_gamesettings`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `tbl_manualresult`
--
ALTER TABLE `tbl_manualresult`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `tbl_manualresultswitch`
--
ALTER TABLE `tbl_manualresultswitch`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `tbl_order`
--
ALTER TABLE `tbl_order`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `tbl_paymentsetting`
--
ALTER TABLE `tbl_paymentsetting`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `tbl_product`
--
ALTER TABLE `tbl_product`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `tbl_productfeature`
--
ALTER TABLE `tbl_productfeature`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `tbl_randomdata`
--
ALTER TABLE `tbl_randomdata`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `tbl_result`
--
ALTER TABLE `tbl_result`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `tbl_reward`
--
ALTER TABLE `tbl_reward`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `tbl_tempwinner`
--
ALTER TABLE `tbl_tempwinner`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `tbl_test`
--
ALTER TABLE `tbl_test`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `tbl_user`
--
ALTER TABLE `tbl_user`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `tbl_userresult`
--
ALTER TABLE `tbl_userresult`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `tbl_wallet`
--
ALTER TABLE `tbl_wallet`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `tbl_walletsummery`
--
ALTER TABLE `tbl_walletsummery`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `tbl_withdrawal`
--
ALTER TABLE `tbl_withdrawal`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `wager_amount`
--
ALTER TABLE `wager_amount`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `wallet`
--
ALTER TABLE `wallet`
  ADD PRIMARY KEY (`id`),
  ADD KEY `uid` (`uid`);

--
-- AUTO_INCREMENT for dumped tables
--

--
-- AUTO_INCREMENT for table `banner`
--
ALTER TABLE `banner`
  MODIFY `id` int(255) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=25;

--
-- AUTO_INCREMENT for table `child_menu`
--
ALTER TABLE `child_menu`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=22;

--
-- AUTO_INCREMENT for table `deposits`
--
ALTER TABLE `deposits`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=12;

--
-- AUTO_INCREMENT for table `Red envlop`
--
ALTER TABLE `Red envlop`
  MODIFY `red envelop` int(1) NOT NULL AUTO_INCREMENT;

--
-- AUTO_INCREMENT for table `role`
--
ALTER TABLE `role`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=16;

--
-- AUTO_INCREMENT for table `services`
--
ALTER TABLE `services`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=18;

--
-- AUTO_INCREMENT for table `site_setting`
--
ALTER TABLE `site_setting`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=2;

--
-- AUTO_INCREMENT for table `task`
--
ALTER TABLE `task`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=12;

--
-- AUTO_INCREMENT for table `tbl_admin`
--
ALTER TABLE `tbl_admin`
  MODIFY `id` int(255) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=5;

--
-- AUTO_INCREMENT for table `tbl_bankdetail`
--
ALTER TABLE `tbl_bankdetail`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=3;

--
-- AUTO_INCREMENT for table `tbl_betting`
--
ALTER TABLE `tbl_betting`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=41;

--
-- AUTO_INCREMENT for table `tbl_bonus`
--
ALTER TABLE `tbl_bonus`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT;

--
-- AUTO_INCREMENT for table `tbl_bonussummery`
--
ALTER TABLE `tbl_bonussummery`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=41;

--
-- AUTO_INCREMENT for table `tbl_bonuswithdrawal`
--
ALTER TABLE `tbl_bonuswithdrawal`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT;

--
-- AUTO_INCREMENT for table `tbl_envelop`
--
ALTER TABLE `tbl_envelop`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT;

--
-- AUTO_INCREMENT for table `tbl_gameid`
--
ALTER TABLE `tbl_gameid`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=431;

--
-- AUTO_INCREMENT for table `tbl_gamesettings`
--
ALTER TABLE `tbl_gamesettings`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=2;

--
-- AUTO_INCREMENT for table `tbl_manualresult`
--
ALTER TABLE `tbl_manualresult`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=11;

--
-- AUTO_INCREMENT for table `tbl_manualresultswitch`
--
ALTER TABLE `tbl_manualresultswitch`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=2;

--
-- AUTO_INCREMENT for table `tbl_order`
--
ALTER TABLE `tbl_order`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=65;

--
-- AUTO_INCREMENT for table `tbl_paymentsetting`
--
ALTER TABLE `tbl_paymentsetting`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=2;

--
-- AUTO_INCREMENT for table `tbl_product`
--
ALTER TABLE `tbl_product`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=15;

--
-- AUTO_INCREMENT for table `tbl_productfeature`
--
ALTER TABLE `tbl_productfeature`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=21;

--
-- AUTO_INCREMENT for table `tbl_randomdata`
--
ALTER TABLE `tbl_randomdata`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=481;

--
-- AUTO_INCREMENT for table `tbl_result`
--
ALTER TABLE `tbl_result`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=1717;

--
-- AUTO_INCREMENT for table `tbl_reward`
--
ALTER TABLE `tbl_reward`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=124;

--
-- AUTO_INCREMENT for table `tbl_tempwinner`
--
ALTER TABLE `tbl_tempwinner`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT;

--
-- AUTO_INCREMENT for table `tbl_test`
--
ALTER TABLE `tbl_test`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT;

--
-- AUTO_INCREMENT for table `tbl_user`
--
ALTER TABLE `tbl_user`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=843;

--
-- AUTO_INCREMENT for table `tbl_userresult`
--
ALTER TABLE `tbl_userresult`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=41;

--
-- AUTO_INCREMENT for table `tbl_wallet`
--
ALTER TABLE `tbl_wallet`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=3;

--
-- AUTO_INCREMENT for table `tbl_walletsummery`
--
ALTER TABLE `tbl_walletsummery`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=65;

--
-- AUTO_INCREMENT for table `tbl_withdrawal`
--
ALTER TABLE `tbl_withdrawal`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=5;

--
-- AUTO_INCREMENT for table `wager_amount`
--
ALTER TABLE `wager_amount`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=19;

--
-- AUTO_INCREMENT for table `wallet`
--
ALTER TABLE `wallet`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=13;
COMMIT;

/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;
