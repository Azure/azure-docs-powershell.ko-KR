---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/powershell/module/az.customproviders/update-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
ms.openlocfilehash: 0f124d818b95928f12cdc71f60c436f5691f8151
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998732"
---
# <span data-ttu-id="2855f-101">Update-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="2855f-101">Update-AzCustomProvider</span></span>

## <span data-ttu-id="2855f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2855f-102">SYNOPSIS</span></span>
<span data-ttu-id="2855f-103">기존 사용자 지정 리소스 공급자를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2855f-103">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="2855f-104">현재 PATCH를 통해 업데이트할 수 있는 유일한 값은 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="2855f-104">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="2855f-105">구문</span><span class="sxs-lookup"><span data-stu-id="2855f-105">SYNTAX</span></span>

### <span data-ttu-id="2855f-106">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="2855f-106">UpdateExpanded (Default)</span></span>
```
Update-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2855f-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="2855f-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2855f-108">설명</span><span class="sxs-lookup"><span data-stu-id="2855f-108">DESCRIPTION</span></span>
<span data-ttu-id="2855f-109">기존 사용자 지정 리소스 공급자를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2855f-109">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="2855f-110">현재 PATCH를 통해 업데이트할 수 있는 유일한 값은 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="2855f-110">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="2855f-111">예제</span><span class="sxs-lookup"><span data-stu-id="2855f-111">EXAMPLES</span></span>

### <span data-ttu-id="2855f-112">예제 1: 사용자 지정 공급자에 태그 추가</span><span class="sxs-lookup"><span data-stu-id="2855f-112">Example 1: Add Tags to a custom Provider</span></span>
```powershell
PS C:\> Update-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type -Tag @{MyTag="MyValue"} | Format-List

Action            :
Id                : /subscriptions/xxxxx-yyyyy-xxxx-yyyy/resourceGroups/mc-cp01/providers/Microsoft.CustomProviders/resourceproviders/Namespace.Type
Location          : West US 2
Name              : Namespace.Type
ProvisioningState : Succeeded
ResourceType      : {CustomRoute1, associations}
Tag               : Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ResourceTags
Type              : Microsoft.CustomProviders/resourceproviders
Validation        :
```

<span data-ttu-id="2855f-113">사용자 지정 공급자의 태그를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2855f-113">Update the tags of a custom provider.</span></span>

### <span data-ttu-id="2855f-114">예제 2: 배관으로 사용자 지정 공급자 업데이트</span><span class="sxs-lookup"><span data-stu-id="2855f-114">Example 2: Update custom provider with piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type | Update-AzCustomProvider -Tag @{MyTag="MyValue"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="2855f-115">배관을 사용하여 사용자 지정 공급자를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2855f-115">Update a custom provider using piping.</span></span>

## <span data-ttu-id="2855f-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2855f-116">PARAMETERS</span></span>

### <span data-ttu-id="2855f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2855f-117">-DefaultProfile</span></span>
<span data-ttu-id="2855f-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2855f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2855f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2855f-119">-InputObject</span></span>
<span data-ttu-id="2855f-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="2855f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2855f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2855f-121">-Name</span></span>
<span data-ttu-id="2855f-122">리소스 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2855f-122">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2855f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2855f-123">-ResourceGroupName</span></span>
<span data-ttu-id="2855f-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2855f-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2855f-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2855f-125">-SubscriptionId</span></span>
<span data-ttu-id="2855f-126">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2855f-126">The Azure subscription ID.</span></span>
<span data-ttu-id="2855f-127">GUID 형식 문자열입니다(예: 00000000-0000-0000-000000000)입니다.</span><span class="sxs-lookup"><span data-stu-id="2855f-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2855f-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="2855f-128">-Tag</span></span>
<span data-ttu-id="2855f-129">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="2855f-129">Resource tags</span></span>

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

### <span data-ttu-id="2855f-130">-확인</span><span class="sxs-lookup"><span data-stu-id="2855f-130">-Confirm</span></span>
<span data-ttu-id="2855f-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2855f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2855f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2855f-132">-WhatIf</span></span>
<span data-ttu-id="2855f-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="2855f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2855f-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2855f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2855f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2855f-135">CommonParameters</span></span>
<span data-ttu-id="2855f-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2855f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2855f-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2855f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2855f-138">입력</span><span class="sxs-lookup"><span data-stu-id="2855f-138">INPUTS</span></span>

### <span data-ttu-id="2855f-139">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="2855f-139">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="2855f-140">출력</span><span class="sxs-lookup"><span data-stu-id="2855f-140">OUTPUTS</span></span>

### <span data-ttu-id="2855f-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="2855f-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="2855f-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2855f-142">NOTES</span></span>

<span data-ttu-id="2855f-143">별칭</span><span class="sxs-lookup"><span data-stu-id="2855f-143">ALIASES</span></span>

<span data-ttu-id="2855f-144">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="2855f-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2855f-145">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="2855f-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2855f-146">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2855f-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2855f-147">INPUTOBJECT <ICustomProvidersIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="2855f-147">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2855f-148">`[AssociationName <String>]`: 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2855f-148">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="2855f-149">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="2855f-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2855f-150">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2855f-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="2855f-151">`[ResourceProviderName <String>]`: 리소스 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2855f-151">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="2855f-152">`[Scope <String>]`: 연결의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="2855f-152">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="2855f-153">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2855f-153">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="2855f-154">GUID 형식 문자열입니다(예: 00000000-0000-0000-000000000)입니다.</span><span class="sxs-lookup"><span data-stu-id="2855f-154">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="2855f-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2855f-155">RELATED LINKS</span></span>

