---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroup.md
ms.openlocfilehash: 32370d88de54b7a6004da6b66e15e08c9eca26e7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042028"
---
# <span data-ttu-id="c076e-101">Get-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="c076e-101">Get-AzADGroup</span></span>

## <span data-ttu-id="c076e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c076e-102">SYNOPSIS</span></span>
<span data-ttu-id="c076e-103">Active directory 그룹을 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="c076e-103">Filters active directory groups.</span></span>

## <span data-ttu-id="c076e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c076e-104">SYNTAX</span></span>

### <span data-ttu-id="c076e-105">EmptyParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c076e-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="c076e-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="c076e-106">SearchStringParameterSet</span></span>
```
Get-AzADGroup -DisplayNameStartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="c076e-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c076e-107">DisplayNameParameterSet</span></span>
```
Get-AzADGroup -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="c076e-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c076e-108">ObjectIdParameterSet</span></span>
```
Get-AzADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="c076e-109">설명은</span><span class="sxs-lookup"><span data-stu-id="c076e-109">DESCRIPTION</span></span>
<span data-ttu-id="c076e-110">Active directory 그룹을 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="c076e-110">Filters active directory groups.</span></span>

## <span data-ttu-id="c076e-111">예제의</span><span class="sxs-lookup"><span data-stu-id="c076e-111">EXAMPLES</span></span>

### <span data-ttu-id="c076e-112">예제 1-모든 광고 그룹 나열</span><span class="sxs-lookup"><span data-stu-id="c076e-112">Example 1 - List all AD groups</span></span>
```
PS C:\> Get-AzADGroup
```

<span data-ttu-id="c076e-113">테 넌 트에서 모든 광고 그룹을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="c076e-113">Lists all AD groups in a tenant.</span></span>

### <span data-ttu-id="c076e-114">예제 2-페이징을 사용 하 여 모든 광고 그룹 나열</span><span class="sxs-lookup"><span data-stu-id="c076e-114">Example 2 - List all AD groups using paging</span></span>

```
PS C:\> Get-AzADGroup -First 100
```

<span data-ttu-id="c076e-115">테 넌 트에서 첫 번째 100 광고 그룹을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="c076e-115">Lists the first 100 AD groups in a tenant.</span></span>

### <span data-ttu-id="c076e-116">예제 3-개체 id 별 광고 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="c076e-116">Example 3 - Get AD group by object id</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="c076e-117">개체 id가 ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' 인 광고 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c076e-117">Gets an AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="c076e-118">예제 4-검색 문자열을 기준으로 그룹 나열</span><span class="sxs-lookup"><span data-stu-id="c076e-118">Example 4 - List groups by search string</span></span>

```
PS C:\> Get-AzADGroup -SearchString Joe
```

<span data-ttu-id="c076e-119">표시 이름이 ' t e '로 시작 하는 모든 광고 그룹을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="c076e-119">Lists all AD groups whose display name begins with 'Joe'.</span></span>

## <span data-ttu-id="c076e-120">변수</span><span class="sxs-lookup"><span data-stu-id="c076e-120">PARAMETERS</span></span>

### <span data-ttu-id="c076e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c076e-121">-DefaultProfile</span></span>
<span data-ttu-id="c076e-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c076e-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c076e-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c076e-123">-DisplayName</span></span>
<span data-ttu-id="c076e-124">그룹의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c076e-124">The display name of the group.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c076e-125">-DisplayNameStartsWith</span><span class="sxs-lookup"><span data-stu-id="c076e-125">-DisplayNameStartsWith</span></span>
<span data-ttu-id="c076e-126">제공 된 문자열로 시작 하는 그룹을 찾는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c076e-126">Used to find groups that begin with the provided string.</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: SearchString

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c076e-127">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c076e-127">-ObjectId</span></span>
<span data-ttu-id="c076e-128">그룹의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="c076e-128">Object id of the group.</span></span>

```yaml
Type: System.Guid
Parameter Sets: EmptyParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c076e-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="c076e-129">-IncludeTotalCount</span></span>
<span data-ttu-id="c076e-130">데이터 집합의 개체 수를 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="c076e-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="c076e-131">현재이 매개 변수는 아무런 작업도 수행 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c076e-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="c076e-132">-생략</span><span class="sxs-lookup"><span data-stu-id="c076e-132">-Skip</span></span>
<span data-ttu-id="c076e-133">첫 N 개 개체를 무시 하 고 나머지 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c076e-133">Ignores the first N objects and then gets the remaining objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c076e-134">-첫 번째</span><span class="sxs-lookup"><span data-stu-id="c076e-134">-First</span></span>
<span data-ttu-id="c076e-135">반환할 최대 개체 수입니다.</span><span class="sxs-lookup"><span data-stu-id="c076e-135">The maximum number of objects to return.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c076e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c076e-136">CommonParameters</span></span>
<span data-ttu-id="c076e-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c076e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c076e-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c076e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c076e-139">입력</span><span class="sxs-lookup"><span data-stu-id="c076e-139">INPUTS</span></span>

### <span data-ttu-id="c076e-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c076e-140">System.String</span></span>

### <span data-ttu-id="c076e-141">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="c076e-141">System.Guid</span></span>

## <span data-ttu-id="c076e-142">출력</span><span class="sxs-lookup"><span data-stu-id="c076e-142">OUTPUTS</span></span>

### <span data-ttu-id="c076e-143">ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="c076e-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="c076e-144">상속자</span><span class="sxs-lookup"><span data-stu-id="c076e-144">NOTES</span></span>

## <span data-ttu-id="c076e-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c076e-145">RELATED LINKS</span></span>

[<span data-ttu-id="c076e-146">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="c076e-146">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="c076e-147">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c076e-147">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="c076e-148">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="c076e-148">Get-AzADGroupMember</span></span>](./Get-AzADGroupMember.md)

