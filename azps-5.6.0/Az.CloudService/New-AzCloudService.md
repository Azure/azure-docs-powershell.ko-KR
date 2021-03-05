---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/new-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudService.md
ms.openlocfilehash: 607ac4e9854f3871c4a9a0f2859c6f1fe555f392
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983403"
---
# <span data-ttu-id="691ce-101">New-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="691ce-101">New-AzCloudService</span></span>

## <span data-ttu-id="691ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="691ce-102">SYNOPSIS</span></span>
<span data-ttu-id="691ce-103">클라우드 서비스를 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-103">Create or update a cloud service.</span></span>
<span data-ttu-id="691ce-104">일부 속성은 클라우드 서비스 생성 중에만 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-104">Please note some properties can be set only during cloud service creation.</span></span>

## <span data-ttu-id="691ce-105">구문</span><span class="sxs-lookup"><span data-stu-id="691ce-105">SYNTAX</span></span>

```
New-AzCloudService -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Configuration <String>] [-ConfigurationUrl <String>] [-ExtensionProfile <ICloudServiceExtensionProfile>]
 [-NetworkProfile <ICloudServiceNetworkProfile>] [-OSProfile <ICloudServiceOSProfile>] [-PackageUrl <String>]
 [-RoleProfile <ICloudServiceRoleProfile>] [-StartCloudService] [-Tag <Hashtable>]
 [-UpgradeMode <CloudServiceUpgradeMode>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="691ce-106">설명</span><span class="sxs-lookup"><span data-stu-id="691ce-106">DESCRIPTION</span></span>
<span data-ttu-id="691ce-107">클라우드 서비스를 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-107">Create or update a cloud service.</span></span>
<span data-ttu-id="691ce-108">일부 속성은 클라우드 서비스 생성 중에만 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-108">Please note some properties can be set only during cloud service creation.</span></span>

## <span data-ttu-id="691ce-109">예제</span><span class="sxs-lookup"><span data-stu-id="691ce-109">EXAMPLES</span></span>

### <span data-ttu-id="691ce-110">예제 1: 단일 역할로 새 클라우드 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="691ce-110">Example 1: Create new cloud service with single role</span></span>
```powershell
# Create role profile object
PS C:\> $role = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile
```

<span data-ttu-id="691ce-111">위의 명령 집합에서 단일 역할이 있는 클라우드 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-111">Above set of commands creates a cloud service with single role</span></span>

### <span data-ttu-id="691ce-112">예제 2: 단일 역할 및 RDP 확장을 사용하여 새 클라우드 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="691ce-112">Example 2: Create new cloud service with single role and RDP extension</span></span>
```powershell
# Create role profile object
PS C:\> $role = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosoOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Create RDP extension object
PS C:\> $credential = Get-Credential
PS C:\> $expiration = (Get-Date).AddYears(1)
PS C:\> $extension = New-AzCloudServiceRemoteDesktopExtensionObject -Name 'RDPExtension' -Credential $credential -Expiration $expiration -TypeHandlerVersion '1.2.1'
PS C:\> $extensionProfile = @{extension = @($extension)}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile                               `
                  -ExtensionProfile $extensionProfile
```

<span data-ttu-id="691ce-113">위의 명령 집합은 단일 역할 및 RDP 확장을 사용하여 클라우드 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-113">Above set of commands creates a cloud service with single role and RDP extension</span></span>

### <span data-ttu-id="691ce-114">예제 3: 키 자격 증명 모음에서 단일 역할 및 인증서를 사용하여 새 클라우드 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="691ce-114">Example 3: Create new cloud service with single role and certificate from key vault</span></span>
```powershell
# Create role profile object
PS C:\> $role = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role)}

# Create OS profile object
$keyVault = Get-AzKeyVault -ResourceGroupName ContosOrg -VaultName ContosKeyVault
$certificate=Get-AzKeyVaultCertificate -VaultName ContosKeyVault -Name ContosCert
$secretGroup = New-AzCloudServiceVaultSecretGroupObject -Id $keyVault.ResourceId -CertificateUrl $certificate.SecretId
$osProfile = @{secret = @($secretGroup)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile                               `
                  -OSProfile $osProfile
