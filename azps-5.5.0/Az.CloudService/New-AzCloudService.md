---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/new-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudService.md
ms.openlocfilehash: 24e90ebae59c9d9a4449c57270b7ca69f9b05b88
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199436"
---
# <span data-ttu-id="ee630-101">New-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="ee630-101">New-AzCloudService</span></span>

## <span data-ttu-id="ee630-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee630-102">SYNOPSIS</span></span>
<span data-ttu-id="ee630-103">클라우드 서비스를 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-103">Create or update a cloud service.</span></span>
<span data-ttu-id="ee630-104">일부 속성은 클라우드 서비스를 만들 때만 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-104">Please note some properties can be set only during cloud service creation.</span></span>

## <span data-ttu-id="ee630-105">구문</span><span class="sxs-lookup"><span data-stu-id="ee630-105">SYNTAX</span></span>

```
New-AzCloudService -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Configuration <String>] [-ConfigurationUrl <String>] [-ExtensionProfile <ICloudServiceExtensionProfile>]
 [-NetworkProfile <ICloudServiceNetworkProfile>] [-OSProfile <ICloudServiceOSProfile>] [-PackageUrl <String>]
 [-RoleProfile <ICloudServiceRoleProfile>] [-StartCloudService] [-Tag <Hashtable>]
 [-UpgradeMode <CloudServiceUpgradeMode>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="ee630-106">설명</span><span class="sxs-lookup"><span data-stu-id="ee630-106">DESCRIPTION</span></span>
<span data-ttu-id="ee630-107">클라우드 서비스를 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-107">Create or update a cloud service.</span></span>
<span data-ttu-id="ee630-108">일부 속성은 클라우드 서비스를 만들 때만 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-108">Please note some properties can be set only during cloud service creation.</span></span>

## <span data-ttu-id="ee630-109">예제</span><span class="sxs-lookup"><span data-stu-id="ee630-109">EXAMPLES</span></span>

### <span data-ttu-id="ee630-110">예제 1: 단일 역할로 새 클라우드 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="ee630-110">Example 1: Create new cloud service with single role</span></span>
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

<span data-ttu-id="ee630-111">위의 명령 집합은 단일 역할로 클라우드 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-111">Above set of commands creates a cloud service with single role</span></span>

### <span data-ttu-id="ee630-112">예제 2: 단일 역할 및 RDP 확장을 사용하여 새 클라우드 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="ee630-112">Example 2: Create new cloud service with single role and RDP extension</span></span>
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

<span data-ttu-id="ee630-113">위의 명령 집합은 단일 역할 및 RDP 확장을 사용하여 클라우드 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-113">Above set of commands creates a cloud service with single role and RDP extension</span></span>

### <span data-ttu-id="ee630-114">예제 3: 단일 역할 및 Key Vault의 인증서를 사용하여 새 클라우드 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="ee630-114">Example 3: Create new cloud service with single role and certificate from key vault</span></span>
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

<span data-ttu-id="ee630-115">위의 명령 집합은 키 자격 증명 모음의 단일 역할 및 인증서를 사용하여 클라우드 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-115">Above set of commands creates a cloud service with single role and certificate from key vault.</span></span>

### <span data-ttu-id="ee630-116">예제 4: 여러 역할 및 확장이 있는 새 클라우드 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="ee630-116">Example 4: Create new cloud service with multiple roles and extensions</span></span>
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

<span data-ttu-id="ee630-117">위의 명령 집합은 키 자격 증명 모음의 단일 역할 및 인증서를 사용하여 클라우드 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-117">Above set of commands creates a cloud service with single role and certificate from key vault.</span></span>

## <span data-ttu-id="ee630-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee630-118">PARAMETERS</span></span>

### <span data-ttu-id="ee630-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee630-119">-AsJob</span></span>
<span data-ttu-id="ee630-120">명령 실행</span><span class="sxs-lookup"><span data-stu-id="ee630-120">Run the command as a job</span></span>

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

### <span data-ttu-id="ee630-121">-Configuration</span><span class="sxs-lookup"><span data-stu-id="ee630-121">-Configuration</span></span>
<span data-ttu-id="ee630-122">클라우드 서비스에 대한 XML 서비스 구성(.cscfg)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-122">Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>

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

### <span data-ttu-id="ee630-123">-ConfigurationUrl</span><span class="sxs-lookup"><span data-stu-id="ee630-123">-ConfigurationUrl</span></span>
<span data-ttu-id="ee630-124">Blob service에서 서비스 구성의 위치를 참조하는 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-124">Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span>
<span data-ttu-id="ee630-125">서비스 패키지 URL은 모든 저장소 계정에서 SAS(공유 액세스 서명) URI일 수 있습니다. 쓰기 전용 속성으로 GET 호출에서 반환되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-125">The service package URL can be Shared Access Signature (SAS) URI from any storage account.This is a write-only property and is not returned in GET calls.</span></span>

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

### <span data-ttu-id="ee630-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee630-126">-DefaultProfile</span></span>
<span data-ttu-id="ee630-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee630-128">-ExtensionProfile</span><span class="sxs-lookup"><span data-stu-id="ee630-128">-ExtensionProfile</span></span>
<span data-ttu-id="ee630-129">클라우드 서비스 확장 프로필을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-129">Describes a cloud service extension profile.</span></span>
<span data-ttu-id="ee630-130">생성을 위해 EXTENSIONPROFILE 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="ee630-130">To construct, see NOTES section for EXTENSIONPROFILE properties and create a hash table.</span></span>

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

### <span data-ttu-id="ee630-131">-Location</span><span class="sxs-lookup"><span data-stu-id="ee630-131">-Location</span></span>
<span data-ttu-id="ee630-132">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-132">Resource location.</span></span>

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

### <span data-ttu-id="ee630-133">-Name</span><span class="sxs-lookup"><span data-stu-id="ee630-133">-Name</span></span>
<span data-ttu-id="ee630-134">클라우드 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-134">Name of the cloud service.</span></span>

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

### <span data-ttu-id="ee630-135">-NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ee630-135">-NetworkProfile</span></span>
<span data-ttu-id="ee630-136">클라우드 서비스에 대한 네트워크 프로필입니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-136">Network Profile for the cloud service.</span></span>
<span data-ttu-id="ee630-137">생성을 위해 NETWORKPROFILE 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="ee630-137">To construct, see NOTES section for NETWORKPROFILE properties and create a hash table.</span></span>

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

### <span data-ttu-id="ee630-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ee630-138">-NoWait</span></span>
<span data-ttu-id="ee630-139">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="ee630-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ee630-140">-OSProfile</span><span class="sxs-lookup"><span data-stu-id="ee630-140">-OSProfile</span></span>
<span data-ttu-id="ee630-141">클라우드 서비스에 대한 OS 프로필을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-141">Describes the OS profile for the cloud service.</span></span>
<span data-ttu-id="ee630-142">구성을 위해 OSPROFILE 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="ee630-142">To construct, see NOTES section for OSPROFILE properties and create a hash table.</span></span>

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

### <span data-ttu-id="ee630-143">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="ee630-143">-PackageUrl</span></span>
<span data-ttu-id="ee630-144">Blob service에서 서비스 패키지의 위치를 참조하는 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-144">Specifies a URL that refers to the location of the service package in the Blob service.</span></span>
<span data-ttu-id="ee630-145">서비스 패키지 URL은 모든 저장소 계정에서 SAS(공유 액세스 서명) URI일 수 있습니다. 쓰기 전용 속성으로 GET 호출에서 반환되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-145">The service package URL can be Shared Access Signature (SAS) URI from any storage account.This is a write-only property and is not returned in GET calls.</span></span>

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

### <span data-ttu-id="ee630-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee630-146">-ResourceGroupName</span></span>
<span data-ttu-id="ee630-147">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-147">Name of the resource group.</span></span>

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

### <span data-ttu-id="ee630-148">-RoleProfile</span><span class="sxs-lookup"><span data-stu-id="ee630-148">-RoleProfile</span></span>
<span data-ttu-id="ee630-149">클라우드 서비스에 대한 역할 프로필을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-149">Describes the role profile for the cloud service.</span></span>
<span data-ttu-id="ee630-150">생성을 위해 ROLEPROFILE 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="ee630-150">To construct, see NOTES section for ROLEPROFILE properties and create a hash table.</span></span>

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

### <span data-ttu-id="ee630-151">-StartCloudService</span><span class="sxs-lookup"><span data-stu-id="ee630-151">-StartCloudService</span></span>
<span data-ttu-id="ee630-152">(선택 사항) 클라우드 서비스를 만든 직후 시작할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-152">(Optional) Indicates whether to start the cloud service immediately after it is created.</span></span>
<span data-ttu-id="ee630-153">기본값은 `true` . false이면 서비스 모델이 여전히 배포되지만 코드는 즉시 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-153">The default value is `true`.If false, the service model is still deployed, but the code is not run immediately.</span></span>
<span data-ttu-id="ee630-154">대신, 서비스가 시작될 때 시작을 호출할 때까지 PoweredOff입니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-154">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span>
<span data-ttu-id="ee630-155">배포된 서비스는 전원이 공급되는 경우에도 요금이 계속 부과됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-155">A deployed service still incurs charges, even if it is poweredoff.</span></span>

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

### <span data-ttu-id="ee630-156">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ee630-156">-SubscriptionId</span></span>
<span data-ttu-id="ee630-157">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-157">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ee630-158">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-158">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ee630-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="ee630-159">-Tag</span></span>
<span data-ttu-id="ee630-160">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="ee630-160">Resource tags.</span></span>

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

### <span data-ttu-id="ee630-161">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="ee630-161">-UpgradeMode</span></span>
<span data-ttu-id="ee630-162">클라우드 서비스에 대한 업데이트 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-162">Update mode for the cloud service.</span></span>
<span data-ttu-id="ee630-163">역할 인스턴스는 서비스가 배포될 때 도메인을 업데이트하기 위해 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-163">Role instances are allocated to update domains when the service is deployed.</span></span>
<span data-ttu-id="ee630-164">업데이트는 각 업데이트 도메인에서 수동으로 시작하거나 모든 업데이트 도메인에서 자동으로 시작할 수 있습니다. 가능한 값은 지정되지 않은 경우 자동 수동 동시 \<br /\> \<br /\>  \<br /\> \<br /\>  \<br /\> \<br /\>  \<br /\> \<br /\> 값으로, 기본값은 자동입니다. Manual로 설정된 경우 PUT UpdateDomain을 호출하여 업데이트를 적용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-164">Updates can be initiated manually in each update domain or initiated automatically in all update domains.Possible Values are \<br /\>\<br /\>**Auto**\<br /\>\<br /\>**Manual** \<br /\>\<br /\>**Simultaneous**\<br /\>\<br /\>If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span>
<span data-ttu-id="ee630-165">자동으로 설정하면 업데이트가 순서대로 각 업데이트 도메인에 자동으로 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-165">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

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

### <span data-ttu-id="ee630-166">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee630-166">-Confirm</span></span>
<span data-ttu-id="ee630-167">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee630-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee630-168">-WhatIf</span></span>
<span data-ttu-id="ee630-169">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ee630-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee630-170">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee630-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee630-171">CommonParameters</span></span>
<span data-ttu-id="ee630-172">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee630-173">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ee630-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee630-174">입력</span><span class="sxs-lookup"><span data-stu-id="ee630-174">INPUTS</span></span>

## <span data-ttu-id="ee630-175">출력</span><span class="sxs-lookup"><span data-stu-id="ee630-175">OUTPUTS</span></span>

### <span data-ttu-id="ee630-176">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span><span class="sxs-lookup"><span data-stu-id="ee630-176">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span></span>

## <span data-ttu-id="ee630-177">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ee630-177">NOTES</span></span>

<span data-ttu-id="ee630-178">별칭</span><span class="sxs-lookup"><span data-stu-id="ee630-178">ALIASES</span></span>

<span data-ttu-id="ee630-179">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="ee630-179">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ee630-180">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-180">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ee630-181">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ee630-181">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ee630-182">EXTENSIONPROFILE: 클라우드 서비스 <ICloudServiceExtensionProfile> 확장 프로필을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-182">EXTENSIONPROFILE <ICloudServiceExtensionProfile>: Describes a cloud service extension profile.</span></span>
  - <span data-ttu-id="ee630-183">`[Extension <IExtension[]>]`: 클라우드 서비스에 대한 확장 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-183">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
    - <span data-ttu-id="ee630-184">`[AutoUpgradeMinorVersion <Boolean?>]`: 플랫폼이 사용 가능해질 때 typeHandlerVersion을 더 높은 부 버전으로 자동으로 업그레이드할 수 있는지 여부를 명시적으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
    - <span data-ttu-id="ee630-185">`[ForceUpdateTag <String>]`: 제공된 공용 및 보호된 설정을 강제 적용하기 위한 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-185">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="ee630-186">태그 값을 변경하면 공용 또는 보호된 설정을 변경하지 않고 확장을 다시 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-186">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="ee630-187">forceUpdateTag가 변경되지 않은 경우 공용 또는 보호된 설정에 대한 업데이트는 처리기에서 계속 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-187">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="ee630-188">forceUpdateTag 또는 공용 또는 보호된 설정이 변경되지 않는 경우 확장은 동일한 시퀀스 번호의 역할 인스턴스로 흐르며, 다시 실행할지 여부는 처리기 구현에 따라 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-188">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
    - <span data-ttu-id="ee630-189">`[Name <String>]`: 확장의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-189">`[Name <String>]`: The name of the extension.</span></span>
    - <span data-ttu-id="ee630-190">`[ProtectedSetting <String>]`: 역할 인스턴스로 보내기 전에 암호화되는 확장에 대한 보호된 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-190">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
    - <span data-ttu-id="ee630-191">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="ee630-191">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
    - <span data-ttu-id="ee630-192">`[Publisher <String>]`: 확장 처리기 게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-192">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
    - <span data-ttu-id="ee630-193">`[RolesAppliedTo <String[]>]`: 이 확장을 적용할 역할의 선택적 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-193">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="ee630-194">속성을 지정하지 않은 경우 또는 '\*'를 지정하면 클라우드 서비스의 모든 역할에 확장이 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-194">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
    - <span data-ttu-id="ee630-195">`[Setting <String>]`: 확장에 대한 공용 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-195">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="ee630-196">JSON 확장의 경우 확장에 대한 JSON 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-196">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="ee630-197">XML 확장(예: RDP)의 경우 확장에 대한 XML 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-197">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
    - <span data-ttu-id="ee630-198">`[SourceVaultId <String>]`: 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="ee630-198">`[SourceVaultId <String>]`: Resource Id</span></span>
    - <span data-ttu-id="ee630-199">`[Type <String>]`: 확장의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-199">`[Type <String>]`: Specifies the type of the extension.</span></span>
    - <span data-ttu-id="ee630-200">`[TypeHandlerVersion <String>]`: 확장의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-200">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="ee630-201">확장의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-201">Specifies the version of the extension.</span></span> <span data-ttu-id="ee630-202">이 요소를 지정하지 않은 경우 또는 값으로 추가(\*)를 사용하는 경우 최신 버전의 확장이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-202">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="ee630-203">값이 주 버전 번호와 부 버전 번호(X.)로 지정된 경우 지정된 주 버전의 최신 부 버전이 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-203">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="ee630-204">주 버전 번호와 부 버전 번호(X.Y)가 지정되면 특정 확장 버전이 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-204">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="ee630-205">버전이 지정된 경우 역할 인스턴스에서 자동 업그레이드가 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-205">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>

<span data-ttu-id="ee630-206">NETWORKPROFILE: <ICloudServiceNetworkProfile> 클라우드 서비스에 대한 네트워크 프로필입니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-206">NETWORKPROFILE <ICloudServiceNetworkProfile>: Network Profile for the cloud service.</span></span>
  - <span data-ttu-id="ee630-207">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: 클라우드 서비스에 대한 부하 균형 조정기 구성 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-207">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
    - <span data-ttu-id="ee630-208">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: IP 목록</span><span class="sxs-lookup"><span data-stu-id="ee630-208">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
      - <span data-ttu-id="ee630-209">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="ee630-209">`[Name <String>]`:</span></span> 
      - <span data-ttu-id="ee630-210">`[PrivateIPAddress <String>]`: 클라우드 서비스에서 참조하는 개인 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-210">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
      - <span data-ttu-id="ee630-211">`[PublicIPAddressId <String>]`: 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="ee630-211">`[PublicIPAddressId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="ee630-212">`[SubnetId <String>]`: 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="ee630-212">`[SubnetId <String>]`: Resource Id</span></span>
    - <span data-ttu-id="ee630-213">`[Name <String>]`: 리소스 이름</span><span class="sxs-lookup"><span data-stu-id="ee630-213">`[Name <String>]`: Resource Name</span></span>
  - <span data-ttu-id="ee630-214">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="ee630-214">`[SwappableCloudService <ISubResource>]`:</span></span> 
    - <span data-ttu-id="ee630-215">`[Id <String>]`: 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="ee630-215">`[Id <String>]`: Resource Id</span></span>

<span data-ttu-id="ee630-216">OSPROFILE: <ICloudServiceOSProfile> 클라우드 서비스에 대한 OS 프로필을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-216">OSPROFILE <ICloudServiceOSProfile>: Describes the OS profile for the cloud service.</span></span>
  - <span data-ttu-id="ee630-217">`[Secret <ICloudServiceVaultSecretGroup[]>]`: 역할 인스턴스에 설치해야 하는 인증서 집합을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-217">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
    - <span data-ttu-id="ee630-218">`[SourceVaultId <String>]`: 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="ee630-218">`[SourceVaultId <String>]`: Resource Id</span></span>
    - <span data-ttu-id="ee630-219">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: 인증서를 포함하는 SourceVault의 키 자격 증명 모음 참조 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-219">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
      - <span data-ttu-id="ee630-220">`[CertificateUrl <String>]`: Key Vault에 비밀로 업로드된 인증서의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-220">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>

<span data-ttu-id="ee630-221">ROLEPROFILE: 클라우드 서비스에 대한 역할 <ICloudServiceRoleProfile> 프로필을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-221">ROLEPROFILE <ICloudServiceRoleProfile>: Describes the role profile for the cloud service.</span></span>
  - <span data-ttu-id="ee630-222">`[Role <ICloudServiceRoleProfileProperties[]>]`: 클라우드 서비스에 대한 역할 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-222">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
    - <span data-ttu-id="ee630-223">`[Name <String>]`: 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-223">`[Name <String>]`: Resource name.</span></span>
    - <span data-ttu-id="ee630-224">`[SkuCapacity <Int64?>]`: 클라우드 서비스의 역할 인스턴스 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-224">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
    - <span data-ttu-id="ee630-225">`[SkuName <String>]`: SKU 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-225">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="ee630-226">참고: 클라우드 서비스가 현재 있는 하드웨어에서 새 SKU가 지원되지 않는 경우 클라우드 서비스를 삭제하고 다시 새로 고치거나 이전 SKU로 다시 이동해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-226">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
    - <span data-ttu-id="ee630-227">`[SkuTier <String>]`: 클라우드 서비스의 계층을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ee630-227">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="ee630-228">가능한 값은</span><span class="sxs-lookup"><span data-stu-id="ee630-228">Possible Values are</span></span> <br /><br /> <span data-ttu-id="ee630-229">**표준**</span><span class="sxs-lookup"><span data-stu-id="ee630-229">**Standard**</span></span> <br /><br /> <span data-ttu-id="ee630-230">**기본**</span><span class="sxs-lookup"><span data-stu-id="ee630-230">**Basic**</span></span>

## <span data-ttu-id="ee630-231">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ee630-231">RELATED LINKS</span></span>

