---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/update-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
ms.openlocfilehash: 6691586d454952f92d71a26d5b8ed02904f37bf8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351974"
---
# <span data-ttu-id="a4e78-101">Update-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="a4e78-101">Update-AzCustomProvider</span></span>

## <span data-ttu-id="a4e78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4e78-102">SYNOPSIS</span></span>
<span data-ttu-id="a4e78-103">기존 사용자 지정 리소스 공급자를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a4e78-103">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="a4e78-104">현재 PATCH를 통해 업데이트할 수 있는 유일한 값은 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="a4e78-104">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="a4e78-105">구문</span><span class="sxs-lookup"><span data-stu-id="a4e78-105">SYNTAX</span></span>

### <span data-ttu-id="a4e78-106">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="a4e78-106">UpdateExpanded (Default)</span></span>
```
Update-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a4e78-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a4e78-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a4e78-108">설명</span><span class="sxs-lookup"><span data-stu-id="a4e78-108">DESCRIPTION</span></span>
<span data-ttu-id="a4e78-109">기존 사용자 지정 리소스 공급자를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a4e78-109">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="a4e78-110">현재 PATCH를 통해 업데이트할 수 있는 유일한 값은 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="a4e78-110">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="a4e78-111">예제</span><span class="sxs-lookup"><span data-stu-id="a4e78-111">EXAMPLES</span></span>

### <span data-ttu-id="a4e78-112">예제 1: 사용자 지정 공급자에 태그 추가</span><span class="sxs-lookup"><span data-stu-id="a4e78-112">Example 1: Add Tags to a custom Provider</span></span>
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

<span data-ttu-id="a4e78-113">사용자 지정 공급자의 태그를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a4e78-113">Update the tags of a custom provider.</span></span>

### <span data-ttu-id="a4e78-114">예제 2: 파이핑을 사용하여 사용자 지정 공급자 업데이트</span><span class="sxs-lookup"><span data-stu-id="a4e78-114">Example 2: Update custom provider with piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type | Update-AzCustomProvider -Tag @{MyTag="MyValue"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="a4e78-115">파이핑을 사용하여 사용자 지정 공급자를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a4e78-115">Update a custom provider using piping.</span></span>

## <span data-ttu-id="a4e78-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4e78-116">PARAMETERS</span></span>

### <span data-ttu-id="a4e78-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4e78-117">-DefaultProfile</span></span>
<span data-ttu-id="a4e78-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a4e78-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4e78-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4e78-119">-InputObject</span></span>
<span data-ttu-id="a4e78-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="a4e78-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a4e78-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a4e78-121">-Name</span></span>
<span data-ttu-id="a4e78-122">리소스 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a4e78-122">The name of the resource provider.</span></span>

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

### <span data-ttu-id="a4e78-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4e78-123">-ResourceGroupName</span></span>
<span data-ttu-id="a4e78-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a4e78-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="a4e78-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a4e78-125">-SubscriptionId</span></span>
<span data-ttu-id="a4e78-126">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a4e78-126">The Azure subscription ID.</span></span>
<span data-ttu-id="a4e78-127">GUID 형식 문자열입니다(예: 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="a4e78-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="a4e78-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="a4e78-128">-Tag</span></span>
<span data-ttu-id="a4e78-129">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="a4e78-129">Resource tags</span></span>

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

### <span data-ttu-id="a4e78-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4e78-130">-Confirm</span></span>
<span data-ttu-id="a4e78-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4e78-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4e78-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4e78-132">-WhatIf</span></span>
<span data-ttu-id="a4e78-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a4e78-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4e78-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a4e78-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4e78-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4e78-135">CommonParameters</span></span>
<span data-ttu-id="a4e78-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a4e78-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4e78-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a4e78-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4e78-138">입력</span><span class="sxs-lookup"><span data-stu-id="a4e78-138">INPUTS</span></span>

### <span data-ttu-id="a4e78-139">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="a4e78-139">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="a4e78-140">출력</span><span class="sxs-lookup"><span data-stu-id="a4e78-140">OUTPUTS</span></span>

### <span data-ttu-id="a4e78-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="a4e78-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="a4e78-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a4e78-142">NOTES</span></span>

<span data-ttu-id="a4e78-143">별칭</span><span class="sxs-lookup"><span data-stu-id="a4e78-143">ALIASES</span></span>

<span data-ttu-id="a4e78-144">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="a4e78-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a4e78-145">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="a4e78-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a4e78-146">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a4e78-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a4e78-147">INPUTOBJECT: <ICustomProvidersIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="a4e78-147">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a4e78-148">`[AssociationName <String>]`: 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a4e78-148">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="a4e78-149">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="a4e78-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a4e78-150">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a4e78-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="a4e78-151">`[ResourceProviderName <String>]`: 리소스 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a4e78-151">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="a4e78-152">`[Scope <String>]`: 연결의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="a4e78-152">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="a4e78-153">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a4e78-153">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="a4e78-154">GUID 형식 문자열입니다(예: 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="a4e78-154">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="a4e78-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a4e78-155">RELATED LINKS</span></span>

