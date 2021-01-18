---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/get-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
ms.openlocfilehash: 08d760c73256b71842fac36a7d095db2aab21128
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493625"
---
# <span data-ttu-id="d71a1-101">Get-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="d71a1-101">Get-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="d71a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d71a1-102">SYNOPSIS</span></span>
<span data-ttu-id="d71a1-103">연결합니다.</span><span class="sxs-lookup"><span data-stu-id="d71a1-103">Get an association.</span></span>

## <span data-ttu-id="d71a1-104">구문</span><span class="sxs-lookup"><span data-stu-id="d71a1-104">SYNTAX</span></span>

### <span data-ttu-id="d71a1-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="d71a1-105">List (Default)</span></span>
```
Get-AzCustomProviderAssociation -Scope <String> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d71a1-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="d71a1-106">Get</span></span>
```
Get-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="d71a1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d71a1-107">GetViaIdentity</span></span>
```
Get-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d71a1-108">설명</span><span class="sxs-lookup"><span data-stu-id="d71a1-108">DESCRIPTION</span></span>
<span data-ttu-id="d71a1-109">연결합니다.</span><span class="sxs-lookup"><span data-stu-id="d71a1-109">Get an association.</span></span>

## <span data-ttu-id="d71a1-110">예제</span><span class="sxs-lookup"><span data-stu-id="d71a1-110">EXAMPLES</span></span>

### <span data-ttu-id="d71a1-111">예제 1: 사용자 지정 공급자 연결 나열</span><span class="sxs-lookup"><span data-stu-id="d71a1-111">Example 1: List custom provider associations</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="d71a1-112">지정한 범위에 대한 모든 사용자 지정 공급자 연결 나열</span><span class="sxs-lookup"><span data-stu-id="d71a1-112">List all custom provider associations for a given scope.</span></span>

### <span data-ttu-id="d71a1-113">예제 2: 연결하기</span><span class="sxs-lookup"><span data-stu-id="d71a1-113">Example 2: Get an association</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="d71a1-114">단일 CustomProvider 연결에 대한 세부 정보 확인</span><span class="sxs-lookup"><span data-stu-id="d71a1-114">Get details for a single CustomProvider association</span></span>

## <span data-ttu-id="d71a1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d71a1-115">PARAMETERS</span></span>

### <span data-ttu-id="d71a1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d71a1-116">-DefaultProfile</span></span>
<span data-ttu-id="d71a1-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d71a1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d71a1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d71a1-118">-InputObject</span></span>
<span data-ttu-id="d71a1-119">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="d71a1-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d71a1-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d71a1-120">-Name</span></span>
<span data-ttu-id="d71a1-121">연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d71a1-121">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AssociationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d71a1-122">-Scope</span><span class="sxs-lookup"><span data-stu-id="d71a1-122">-Scope</span></span>
<span data-ttu-id="d71a1-123">연결의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="d71a1-123">The scope of the association.</span></span>

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

### <span data-ttu-id="d71a1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d71a1-124">CommonParameters</span></span>
<span data-ttu-id="d71a1-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d71a1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d71a1-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d71a1-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d71a1-127">입력</span><span class="sxs-lookup"><span data-stu-id="d71a1-127">INPUTS</span></span>

### <span data-ttu-id="d71a1-128">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="d71a1-128">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="d71a1-129">출력</span><span class="sxs-lookup"><span data-stu-id="d71a1-129">OUTPUTS</span></span>

### <span data-ttu-id="d71a1-130">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span><span class="sxs-lookup"><span data-stu-id="d71a1-130">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="d71a1-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d71a1-131">NOTES</span></span>

<span data-ttu-id="d71a1-132">별칭</span><span class="sxs-lookup"><span data-stu-id="d71a1-132">ALIASES</span></span>

<span data-ttu-id="d71a1-133">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="d71a1-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d71a1-134">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d71a1-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d71a1-135">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d71a1-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d71a1-136">INPUTOBJECT: <ICustomProvidersIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d71a1-136">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d71a1-137">`[AssociationName <String>]`: 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d71a1-137">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="d71a1-138">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="d71a1-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d71a1-139">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d71a1-139">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="d71a1-140">`[ResourceProviderName <String>]`: 리소스 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d71a1-140">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="d71a1-141">`[Scope <String>]`: 연결의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="d71a1-141">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="d71a1-142">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d71a1-142">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="d71a1-143">GUID 형식 문자열입니다(예: 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="d71a1-143">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="d71a1-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d71a1-144">RELATED LINKS</span></span>

