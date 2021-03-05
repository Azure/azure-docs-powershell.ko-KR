---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/Switch-AzCloudService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Switch-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Switch-AzCloudService.md
ms.openlocfilehash: b46ab9b8dee108f6d2126c199e5609d92452b95a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007211"
---
# <span data-ttu-id="a4d2f-101">Switch-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="a4d2f-101">Switch-AzCloudService</span></span>

## <span data-ttu-id="a4d2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4d2f-102">SYNOPSIS</span></span>
<span data-ttu-id="a4d2f-103">두 클라우드 서비스(확장 지원) 부하 균형 조정기 간에 VIP를 교환합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-103">Swaps VIPs between two cloud service (extended support) load balancers.</span></span>

## <span data-ttu-id="a4d2f-104">구문</span><span class="sxs-lookup"><span data-stu-id="a4d2f-104">SYNTAX</span></span>

### <span data-ttu-id="a4d2f-105">CloudServiceName(기본값)</span><span class="sxs-lookup"><span data-stu-id="a4d2f-105">CloudServiceName (Default)</span></span>
```
Switch-AzCloudService -CloudServiceName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Async] [-DefaultProfile <PSObject>] [-AsJob] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a4d2f-106">CloudService</span><span class="sxs-lookup"><span data-stu-id="a4d2f-106">CloudService</span></span>
```
Switch-AzCloudService -CloudService <CloudService> [-SubscriptionId <String>] [-Async]
 [-DefaultProfile <PSObject>] [-AsJob] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a4d2f-107">설명</span><span class="sxs-lookup"><span data-stu-id="a4d2f-107">DESCRIPTION</span></span>
<span data-ttu-id="a4d2f-108">두 클라우드 서비스(확장 지원) 부하 균형 조정기 간에 VIP를 교환합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-108">Swaps VIPs between two cloud service (extended support) load balancers.</span></span>

## <span data-ttu-id="a4d2f-109">예제</span><span class="sxs-lookup"><span data-stu-id="a4d2f-109">EXAMPLES</span></span>

### <span data-ttu-id="a4d2f-110">예제 1: 이름을 사용하여 클라우드 서비스 전환</span><span class="sxs-lookup"><span data-stu-id="a4d2f-110">Example 1: Switch cloud service using name</span></span>
```powershell
PS C:\> Switch-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca

```

<span data-ttu-id="a4d2f-111">위의 명령은 'BService'를 사용하여 클라우드 서비스의 vipswap 작업을 호출하고 사용자가 확인 프롬프트에 대한 작업을 확인하면 작업을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-111">Above command invokes the vipswap operation on the Cloud service with name 'BService' and will perform the operation once the user confirms the action on the confirmation prompt.</span></span>
<span data-ttu-id="a4d2f-112">'BService'와 교환 가능한 클라우드 서비스로 교환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-112">'BService' with be swapped with its swappable cloud service.</span></span>

### <span data-ttu-id="a4d2f-113">예제 2: 클라우드 서비스 개체를 사용하여 클라우드 서비스 전환</span><span class="sxs-lookup"><span data-stu-id="a4d2f-113">Example 2: Switch cloud service using cloud service object</span></span>
```powershell
PS C:\> $cs = Get-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca
PS C:\> Switch-AzCloudService -CloudService $cs

```

<span data-ttu-id="a4d2f-114">위의 명령은 'BService'를 사용하여 클라우드 서비스의 vipswap 작업을 호출하고 사용자가 확인 프롬프트에 대한 작업을 확인하면 작업을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-114">Above command invokes the vipswap operation on the Cloud service with name 'BService' and will perform the operation once the user confirms the action on the confirmation prompt.</span></span>
<span data-ttu-id="a4d2f-115">'BService'와 교환 가능한 클라우드 서비스로 교환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-115">'BService' with be swapped with its swappable cloud service.</span></span>

## <span data-ttu-id="a4d2f-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a4d2f-116">PARAMETERS</span></span>

### <span data-ttu-id="a4d2f-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4d2f-117">-AsJob</span></span>
<span data-ttu-id="a4d2f-118">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-118">Run the command as a job</span></span>

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

### <span data-ttu-id="a4d2f-119">-비동기</span><span class="sxs-lookup"><span data-stu-id="a4d2f-119">-Async</span></span>


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

### <span data-ttu-id="a4d2f-120">-CloudService</span><span class="sxs-lookup"><span data-stu-id="a4d2f-120">-CloudService</span></span>
<span data-ttu-id="a4d2f-121">생성을 위해 CLOUDSERVICE 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-121">To construct, see NOTES section for CLOUDSERVICE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudService
Parameter Sets: CloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4d2f-122">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="a4d2f-122">-CloudServiceName</span></span>


