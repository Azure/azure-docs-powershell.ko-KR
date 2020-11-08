---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/update-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
ms.openlocfilehash: 6691586d454952f92d71a26d5b8ed02904f37bf8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056456"
---
# <span data-ttu-id="a8074-101">Update-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="a8074-101">Update-AzCustomProvider</span></span>

## <span data-ttu-id="a8074-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8074-102">SYNOPSIS</span></span>
<span data-ttu-id="a8074-103">기존 사용자 지정 리소스 공급자를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8074-103">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="a8074-104">현재 패치를 통해 업데이트할 수 있는 값은 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="a8074-104">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="a8074-105">구문과</span><span class="sxs-lookup"><span data-stu-id="a8074-105">SYNTAX</span></span>

### <span data-ttu-id="a8074-106">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="a8074-106">UpdateExpanded (Default)</span></span>
```
Update-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a8074-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a8074-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a8074-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a8074-108">DESCRIPTION</span></span>
<span data-ttu-id="a8074-109">기존 사용자 지정 리소스 공급자를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8074-109">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="a8074-110">현재 패치를 통해 업데이트할 수 있는 값은 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="a8074-110">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="a8074-111">예제의</span><span class="sxs-lookup"><span data-stu-id="a8074-111">EXAMPLES</span></span>

### <span data-ttu-id="a8074-112">예제 1: 사용자 지정 공급자에 태그 추가</span><span class="sxs-lookup"><span data-stu-id="a8074-112">Example 1: Add Tags to a custom Provider</span></span>
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

<span data-ttu-id="a8074-113">사용자 지정 공급자의 태그를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8074-113">Update the tags of a custom provider.</span></span>

### <span data-ttu-id="a8074-114">예제 2: 파이핑을 사용 하 여 사용자 지정 공급자 업데이트</span><span class="sxs-lookup"><span data-stu-id="a8074-114">Example 2: Update custom provider with piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type | Update-AzCustomProvider -Tag @{MyTag="MyValue"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="a8074-115">파이핑을 사용 하 여 사용자 지정 공급자를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8074-115">Update a custom provider using piping.</span></span>

## <span data-ttu-id="a8074-116">변수</span><span class="sxs-lookup"><span data-stu-id="a8074-116">PARAMETERS</span></span>

### <span data-ttu-id="a8074-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8074-117">-DefaultProfile</span></span>
<span data-ttu-id="a8074-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a8074-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8074-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8074-119">-InputObject</span></span>
<span data-ttu-id="a8074-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a8074-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a8074-121">-이름</span><span class="sxs-lookup"><span data-stu-id="a8074-121">-Name</span></span>
<span data-ttu-id="a8074-122">리소스 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a8074-122">The name of the resource provider.</span></span>

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

### <span data-ttu-id="a8074-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8074-123">-ResourceGroupName</span></span>
<span data-ttu-id="a8074-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a8074-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="a8074-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a8074-125">-SubscriptionId</span></span>
<span data-ttu-id="a8074-126">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a8074-126">The Azure subscription ID.</span></span>
<span data-ttu-id="a8074-127">GUID 형식 문자열입니다 (예: 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="a8074-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="a8074-128">태그</span><span class="sxs-lookup"><span data-stu-id="a8074-128">-Tag</span></span>
<span data-ttu-id="a8074-129">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="a8074-129">Resource tags</span></span>

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

### <span data-ttu-id="a8074-130">-확인</span><span class="sxs-lookup"><span data-stu-id="a8074-130">-Confirm</span></span>
<span data-ttu-id="a8074-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8074-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8074-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8074-132">-WhatIf</span></span>
<span data-ttu-id="a8074-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a8074-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8074-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a8074-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8074-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8074-135">CommonParameters</span></span>
<span data-ttu-id="a8074-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8074-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8074-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a8074-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8074-138">입력</span><span class="sxs-lookup"><span data-stu-id="a8074-138">INPUTS</span></span>

### <span data-ttu-id="a8074-139">ICustomProvidersIdentity (Microsoft. PowerShell. i m m</span><span class="sxs-lookup"><span data-stu-id="a8074-139">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="a8074-140">출력</span><span class="sxs-lookup"><span data-stu-id="a8074-140">OUTPUTS</span></span>

### <span data-ttu-id="a8074-141">Api20180901Preview. ICustomRpManifest에 대 한 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a8074-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="a8074-142">상속자</span><span class="sxs-lookup"><span data-stu-id="a8074-142">NOTES</span></span>

<span data-ttu-id="a8074-143">별칭과</span><span class="sxs-lookup"><span data-stu-id="a8074-143">ALIASES</span></span>

<span data-ttu-id="a8074-144">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="a8074-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a8074-145">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8074-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a8074-146">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="a8074-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a8074-147">INPUTOBJECT <ICustomProvidersIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="a8074-147">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a8074-148">`[AssociationName <String>]`: 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a8074-148">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="a8074-149">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="a8074-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a8074-150">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a8074-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="a8074-151">`[ResourceProviderName <String>]`: 리소스 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a8074-151">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="a8074-152">`[Scope <String>]`: 연결의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="a8074-152">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="a8074-153">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a8074-153">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="a8074-154">GUID 형식 문자열입니다 (예: 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="a8074-154">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="a8074-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a8074-155">RELATED LINKS</span></span>

