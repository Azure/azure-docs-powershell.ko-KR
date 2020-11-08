---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/get-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProvider.md
ms.openlocfilehash: 42b4059b146a752980b1067272713bf0a22c2c46
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94215067"
---
# <span data-ttu-id="4d217-101">Get-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="4d217-101">Get-AzCustomProvider</span></span>

## <span data-ttu-id="4d217-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d217-102">SYNOPSIS</span></span>
<span data-ttu-id="4d217-103">사용자 지정 리소스 공급자 매니페스트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4d217-103">Gets the custom resource provider manifest.</span></span>

## <span data-ttu-id="4d217-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4d217-104">SYNTAX</span></span>

### <span data-ttu-id="4d217-105">List1 (기본값)</span><span class="sxs-lookup"><span data-stu-id="4d217-105">List1 (Default)</span></span>
```
Get-AzCustomProvider [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4d217-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="4d217-106">Get</span></span>
```
Get-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4d217-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4d217-107">GetViaIdentity</span></span>
```
Get-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4d217-108">목록</span><span class="sxs-lookup"><span data-stu-id="4d217-108">List</span></span>
```
Get-AzCustomProvider -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="4d217-109">설명은</span><span class="sxs-lookup"><span data-stu-id="4d217-109">DESCRIPTION</span></span>
<span data-ttu-id="4d217-110">사용자 지정 리소스 공급자 매니페스트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4d217-110">Gets the custom resource provider manifest.</span></span>

## <span data-ttu-id="4d217-111">예제의</span><span class="sxs-lookup"><span data-stu-id="4d217-111">EXAMPLES</span></span>

### <span data-ttu-id="4d217-112">예제 1: 구독의 모든 사용자 지정 공급자 나열</span><span class="sxs-lookup"><span data-stu-id="4d217-112">Example 1: List all Custom Providers in a subscription</span></span>
```powershell
PS C:\> Get-AzCustomProvider

Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
East US 2 Namespace2.Type  Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="4d217-113">구독의 모든 사용자 지정 공급자를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d217-113">Lists all the custom providers in a subscription</span></span>

### <span data-ttu-id="4d217-114">예제 2: 단일 사용자 지정 공급자 가져오기</span><span class="sxs-lookup"><span data-stu-id="4d217-114">Example 2: Get a single custom provider</span></span>
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

<span data-ttu-id="4d217-115">단일 사용자 지정 공급자에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4d217-115">Gets details for a single custom provider.</span></span>
<span data-ttu-id="4d217-116">Format-List를 사용 하 여 화면에 개체 세부 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d217-116">Use Format-List to show object details on the screen.</span></span>

## <span data-ttu-id="4d217-117">변수</span><span class="sxs-lookup"><span data-stu-id="4d217-117">PARAMETERS</span></span>

### <span data-ttu-id="4d217-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d217-118">-DefaultProfile</span></span>
<span data-ttu-id="4d217-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4d217-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d217-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d217-120">-InputObject</span></span>
<span data-ttu-id="4d217-121">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4d217-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4d217-122">-이름</span><span class="sxs-lookup"><span data-stu-id="4d217-122">-Name</span></span>
<span data-ttu-id="4d217-123">리소스 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d217-123">The name of the resource provider.</span></span>

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

### <span data-ttu-id="4d217-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d217-124">-ResourceGroupName</span></span>
<span data-ttu-id="4d217-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d217-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="4d217-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4d217-126">-SubscriptionId</span></span>
<span data-ttu-id="4d217-127">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4d217-127">The Azure subscription ID.</span></span>
<span data-ttu-id="4d217-128">GUID 형식 문자열입니다 (예: 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="4d217-128">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="4d217-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d217-129">CommonParameters</span></span>
<span data-ttu-id="4d217-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d217-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d217-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4d217-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d217-132">입력</span><span class="sxs-lookup"><span data-stu-id="4d217-132">INPUTS</span></span>

### <span data-ttu-id="4d217-133">ICustomProvidersIdentity (Microsoft. PowerShell. i m m</span><span class="sxs-lookup"><span data-stu-id="4d217-133">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="4d217-134">출력</span><span class="sxs-lookup"><span data-stu-id="4d217-134">OUTPUTS</span></span>

### <span data-ttu-id="4d217-135">Api20180901Preview. ICustomRpManifest에 대 한 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4d217-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="4d217-136">상속자</span><span class="sxs-lookup"><span data-stu-id="4d217-136">NOTES</span></span>

<span data-ttu-id="4d217-137">별칭과</span><span class="sxs-lookup"><span data-stu-id="4d217-137">ALIASES</span></span>

<span data-ttu-id="4d217-138">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="4d217-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4d217-139">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d217-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4d217-140">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="4d217-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4d217-141">INPUTOBJECT <ICustomProvidersIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="4d217-141">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4d217-142">`[AssociationName <String>]`: 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d217-142">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="4d217-143">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="4d217-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4d217-144">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d217-144">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="4d217-145">`[ResourceProviderName <String>]`: 리소스 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d217-145">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="4d217-146">`[Scope <String>]`: 연결의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="4d217-146">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="4d217-147">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4d217-147">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="4d217-148">GUID 형식 문자열입니다 (예: 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="4d217-148">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="4d217-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4d217-149">RELATED LINKS</span></span>