```yaml
Type: System.String
Parameter Sets: CloudServiceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4d2f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4d2f-123">-DefaultProfile</span></span>
<span data-ttu-id="a4d2f-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4d2f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4d2f-125">-ResourceGroupName</span></span>


```yaml
Type: System.String
Parameter Sets: CloudServiceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4d2f-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a4d2f-126">-SubscriptionId</span></span>
<span data-ttu-id="a4d2f-127">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-127">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a4d2f-128">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a4d2f-129">-확인</span><span class="sxs-lookup"><span data-stu-id="a4d2f-129">-Confirm</span></span>
<span data-ttu-id="a4d2f-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4d2f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4d2f-131">-WhatIf</span></span>
<span data-ttu-id="a4d2f-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4d2f-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4d2f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4d2f-134">CommonParameters</span></span>
<span data-ttu-id="a4d2f-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4d2f-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a4d2f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4d2f-137">입력</span><span class="sxs-lookup"><span data-stu-id="a4d2f-137">INPUTS</span></span>

## <span data-ttu-id="a4d2f-138">출력</span><span class="sxs-lookup"><span data-stu-id="a4d2f-138">OUTPUTS</span></span>

### <span data-ttu-id="a4d2f-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a4d2f-139">System.Boolean</span></span>

## <span data-ttu-id="a4d2f-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a4d2f-140">NOTES</span></span>

<span data-ttu-id="a4d2f-141">별칭</span><span class="sxs-lookup"><span data-stu-id="a4d2f-141">ALIASES</span></span>

