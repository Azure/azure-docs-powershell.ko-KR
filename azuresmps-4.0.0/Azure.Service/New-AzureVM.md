---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1999C880-F8F9-4CED-91A9-33E9BBDFE27D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 09a3d7be7bf71e73443dcbb31464ee6f7f19b43a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046200"
---
# <span data-ttu-id="7d801-101">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="7d801-101">New-AzureVM</span></span>

## <span data-ttu-id="7d801-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d801-102">SYNOPSIS</span></span>
<span data-ttu-id="7d801-103">Azure 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7d801-103">Creates an Azure virtual machine.</span></span>

## <span data-ttu-id="7d801-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7d801-104">SYNTAX</span></span>

### <span data-ttu-id="7d801-105">ExistingService (기본값)</span><span class="sxs-lookup"><span data-stu-id="7d801-105">ExistingService (Default)</span></span>
```
New-AzureVM -ServiceName <String> [-DeploymentLabel <String>] [-DeploymentName <String>] [-VNetName <String>]
 [-DnsSettings <DnsServer[]>] [-InternalLoadBalancerConfig <InternalLoadBalancerConfig>] -VMs <PersistentVM[]>
 [-WaitForBoot] [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7d801-106">CreateService</span><span class="sxs-lookup"><span data-stu-id="7d801-106">CreateService</span></span>
```
New-AzureVM -ServiceName <String> [-Location <String>] [-AffinityGroup <String>] [-ServiceLabel <String>]
 [-ReverseDnsFqdn <String>] [-ServiceDescription <String>] [-DeploymentLabel <String>]
 [-DeploymentName <String>] [-VNetName <String>] [-DnsSettings <DnsServer[]>]
 [-InternalLoadBalancerConfig <InternalLoadBalancerConfig>] -VMs <PersistentVM[]> [-WaitForBoot]
 [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7d801-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7d801-107">DESCRIPTION</span></span>
<span data-ttu-id="7d801-108">**뉴욕** cmdlet은 새 가상 컴퓨터를 기존 Azure 서비스에 추가 하거나, *위치* 또는 *AffinityGroup* 가 지정 된 경우 현재 구독에 가상 컴퓨터와 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7d801-108">The **New-AzureVM** cmdlet adds a new virtual machine to an existing Azure service, or creates a virtual machine and service in the current subscription if either the *Location* or *AffinityGroup* is specified.</span></span>

## <span data-ttu-id="7d801-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7d801-109">EXAMPLES</span></span>

### <span data-ttu-id="7d801-110">예제 1: Windows 구성에 대 한 가상 컴퓨터 만들기</span><span class="sxs-lookup"><span data-stu-id="7d801-110">Example 1: Create a virtual machine for a Windows configuration</span></span>
```
PS C:\> New-AzureVMConfig -Name "VirtualMachine07" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[4].ImageName | Add-AzureProvisioningConfig -Windows -Password $adminPassword -AdminUsername PsTestAdmin | New-AzureVM -ServiceName "ContosoService" -AffinityGroup "Contoso" -WaitForBoot
```

<span data-ttu-id="7d801-111">이 명령은 Windows 운영 체제에 대 한 가상 컴퓨터 구성을 기반으로 하는 프로비저닝 구성을 만들고이를 사용 하 여 지정 된 선호도 그룹에 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7d801-111">This command creates a provisioning configuration based on a virtual machine configuration for the Windows operating system, and uses it to create a virtual machine in a specified affinity group.</span></span>

### <span data-ttu-id="7d801-112">예제 2: Linux 용 가상 컴퓨터 만들기 구성</span><span class="sxs-lookup"><span data-stu-id="7d801-112">Example 2: Create a virtual machine for a Linux configuration</span></span>
```
PS C:\> New-AzureVMConfig -Name "SUSEVM02" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[7].ImageName | Add-AzureProvisioningConfig -Linux -LinuxUser "RootMain" -Password "password" -AdminUsername PsTestAdmin | New-AzureVM
```

<span data-ttu-id="7d801-113">이 명령은 Linux에 대 한 가상 컴퓨터 구성을 기반으로 하는 프로비저닝 구성을 만들고이를 사용 하 여 지정 된 선호도 그룹에 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7d801-113">This command creates a provisioning configuration based on a virtual machine configuration for Linux, and uses it to create a virtual machine in a specified affinity group.</span></span>

### <span data-ttu-id="7d801-114">예제 3: 가상 컴퓨터 만들기 및 데이터 디스크 추가</span><span class="sxs-lookup"><span data-stu-id="7d801-114">Example 3: Create a virtual machine and add a data disk</span></span>
```
PS C:\> $Images = Get-AzureVMImage
PS C:\> $Image = $Images[4]
PS C:\> $VirtualMachine02 = New-AzureVMConfig -Name "VirtualMachine02" -InstanceSize ExtraSmall -ImageName $myImage.ImageName | Add-AzureProvisioningConfig -Windows -Password "password" | Add-AzureDataDisk -CreateNew -DiskSizeInGB 50 -DiskLabel "DataDisk50" -LUN 0
```

<span data-ttu-id="7d801-115">처음 두 명령은 **get-AzureVMImage** cmdlet을 사용 하 여 사용할 수 있는 이미지를 가져오고 둘 중 하나를 $Image 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d801-115">The first two commands get available images by using the **Get-AzureVMImage** cmdlet, and stores one of them in the $Image variable.</span></span>

<span data-ttu-id="7d801-116">이 명령은 Windows 운영 체제에 대 한 가상 컴퓨터 구성을 기반으로 하는 프로비저닝 구성을 만들고이를 사용 하 여 Azure data disk를 사용 하 여 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7d801-116">This command creates a provisioning configuration based on a virtual machine configuration for the Windows operating system, and uses it to create a virtual machine with an Azure data disk.</span></span>

### <span data-ttu-id="7d801-117">예제 4: 예약 된 IP 주소를 사용 하 여 가상 컴퓨터 만들기</span><span class="sxs-lookup"><span data-stu-id="7d801-117">Example 4: Create a virtual machine with a reserved IP address</span></span>
```
PS C:\> New-AzureVMConfig -Name "VirtualMachine06" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[4].ImageName | Add-AzureProvisioningConfig -Windows -Password $adminPassword -AdminUsername "AdminMain" | New-AzureVM -ServiceName "ContosoService02" -AffinityGroup "Contoso" -ReservedIPName $ipName
```

<span data-ttu-id="7d801-118">이 명령은 Windows 운영 체제에 대 한 가상 컴퓨터 구성을 기반으로 하는 프로비저닝 구성을 만들고이를 사용 하 여 예약 된 IP 주소를 사용 하 여 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7d801-118">This command creates a provisioning configuration based on a virtual machine configuration for the Windows operating system, and uses it to create a virtual machine with a reserved IP address.</span></span>

## <span data-ttu-id="7d801-119">변수</span><span class="sxs-lookup"><span data-stu-id="7d801-119">PARAMETERS</span></span>

### <span data-ttu-id="7d801-120">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="7d801-120">-AffinityGroup</span></span>
<span data-ttu-id="7d801-121">클라우드 서비스가 상주 하는 Azure 선호도 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d801-121">Specifies the Azure affinity group in which the cloud service resides.</span></span>
<span data-ttu-id="7d801-122">이 매개 변수는이 cmdlet이 클라우드 서비스를 만들 때만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d801-122">This parameter is required only when this cmdlet creates a cloud service.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d801-123">-DeploymentLabel</span><span class="sxs-lookup"><span data-stu-id="7d801-123">-DeploymentLabel</span></span>
<span data-ttu-id="7d801-124">배포에 대 한 레이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d801-124">Specifies a label for the deployment.</span></span>

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

### <span data-ttu-id="7d801-125">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="7d801-125">-DeploymentName</span></span>
<span data-ttu-id="7d801-126">배포 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d801-126">Specifies a deployment name.</span></span>
<span data-ttu-id="7d801-127">지정 하지 않으면이 cmdlet은 배포 이름으로 서비스 이름을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d801-127">If not specified, this cmdlet uses the service name as the deployment name.</span></span>

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

### <span data-ttu-id="7d801-128">-DnsSettings</span><span class="sxs-lookup"><span data-stu-id="7d801-128">-DnsSettings</span></span>
<span data-ttu-id="7d801-129">새 배포에 대 한 DNS 설정을 정의 하는 DNS 서버 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d801-129">Specifies a DNS Server object that defines the DNS settings for the new deployment.</span></span>

```yaml
Type: DnsServer[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d801-130">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="7d801-130">-InformationAction</span></span>
<span data-ttu-id="7d801-131">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d801-131">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7d801-132">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7d801-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7d801-133">하기로</span><span class="sxs-lookup"><span data-stu-id="7d801-133">Continue</span></span>
- <span data-ttu-id="7d801-134">숨기기</span><span class="sxs-lookup"><span data-stu-id="7d801-134">Ignore</span></span>
- <span data-ttu-id="7d801-135">Inquire</span><span class="sxs-lookup"><span data-stu-id="7d801-135">Inquire</span></span>
- <span data-ttu-id="7d801-136">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7d801-136">SilentlyContinue</span></span>
- <span data-ttu-id="7d801-137">중지가</span><span class="sxs-lookup"><span data-stu-id="7d801-137">Stop</span></span>
- <span data-ttu-id="7d801-138">대기</span><span class="sxs-lookup"><span data-stu-id="7d801-138">Suspend</span></span>

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

### <span data-ttu-id="7d801-139">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7d801-139">-InformationVariable</span></span>
<span data-ttu-id="7d801-140">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d801-140">Specifies an information variable.</span></span>

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

### <span data-ttu-id="7d801-141">-InternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="7d801-141">-InternalLoadBalancerConfig</span></span>
<span data-ttu-id="7d801-142">내부 부하 분산 장치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d801-142">Specifies an internal load balancer.</span></span>
<span data-ttu-id="7d801-143">이 매개 변수는 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7d801-143">This parameter is not used.</span></span>

```yaml
Type: InternalLoadBalancerConfig
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d801-144">-위치</span><span class="sxs-lookup"><span data-stu-id="7d801-144">-Location</span></span>
<span data-ttu-id="7d801-145">새 서비스를 호스팅하는 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d801-145">Specifies the location that hosts the new service.</span></span>
<span data-ttu-id="7d801-146">서비스가 이미 있는 경우에는이 매개 변수를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="7d801-146">If the service already exists, do not specify this parameter.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d801-147">-프로필</span><span class="sxs-lookup"><span data-stu-id="7d801-147">-Profile</span></span>
<span data-ttu-id="7d801-148">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d801-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7d801-149">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="7d801-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7d801-150">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="7d801-150">-ReservedIPName</span></span>
<span data-ttu-id="7d801-151">예약 된 IP 주소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d801-151">Specifies the name of the reserved IP address.</span></span>

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

### <span data-ttu-id="7d801-152">-ReverseDnsFqdn</span><span class="sxs-lookup"><span data-stu-id="7d801-152">-ReverseDnsFqdn</span></span>
<span data-ttu-id="7d801-153">역방향 DNS에 대 한 정규화 된 도메인 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d801-153">Specifies the fully-qualified domain name for reverse DNS.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d801-154">-ServiceDescription</span><span class="sxs-lookup"><span data-stu-id="7d801-154">-ServiceDescription</span></span>
<span data-ttu-id="7d801-155">새 서비스에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d801-155">Specifies a description for the new service.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d801-156">-ServiceLabel</span><span class="sxs-lookup"><span data-stu-id="7d801-156">-ServiceLabel</span></span>
<span data-ttu-id="7d801-157">새 서비스에 대 한 레이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d801-157">Specifies a label for the new service.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d801-158">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7d801-158">-ServiceName</span></span>
<span data-ttu-id="7d801-159">새 또는 기존 서비스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d801-159">Specifies the new or existing service name.</span></span>

<span data-ttu-id="7d801-160">서비스가 없으면이 cmdlet이 해당 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7d801-160">If the service does not exist, this cmdlet creates it for you.</span></span>
<span data-ttu-id="7d801-161">*Location* 또는 *AffinityGroup* 매개 변수를 사용 하 여 서비스를 만들 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d801-161">Use the *Location* or *AffinityGroup* parameter to specify where to create the service.</span></span>

<span data-ttu-id="7d801-162">서비스가 존재 하는 경우에는 *위치* 또는 *AffinityGroup* 매개 변수가 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7d801-162">If the service exists, the *Location* or *AffinityGroup* parameter is not needed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d801-163">-Vm</span><span class="sxs-lookup"><span data-stu-id="7d801-163">-VMs</span></span>
<span data-ttu-id="7d801-164">만들 가상 컴퓨터 개체의 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d801-164">Specifies a list of virtual machine objects to create.</span></span>

```yaml
Type: PersistentVM[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d801-165">-VNetName</span><span class="sxs-lookup"><span data-stu-id="7d801-165">-VNetName</span></span>
<span data-ttu-id="7d801-166">이 cmdlet이 가상 컴퓨터를 배포 하는 가상 네트워크 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d801-166">Specifies the virtual network name where this cmdlet deploys the virtual machine.</span></span>

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

### <span data-ttu-id="7d801-167">-WaitForBoot</span><span class="sxs-lookup"><span data-stu-id="7d801-167">-WaitForBoot</span></span>
<span data-ttu-id="7d801-168">이 cmdlet이 가상 머신이 **ReadyRole** state에 도달할 때까지 대기 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d801-168">Specifies that this cmdlet waits for the virtual machine to reach the **ReadyRole** state.</span></span>
<span data-ttu-id="7d801-169">FailedStartingVM, ProvisioningFailed, ProvisioningTimeout 중에 가상 머신이 다음 상태 중 하나에 속하면이 cmdlet이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d801-169">This cmdlet fails if the virtual machine falls in one of the following states while waiting: FailedStartingVM, ProvisioningFailed, ProvisioningTimeout.</span></span>

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

### <span data-ttu-id="7d801-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d801-170">CommonParameters</span></span>
<span data-ttu-id="7d801-171">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d801-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d801-172">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d801-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d801-173">입력</span><span class="sxs-lookup"><span data-stu-id="7d801-173">INPUTS</span></span>

## <span data-ttu-id="7d801-174">출력</span><span class="sxs-lookup"><span data-stu-id="7d801-174">OUTPUTS</span></span>

## <span data-ttu-id="7d801-175">상속자</span><span class="sxs-lookup"><span data-stu-id="7d801-175">NOTES</span></span>

## <span data-ttu-id="7d801-176">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7d801-176">RELATED LINKS</span></span>

[<span data-ttu-id="7d801-177">-AzureDataDisk 추가</span><span class="sxs-lookup"><span data-stu-id="7d801-177">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="7d801-178">추가-AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="7d801-178">Add-AzureProvisioningConfig</span></span>](./Add-AzureProvisioningConfig.md)

[<span data-ttu-id="7d801-179">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="7d801-179">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="7d801-180">새로운 AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="7d801-180">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)