```

<span data-ttu-id="691ce-115">위의 명령 집합은 키 자격 증명 모음의 단일 역할 및 인증서를 사용하여 클라우드 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-115">Above set of commands creates a cloud service with single role and certificate from key vault.</span></span>

### <span data-ttu-id="691ce-116">예제 4: 여러 역할 및 확장을 사용하여 새 클라우드 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="691ce-116">Example 4: Create new cloud service with multiple roles and extensions</span></span>
```powershell
# Create role profile object
PS C:\> $role1 = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $role2 = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoBackend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role1, $role2)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Create RDP extension object
PS C:\> $credential = Get-Credential
PS C:\> $expiration = (Get-Date).AddYears(1)
PS C:\> $rdpExtension = New-AzCloudServiceRemoteDesktopExtensionObject -Name 'RDPExtension' -Credential $credential -Expiration $expiration -TypeHandlerVersion '1.2.1'

# Create Geneva extension object
PS C:\> $genevaExtension = New-AzCloudServiceExtensionObject -Name GenevaExtension -Publisher Microsoft.Azure.Geneva -Type GenevaMonitoringPaaS -TypeHandlerVersion "2.14.0.2"
PS C:\> $extensionProfile = @{extension = @($rdpExtension, $genevaExtension)}

# Add tags
$tag=@{"Owner" = "Contoso"}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile                               `
                  -ExtensionProfile $extensionProfile                           `
                  -Tag $tag