<span data-ttu-id="a4d2f-142">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="a4d2f-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a4d2f-143">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a4d2f-144">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a4d2f-145">CLOUDSERVICE <CloudService> :</span><span class="sxs-lookup"><span data-stu-id="a4d2f-145">CLOUDSERVICE <CloudService>:</span></span> 
  - <span data-ttu-id="a4d2f-146">`Location <String>`: 리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-146">`Location <String>`: Resource location.</span></span>
  - <span data-ttu-id="a4d2f-147">`[Configuration <String>]`: 클라우드 서비스에 대한 XML 서비스 구성(.cscfg)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-147">`[Configuration <String>]`: Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>
  - <span data-ttu-id="a4d2f-148">`[ConfigurationUrl <String>]`: Blob 서비스의 서비스 구성 위치를 참조하는 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-148">`[ConfigurationUrl <String>]`: Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span> <span data-ttu-id="a4d2f-149">서비스 패키지 URL은 모든 저장소 계정의 SAS(공유 액세스 서명) URI일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-149">The service package URL  can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="a4d2f-150">이 속성은 쓰기 전용 속성으로 GET 호출에서 반환되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-150">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="a4d2f-151">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: 클라우드 서비스 확장 프로필을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-151">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Describes a cloud service extension profile.</span></span>
    - <span data-ttu-id="a4d2f-152">`[Extension <IExtension[]>]`: 클라우드 서비스에 대한 확장 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-152">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
      - <span data-ttu-id="a4d2f-153">`[AutoUpgradeMinorVersion <Boolean?>]`: 플랫폼이 사용할 수 있는 경우 형식HandlerVersion을 더 높은 부 버전으로 자동으로 업그레이드할 수 있는지 여부를 명시적으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-153">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
      - <span data-ttu-id="a4d2f-154">`[ForceUpdateTag <String>]`: 제공된 공용 및 보호된 설정을 강제 적용하려면 태그를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-154">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="a4d2f-155">태그 값을 변경하면 공개 또는 보호된 설정을 변경하지 않고 확장을 다시 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-155">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="a4d2f-156">forceUpdateTag가 변경되지 않은 경우 처리기에서 공용 또는 보호된 설정에 대한 업데이트가 계속 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-156">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="a4d2f-157">ForceUpdateTag 또는 공용 또는 보호된 설정이 변경되지 않은 경우 확장은 동일한 시퀀스 번호가 있는 역할 인스턴스로 흐르며 다시 실행할지 여부를 처리기 구현에 따라 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-157">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
      - <span data-ttu-id="a4d2f-158">`[Name <String>]`: 확장의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-158">`[Name <String>]`: The name of the extension.</span></span>
      - <span data-ttu-id="a4d2f-159">`[ProtectedSetting <String>]`: 역할 인스턴스로 보내기 전에 암호화된 확장에 대한 보호된 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-159">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
      - <span data-ttu-id="a4d2f-160">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="a4d2f-160">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
      - <span data-ttu-id="a4d2f-161">`[Publisher <String>]`: 확장 처리기 게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-161">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
      - <span data-ttu-id="a4d2f-162">`[RolesAppliedTo <String[]>]`: 이 확장을 적용할 역할의 선택적 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-162">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="a4d2f-163">속성이 지정되지 않은 경우 또는 '\*'가 지정되어 있는 경우 클라우드 서비스의 모든 역할에 확장이 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-163">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
      - <span data-ttu-id="a4d2f-164">`[Setting <String>]`: 확장에 대한 공용 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-164">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="a4d2f-165">JSON 확장의 경우 확장에 대한 JSON 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-165">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="a4d2f-166">XML 확장(예: RDP)의 경우 확장에 대한 XML 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-166">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
      - <span data-ttu-id="a4d2f-167">`[SourceVaultId <String>]`: 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="a4d2f-167">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="a4d2f-168">`[Type <String>]`: 확장의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-168">`[Type <String>]`: Specifies the type of the extension.</span></span>
      - <span data-ttu-id="a4d2f-169">`[TypeHandlerVersion <String>]`: 확장의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-169">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="a4d2f-170">확장의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-170">Specifies the version of the extension.</span></span> <span data-ttu-id="a4d2f-171">이 요소를 지정하지 않은 경우 또는 (\*) 를 값으로 사용하는 경우 확장의 최신 버전이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-171">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="a4d2f-172">값이 주 버전 번호와 부 버전 번호(X)로 지정된 경우 지정된 주 버전의 최신 부 버전이 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-172">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="a4d2f-173">주 버전 번호와 부 버전 번호가 지정된 경우(X.Y) 특정 확장 버전이 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-173">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="a4d2f-174">버전을 지정하면 역할 인스턴스에서 자동 업그레이드가 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-174">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>
  - <span data-ttu-id="a4d2f-175">`[NetworkProfile <ICloudServiceNetworkProfile>]`: 클라우드 서비스에 대한 네트워크 프로필입니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-175">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Network Profile for the cloud service.</span></span>
    - <span data-ttu-id="a4d2f-176">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: 클라우드 서비스에 대한 부하 균형 조정기 구성 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-176">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
      - <span data-ttu-id="a4d2f-177">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: IP 목록</span><span class="sxs-lookup"><span data-stu-id="a4d2f-177">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
        - <span data-ttu-id="a4d2f-178">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="a4d2f-178">`[Name <String>]`:</span></span> 
        - <span data-ttu-id="a4d2f-179">`[PrivateIPAddress <String>]`: 클라우드 서비스에서 참조하는 개인 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-179">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
        - <span data-ttu-id="a4d2f-180">`[PublicIPAddressId <String>]`: 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="a4d2f-180">`[PublicIPAddressId <String>]`: Resource Id</span></span>
        - <span data-ttu-id="a4d2f-181">`[SubnetId <String>]`: 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="a4d2f-181">`[SubnetId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="a4d2f-182">`[Name <String>]`: 리소스 이름</span><span class="sxs-lookup"><span data-stu-id="a4d2f-182">`[Name <String>]`: Resource Name</span></span>
    - <span data-ttu-id="a4d2f-183">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="a4d2f-183">`[SwappableCloudService <ISubResource>]`:</span></span> 
      - <span data-ttu-id="a4d2f-184">`[Id <String>]`: 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="a4d2f-184">`[Id <String>]`: Resource Id</span></span>
  - <span data-ttu-id="a4d2f-185">`[OSProfile <ICloudServiceOSProfile>]`: 클라우드 서비스에 대한 OS 프로필을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-185">`[OSProfile <ICloudServiceOSProfile>]`: Describes the OS profile for the cloud service.</span></span>
    - <span data-ttu-id="a4d2f-186">`[Secret <ICloudServiceVaultSecretGroup[]>]`: 역할 인스턴스에 설치해야 하는 인증서 집합을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-186">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
      - <span data-ttu-id="a4d2f-187">`[SourceVaultId <String>]`: 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="a4d2f-187">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="a4d2f-188">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: 인증서를 포함하는 SourceVault의 주요 자격 증명 모음 참조 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-188">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
        - <span data-ttu-id="a4d2f-189">`[CertificateUrl <String>]`: Key Vault에 비밀로 업로드된 인증서의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-189">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
  - <span data-ttu-id="a4d2f-190">`[PackageUrl <String>]`: Blob 서비스에서 서비스 패키지의 위치를 참조하는 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-190">`[PackageUrl <String>]`: Specifies a URL that refers to the location of the service package in the Blob service.</span></span> <span data-ttu-id="a4d2f-191">서비스 패키지 URL은 모든 저장소 계정의 SAS(공유 액세스 서명) URI일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-191">The service package URL can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="a4d2f-192">이 속성은 쓰기 전용 속성으로 GET 호출에서 반환되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-192">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="a4d2f-193">`[RoleProfile <ICloudServiceRoleProfile>]`: 클라우드 서비스의 역할 프로필을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-193">`[RoleProfile <ICloudServiceRoleProfile>]`: Describes the role profile for the cloud service.</span></span>
    - <span data-ttu-id="a4d2f-194">`[Role <ICloudServiceRoleProfileProperties[]>]`: 클라우드 서비스에 대한 역할 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-194">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
      - <span data-ttu-id="a4d2f-195">`[Name <String>]`: 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-195">`[Name <String>]`: Resource name.</span></span>
      - <span data-ttu-id="a4d2f-196">`[SkuCapacity <Int64?>]`: 클라우드 서비스의 역할 인스턴스 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-196">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
      - <span data-ttu-id="a4d2f-197">`[SkuName <String>]`: sku 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-197">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="a4d2f-198">참고: 클라우드 서비스가 현재 있는 하드웨어에서 새 SKU가 지원되지 않는 경우 클라우드 서비스를 삭제하고 다시하거나 이전 sku로 다시 이동해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-198">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
      - <span data-ttu-id="a4d2f-199">`[SkuTier <String>]`: 클라우드 서비스의 계층을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-199">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="a4d2f-200">가능한 값은</span><span class="sxs-lookup"><span data-stu-id="a4d2f-200">Possible Values are</span></span> <br /><br /> <span data-ttu-id="a4d2f-201">**표준**</span><span class="sxs-lookup"><span data-stu-id="a4d2f-201">**Standard**</span></span> <br /><br /> <span data-ttu-id="a4d2f-202">**기본**</span><span class="sxs-lookup"><span data-stu-id="a4d2f-202">**Basic**</span></span>
  - <span data-ttu-id="a4d2f-203">`[StartCloudService <Boolean?>]`: (선택 사항) 클라우드 서비스를 만들자마자 시작할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-203">`[StartCloudService <Boolean?>]`: (Optional) Indicates whether to start the cloud service immediately after it is created.</span></span> <span data-ttu-id="a4d2f-204">기본값은 `true` 입니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-204">The default value is `true`.</span></span>         <span data-ttu-id="a4d2f-205">false인 경우 서비스 모델이 여전히 배포되지만 코드는 즉시 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-205">If false, the service model is still deployed, but the code is not run immediately.</span></span> <span data-ttu-id="a4d2f-206">대신 서비스가 시작을 호출할 때까지 PoweredOff가 됩니다. 이 때 서비스가 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-206">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span> <span data-ttu-id="a4d2f-207">배포된 서비스는 여전히 전원이 공급되는 경우에도 요금이 청구됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-207">A deployed service still incurs charges, even if it is poweredoff.</span></span>
  - <span data-ttu-id="a4d2f-208">`[Tag <ICloudServiceTags>]`: 리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-208">`[Tag <ICloudServiceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="a4d2f-209">`[(Any) <String>]`: 이 개체에 속성을 추가할 수 있는 경우를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-209">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="a4d2f-210">`[UpgradeMode <CloudServiceUpgradeMode?>]`: 클라우드 서비스에 대한 업데이트 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-210">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Update mode for the cloud service.</span></span> <span data-ttu-id="a4d2f-211">역할 인스턴스는 서비스가 배포될 때 도메인을 업데이트하기 위해 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-211">Role instances are allocated to update domains when the service is deployed.</span></span> <span data-ttu-id="a4d2f-212">업데이트는 각 업데이트 도메인에서 수동으로 시작하거나 모든 업데이트 도메인에서 자동으로 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-212">Updates can be initiated manually in each update domain or initiated automatically in all update domains.</span></span>         <span data-ttu-id="a4d2f-213">가능한 값은</span><span class="sxs-lookup"><span data-stu-id="a4d2f-213">Possible Values are</span></span> <br /><br /><span data-ttu-id="a4d2f-214">**자동**</span><span class="sxs-lookup"><span data-stu-id="a4d2f-214">**Auto**</span></span><br /><br /><span data-ttu-id="a4d2f-215">**수동**</span><span class="sxs-lookup"><span data-stu-id="a4d2f-215">**Manual**</span></span> <br /><br /><span data-ttu-id="a4d2f-216">**동시**</span><span class="sxs-lookup"><span data-stu-id="a4d2f-216">**Simultaneous**</span></span><br /><br />         <span data-ttu-id="a4d2f-217">지정하지 않으면 기본값은 자동입니다. 수동으로 설정하면 업데이트를 적용하려면 PUT UpdateDomain을 호출해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-217">If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span> <span data-ttu-id="a4d2f-218">자동으로 설정하면 업데이트가 순차적으로 각 업데이트 도메인에 자동으로 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4d2f-218">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

## <span data-ttu-id="a4d2f-219">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a4d2f-219">RELATED LINKS</span></span>

