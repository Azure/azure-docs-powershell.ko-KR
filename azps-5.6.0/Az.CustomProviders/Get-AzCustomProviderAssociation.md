---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/powershell/module/az.customproviders/get-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
ms.openlocfilehash: f7c36ca53b00c0fc99e5afc6e6ba74f4cff62afb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998783"
---
# <span data-ttu-id="0340d-101">Get-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="0340d-101">Get-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="0340d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0340d-102">SYNOPSIS</span></span>
<span data-ttu-id="0340d-103">연결합니다.</span><span class="sxs-lookup"><span data-stu-id="0340d-103">Get an association.</span></span>

## <span data-ttu-id="0340d-104">구문</span><span class="sxs-lookup"><span data-stu-id="0340d-104">SYNTAX</span></span>

### <span data-ttu-id="0340d-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="0340d-105">List (Default)</span></span>
```
Get-AzCustomProviderAssociation -Scope <String> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0340d-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="0340d-106">Get</span></span>
```
Get-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="0340d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0340d-107">GetViaIdentity</span></span>
```
Get-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="0340d-108">설명</span><span class="sxs-lookup"><span data-stu-id="0340d-108">DESCRIPTION</span></span>
<span data-ttu-id="0340d-109">연결합니다.</span><span class="sxs-lookup"><span data-stu-id="0340d-109">Get an association.</span></span>

## <span data-ttu-id="0340d-110">예제</span><span class="sxs-lookup"><span data-stu-id="0340d-110">EXAMPLES</span></span>

### <span data-ttu-id="0340d-111">예제 1: 사용자 지정 공급자 연결 나열</span><span class="sxs-lookup"><span data-stu-id="0340d-111">Example 1: List custom provider associations</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="0340d-112">지정한 범위에 대한 모든 사용자 지정 공급자 연결 목록을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="0340d-112">List all custom provider associations for a given scope.</span></span>

### <span data-ttu-id="0340d-113">예제 2: 연결 얻기</span><span class="sxs-lookup"><span data-stu-id="0340d-113">Example 2: Get an association</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="0340d-114">단일 CustomProvider 연결에 대한 세부 정보 확인</span><span class="sxs-lookup"><span data-stu-id="0340d-114">Get details for a single CustomProvider association</span></span>

## <span data-ttu-id="0340d-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0340d-115">PARAMETERS</span></span>

### <span data-ttu-id="0340d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0340d-116">-DefaultProfile</span></span>
<span data-ttu-id="0340d-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0340d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0340d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0340d-118">-InputObject</span></span>
<span data-ttu-id="0340d-119">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="0340d-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0340d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0340d-120">-Name</span></span>
<span data-ttu-id="0340d-121">연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0340d-121">The name of the association.</span></span>

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

### <span data-ttu-id="0340d-122">-Scope</span><span class="sxs-lookup"><span data-stu-id="0340d-122">-Scope</span></span>
<span data-ttu-id="0340d-123">연결의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="0340d-123">The scope of the association.</span></span>

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

### <span data-ttu-id="0340d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0340d-124">CommonParameters</span></span>
<span data-ttu-id="0340d-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0340d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0340d-126">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0340d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0340d-127">입력</span><span class="sxs-lookup"><span data-stu-id="0340d-127">INPUTS</span></span>

### <span data-ttu-id="0340d-128">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="0340d-128">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="0340d-129">출력</span><span class="sxs-lookup"><span data-stu-id="0340d-129">OUTPUTS</span></span>

### <span data-ttu-id="0340d-130">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span><span class="sxs-lookup"><span data-stu-id="0340d-130">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="0340d-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0340d-131">NOTES</span></span>

<span data-ttu-id="0340d-132">별칭</span><span class="sxs-lookup"><span data-stu-id="0340d-132">ALIASES</span></span>

<span data-ttu-id="0340d-133">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="0340d-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0340d-134">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="0340d-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0340d-135">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0340d-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0340d-136">INPUTOBJECT <ICustomProvidersIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0340d-136">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0340d-137">`[AssociationName <String>]`: 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0340d-137">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="0340d-138">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="0340d-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0340d-139">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0340d-139">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="0340d-140">`[ResourceProviderName <String>]`: 리소스 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0340d-140">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="0340d-141">`[Scope <String>]`: 연결의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="0340d-141">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="0340d-142">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0340d-142">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="0340d-143">GUID 형식 문자열입니다(예: 00000000-0000-0000-000000000)입니다.</span><span class="sxs-lookup"><span data-stu-id="0340d-143">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="0340d-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0340d-144">RELATED LINKS</span></span>

