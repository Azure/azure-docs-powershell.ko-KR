---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/get-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProvider.md
ms.openlocfilehash: 42b4059b146a752980b1067272713bf0a22c2c46
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181161"
---
# <span data-ttu-id="4c9ae-101">Get-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="4c9ae-101">Get-AzCustomProvider</span></span>

## <span data-ttu-id="4c9ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c9ae-102">SYNOPSIS</span></span>
<span data-ttu-id="4c9ae-103">사용자 지정 리소스 공급자 매니페스트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4c9ae-103">Gets the custom resource provider manifest.</span></span>

## <span data-ttu-id="4c9ae-104">구문</span><span class="sxs-lookup"><span data-stu-id="4c9ae-104">SYNTAX</span></span>

### <span data-ttu-id="4c9ae-105">List1(기본값)</span><span class="sxs-lookup"><span data-stu-id="4c9ae-105">List1 (Default)</span></span>
```
Get-AzCustomProvider [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4c9ae-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="4c9ae-106">Get</span></span>
```
Get-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4c9ae-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4c9ae-107">GetViaIdentity</span></span>
```
Get-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4c9ae-108">목록</span><span class="sxs-lookup"><span data-stu-id="4c9ae-108">List</span></span>
```
Get-AzCustomProvider -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="4c9ae-109">설명</span><span class="sxs-lookup"><span data-stu-id="4c9ae-109">DESCRIPTION</span></span>
<span data-ttu-id="4c9ae-110">사용자 지정 리소스 공급자 매니페스트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4c9ae-110">Gets the custom resource provider manifest.</span></span>

## <span data-ttu-id="4c9ae-111">예제</span><span class="sxs-lookup"><span data-stu-id="4c9ae-111">EXAMPLES</span></span>

### <span data-ttu-id="4c9ae-112">예제 1: 구독의 모든 사용자 지정 공급자 나열</span><span class="sxs-lookup"><span data-stu-id="4c9ae-112">Example 1: List all Custom Providers in a subscription</span></span>
```powershell
PS C:\> Get-AzCustomProvider

Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
East US 2 Namespace2.Type  Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="4c9ae-113">구독의 모든 사용자 지정 공급자를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9ae-113">Lists all the custom providers in a subscription</span></span>

### <span data-ttu-id="4c9ae-114">예제 2: 단일 사용자 지정 공급자를 얻게</span><span class="sxs-lookup"><span data-stu-id="4c9ae-114">Example 2: Get a single custom provider</span></span>
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

<span data-ttu-id="4c9ae-115">단일 사용자 지정 공급자에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4c9ae-115">Gets details for a single custom provider.</span></span>
<span data-ttu-id="4c9ae-116">이 Format-List 사용하여 화면에 개체 세부 정보를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9ae-116">Use Format-List to show object details on the screen.</span></span>

## <span data-ttu-id="4c9ae-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c9ae-117">PARAMETERS</span></span>

### <span data-ttu-id="4c9ae-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c9ae-118">-DefaultProfile</span></span>
<span data-ttu-id="4c9ae-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4c9ae-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c9ae-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c9ae-120">-InputObject</span></span>
<span data-ttu-id="4c9ae-121">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="4c9ae-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4c9ae-122">-Name</span><span class="sxs-lookup"><span data-stu-id="4c9ae-122">-Name</span></span>
<span data-ttu-id="4c9ae-123">리소스 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4c9ae-123">The name of the resource provider.</span></span>

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

### <span data-ttu-id="4c9ae-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c9ae-124">-ResourceGroupName</span></span>
<span data-ttu-id="4c9ae-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4c9ae-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="4c9ae-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4c9ae-126">-SubscriptionId</span></span>
<span data-ttu-id="4c9ae-127">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4c9ae-127">The Azure subscription ID.</span></span>
<span data-ttu-id="4c9ae-128">GUID 형식 문자열입니다(예: 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="4c9ae-128">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="4c9ae-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c9ae-129">CommonParameters</span></span>
<span data-ttu-id="4c9ae-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9ae-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c9ae-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4c9ae-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c9ae-132">입력</span><span class="sxs-lookup"><span data-stu-id="4c9ae-132">INPUTS</span></span>

### <span data-ttu-id="4c9ae-133">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="4c9ae-133">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="4c9ae-134">출력</span><span class="sxs-lookup"><span data-stu-id="4c9ae-134">OUTPUTS</span></span>

### <span data-ttu-id="4c9ae-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="4c9ae-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="4c9ae-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4c9ae-136">NOTES</span></span>

<span data-ttu-id="4c9ae-137">별칭</span><span class="sxs-lookup"><span data-stu-id="4c9ae-137">ALIASES</span></span>

<span data-ttu-id="4c9ae-138">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="4c9ae-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4c9ae-139">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="4c9ae-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4c9ae-140">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4c9ae-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4c9ae-141">INPUTOBJECT: <ICustomProvidersIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="4c9ae-141">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4c9ae-142">`[AssociationName <String>]`: 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4c9ae-142">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="4c9ae-143">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="4c9ae-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4c9ae-144">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4c9ae-144">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="4c9ae-145">`[ResourceProviderName <String>]`: 리소스 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4c9ae-145">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="4c9ae-146">`[Scope <String>]`: 연결의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="4c9ae-146">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="4c9ae-147">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4c9ae-147">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="4c9ae-148">GUID 형식 문자열입니다(예: 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="4c9ae-148">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="4c9ae-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4c9ae-149">RELATED LINKS</span></span>