```

<span data-ttu-id="691ce-117">위의 명령 집합은 키 자격 증명 모음의 단일 역할 및 인증서를 사용하여 클라우드 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-117">Above set of commands creates a cloud service with single role and certificate from key vault.</span></span>

## <span data-ttu-id="691ce-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="691ce-118">PARAMETERS</span></span>

### <span data-ttu-id="691ce-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="691ce-119">-AsJob</span></span>
<span data-ttu-id="691ce-120">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-120">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="691ce-121">-Configuration</span><span class="sxs-lookup"><span data-stu-id="691ce-121">-Configuration</span></span>
<span data-ttu-id="691ce-122">클라우드 서비스에 대한 XML 서비스 구성(.cscfg)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-122">Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="691ce-123">-ConfigurationUrl</span><span class="sxs-lookup"><span data-stu-id="691ce-123">-ConfigurationUrl</span></span>
<span data-ttu-id="691ce-124">Blob 서비스의 서비스 구성 위치를 참조하는 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-124">Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span>
<span data-ttu-id="691ce-125">서비스 패키지 URL은 모든 저장소 계정의 SAS(공유 액세스 서명) URI일 수 있습니다. 이 속성은 쓰기 전용 속성으로 GET 호출에서 반환되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-125">The service package URL can be Shared Access Signature (SAS) URI from any storage account.This is a write-only property and is not returned in GET calls.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="691ce-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="691ce-126">-DefaultProfile</span></span>
<span data-ttu-id="691ce-127">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="691ce-128">-ExtensionProfile</span><span class="sxs-lookup"><span data-stu-id="691ce-128">-ExtensionProfile</span></span>
<span data-ttu-id="691ce-129">클라우드 서비스 확장 프로필을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-129">Describes a cloud service extension profile.</span></span>
<span data-ttu-id="691ce-130">생성을 위해 EXTENSIONPROFILE 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="691ce-130">To construct, see NOTES section for EXTENSIONPROFILE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceExtensionProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="691ce-131">-Location</span><span class="sxs-lookup"><span data-stu-id="691ce-131">-Location</span></span>
<span data-ttu-id="691ce-132">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-132">Resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="691ce-133">-Name</span><span class="sxs-lookup"><span data-stu-id="691ce-133">-Name</span></span>
<span data-ttu-id="691ce-134">클라우드 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-134">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="691ce-135">-NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="691ce-135">-NetworkProfile</span></span>
<span data-ttu-id="691ce-136">클라우드 서비스에 대한 네트워크 프로필입니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-136">Network Profile for the cloud service.</span></span>
<span data-ttu-id="691ce-137">생성을 위해 NETWORKPROFILE 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="691ce-137">To construct, see NOTES section for NETWORKPROFILE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceNetworkProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="691ce-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="691ce-138">-NoWait</span></span>
<span data-ttu-id="691ce-139">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="691ce-139">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="691ce-140">-OSProfile</span><span class="sxs-lookup"><span data-stu-id="691ce-140">-OSProfile</span></span>
<span data-ttu-id="691ce-141">클라우드 서비스에 대한 OS 프로필을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-141">Describes the OS profile for the cloud service.</span></span>
<span data-ttu-id="691ce-142">생성을 위해 OSPROFILE 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="691ce-142">To construct, see NOTES section for OSPROFILE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceOSProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="691ce-143">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="691ce-143">-PackageUrl</span></span>
<span data-ttu-id="691ce-144">Blob 서비스에서 서비스 패키지의 위치를 참조하는 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-144">Specifies a URL that refers to the location of the service package in the Blob service.</span></span>
<span data-ttu-id="691ce-145">서비스 패키지 URL은 모든 저장소 계정의 SAS(공유 액세스 서명) URI일 수 있습니다. 이 속성은 쓰기 전용 속성으로 GET 호출에서 반환되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-145">The service package URL can be Shared Access Signature (SAS) URI from any storage account.This is a write-only property and is not returned in GET calls.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="691ce-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="691ce-146">-ResourceGroupName</span></span>
<span data-ttu-id="691ce-147">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-147">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="691ce-148">-RoleProfile</span><span class="sxs-lookup"><span data-stu-id="691ce-148">-RoleProfile</span></span>
<span data-ttu-id="691ce-149">클라우드 서비스의 역할 프로필을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-149">Describes the role profile for the cloud service.</span></span>
<span data-ttu-id="691ce-150">생성을 위해 ROLEPROFILE 속성에 대한 메모 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="691ce-150">To construct, see NOTES section for ROLEPROFILE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceRoleProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="691ce-151">-StartCloudService</span><span class="sxs-lookup"><span data-stu-id="691ce-151">-StartCloudService</span></span>
<span data-ttu-id="691ce-152">(선택 사항) 클라우드 서비스를 만든 직후에 시작할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-152">(Optional) Indicates whether to start the cloud service immediately after it is created.</span></span>
<span data-ttu-id="691ce-153">기본값은 `true` 입니다. false인 경우 서비스 모델이 여전히 배포되지만 코드는 즉시 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-153">The default value is `true`.If false, the service model is still deployed, but the code is not run immediately.</span></span>
<span data-ttu-id="691ce-154">대신 서비스가 시작을 호출할 때까지 PoweredOff가 됩니다. 이 때 서비스가 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-154">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span>
<span data-ttu-id="691ce-155">배포된 서비스는 여전히 전원이 공급되는 경우에도 요금이 청구됩니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-155">A deployed service still incurs charges, even if it is poweredoff.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="691ce-156">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="691ce-156">-SubscriptionId</span></span>
<span data-ttu-id="691ce-157">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-157">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="691ce-158">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-158">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="691ce-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="691ce-159">-Tag</span></span>
<span data-ttu-id="691ce-160">리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-160">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="691ce-161">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="691ce-161">-UpgradeMode</span></span>
<span data-ttu-id="691ce-162">클라우드 서비스에 대한 업데이트 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-162">Update mode for the cloud service.</span></span>
<span data-ttu-id="691ce-163">역할 인스턴스는 서비스가 배포될 때 도메인을 업데이트하기 위해 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-163">Role instances are allocated to update domains when the service is deployed.</span></span>
<span data-ttu-id="691ce-164">업데이트는 각 업데이트 도메인에서 수동으로 시작하거나 모든 업데이트 도메인에서 자동으로 시작할 수 있습니다. 가능한 값은 지정되지 않은 경우 자동 수동 동시 \<br /\> \<br /\>  \<br /\> \<br /\>  \<br /\> \<br /\>  \<br /\> \<br /\> 값입니다. 기본값은 자동입니다. 수동으로 설정하면 업데이트를 적용하려면 PUT UpdateDomain을 호출해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-164">Updates can be initiated manually in each update domain or initiated automatically in all update domains.Possible Values are \<br /\>\<br /\>**Auto**\<br /\>\<br /\>**Manual** \<br /\>\<br /\>**Simultaneous**\<br /\>\<br /\>If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span>
<span data-ttu-id="691ce-165">자동으로 설정하면 업데이트가 순차적으로 각 업데이트 도메인에 자동으로 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-165">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Support.CloudServiceUpgradeMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="691ce-166">-확인</span><span class="sxs-lookup"><span data-stu-id="691ce-166">-Confirm</span></span>
<span data-ttu-id="691ce-167">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-167">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="691ce-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="691ce-168">-WhatIf</span></span>
<span data-ttu-id="691ce-169">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="691ce-170">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-170">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="691ce-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="691ce-171">CommonParameters</span></span>
<span data-ttu-id="691ce-172">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="691ce-173">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="691ce-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="691ce-174">입력</span><span class="sxs-lookup"><span data-stu-id="691ce-174">INPUTS</span></span>

## <span data-ttu-id="691ce-175">출력</span><span class="sxs-lookup"><span data-stu-id="691ce-175">OUTPUTS</span></span>

### <span data-ttu-id="691ce-176">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span><span class="sxs-lookup"><span data-stu-id="691ce-176">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span></span>

## <span data-ttu-id="691ce-177">참고 사항</span><span class="sxs-lookup"><span data-stu-id="691ce-177">NOTES</span></span>

<span data-ttu-id="691ce-178">별칭</span><span class="sxs-lookup"><span data-stu-id="691ce-178">ALIASES</span></span>

<span data-ttu-id="691ce-179">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="691ce-179">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="691ce-180">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-180">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="691ce-181">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="691ce-181">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="691ce-182">EXTENSIONPROFILE : 클라우드 서비스 확장 <ICloudServiceExtensionProfile> 프로필을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-182">EXTENSIONPROFILE <ICloudServiceExtensionProfile>: Describes a cloud service extension profile.</span></span>
  - <span data-ttu-id="691ce-183">`[Extension <IExtension[]>]`: 클라우드 서비스에 대한 확장 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-183">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
    - <span data-ttu-id="691ce-184">`[AutoUpgradeMinorVersion <Boolean?>]`: 플랫폼이 사용할 수 있는 경우 형식HandlerVersion을 더 높은 부 버전으로 자동으로 업그레이드할 수 있는지 여부를 명시적으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
    - <span data-ttu-id="691ce-185">`[ForceUpdateTag <String>]`: 제공된 공용 및 보호된 설정을 강제 적용하려면 태그를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-185">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="691ce-186">태그 값을 변경하면 공개 또는 보호된 설정을 변경하지 않고 확장을 다시 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-186">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="691ce-187">forceUpdateTag가 변경되지 않은 경우 처리기에서 공용 또는 보호된 설정에 대한 업데이트가 계속 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-187">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="691ce-188">ForceUpdateTag 또는 공용 또는 보호된 설정이 변경되지 않은 경우 확장은 동일한 시퀀스 번호가 있는 역할 인스턴스로 흐르며 다시 실행할지 여부를 처리기 구현에 따라 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-188">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
    - <span data-ttu-id="691ce-189">`[Name <String>]`: 확장의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-189">`[Name <String>]`: The name of the extension.</span></span>
    - <span data-ttu-id="691ce-190">`[ProtectedSetting <String>]`: 역할 인스턴스로 보내기 전에 암호화된 확장에 대한 보호된 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-190">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
    - <span data-ttu-id="691ce-191">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="691ce-191">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
    - <span data-ttu-id="691ce-192">`[Publisher <String>]`: 확장 처리기 게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-192">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
    - <span data-ttu-id="691ce-193">`[RolesAppliedTo <String[]>]`: 이 확장을 적용할 역할의 선택적 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-193">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="691ce-194">속성이 지정되지 않은 경우 또는 '\*'가 지정되어 있는 경우 클라우드 서비스의 모든 역할에 확장이 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-194">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
    - <span data-ttu-id="691ce-195">`[Setting <String>]`: 확장에 대한 공용 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-195">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="691ce-196">JSON 확장의 경우 확장에 대한 JSON 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-196">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="691ce-197">XML 확장(예: RDP)의 경우 확장에 대한 XML 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-197">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
    - <span data-ttu-id="691ce-198">`[SourceVaultId <String>]`: 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="691ce-198">`[SourceVaultId <String>]`: Resource Id</span></span>
    - <span data-ttu-id="691ce-199">`[Type <String>]`: 확장의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-199">`[Type <String>]`: Specifies the type of the extension.</span></span>
    - <span data-ttu-id="691ce-200">`[TypeHandlerVersion <String>]`: 확장의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-200">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="691ce-201">확장의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-201">Specifies the version of the extension.</span></span> <span data-ttu-id="691ce-202">이 요소를 지정하지 않은 경우 또는 (\*) 를 값으로 사용하는 경우 확장의 최신 버전이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-202">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="691ce-203">값이 주 버전 번호와 부 버전 번호(X)로 지정된 경우 지정된 주 버전의 최신 부 버전이 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-203">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="691ce-204">주 버전 번호와 부 버전 번호가 지정된 경우(X.Y) 특정 확장 버전이 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-204">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="691ce-205">버전을 지정하면 역할 인스턴스에서 자동 업그레이드가 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-205">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>

<span data-ttu-id="691ce-206">NETWORKPROFILE <ICloudServiceNetworkProfile> : 클라우드 서비스에 대한 네트워크 프로필입니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-206">NETWORKPROFILE <ICloudServiceNetworkProfile>: Network Profile for the cloud service.</span></span>
  - <span data-ttu-id="691ce-207">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: 클라우드 서비스에 대한 부하 균형 조정기 구성 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-207">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
    - <span data-ttu-id="691ce-208">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: IP 목록</span><span class="sxs-lookup"><span data-stu-id="691ce-208">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
      - <span data-ttu-id="691ce-209">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="691ce-209">`[Name <String>]`:</span></span> 
      - <span data-ttu-id="691ce-210">`[PrivateIPAddress <String>]`: 클라우드 서비스에서 참조하는 개인 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-210">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
      - <span data-ttu-id="691ce-211">`[PublicIPAddressId <String>]`: 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="691ce-211">`[PublicIPAddressId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="691ce-212">`[SubnetId <String>]`: 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="691ce-212">`[SubnetId <String>]`: Resource Id</span></span>
    - <span data-ttu-id="691ce-213">`[Name <String>]`: 리소스 이름</span><span class="sxs-lookup"><span data-stu-id="691ce-213">`[Name <String>]`: Resource Name</span></span>
  - <span data-ttu-id="691ce-214">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="691ce-214">`[SwappableCloudService <ISubResource>]`:</span></span> 
    - <span data-ttu-id="691ce-215">`[Id <String>]`: 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="691ce-215">`[Id <String>]`: Resource Id</span></span>

<span data-ttu-id="691ce-216">OSPROFILE <ICloudServiceOSProfile> : 클라우드 서비스에 대한 OS 프로필을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-216">OSPROFILE <ICloudServiceOSProfile>: Describes the OS profile for the cloud service.</span></span>
  - <span data-ttu-id="691ce-217">`[Secret <ICloudServiceVaultSecretGroup[]>]`: 역할 인스턴스에 설치해야 하는 인증서 집합을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-217">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
    - <span data-ttu-id="691ce-218">`[SourceVaultId <String>]`: 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="691ce-218">`[SourceVaultId <String>]`: Resource Id</span></span>
    - <span data-ttu-id="691ce-219">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: 인증서를 포함하는 SourceVault의 주요 자격 증명 모음 참조 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-219">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
      - <span data-ttu-id="691ce-220">`[CertificateUrl <String>]`: Key Vault에 비밀로 업로드된 인증서의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-220">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>

<span data-ttu-id="691ce-221">ROLEPROFILE : 클라우드 서비스에 대한 <ICloudServiceRoleProfile> 역할 프로필을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-221">ROLEPROFILE <ICloudServiceRoleProfile>: Describes the role profile for the cloud service.</span></span>
  - <span data-ttu-id="691ce-222">`[Role <ICloudServiceRoleProfileProperties[]>]`: 클라우드 서비스에 대한 역할 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-222">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
    - <span data-ttu-id="691ce-223">`[Name <String>]`: 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-223">`[Name <String>]`: Resource name.</span></span>
    - <span data-ttu-id="691ce-224">`[SkuCapacity <Int64?>]`: 클라우드 서비스의 역할 인스턴스 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-224">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
    - <span data-ttu-id="691ce-225">`[SkuName <String>]`: sku 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-225">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="691ce-226">참고: 클라우드 서비스가 현재 있는 하드웨어에서 새 SKU가 지원되지 않는 경우 클라우드 서비스를 삭제하고 다시하거나 이전 sku로 다시 이동해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-226">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
    - <span data-ttu-id="691ce-227">`[SkuTier <String>]`: 클라우드 서비스의 계층을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="691ce-227">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="691ce-228">가능한 값은</span><span class="sxs-lookup"><span data-stu-id="691ce-228">Possible Values are</span></span> <br /><br /> <span data-ttu-id="691ce-229">**표준**</span><span class="sxs-lookup"><span data-stu-id="691ce-229">**Standard**</span></span> <br /><br /> <span data-ttu-id="691ce-230">**기본**</span><span class="sxs-lookup"><span data-stu-id="691ce-230">**Basic**</span></span>

## <span data-ttu-id="691ce-231">관련 링크</span><span class="sxs-lookup"><span data-stu-id="691ce-231">RELATED LINKS</span></span>

