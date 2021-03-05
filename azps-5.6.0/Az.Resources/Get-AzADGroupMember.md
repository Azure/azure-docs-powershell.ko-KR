---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
ms.openlocfilehash: d351ee85c36b9f5f8493879cded058fd7220450f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986678"
---
# <span data-ttu-id="ea60a-101">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="ea60a-101">Get-AzADGroupMember</span></span>

## <span data-ttu-id="ea60a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea60a-102">SYNOPSIS</span></span>
<span data-ttu-id="ea60a-103">현재 테넌트에 AD 그룹의 구성원을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="ea60a-103">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="ea60a-104">구문</span><span class="sxs-lookup"><span data-stu-id="ea60a-104">SYNTAX</span></span>

### <span data-ttu-id="ea60a-105">ObjectIdParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ea60a-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADGroupMember [-GroupObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="ea60a-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea60a-106">DisplayNameParameterSet</span></span>
```
Get-AzADGroupMember -GroupDisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="ea60a-107">GroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea60a-107">GroupObjectParameterSet</span></span>
```
Get-AzADGroupMember -GroupObject <PSADGroup> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="ea60a-108">설명</span><span class="sxs-lookup"><span data-stu-id="ea60a-108">DESCRIPTION</span></span>
<span data-ttu-id="ea60a-109">현재 테넌트에 AD 그룹의 구성원을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="ea60a-109">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="ea60a-110">예제</span><span class="sxs-lookup"><span data-stu-id="ea60a-110">EXAMPLES</span></span>

### <span data-ttu-id="ea60a-111">예제 1: AD 그룹 개체 ID로 구성원 나열</span><span class="sxs-lookup"><span data-stu-id="ea60a-111">Example 1: List members by AD group object id</span></span>

```powershell
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="ea60a-112">개체 ID '85F89C90-780E-4AA6-9F4F-6F268D322EEE'가 있는 AD 그룹의 구성원을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="ea60a-112">Lists members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="ea60a-113">예제 2: Paging를 사용하여 AD 그룹 개체 ID로 멤버 나열</span><span class="sxs-lookup"><span data-stu-id="ea60a-113">Example 2: List members by AD group object id using paging</span></span>

```powershell
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE -First 100
```

<span data-ttu-id="ea60a-114">개체 ID '85F89C90-780E-4AA6-9F4F-6F268D322EEE'가 있는 AD 그룹의 처음 100개 멤버를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="ea60a-114">Lists the first 100 members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="ea60a-115">예제 3: 배관을 통해 멤버 나열</span><span class="sxs-lookup"><span data-stu-id="ea60a-115">Example 3: List members by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Get-AzADGroupMember
```

<span data-ttu-id="ea60a-116">개체 ID '85F89C90-780E-4AA6-9F4F-6F268D322EEE'가 있는 AD 그룹을 시작하고 해당 Get-AzADGroupMember cmdlet에 파이프합니다.</span><span class="sxs-lookup"><span data-stu-id="ea60a-116">Gets the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Get-AzADGroupMember cmdlet to list all members in that group.</span></span> 

## <span data-ttu-id="ea60a-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ea60a-117">PARAMETERS</span></span>

### <span data-ttu-id="ea60a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea60a-118">-DefaultProfile</span></span>
<span data-ttu-id="ea60a-119">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ea60a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea60a-120">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="ea60a-120">-GroupDisplayName</span></span>
<span data-ttu-id="ea60a-121">그룹의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea60a-121">The display name of the group.</span></span>

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

### <span data-ttu-id="ea60a-122">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="ea60a-122">-GroupObject</span></span>
<span data-ttu-id="ea60a-123">구성원을 나열하는 그룹 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ea60a-123">The group object that you are listing members from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADGroup
Parameter Sets: GroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea60a-124">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="ea60a-124">-GroupObjectId</span></span>
<span data-ttu-id="ea60a-125">그룹의 개체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ea60a-125">Object Id of the group.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: Id, ObjectId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea60a-126">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="ea60a-126">-IncludeTotalCount</span></span>
<span data-ttu-id="ea60a-127">데이터 집합의 개체 수를 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="ea60a-127">Reports the number of objects in the data set.</span></span> <span data-ttu-id="ea60a-128">현재 이 매개 변수는 아무 것도 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ea60a-128">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="ea60a-129">-Skip</span><span class="sxs-lookup"><span data-stu-id="ea60a-129">-Skip</span></span>
<span data-ttu-id="ea60a-130">첫 번째 N 개체를 무시한 다음 나머지 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ea60a-130">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="ea60a-131">-First</span><span class="sxs-lookup"><span data-stu-id="ea60a-131">-First</span></span>
<span data-ttu-id="ea60a-132">반환할 개체의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="ea60a-132">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="ea60a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea60a-133">CommonParameters</span></span>
<span data-ttu-id="ea60a-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ea60a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea60a-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea60a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea60a-136">입력</span><span class="sxs-lookup"><span data-stu-id="ea60a-136">INPUTS</span></span>

### <span data-ttu-id="ea60a-137">System.String</span><span class="sxs-lookup"><span data-stu-id="ea60a-137">System.String</span></span>

### <span data-ttu-id="ea60a-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="ea60a-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="ea60a-139">출력</span><span class="sxs-lookup"><span data-stu-id="ea60a-139">OUTPUTS</span></span>

### <span data-ttu-id="ea60a-140">Microsoft.Azure.Commands.ActiveDirectory.PSADObject</span><span class="sxs-lookup"><span data-stu-id="ea60a-140">Microsoft.Azure.Commands.ActiveDirectory.PSADObject</span></span>

## <span data-ttu-id="ea60a-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ea60a-141">NOTES</span></span>

## <span data-ttu-id="ea60a-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ea60a-142">RELATED LINKS</span></span>

[<span data-ttu-id="ea60a-143">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="ea60a-143">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="ea60a-144">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ea60a-144">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

