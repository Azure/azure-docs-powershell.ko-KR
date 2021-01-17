---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
ms.openlocfilehash: 984b5ef9a1ff19142ef044e1f3c919f8fb2a3dce
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490599"
---
# <span data-ttu-id="baa45-101">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="baa45-101">Get-AzADGroupMember</span></span>

## <span data-ttu-id="baa45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="baa45-102">SYNOPSIS</span></span>
<span data-ttu-id="baa45-103">현재 테넌트에서 AD 그룹의 멤버를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="baa45-103">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="baa45-104">구문</span><span class="sxs-lookup"><span data-stu-id="baa45-104">SYNTAX</span></span>

### <span data-ttu-id="baa45-105">ObjectIdParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="baa45-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADGroupMember [-GroupObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="baa45-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="baa45-106">DisplayNameParameterSet</span></span>
```
Get-AzADGroupMember -GroupDisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="baa45-107">GroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="baa45-107">GroupObjectParameterSet</span></span>
```
Get-AzADGroupMember -GroupObject <PSADGroup> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="baa45-108">설명</span><span class="sxs-lookup"><span data-stu-id="baa45-108">DESCRIPTION</span></span>
<span data-ttu-id="baa45-109">현재 테넌트에서 AD 그룹의 멤버를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="baa45-109">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="baa45-110">예제</span><span class="sxs-lookup"><span data-stu-id="baa45-110">EXAMPLES</span></span>

### <span data-ttu-id="baa45-111">예제 1: AD 그룹 개체 ID로 멤버 나열</span><span class="sxs-lookup"><span data-stu-id="baa45-111">Example 1: List members by AD group object id</span></span>

```powershell
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="baa45-112">개체 ID가 '85F89C90-780E-4AA6-9F4F-6F268D322EEE'인 AD 그룹의 멤버를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="baa45-112">Lists members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="baa45-113">예제 2: Paging를 사용하여 AD 그룹 개체 ID로 멤버 나열</span><span class="sxs-lookup"><span data-stu-id="baa45-113">Example 2: List members by AD group object id using paging</span></span>

```powershell
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE -First 100
```

<span data-ttu-id="baa45-114">개체 ID가 '85F89C90-780E-4AA6-9F4F-6F268D322EEE'인 AD 그룹의 처음 100개 멤버를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="baa45-114">Lists the first 100 members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="baa45-115">예제 3: 파이핑을 통해 멤버 나열</span><span class="sxs-lookup"><span data-stu-id="baa45-115">Example 3: List members by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Get-AzADGroupMember
```

<span data-ttu-id="baa45-116">개체 ID가 '85F89C90-780E-4AA6-9F4F-6F268D322EEE'인 AD 그룹을 Get-AzADGroupMember cmdlet에 파이프하여 해당 그룹의 모든 멤버를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="baa45-116">Gets the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Get-AzADGroupMember cmdlet to list all members in that group.</span></span> 

## <span data-ttu-id="baa45-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="baa45-117">PARAMETERS</span></span>

### <span data-ttu-id="baa45-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baa45-118">-DefaultProfile</span></span>
<span data-ttu-id="baa45-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="baa45-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="baa45-120">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="baa45-120">-GroupDisplayName</span></span>
<span data-ttu-id="baa45-121">그룹의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="baa45-121">The display name of the group.</span></span>

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

### <span data-ttu-id="baa45-122">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="baa45-122">-GroupObject</span></span>
<span data-ttu-id="baa45-123">멤버를 나열하는 그룹 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="baa45-123">The group object that you are listing members from.</span></span>

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

### <span data-ttu-id="baa45-124">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="baa45-124">-GroupObjectId</span></span>
<span data-ttu-id="baa45-125">그룹의 개체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="baa45-125">Object Id of the group.</span></span>

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

### <span data-ttu-id="baa45-126">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="baa45-126">-IncludeTotalCount</span></span>
<span data-ttu-id="baa45-127">데이터 집합의 개체 수를 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="baa45-127">Reports the number of objects in the data set.</span></span> <span data-ttu-id="baa45-128">현재 이 매개 변수는 아무 것도 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="baa45-128">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="baa45-129">-Skip</span><span class="sxs-lookup"><span data-stu-id="baa45-129">-Skip</span></span>
<span data-ttu-id="baa45-130">첫 번째 N개 개체를 무시하고 나머지 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="baa45-130">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="baa45-131">-First</span><span class="sxs-lookup"><span data-stu-id="baa45-131">-First</span></span>
<span data-ttu-id="baa45-132">반환할 개체의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="baa45-132">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="baa45-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baa45-133">CommonParameters</span></span>
<span data-ttu-id="baa45-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="baa45-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baa45-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="baa45-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baa45-136">입력</span><span class="sxs-lookup"><span data-stu-id="baa45-136">INPUTS</span></span>

### <span data-ttu-id="baa45-137">System.String</span><span class="sxs-lookup"><span data-stu-id="baa45-137">System.String</span></span>

### <span data-ttu-id="baa45-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="baa45-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="baa45-139">출력</span><span class="sxs-lookup"><span data-stu-id="baa45-139">OUTPUTS</span></span>

### <span data-ttu-id="baa45-140">Microsoft.Azure.Commands.ActiveDirectory.PSADObject</span><span class="sxs-lookup"><span data-stu-id="baa45-140">Microsoft.Azure.Commands.ActiveDirectory.PSADObject</span></span>

## <span data-ttu-id="baa45-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="baa45-141">NOTES</span></span>

## <span data-ttu-id="baa45-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="baa45-142">RELATED LINKS</span></span>

[<span data-ttu-id="baa45-143">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="baa45-143">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="baa45-144">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="baa45-144">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

