---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/get-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
ms.openlocfilehash: 08d760c73256b71842fac36a7d095db2aab21128
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306707"
---
# <span data-ttu-id="b3d5b-101">Get-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="b3d5b-101">Get-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="b3d5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3d5b-102">SYNOPSIS</span></span>
<span data-ttu-id="b3d5b-103">연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b3d5b-103">Get an association.</span></span>

## <span data-ttu-id="b3d5b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b3d5b-104">SYNTAX</span></span>

### <span data-ttu-id="b3d5b-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="b3d5b-105">List (Default)</span></span>
```
Get-AzCustomProviderAssociation -Scope <String> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b3d5b-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="b3d5b-106">Get</span></span>
```
Get-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="b3d5b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b3d5b-107">GetViaIdentity</span></span>
```
Get-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b3d5b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b3d5b-108">DESCRIPTION</span></span>
<span data-ttu-id="b3d5b-109">연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b3d5b-109">Get an association.</span></span>

## <span data-ttu-id="b3d5b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b3d5b-110">EXAMPLES</span></span>

### <span data-ttu-id="b3d5b-111">예제 1: 사용자 지정 공급자 연결 목록</span><span class="sxs-lookup"><span data-stu-id="b3d5b-111">Example 1: List custom provider associations</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="b3d5b-112">지정 된 범위에 대 한 모든 사용자 지정 공급자 연결을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3d5b-112">List all custom provider associations for a given scope.</span></span>

### <span data-ttu-id="b3d5b-113">예제 2: 연결 가져오기</span><span class="sxs-lookup"><span data-stu-id="b3d5b-113">Example 2: Get an association</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="b3d5b-114">단일 CustomProvider 연결에 대 한 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="b3d5b-114">Get details for a single CustomProvider association</span></span>

## <span data-ttu-id="b3d5b-115">변수</span><span class="sxs-lookup"><span data-stu-id="b3d5b-115">PARAMETERS</span></span>

### <span data-ttu-id="b3d5b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3d5b-116">-DefaultProfile</span></span>
<span data-ttu-id="b3d5b-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b3d5b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3d5b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3d5b-118">-InputObject</span></span>
<span data-ttu-id="b3d5b-119">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b3d5b-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b3d5b-120">-이름</span><span class="sxs-lookup"><span data-stu-id="b3d5b-120">-Name</span></span>
<span data-ttu-id="b3d5b-121">연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b3d5b-121">The name of the association.</span></span>

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

### <span data-ttu-id="b3d5b-122">-범위</span><span class="sxs-lookup"><span data-stu-id="b3d5b-122">-Scope</span></span>
<span data-ttu-id="b3d5b-123">연결의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="b3d5b-123">The scope of the association.</span></span>

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

### <span data-ttu-id="b3d5b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3d5b-124">CommonParameters</span></span>
<span data-ttu-id="b3d5b-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3d5b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3d5b-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b3d5b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3d5b-127">입력</span><span class="sxs-lookup"><span data-stu-id="b3d5b-127">INPUTS</span></span>

### <span data-ttu-id="b3d5b-128">ICustomProvidersIdentity (Microsoft. PowerShell. i m m</span><span class="sxs-lookup"><span data-stu-id="b3d5b-128">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="b3d5b-129">출력</span><span class="sxs-lookup"><span data-stu-id="b3d5b-129">OUTPUTS</span></span>

### <span data-ttu-id="b3d5b-130">Api20180901Preview 연결을 위한. i i m.</span><span class="sxs-lookup"><span data-stu-id="b3d5b-130">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="b3d5b-131">상속자</span><span class="sxs-lookup"><span data-stu-id="b3d5b-131">NOTES</span></span>

<span data-ttu-id="b3d5b-132">별칭과</span><span class="sxs-lookup"><span data-stu-id="b3d5b-132">ALIASES</span></span>

<span data-ttu-id="b3d5b-133">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="b3d5b-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b3d5b-134">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3d5b-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b3d5b-135">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="b3d5b-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b3d5b-136">INPUTOBJECT <ICustomProvidersIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b3d5b-136">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b3d5b-137">`[AssociationName <String>]`: 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b3d5b-137">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="b3d5b-138">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="b3d5b-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b3d5b-139">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b3d5b-139">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="b3d5b-140">`[ResourceProviderName <String>]`: 리소스 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b3d5b-140">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="b3d5b-141">`[Scope <String>]`: 연결의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="b3d5b-141">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="b3d5b-142">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b3d5b-142">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="b3d5b-143">GUID 형식 문자열입니다 (예: 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="b3d5b-143">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="b3d5b-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b3d5b-144">RELATED LINKS</span></span>

