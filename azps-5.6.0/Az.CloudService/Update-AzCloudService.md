---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/update-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Update-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Update-AzCloudService.md
ms.openlocfilehash: bb67420e3fbb4479a79c7a837aad3b9a65635d88
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007179"
---
# <span data-ttu-id="89980-101">Update-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="89980-101">Update-AzCloudService</span></span>

## <span data-ttu-id="89980-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89980-102">SYNOPSIS</span></span>
<span data-ttu-id="89980-103">클라우드 서비스를 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="89980-103">Create or update a cloud service.</span></span>
<span data-ttu-id="89980-104">일부 속성은 클라우드 서비스 생성 중에만 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="89980-104">Please note some properties can be set only during cloud service creation.</span></span>

## <span data-ttu-id="89980-105">구문</span><span class="sxs-lookup"><span data-stu-id="89980-105">SYNTAX</span></span>

```
Update-AzCloudService -InputObject <ICloudServiceIdentity> -Parameter <ICloudService>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="89980-106">설명</span><span class="sxs-lookup"><span data-stu-id="89980-106">DESCRIPTION</span></span>
<span data-ttu-id="89980-107">클라우드 서비스를 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="89980-107">Create or update a cloud service.</span></span>
<span data-ttu-id="89980-108">일부 속성은 클라우드 서비스 생성 중에만 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="89980-108">Please note some properties can be set only during cloud service creation.</span></span>

## <span data-ttu-id="89980-109">예제</span><span class="sxs-lookup"><span data-stu-id="89980-109">EXAMPLES</span></span>

### <span data-ttu-id="89980-110">예제 1: 기존 클라우드 서비스에 RDP 확장 추가</span><span class="sxs-lookup"><span data-stu-id="89980-110">Example 1: Add RDP extension to existing cloud service</span></span>
```powershell
# Create RDP extension object
PS C:\> $rdpExtension = New-AzCloudServiceRemoteDesktopExtensionObject -Name "RDPExtension" -Credential $credential -Expiration $expiration -TypeHandlerVersion "1.2.1"
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Add RDP extension to existing cloud service extension object
PS C:\> $cloudService.ExtensionProfile.Extension = $cloudService.ExtensionProfile.Extension + $rdpExtension
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

<span data-ttu-id="89980-111">위의 명령 집합은 ContosOrg라는 리소스 그룹에 속하는 ContosoCS라는 기존 클라우드 서비스에 RDP 확장을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="89980-111">Above set of commands adds a RDP extension to already existing cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="89980-112">예제 2: 클라우드 서비스에서 모든 확장 제거</span><span class="sxs-lookup"><span data-stu-id="89980-112">Example 2: Remove all extensions from cloud service</span></span>
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Set extension to empty list
PS C:\> $cloudService.ExtensionProfile.Extension = @()
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

<span data-ttu-id="89980-113">위의 명령 집합은 ContosOrg라는 리소스 그룹에 속하는 ContosoCS라는 기존 클라우드 서비스에서 모든 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="89980-113">Above set of commands removes all extensions from existing cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="89980-114">예제 3: 클라우드 서비스에서 RDP 확장 제거</span><span class="sxs-lookup"><span data-stu-id="89980-114">Example 3: Remove RDP extension from cloud service</span></span>
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Remove extension by name RDPExtension
PS C:\> $cloudService.ExtensionProfile.Extension = $cloudService.ExtensionProfile.Extension | Where-Object { $_.Name -ne "RDPExtension" }
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

<span data-ttu-id="89980-115">위의 명령 집합은 ContosOrg라는 리소스 그룹에 속하는 ContosoCS라는 기존 클라우드 서비스에서 RDP 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="89980-115">Above set of commands removes RDP extension from existing cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="89980-116">예제 4: Scale-Out/Scale-In 인스턴스</span><span class="sxs-lookup"><span data-stu-id="89980-116">Example 4: Scale-Out / Scale-In role instances</span></span>
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"

# Scale-out all role instance count by 1
PS C:\> $cloudService.RoleProfile.Role | ForEach-Object {$_.SkuCapacity += 1}

