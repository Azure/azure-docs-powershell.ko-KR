---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroup.md
ms.openlocfilehash: 764b2d091b0019cc4231828066b4067c5f054476
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490600"
---
# <span data-ttu-id="73791-101">Get-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="73791-101">Get-AzADGroup</span></span>

## <span data-ttu-id="73791-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73791-102">SYNOPSIS</span></span>
<span data-ttu-id="73791-103">Active Directory 그룹을 필터합니다.</span><span class="sxs-lookup"><span data-stu-id="73791-103">Filters active directory groups.</span></span>

## <span data-ttu-id="73791-104">구문</span><span class="sxs-lookup"><span data-stu-id="73791-104">SYNTAX</span></span>

### <span data-ttu-id="73791-105">EmptyParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="73791-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="73791-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="73791-106">SearchStringParameterSet</span></span>
```
Get-AzADGroup -DisplayNameStartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="73791-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="73791-107">DisplayNameParameterSet</span></span>
```
Get-AzADGroup -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="73791-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="73791-108">ObjectIdParameterSet</span></span>
```
Get-AzADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="73791-109">설명</span><span class="sxs-lookup"><span data-stu-id="73791-109">DESCRIPTION</span></span>
<span data-ttu-id="73791-110">Active Directory 그룹을 필터합니다.</span><span class="sxs-lookup"><span data-stu-id="73791-110">Filters active directory groups.</span></span>

## <span data-ttu-id="73791-111">예제</span><span class="sxs-lookup"><span data-stu-id="73791-111">EXAMPLES</span></span>

### <span data-ttu-id="73791-112">예제 1: 모든 AD 그룹 나열</span><span class="sxs-lookup"><span data-stu-id="73791-112">Example 1: List all AD groups</span></span>
```powershell
PS C:\> Get-AzADGroup
```

<span data-ttu-id="73791-113">테넌트의 모든 AD 그룹을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="73791-113">Lists all AD groups in a tenant.</span></span>

### <span data-ttu-id="73791-114">예제 2: Paging를 사용하여 모든 AD 그룹 나열</span><span class="sxs-lookup"><span data-stu-id="73791-114">Example 2: List all AD groups using paging</span></span>

```powershell
PS C:\> Get-AzADGroup -First 100
```

<span data-ttu-id="73791-115">테넌트의 처음 100개 AD 그룹을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="73791-115">Lists the first 100 AD groups in a tenant.</span></span>

### <span data-ttu-id="73791-116">예제 3: 개체 ID로 AD 그룹 얻기</span><span class="sxs-lookup"><span data-stu-id="73791-116">Example 3: Get AD group by object id</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="73791-117">개체 ID가 '85F89C90-780E-4AA6-9F4F-6F268D322EEE'인 AD 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="73791-117">Gets an AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="73791-118">예제 4: 검색 문자열로 그룹 나열</span><span class="sxs-lookup"><span data-stu-id="73791-118">Example 4: List groups by search string</span></span>

```powershell
PS C:\> Get-AzADGroup -SearchString Joe
```

<span data-ttu-id="73791-119">표시 이름이 'Joe'로 시작하는 모든 AD 그룹을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="73791-119">Lists all AD groups whose display name begins with 'Joe'.</span></span>

## <span data-ttu-id="73791-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73791-120">PARAMETERS</span></span>

### <span data-ttu-id="73791-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73791-121">-DefaultProfile</span></span>
<span data-ttu-id="73791-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="73791-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="73791-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="73791-123">-DisplayName</span></span>
<span data-ttu-id="73791-124">그룹의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73791-124">The display name of the group.</span></span>

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

### <span data-ttu-id="73791-125">-DisplayNameStartsWith</span><span class="sxs-lookup"><span data-stu-id="73791-125">-DisplayNameStartsWith</span></span>
<span data-ttu-id="73791-126">제공된 문자열로 시작하는 그룹을 찾는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="73791-126">Used to find groups that begin with the provided string.</span></span>

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

### <span data-ttu-id="73791-127">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="73791-127">-ObjectId</span></span>
<span data-ttu-id="73791-128">그룹의 개체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="73791-128">Object id of the group.</span></span>

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

### <span data-ttu-id="73791-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="73791-129">-IncludeTotalCount</span></span>
<span data-ttu-id="73791-130">데이터 집합의 개체 수를 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="73791-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="73791-131">현재 이 매개 변수는 아무 것도 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73791-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="73791-132">-Skip</span><span class="sxs-lookup"><span data-stu-id="73791-132">-Skip</span></span>
<span data-ttu-id="73791-133">첫 번째 N개 개체를 무시하고 나머지 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="73791-133">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="73791-134">-First</span><span class="sxs-lookup"><span data-stu-id="73791-134">-First</span></span>
<span data-ttu-id="73791-135">반환할 개체의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="73791-135">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="73791-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73791-136">CommonParameters</span></span>
<span data-ttu-id="73791-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="73791-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73791-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="73791-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73791-139">입력</span><span class="sxs-lookup"><span data-stu-id="73791-139">INPUTS</span></span>

### <span data-ttu-id="73791-140">System.String</span><span class="sxs-lookup"><span data-stu-id="73791-140">System.String</span></span>

### <span data-ttu-id="73791-141">System.Guid</span><span class="sxs-lookup"><span data-stu-id="73791-141">System.Guid</span></span>

## <span data-ttu-id="73791-142">출력</span><span class="sxs-lookup"><span data-stu-id="73791-142">OUTPUTS</span></span>

### <span data-ttu-id="73791-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="73791-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="73791-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="73791-144">NOTES</span></span>

## <span data-ttu-id="73791-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="73791-145">RELATED LINKS</span></span>

[<span data-ttu-id="73791-146">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="73791-146">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="73791-147">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="73791-147">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="73791-148">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="73791-148">Get-AzADGroupMember</span></span>](./Get-AzADGroupMember.md)

