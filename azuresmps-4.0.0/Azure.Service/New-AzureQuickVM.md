---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F94584BC-EC02-412D-B089-B98A6FF8F505
online version: ''
schema: 2.0.0
ms.openlocfilehash: a5b7758a7316fa6c34ffe6b5225cd252f39c5d7c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045909"
---
# <span data-ttu-id="ca1ac-101">New-AzureQuickVM</span><span class="sxs-lookup"><span data-stu-id="ca1ac-101">New-AzureQuickVM</span></span>

## <span data-ttu-id="ca1ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca1ac-102">SYNOPSIS</span></span>
<span data-ttu-id="ca1ac-103">Azure 가상 컴퓨터를 구성 하 고 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-103">Configures and creates an Azure virtual machine.</span></span>

## <span data-ttu-id="ca1ac-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ca1ac-104">SYNTAX</span></span>

### <span data-ttu-id="ca1ac-105">Windows (기본값)</span><span class="sxs-lookup"><span data-stu-id="ca1ac-105">Windows (Default)</span></span>
```
New-AzureQuickVM [-Windows] -ServiceName <String> [-Name <String>] -ImageName <String> [-Password <String>]
 [-ReverseDnsFqdn <String>] [-Location <String>] [-AffinityGroup <String>] [-AdminUsername <String>]
 [-Certificates <CertificateSettingList>] [-WaitForBoot] [-DisableWinRMHttps] [-EnableWinRMHttp]
 [-WinRMCertificate <X509Certificate2>] [-X509Certificates <X509Certificate2[]>] [-NoExportPrivateKey]
 [-NoWinRMEndpoint] [-VNetName <String>] [-SubnetNames <String[]>] [-DnsSettings <DnsServer[]>]
 [-HostCaching <String>] [-AvailabilitySetName <String>] [-InstanceSize <String>] [-MediaLocation <String>]
 [-DisableGuestAgent] [-CustomDataFile <String>] [-ReservedIPName <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ca1ac-106">Linux</span><span class="sxs-lookup"><span data-stu-id="ca1ac-106">Linux</span></span>
```
New-AzureQuickVM [-Linux] -ServiceName <String> [-Name <String>] -ImageName <String> [-Password <String>]
 [-ReverseDnsFqdn <String>] [-Location <String>] [-AffinityGroup <String>] [-LinuxUser <String>] [-WaitForBoot]
 [-SSHPublicKeys <SSHPublicKeyList>] [-SSHKeyPairs <SSHKeyPairList>] [-VNetName <String>]
 [-SubnetNames <String[]>] [-DnsSettings <DnsServer[]>] [-HostCaching <String>] [-AvailabilitySetName <String>]
 [-InstanceSize <String>] [-MediaLocation <String>] [-DisableGuestAgent] [-CustomDataFile <String>]
 [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ca1ac-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ca1ac-107">DESCRIPTION</span></span>
<span data-ttu-id="ca1ac-108">**AzureQuickVM** Cmdlet은 Azure 가상 컴퓨터를 구성 하 고 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-108">The **New-AzureQuickVM** cmdlet configures and creates an Azure virtual machine.</span></span>
<span data-ttu-id="ca1ac-109">이 cmdlet은 가상 컴퓨터를 기존 Azure 서비스에 배포할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-109">This cmdlet can deploy a virtual machine into an existing Azure service.</span></span>
<span data-ttu-id="ca1ac-110">이 cmdlet은 새 가상 컴퓨터를 호스트 하는 Azure 서비스를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-110">This cmdlet can alternatively create an Azure service that hosts the new virtual machine.</span></span>

## <span data-ttu-id="ca1ac-111">예제의</span><span class="sxs-lookup"><span data-stu-id="ca1ac-111">EXAMPLES</span></span>

### <span data-ttu-id="ca1ac-112">예제 1: 가상 컴퓨터 만들기</span><span class="sxs-lookup"><span data-stu-id="ca1ac-112">Example 1: Create a virtual machine</span></span>
```
PS C:\> New-AzureQuickVM -Windows -ServiceName "ContosoService17" -Name "VirutalMachine01" -ImageName "Image07" -Password "password" -AdminUsername "AdminMain" -WaitForBoot
```

<span data-ttu-id="ca1ac-113">이 명령은 기존 서비스에서 Windows 운영 체제를 실행 하는 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-113">This command creates a virtual machine that runs the Windows operating system in an existing service.</span></span>
<span data-ttu-id="ca1ac-114">Cmdlet은 지정 된 이미지의 가상 컴퓨터를 기반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-114">The cmdlet bases the virtual machine on the specified image.</span></span>
<span data-ttu-id="ca1ac-115">명령에서 *Waitforboot* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-115">The command specifies the *WaitForBoot* parameter.</span></span>
<span data-ttu-id="ca1ac-116">따라서 cmdlet은 가상 컴퓨터가 시작 될 때까지 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-116">Therefore, the cmdlet waits for the virtual machine to start.</span></span>

### <span data-ttu-id="ca1ac-117">예제 2: 인증서를 사용 하 여 가상 컴퓨터 만들기</span><span class="sxs-lookup"><span data-stu-id="ca1ac-117">Example 2: Create a virtual machine that by using certificates</span></span>
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
PS C:\> New-AzureQuickVM -Windows -ServiceName "MySvc1" -name "MyWinVM1" -ImageName "Image07" -Password "password" -AdminUserName "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] -WaitForBoot
```

<span data-ttu-id="ca1ac-118">첫 번째 명령은 저장소에서 인증서를 가져와 $certs 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-118">The first command gets certificates from a store, and stores them in the $certs variable.</span></span>

<span data-ttu-id="ca1ac-119">두 번째 명령은 이미지에서 기존 서비스로 Windows 운영 체제를 실행 하는 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-119">The second command creates a virtual machine that runs the Windows operating system in an existing service from an image.</span></span>
<span data-ttu-id="ca1ac-120">기본적으로 가상 컴퓨터에서 WinRM Https 수신기를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-120">By default, WinRM Https listener is enabled on the virtual machine.</span></span>
<span data-ttu-id="ca1ac-121">명령에서 *Waitforboot* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-121">The command specifies the *WaitForBoot* parameter.</span></span>
<span data-ttu-id="ca1ac-122">따라서 cmdlet은 가상 컴퓨터가 시작 될 때까지 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-122">Therefore, the cmdlet waits for the virtual machine to start.</span></span>
<span data-ttu-id="ca1ac-123">명령이 WinRM 인증서를 업로드 하 고 호스팅된 서비스에 X509Certificates 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-123">The command uploads a WinRM Certificate and X509Certificates to the hosted service.</span></span>

### <span data-ttu-id="ca1ac-124">예제 3: Linux 운영 체제를 실행 하는 가상 컴퓨터 만들기</span><span class="sxs-lookup"><span data-stu-id="ca1ac-124">Example 3: Create a virtual machine that runs the Linux operating system</span></span>
```
PS C:\> New-AzureQuickVM -Linux -ServiceName "ContosoServiceLinux01" -Name "LinuxVirtualMachine01" -ImageName "LinuxImage01" -LinuxUser "RootMain" -Password "password" -Location "Central US"
```

<span data-ttu-id="ca1ac-125">이 명령은 이미지에서 Linux 운영 체제를 실행 하는 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-125">This command creates a virtual machine that runs the Linux operating system from an image.</span></span>
<span data-ttu-id="ca1ac-126">이 명령은 새 가상 컴퓨터를 호스트 하는 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-126">This command creates a service to host the new virtual machine.</span></span>
<span data-ttu-id="ca1ac-127">명령에서 서비스 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-127">The command specifies a location for the service.</span></span>

### <span data-ttu-id="ca1ac-128">예제 4: 가상 컴퓨터 만들기 및 새 가상 컴퓨터를 호스트 하는 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="ca1ac-128">Example 4: Create a virtual machine and create a service to host the new virtual machine</span></span>
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService03" -Name " VirtualMachine25" -ImageName $images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name
```

<span data-ttu-id="ca1ac-129">첫 번째 명령은 **가져오기-AzureLocation** cmdlet을 사용 하 여 위치를 가져온 다음 $Locations 배열 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-129">The first command gets locations by using the **Get-AzureLocation** cmdlet, and then stores them in the $Locations array variable.</span></span>

<span data-ttu-id="ca1ac-130">두 번째 명령은 **AzureVMImage** cmdlet을 사용 하 여 사용 가능한 이미지를 가져온 다음이를 $Images array 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-130">The second command gets available images by using the **Get-AzureVMImage** cmdlet, and then stores them in the $Images array variable.</span></span>

<span data-ttu-id="ca1ac-131">마지막 명령은 VirtualMachine25 이라는 큰 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-131">The final command creates a large virtual machine named VirtualMachine25.</span></span>
<span data-ttu-id="ca1ac-132">가상 컴퓨터에서 Windows 운영 체제를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-132">The virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="ca1ac-133">$Images의 이미지 중 하나를 기준으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-133">It is based on one of the images in $Images.</span></span>
<span data-ttu-id="ca1ac-134">이 명령은 새 가상 컴퓨터에 대 한 ContosoService03 이라는 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-134">The command creates a service named ContosoService03 for the new virtual machine.</span></span>
<span data-ttu-id="ca1ac-135">서비스가 $Locations 위치에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-135">The service is in a location in $Locations.</span></span>

### <span data-ttu-id="ca1ac-136">예제 5: 예약 된 IP 이름을 가진 가상 컴퓨터 만들기</span><span class="sxs-lookup"><span data-stu-id="ca1ac-136">Example 5: Create a virtual machine that has a reserved IP name</span></span>
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService04" -Name "VirtualMachine27" -ImageName $Images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name -ReservedIPName $ipName
```

<span data-ttu-id="ca1ac-137">첫 번째 명령은 위치를 가져온 다음 $Locations 배열 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-137">The first command gets locations, and then stores them in the $Locations array variable.</span></span>

<span data-ttu-id="ca1ac-138">두 번째 명령은 사용할 수 있는 이미지를 가져온 다음 $Images 배열 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-138">The second command gets available images, and then stores them in the $Images array variable.</span></span>

<span data-ttu-id="ca1ac-139">마지막 명령은 $Images의 이미지 중 하나를 기반으로 VirtualMachine27 이라는 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-139">The final command creates a virtual machine named VirtualMachine27 based on one of the images in $Images.</span></span>
<span data-ttu-id="ca1ac-140">이 명령은 $Locations 위치에 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-140">The command creates a service in a location in $Locations.</span></span>
<span data-ttu-id="ca1ac-141">가상 컴퓨터에는 예약 된 IP 이름이 있으며, 이전에 $ipName 변수에 저장 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-141">The virtual machine has a reserved IP name, previously stored in the $ipName variable.</span></span>

## <span data-ttu-id="ca1ac-142">변수</span><span class="sxs-lookup"><span data-stu-id="ca1ac-142">PARAMETERS</span></span>

### <span data-ttu-id="ca1ac-143">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="ca1ac-143">-AdminUsername</span></span>
<span data-ttu-id="ca1ac-144">이 cmdlet이 가상 컴퓨터에서 만드는 관리자 계정의 사용자 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-144">Specifies the user name of the Administrator account that this cmdlet creates on the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ac-145">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="ca1ac-145">-AffinityGroup</span></span>
<span data-ttu-id="ca1ac-146">가상 컴퓨터에 대 한 선호도 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-146">Specifies the affinity group for the virtual machine.</span></span>
<span data-ttu-id="ca1ac-147">이 cmdlet이 가상 컴퓨터에 대 한 Azure 서비스를 만드는 경우에만이 매개 변수 또는 *위치* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-147">Specify this parameter or the *Location* parameter only if this cmdlet creates an Azure service for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ac-148">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="ca1ac-148">-AvailabilitySetName</span></span>
<span data-ttu-id="ca1ac-149">이 cmdlet이 가상 컴퓨터를 만드는 가용성 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-149">Specifies the name of the availability set in which this cmdlet creates the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ac-150">-인증서</span><span class="sxs-lookup"><span data-stu-id="ca1ac-150">-Certificates</span></span>
<span data-ttu-id="ca1ac-151">이 cmdlet에서 서비스를 만드는 데 사용 하는 인증서 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-151">Specifies a list of certificates that this cmdlet uses to create the service.</span></span>

```yaml
Type: CertificateSettingList
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ac-152">-CustomDataFile 접속</span><span class="sxs-lookup"><span data-stu-id="ca1ac-152">-CustomDataFile</span></span>
<span data-ttu-id="ca1ac-153">가상 컴퓨터에 대 한 데이터 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-153">Specifies a data file for the virtual machine.</span></span>
<span data-ttu-id="ca1ac-154">이 cmdlet은 파일의 내용을 Base64로 인코딩합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-154">This cmdlet encodes the contents of the file as Base64.</span></span>
<span data-ttu-id="ca1ac-155">파일의 길이는 64 킬로바이트 미만 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-155">The file must be less than 64 kilobytes long.</span></span>

<span data-ttu-id="ca1ac-156">게스트 운영 체제가 Windows 운영 체제 이면이 cmdlet은이 데이터 를%SYSTEMDRIVE%\AzureData\CustomData.bin. 이라는 이진 파일로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-156">If the guest operating system is the Windows operating system, this cmdlet saves this data as a binary file that is named %SYSTEMDRIVE%\AzureData\CustomData.bin.</span></span>

<span data-ttu-id="ca1ac-157">게스트 운영 체제가 Linux 인 경우이 cmdlet은 ovf-env.xml 파일을 사용 하 여 데이터를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-157">If the guest operating system is Linux, this cmdlet passes the data by using the ovf-env.xml file.</span></span>
<span data-ttu-id="ca1ac-158">설치는 해당 파일을/var/lib/waagent 디렉터리로 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-158">Installation copies that file to the /var/lib/waagent directory.</span></span>
<span data-ttu-id="ca1ac-159">또한 에이전트는/var/lib/waagent/CustomData.에 Base64로 인코딩된 데이터를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-159">The agent also stores the Base64 encoded data in /var/lib/waagent/CustomData.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ac-160">-DisableGuestAgent</span><span class="sxs-lookup"><span data-stu-id="ca1ac-160">-DisableGuestAgent</span></span>
<span data-ttu-id="ca1ac-161">이 cmdlet이 IaaS (인프라) 제공 게스트 에이전트를 사용 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-161">Indicates that this cmdlet disables the infrastructure as a service (IaaS) provision guest agent.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ac-162">-DisableWinRMHttps</span><span class="sxs-lookup"><span data-stu-id="ca1ac-162">-DisableWinRMHttps</span></span>
<span data-ttu-id="ca1ac-163">이 cmdlet이 HTTPS에서 WinRM (Windows Remote Management)을 사용 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-163">Indicates that this cmdlet disables Windows Remote Management (WinRM) on HTTPS.</span></span>
<span data-ttu-id="ca1ac-164">기본적으로, WinRM은 HTTPS를 통해 사용 하도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-164">By default, WinRM is enabled over HTTPS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ac-165">-DnsSettings</span><span class="sxs-lookup"><span data-stu-id="ca1ac-165">-DnsSettings</span></span>
<span data-ttu-id="ca1ac-166">새 배포에 대 한 DNS 설정을 정의 하는 DNS 서버 개체의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-166">Specifies an array of DNS server objects that defines the DNS settings for the new deployment.</span></span>
<span data-ttu-id="ca1ac-167">**DnsServer** 개체를 만들려면 **새 azuredns** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-167">To create a **DnsServer** object, use the **New-AzureDns** cmdlet.</span></span>

```yaml
Type: DnsServer[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ac-168">-EnableWinRMHttp</span><span class="sxs-lookup"><span data-stu-id="ca1ac-168">-EnableWinRMHttp</span></span>
<span data-ttu-id="ca1ac-169">이 cmdlet이 HTTP를 통해 WinRM을 사용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-169">Indicates that this cmdlet enables WinRM over HTTP.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ac-170">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="ca1ac-170">-HostCaching</span></span>
<span data-ttu-id="ca1ac-171">운영 체제 디스크에 대 한 호스트 캐싱 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-171">Specifies the host caching mode for the operating system disk.</span></span>
<span data-ttu-id="ca1ac-172">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-172">Valid values are:</span></span> 

- <span data-ttu-id="ca1ac-173">읽기</span><span class="sxs-lookup"><span data-stu-id="ca1ac-173">ReadOnly</span></span>
- <span data-ttu-id="ca1ac-174">쓰기</span><span class="sxs-lookup"><span data-stu-id="ca1ac-174">ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ac-175">-ImageName</span><span class="sxs-lookup"><span data-stu-id="ca1ac-175">-ImageName</span></span>
<span data-ttu-id="ca1ac-176">이 cmdlet에서 운영 체제 디스크를 만드는 데 사용 하는 디스크 이미지의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-176">Specifies the name of the disk image this cmdlet uses to create the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ac-177">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ca1ac-177">-InformationAction</span></span>
<span data-ttu-id="ca1ac-178">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-178">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ca1ac-179">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-179">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ca1ac-180">하기로</span><span class="sxs-lookup"><span data-stu-id="ca1ac-180">Continue</span></span>
- <span data-ttu-id="ca1ac-181">숨기기</span><span class="sxs-lookup"><span data-stu-id="ca1ac-181">Ignore</span></span>
- <span data-ttu-id="ca1ac-182">Inquire</span><span class="sxs-lookup"><span data-stu-id="ca1ac-182">Inquire</span></span>
- <span data-ttu-id="ca1ac-183">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ca1ac-183">SilentlyContinue</span></span>
- <span data-ttu-id="ca1ac-184">중지가</span><span class="sxs-lookup"><span data-stu-id="ca1ac-184">Stop</span></span>
- <span data-ttu-id="ca1ac-185">대기</span><span class="sxs-lookup"><span data-stu-id="ca1ac-185">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ac-186">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ca1ac-186">-InformationVariable</span></span>
<span data-ttu-id="ca1ac-187">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-187">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ac-188">-InstanceSize</span><span class="sxs-lookup"><span data-stu-id="ca1ac-188">-InstanceSize</span></span>
<span data-ttu-id="ca1ac-189">인스턴스의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-189">Specifies the size of the instance.</span></span>
<span data-ttu-id="ca1ac-190">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-190">Valid values are:</span></span> 

- <span data-ttu-id="ca1ac-191">ExtraSmall</span><span class="sxs-lookup"><span data-stu-id="ca1ac-191">ExtraSmall</span></span>
- <span data-ttu-id="ca1ac-192">Small</span><span class="sxs-lookup"><span data-stu-id="ca1ac-192">Small</span></span>
- <span data-ttu-id="ca1ac-193">높음이나</span><span class="sxs-lookup"><span data-stu-id="ca1ac-193">Medium</span></span>
- <span data-ttu-id="ca1ac-194">용량의</span><span class="sxs-lookup"><span data-stu-id="ca1ac-194">Large</span></span>
- <span data-ttu-id="ca1ac-195">ExtraLarge</span><span class="sxs-lookup"><span data-stu-id="ca1ac-195">ExtraLarge</span></span>
- <span data-ttu-id="ca1ac-196">5</span><span class="sxs-lookup"><span data-stu-id="ca1ac-196">A5</span></span>
- <span data-ttu-id="ca1ac-197">A6</span><span class="sxs-lookup"><span data-stu-id="ca1ac-197">A6</span></span>
- <span data-ttu-id="ca1ac-198">(A</span><span class="sxs-lookup"><span data-stu-id="ca1ac-198">A7</span></span>
- <span data-ttu-id="ca1ac-199">A8</span><span class="sxs-lookup"><span data-stu-id="ca1ac-199">A8</span></span>
- <span data-ttu-id="ca1ac-200">A9</span><span class="sxs-lookup"><span data-stu-id="ca1ac-200">A9</span></span>
- <span data-ttu-id="ca1ac-201">Basic_A0</span><span class="sxs-lookup"><span data-stu-id="ca1ac-201">Basic_A0</span></span>
- <span data-ttu-id="ca1ac-202">Basic_A1</span><span class="sxs-lookup"><span data-stu-id="ca1ac-202">Basic_A1</span></span>
- <span data-ttu-id="ca1ac-203">Basic_A2</span><span class="sxs-lookup"><span data-stu-id="ca1ac-203">Basic_A2</span></span>
- <span data-ttu-id="ca1ac-204">Basic_A3</span><span class="sxs-lookup"><span data-stu-id="ca1ac-204">Basic_A3</span></span>
- <span data-ttu-id="ca1ac-205">Basic_A4</span><span class="sxs-lookup"><span data-stu-id="ca1ac-205">Basic_A4</span></span>
- <span data-ttu-id="ca1ac-206">Standard_D1</span><span class="sxs-lookup"><span data-stu-id="ca1ac-206">Standard_D1</span></span>
- <span data-ttu-id="ca1ac-207">Standard_D2</span><span class="sxs-lookup"><span data-stu-id="ca1ac-207">Standard_D2</span></span>
- <span data-ttu-id="ca1ac-208">Standard_D3</span><span class="sxs-lookup"><span data-stu-id="ca1ac-208">Standard_D3</span></span>
- <span data-ttu-id="ca1ac-209">Standard_D4</span><span class="sxs-lookup"><span data-stu-id="ca1ac-209">Standard_D4</span></span>
- <span data-ttu-id="ca1ac-210">Standard_D11</span><span class="sxs-lookup"><span data-stu-id="ca1ac-210">Standard_D11</span></span>
- <span data-ttu-id="ca1ac-211">Standard_D12</span><span class="sxs-lookup"><span data-stu-id="ca1ac-211">Standard_D12</span></span>
- <span data-ttu-id="ca1ac-212">Standard_D13</span><span class="sxs-lookup"><span data-stu-id="ca1ac-212">Standard_D13</span></span>
- <span data-ttu-id="ca1ac-213">Standard_D14</span><span class="sxs-lookup"><span data-stu-id="ca1ac-213">Standard_D14</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ac-214">-Linux</span><span class="sxs-lookup"><span data-stu-id="ca1ac-214">-Linux</span></span>
<span data-ttu-id="ca1ac-215">이 cmdlet이 Linux 기반 가상 컴퓨터를 생성 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-215">Indicates that this cmdlet creates a Linux based virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ac-216">-LinuxUser</span><span class="sxs-lookup"><span data-stu-id="ca1ac-216">-LinuxUser</span></span>
<span data-ttu-id="ca1ac-217">이 cmdlet에서 가상 컴퓨터에 만든 Linux 관리 계정의 사용자 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-217">Specifies the user name of the Linux administrative account that this cmdlet creates on the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ac-218">-위치</span><span class="sxs-lookup"><span data-stu-id="ca1ac-218">-Location</span></span>
<span data-ttu-id="ca1ac-219">가상 컴퓨터를 호스트 하는 Azure datacenter를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-219">Specifies the Azure datacenter that hosts the virtual machine.</span></span>
<span data-ttu-id="ca1ac-220">이 매개 변수를 지정 하는 경우 cmdlet은 지정 된 위치에 Azure 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-220">If you specify this parameter, the cmdlet creates an Azure service in the specified location.</span></span>
<span data-ttu-id="ca1ac-221">이 cmdlet이 가상 컴퓨터에 대 한 Azure 서비스를 만드는 경우에만이 매개 변수 또는 *AffinityGroup* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-221">Specify this parameter or the *AffinityGroup* parameter only if this cmdlet creates an Azure service for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ac-222">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="ca1ac-222">-MediaLocation</span></span>
<span data-ttu-id="ca1ac-223">이 cmdlet이 가상 컴퓨터 디스크를 만드는 Azure 저장소 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-223">Specifies the Azure Storage location where this cmdlet creates the virtual machines disks.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ac-224">-이름</span><span class="sxs-lookup"><span data-stu-id="ca1ac-224">-Name</span></span>
<span data-ttu-id="ca1ac-225">이 cmdlet이 만드는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-225">Specifies the name of the virtual machine that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ac-226">-NoExportPrivateKey</span><span class="sxs-lookup"><span data-stu-id="ca1ac-226">-NoExportPrivateKey</span></span>
<span data-ttu-id="ca1ac-227">이 구성이 개인 키를 업로드 하지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-227">Indicates that this configuration does not upload the private key.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ac-228">-NoWinRMEndpoint</span><span class="sxs-lookup"><span data-stu-id="ca1ac-228">-NoWinRMEndpoint</span></span>
<span data-ttu-id="ca1ac-229">이 cmdlet이 가상 컴퓨터에 대 한 WinRM 끝점을 추가 하지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-229">Indicates that this cmdlet does not add a WinRM endpoint for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ac-230">-암호</span><span class="sxs-lookup"><span data-stu-id="ca1ac-230">-Password</span></span>
<span data-ttu-id="ca1ac-231">관리 계정에 대 한 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-231">Specifies the password for the administrative account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ac-232">-프로필</span><span class="sxs-lookup"><span data-stu-id="ca1ac-232">-Profile</span></span>
<span data-ttu-id="ca1ac-233">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-233">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ca1ac-234">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-234">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ac-235">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="ca1ac-235">-ReservedIPName</span></span>
<span data-ttu-id="ca1ac-236">예약 된 IP 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-236">Specifies the reserved IP name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ac-237">-ReverseDnsFqdn</span><span class="sxs-lookup"><span data-stu-id="ca1ac-237">-ReverseDnsFqdn</span></span>
<span data-ttu-id="ca1ac-238">역방향 DNS 조회에 대 한 정규화 된 도메인 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-238">Specifies the fully qualified domain name for reverse DNS look up.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ac-239">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ca1ac-239">-ServiceName</span></span>
<span data-ttu-id="ca1ac-240">이 cmdlet가 새 가상 컴퓨터를 추가 하는 새 또는 기존 Azure 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-240">Specifies the name of a new or existing Azure service to which this cmdlet adds the new virtual machine.</span></span>

<span data-ttu-id="ca1ac-241">새 서비스를 지정 하는 경우이 cmdlet이이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-241">If you specify a new service, this cmdlets creates it.</span></span>
<span data-ttu-id="ca1ac-242">새 서비스를 만들려면 *Location* 또는 *AffinityGroup* 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-242">To create a new service, you must specify the *Location* or *AffinityGroup* parameter.</span></span>

<span data-ttu-id="ca1ac-243">기존 서비스를 지정 하는 경우 *위치* 또는 *AffinityGroup* 를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-243">If you specify an existing service, do not specify *Location* or *AffinityGroup*.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ac-244">-SSHKeyPairs</span><span class="sxs-lookup"><span data-stu-id="ca1ac-244">-SSHKeyPairs</span></span>
<span data-ttu-id="ca1ac-245">SSH 키 쌍을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-245">Specifies SSH key pairs.</span></span>

```yaml
Type: SSHKeyPairList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ac-246">-SSHPublicKeys</span><span class="sxs-lookup"><span data-stu-id="ca1ac-246">-SSHPublicKeys</span></span>
<span data-ttu-id="ca1ac-247">SSH 공개 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-247">Specifies SSH public keys.</span></span>

```yaml
Type: SSHPublicKeyList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ac-248">-SubnetNames</span><span class="sxs-lookup"><span data-stu-id="ca1ac-248">-SubnetNames</span></span>
<span data-ttu-id="ca1ac-249">가상 컴퓨터의 서브넷 이름 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-249">Specifies an array of names of subnet for the virtual machine.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ac-250">-VNetName</span><span class="sxs-lookup"><span data-stu-id="ca1ac-250">-VNetName</span></span>
<span data-ttu-id="ca1ac-251">가상 컴퓨터에 대 한 가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-251">Specifies the name of a virtual network for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ac-252">-WaitForBoot</span><span class="sxs-lookup"><span data-stu-id="ca1ac-252">-WaitForBoot</span></span>
<span data-ttu-id="ca1ac-253">이 cmdlet이 가상 컴퓨터가 상태 ReadyRole에 도달할 때까지 대기 하 고 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-253">Indicates that this cmdlet waits for the virtual machine to reach the state ReadyRole.</span></span>
<span data-ttu-id="ca1ac-254">가상 머신이 다음 상태 중 하나에 도달 하는 경우 cmdlet이 실패 합니다. FailedStartingVM, ProvisioningFailed 또는 ProvisioningTimeout.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-254">If the virtual machine reaches one of the following states, the cmdlet fails: FailedStartingVM, ProvisioningFailed, or ProvisioningTimeout.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ac-255">-Windows</span><span class="sxs-lookup"><span data-stu-id="ca1ac-255">-Windows</span></span>
<span data-ttu-id="ca1ac-256">이 cmdlet이 Windows 가상 컴퓨터를 생성 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-256">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ac-257">-WinRMCertificate</span><span class="sxs-lookup"><span data-stu-id="ca1ac-257">-WinRMCertificate</span></span>
<span data-ttu-id="ca1ac-258">이 cmdlet이 WinRM 끝점에 연결 하는 인증서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-258">Specifies a certificate that this cmdlet associates to a WinRM endpoint.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ac-259">-X509Certificates</span><span class="sxs-lookup"><span data-stu-id="ca1ac-259">-X509Certificates</span></span>
<span data-ttu-id="ca1ac-260">호스팅된 서비스에 배포 되는 X509 인증서의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-260">Specifies an array of X509 certificates that are deployed to a hosted service.</span></span>

```yaml
Type: X509Certificate2[]
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1ac-261">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca1ac-261">CommonParameters</span></span>
<span data-ttu-id="ca1ac-262">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca1ac-262">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca1ac-263">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca1ac-263">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca1ac-264">입력</span><span class="sxs-lookup"><span data-stu-id="ca1ac-264">INPUTS</span></span>

## <span data-ttu-id="ca1ac-265">출력</span><span class="sxs-lookup"><span data-stu-id="ca1ac-265">OUTPUTS</span></span>

## <span data-ttu-id="ca1ac-266">상속자</span><span class="sxs-lookup"><span data-stu-id="ca1ac-266">NOTES</span></span>

## <span data-ttu-id="ca1ac-267">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ca1ac-267">RELATED LINKS</span></span>

[<span data-ttu-id="ca1ac-268">가져오기-AzureLocation</span><span class="sxs-lookup"><span data-stu-id="ca1ac-268">Get-AzureLocation</span></span>](./Get-AzureLocation.md)

[<span data-ttu-id="ca1ac-269">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="ca1ac-269">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="ca1ac-270">새 AzureDns</span><span class="sxs-lookup"><span data-stu-id="ca1ac-270">New-AzureDns</span></span>](./New-AzureDns.md)