# Scale-in ContosoFrontend role instance count by 1
PS C:\> $role = $cloudService.RoleProfile.Role | Where-Object {$_.Name -eq "ContosoFrontend"}
PS C:\> $role.SkuCapacity -= 1

# Update cloud service configuration as per the new role instance count
PS C:\> $cloudService.Configuration = $configuration

# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

<span data-ttu-id="89980-117">위의 명령 집합에서는 ContosOrg라는 리소스 그룹에 속하는 ContosoCS라는 클라우드 서비스에 대한 확장 및 확장 역할 인스턴스 수를 확장하는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="89980-117">Above set of commands shows how to scale-out and scale-in role instance count for cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="89980-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="89980-118">PARAMETERS</span></span>

### <span data-ttu-id="89980-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89980-119">-AsJob</span></span>
<span data-ttu-id="89980-120">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="89980-120">Run the command as a job</span></span>

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

### <span data-ttu-id="89980-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89980-121">-DefaultProfile</span></span>
<span data-ttu-id="89980-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="89980-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89980-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89980-123">-InputObject</span></span>
<span data-ttu-id="89980-124">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="89980-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89980-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="89980-125">-NoWait</span></span>
<span data-ttu-id="89980-126">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="89980-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="89980-127">-매개 변수</span><span class="sxs-lookup"><span data-stu-id="89980-127">-Parameter</span></span>
<span data-ttu-id="89980-128">클라우드 서비스를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="89980-128">Describes the cloud service.</span></span>
<span data-ttu-id="89980-129">구성을 위해 매개 변수 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="89980-129">To construct, see NOTES section for PARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89980-130">-확인</span><span class="sxs-lookup"><span data-stu-id="89980-130">-Confirm</span></span>
<span data-ttu-id="89980-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="89980-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89980-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89980-132">-WhatIf</span></span>
<span data-ttu-id="89980-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="89980-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89980-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="89980-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89980-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89980-135">CommonParameters</span></span>
<span data-ttu-id="89980-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="89980-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89980-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89980-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89980-138">입력</span><span class="sxs-lookup"><span data-stu-id="89980-138">INPUTS</span></span>

### <span data-ttu-id="89980-139">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span><span class="sxs-lookup"><span data-stu-id="89980-139">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span></span>

### <span data-ttu-id="89980-140">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="89980-140">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="89980-141">출력</span><span class="sxs-lookup"><span data-stu-id="89980-141">OUTPUTS</span></span>

### <span data-ttu-id="89980-142">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span><span class="sxs-lookup"><span data-stu-id="89980-142">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span></span>

## <span data-ttu-id="89980-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="89980-143">NOTES</span></span>

<span data-ttu-id="89980-144">별칭</span><span class="sxs-lookup"><span data-stu-id="89980-144">ALIASES</span></span>

<span data-ttu-id="89980-145">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="89980-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="89980-146">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="89980-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="89980-147">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="89980-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="89980-148">INPUTOBJECT <ICloudServiceIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="89980-148">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="89980-149">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="89980-149">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="89980-150">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="89980-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="89980-151">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="89980-151">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="89980-152">`[RoleInstanceName <String>]`: 역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="89980-152">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="89980-153">`[RoleName <String>]`: 역할의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="89980-153">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="89980-154">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="89980-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="89980-155">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="89980-155">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="89980-156">`[UpdateDomain <Int32?>]`: 업데이트 도메인을 식별하는 정수 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="89980-156">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="89980-157">업데이트 도메인은 0 기반 인덱스로 식별됩니다. 첫 번째 업데이트 도메인에는 ID가 0이고, 두 번째 도메인에는 1의 ID가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="89980-157">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

