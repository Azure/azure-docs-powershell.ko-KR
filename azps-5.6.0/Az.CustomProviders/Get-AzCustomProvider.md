---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/powershell/module/az.customproviders/get-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProvider.md
ms.openlocfilehash: 287472f89e7875411e287fa1315d5622a4c48a6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998181"
---
# <span data-ttu-id="167c6-101">Get-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="167c6-101">Get-AzCustomProvider</span></span>

## <span data-ttu-id="167c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="167c6-102">SYNOPSIS</span></span>
<span data-ttu-id="167c6-103">사용자 지정 리소스 공급자 매니페스트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="167c6-103">Gets the custom resource provider manifest.</span></span>

## <span data-ttu-id="167c6-104">구문</span><span class="sxs-lookup"><span data-stu-id="167c6-104">SYNTAX</span></span>

### <span data-ttu-id="167c6-105">List1(기본값)</span><span class="sxs-lookup"><span data-stu-id="167c6-105">List1 (Default)</span></span>
```
Get-AzCustomProvider [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="167c6-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="167c6-106">Get</span></span>
```
Get-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="167c6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="167c6-107">GetViaIdentity</span></span>
```
Get-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="167c6-108">목록</span><span class="sxs-lookup"><span data-stu-id="167c6-108">List</span></span>
```
Get-AzCustomProvider -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="167c6-109">설명</span><span class="sxs-lookup"><span data-stu-id="167c6-109">DESCRIPTION</span></span>
<span data-ttu-id="167c6-110">사용자 지정 리소스 공급자 매니페스트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="167c6-110">Gets the custom resource provider manifest.</span></span>

## <span data-ttu-id="167c6-111">예제</span><span class="sxs-lookup"><span data-stu-id="167c6-111">EXAMPLES</span></span>

### <span data-ttu-id="167c6-112">예제 1: 구독의 모든 사용자 지정 공급자 나열</span><span class="sxs-lookup"><span data-stu-id="167c6-112">Example 1: List all Custom Providers in a subscription</span></span>
```powershell
PS C:\> Get-AzCustomProvider

Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
East US 2 Namespace2.Type  Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="167c6-113">구독의 모든 사용자 지정 공급자 나열</span><span class="sxs-lookup"><span data-stu-id="167c6-113">Lists all the custom providers in a subscription</span></span>

### <span data-ttu-id="167c6-114">예제 2: 단일 사용자 지정 공급자 사용</span><span class="sxs-lookup"><span data-stu-id="167c6-114">Example 2: Get a single custom provider</span></span>
```powershell
PS C:\> Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type | Format-List

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

<span data-ttu-id="167c6-115">단일 사용자 지정 공급자에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="167c6-115">Gets details for a single custom provider.</span></span>
<span data-ttu-id="167c6-116">화면에서 Format-List 개체 세부 정보를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="167c6-116">Use Format-List to show object details on the screen.</span></span>

## <span data-ttu-id="167c6-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="167c6-117">PARAMETERS</span></span>

### <span data-ttu-id="167c6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="167c6-118">-DefaultProfile</span></span>
<span data-ttu-id="167c6-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="167c6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="167c6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="167c6-120">-InputObject</span></span>
<span data-ttu-id="167c6-121">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="167c6-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="167c6-122">-Name</span><span class="sxs-lookup"><span data-stu-id="167c6-122">-Name</span></span>
<span data-ttu-id="167c6-123">리소스 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="167c6-123">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="167c6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="167c6-124">-ResourceGroupName</span></span>
<span data-ttu-id="167c6-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="167c6-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="167c6-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="167c6-126">-SubscriptionId</span></span>
<span data-ttu-id="167c6-127">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="167c6-127">The Azure subscription ID.</span></span>
<span data-ttu-id="167c6-128">GUID 형식 문자열입니다(예: 00000000-0000-0000-000000000)입니다.</span><span class="sxs-lookup"><span data-stu-id="167c6-128">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="167c6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="167c6-129">CommonParameters</span></span>
<span data-ttu-id="167c6-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="167c6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="167c6-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="167c6-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="167c6-132">입력</span><span class="sxs-lookup"><span data-stu-id="167c6-132">INPUTS</span></span>

### <span data-ttu-id="167c6-133">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="167c6-133">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="167c6-134">출력</span><span class="sxs-lookup"><span data-stu-id="167c6-134">OUTPUTS</span></span>

### <span data-ttu-id="167c6-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="167c6-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="167c6-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="167c6-136">NOTES</span></span>

<span data-ttu-id="167c6-137">별칭</span><span class="sxs-lookup"><span data-stu-id="167c6-137">ALIASES</span></span>

<span data-ttu-id="167c6-138">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="167c6-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="167c6-139">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="167c6-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="167c6-140">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="167c6-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="167c6-141">INPUTOBJECT <ICustomProvidersIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="167c6-141">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="167c6-142">`[AssociationName <String>]`: 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="167c6-142">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="167c6-143">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="167c6-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="167c6-144">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="167c6-144">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="167c6-145">`[ResourceProviderName <String>]`: 리소스 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="167c6-145">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="167c6-146">`[Scope <String>]`: 연결의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="167c6-146">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="167c6-147">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="167c6-147">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="167c6-148">GUID 형식 문자열입니다(예: 00000000-0000-0000-000000000)입니다.</span><span class="sxs-lookup"><span data-stu-id="167c6-148">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="167c6-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="167c6-149">RELATED LINKS</span></span>