<span data-ttu-id="89980-158">매개 <ICloudService> 변수 : 클라우드 서비스를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="89980-158">PARAMETER <ICloudService>: Describes the cloud service.</span></span>
  - <span data-ttu-id="89980-159">`Location <String>`: 리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="89980-159">`Location <String>`: Resource location.</span></span>
  - <span data-ttu-id="89980-160">`[Configuration <String>]`: 클라우드 서비스에 대한 XML 서비스 구성(.cscfg)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="89980-160">`[Configuration <String>]`: Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>
  - <span data-ttu-id="89980-161">`[ConfigurationUrl <String>]`: Blob 서비스의 서비스 구성 위치를 참조하는 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="89980-161">`[ConfigurationUrl <String>]`: Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span> <span data-ttu-id="89980-162">서비스 패키지 URL은 모든 저장소 계정의 SAS(공유 액세스 서명) URI일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="89980-162">The service package URL  can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="89980-163">이 속성은 쓰기 전용 속성으로 GET 호출에서 반환되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="89980-163">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="89980-164">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: 클라우드 서비스 확장 프로필을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="89980-164">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Describes a cloud service extension profile.</span></span>
    - <span data-ttu-id="89980-165">`[Extension <IExtension[]>]`: 클라우드 서비스에 대한 확장 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="89980-165">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
      - <span data-ttu-id="89980-166">`[AutoUpgradeMinorVersion <Boolean?>]`: 플랫폼이 사용할 수 있는 경우 형식HandlerVersion을 더 높은 부 버전으로 자동으로 업그레이드할 수 있는지 여부를 명시적으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="89980-166">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
      - <span data-ttu-id="89980-167">`[ForceUpdateTag <String>]`: 제공된 공용 및 보호된 설정을 강제 적용하려면 태그를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="89980-167">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="89980-168">태그 값을 변경하면 공개 또는 보호된 설정을 변경하지 않고 확장을 다시 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="89980-168">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="89980-169">forceUpdateTag가 변경되지 않은 경우 처리기에서 공용 또는 보호된 설정에 대한 업데이트가 계속 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="89980-169">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="89980-170">ForceUpdateTag 또는 공용 또는 보호된 설정이 변경되지 않은 경우 확장은 동일한 시퀀스 번호가 있는 역할 인스턴스로 흐르며 다시 실행할지 여부를 처리기 구현에 따라 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="89980-170">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
      - <span data-ttu-id="89980-171">`[Name <String>]`: 확장의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="89980-171">`[Name <String>]`: The name of the extension.</span></span>
      - <span data-ttu-id="89980-172">`[ProtectedSetting <String>]`: 역할 인스턴스로 보내기 전에 암호화된 확장에 대한 보호된 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="89980-172">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
      - <span data-ttu-id="89980-173">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="89980-173">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
      - <span data-ttu-id="89980-174">`[Publisher <String>]`: 확장 처리기 게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="89980-174">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
      - <span data-ttu-id="89980-175">`[RolesAppliedTo <String[]>]`: 이 확장을 적용할 역할의 선택적 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="89980-175">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="89980-176">속성이 지정되지 않은 경우 또는 '\*'가 지정되어 있는 경우 클라우드 서비스의 모든 역할에 확장이 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="89980-176">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
      - <span data-ttu-id="89980-177">`[Setting <String>]`: 확장에 대한 공용 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="89980-177">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="89980-178">JSON 확장의 경우 확장에 대한 JSON 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="89980-178">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="89980-179">XML 확장(예: RDP)의 경우 확장에 대한 XML 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="89980-179">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
      - <span data-ttu-id="89980-180">`[SourceVaultId <String>]`: 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="89980-180">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="89980-181">`[Type <String>]`: 확장의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="89980-181">`[Type <String>]`: Specifies the type of the extension.</span></span>
      - <span data-ttu-id="89980-182">`[TypeHandlerVersion <String>]`: 확장의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="89980-182">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="89980-183">확장의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="89980-183">Specifies the version of the extension.</span></span> <span data-ttu-id="89980-184">이 요소를 지정하지 않은 경우 또는 (\*) 를 값으로 사용하는 경우 확장의 최신 버전이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="89980-184">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="89980-185">값이 주 버전 번호와 부 버전 번호(X)로 지정된 경우 지정된 주 버전의 최신 부 버전이 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="89980-185">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="89980-186">주 버전 번호와 부 버전 번호가 지정된 경우(X.Y) 특정 확장 버전이 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="89980-186">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="89980-187">버전을 지정하면 역할 인스턴스에서 자동 업그레이드가 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="89980-187">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>
  - <span data-ttu-id="89980-188">`[NetworkProfile <ICloudServiceNetworkProfile>]`: 클라우드 서비스에 대한 네트워크 프로필입니다.</span><span class="sxs-lookup"><span data-stu-id="89980-188">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Network Profile for the cloud service.</span></span>
    - <span data-ttu-id="89980-189">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: 클라우드 서비스에 대한 부하 균형 조정기 구성 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="89980-189">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
      - <span data-ttu-id="89980-190">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: IP 목록</span><span class="sxs-lookup"><span data-stu-id="89980-190">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
        - <span data-ttu-id="89980-191">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="89980-191">`[Name <String>]`:</span></span> 
        - <span data-ttu-id="89980-192">`[PrivateIPAddress <String>]`: 클라우드 서비스에서 참조하는 개인 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="89980-192">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
        - <span data-ttu-id="89980-193">`[PublicIPAddressId <String>]`: 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="89980-193">`[PublicIPAddressId <String>]`: Resource Id</span></span>
        - <span data-ttu-id="89980-194">`[SubnetId <String>]`: 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="89980-194">`[SubnetId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="89980-195">`[Name <String>]`: 리소스 이름</span><span class="sxs-lookup"><span data-stu-id="89980-195">`[Name <String>]`: Resource Name</span></span>
    - <span data-ttu-id="89980-196">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="89980-196">`[SwappableCloudService <ISubResource>]`:</span></span> 
      - <span data-ttu-id="89980-197">`[Id <String>]`: 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="89980-197">`[Id <String>]`: Resource Id</span></span>
  - <span data-ttu-id="89980-198">`[OSProfile <ICloudServiceOSProfile>]`: 클라우드 서비스에 대한 OS 프로필을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="89980-198">`[OSProfile <ICloudServiceOSProfile>]`: Describes the OS profile for the cloud service.</span></span>
    - <span data-ttu-id="89980-199">`[Secret <ICloudServiceVaultSecretGroup[]>]`: 역할 인스턴스에 설치해야 하는 인증서 집합을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="89980-199">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
      - <span data-ttu-id="89980-200">`[SourceVaultId <String>]`: 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="89980-200">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="89980-201">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: 인증서를 포함하는 SourceVault의 주요 자격 증명 모음 참조 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="89980-201">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
        - <span data-ttu-id="89980-202">`[CertificateUrl <String>]`: Key Vault에 비밀로 업로드된 인증서의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="89980-202">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
  - <span data-ttu-id="89980-203">`[PackageUrl <String>]`: Blob 서비스에서 서비스 패키지의 위치를 참조하는 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="89980-203">`[PackageUrl <String>]`: Specifies a URL that refers to the location of the service package in the Blob service.</span></span> <span data-ttu-id="89980-204">서비스 패키지 URL은 모든 저장소 계정의 SAS(공유 액세스 서명) URI일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="89980-204">The service package URL can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="89980-205">이 속성은 쓰기 전용 속성으로 GET 호출에서 반환되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="89980-205">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="89980-206">`[RoleProfile <ICloudServiceRoleProfile>]`: 클라우드 서비스의 역할 프로필을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="89980-206">`[RoleProfile <ICloudServiceRoleProfile>]`: Describes the role profile for the cloud service.</span></span>
    - <span data-ttu-id="89980-207">`[Role <ICloudServiceRoleProfileProperties[]>]`: 클라우드 서비스에 대한 역할 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="89980-207">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
      - <span data-ttu-id="89980-208">`[Name <String>]`: 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="89980-208">`[Name <String>]`: Resource name.</span></span>
      - <span data-ttu-id="89980-209">`[SkuCapacity <Int64?>]`: 클라우드 서비스의 역할 인스턴스 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="89980-209">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
      - <span data-ttu-id="89980-210">`[SkuName <String>]`: sku 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="89980-210">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="89980-211">참고: 클라우드 서비스가 현재 있는 하드웨어에서 새 SKU가 지원되지 않는 경우 클라우드 서비스를 삭제하고 다시하거나 이전 sku로 다시 이동해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="89980-211">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
      - <span data-ttu-id="89980-212">`[SkuTier <String>]`: 클라우드 서비스의 계층을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="89980-212">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="89980-213">가능한 값은</span><span class="sxs-lookup"><span data-stu-id="89980-213">Possible Values are</span></span> <br /><br /> <span data-ttu-id="89980-214">**표준**</span><span class="sxs-lookup"><span data-stu-id="89980-214">**Standard**</span></span> <br /><br /> <span data-ttu-id="89980-215">**기본**</span><span class="sxs-lookup"><span data-stu-id="89980-215">**Basic**</span></span>
  - <span data-ttu-id="89980-216">`[StartCloudService <Boolean?>]`: (선택 사항) 클라우드 서비스를 만들자마자 시작할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="89980-216">`[StartCloudService <Boolean?>]`: (Optional) Indicates whether to start the cloud service immediately after it is created.</span></span> <span data-ttu-id="89980-217">기본값은 `true` 입니다.</span><span class="sxs-lookup"><span data-stu-id="89980-217">The default value is `true`.</span></span>         <span data-ttu-id="89980-218">false인 경우 서비스 모델이 여전히 배포되지만 코드는 즉시 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="89980-218">If false, the service model is still deployed, but the code is not run immediately.</span></span> <span data-ttu-id="89980-219">대신 서비스가 시작을 호출할 때까지 PoweredOff가 됩니다. 이 때 서비스가 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="89980-219">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span> <span data-ttu-id="89980-220">배포된 서비스는 여전히 전원이 공급되는 경우에도 요금이 청구됩니다.</span><span class="sxs-lookup"><span data-stu-id="89980-220">A deployed service still incurs charges, even if it is poweredoff.</span></span>
  - <span data-ttu-id="89980-221">`[Tag <ICloudServiceTags>]`: 리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="89980-221">`[Tag <ICloudServiceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="89980-222">`[(Any) <String>]`: 이 개체에 속성을 추가할 수 있는 경우를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="89980-222">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="89980-223">`[UpgradeMode <CloudServiceUpgradeMode?>]`: 클라우드 서비스에 대한 업데이트 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="89980-223">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Update mode for the cloud service.</span></span> <span data-ttu-id="89980-224">역할 인스턴스는 서비스가 배포될 때 도메인을 업데이트하기 위해 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="89980-224">Role instances are allocated to update domains when the service is deployed.</span></span> <span data-ttu-id="89980-225">업데이트는 각 업데이트 도메인에서 수동으로 시작하거나 모든 업데이트 도메인에서 자동으로 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="89980-225">Updates can be initiated manually in each update domain or initiated automatically in all update domains.</span></span>         <span data-ttu-id="89980-226">가능한 값은</span><span class="sxs-lookup"><span data-stu-id="89980-226">Possible Values are</span></span> <br /><br /><span data-ttu-id="89980-227">**자동**</span><span class="sxs-lookup"><span data-stu-id="89980-227">**Auto**</span></span><br /><br /><span data-ttu-id="89980-228">**수동**</span><span class="sxs-lookup"><span data-stu-id="89980-228">**Manual**</span></span> <br /><br /><span data-ttu-id="89980-229">**동시**</span><span class="sxs-lookup"><span data-stu-id="89980-229">**Simultaneous**</span></span><br /><br />         <span data-ttu-id="89980-230">지정하지 않으면 기본값은 자동입니다. 수동으로 설정하면 업데이트를 적용하려면 PUT UpdateDomain을 호출해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="89980-230">If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span> <span data-ttu-id="89980-231">자동으로 설정하면 업데이트가 순차적으로 각 업데이트 도메인에 자동으로 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="89980-231">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

## <span data-ttu-id="89980-232">관련 링크</span><span class="sxs-lookup"><span data-stu-id="89980-232">RELATED LINKS</span></span>

