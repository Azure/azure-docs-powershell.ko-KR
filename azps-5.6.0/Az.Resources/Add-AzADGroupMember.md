---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/add-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
ms.openlocfilehash: 7184ee532335d7db84792bf2234d8cbafa9ad201
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999835"
---
# <span data-ttu-id="2abe3-101">Add-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="2abe3-101">Add-AzADGroupMember</span></span>

## <span data-ttu-id="2abe3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2abe3-102">SYNOPSIS</span></span>
<span data-ttu-id="2abe3-103">사용자를 기존 AD 그룹에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="2abe3-103">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="2abe3-104">구문</span><span class="sxs-lookup"><span data-stu-id="2abe3-104">SYNTAX</span></span>

### <span data-ttu-id="2abe3-105">MemberObjectIdWithGroupObjectId(기본값)</span><span class="sxs-lookup"><span data-stu-id="2abe3-105">MemberObjectIdWithGroupObjectId (Default)</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2abe3-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="2abe3-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2abe3-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="2abe3-107">MemberObjectIdWithGroupObject</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2abe3-108">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2abe3-108">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2abe3-109">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2abe3-109">MemberUPNWithGroupObjectParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2abe3-110">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2abe3-110">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2abe3-111">설명</span><span class="sxs-lookup"><span data-stu-id="2abe3-111">DESCRIPTION</span></span>
<span data-ttu-id="2abe3-112">사용자를 기존 AD 그룹에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="2abe3-112">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="2abe3-113">예제</span><span class="sxs-lookup"><span data-stu-id="2abe3-113">EXAMPLES</span></span>

### <span data-ttu-id="2abe3-114">예제 1: 개체 ID로 그룹에 사용자 추가</span><span class="sxs-lookup"><span data-stu-id="2abe3-114">Example 1: Add a user to a group by object id</span></span>

```powershell
PS C:\> Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -TargetGroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="2abe3-115">개체 ID 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405'가 있는 사용자를 개체 ID '85F89C90-780E-4AA6-9F4F-6F268D322EEE'로 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="2abe3-115">Adds the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' to the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="2abe3-116">예제 2: 배관을 통해 그룹에 사용자 추가</span><span class="sxs-lookup"><span data-stu-id="2abe3-116">Example 2: Add a user to a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="2abe3-117">개체 ID '85F89C90-780E-4AA6-9F4F-6F268D322EEE'가 있는 그룹을 시작하고 해당 그룹에 사용자를 Add-AzADGroupMember cmdlet에 파이프합니다.</span><span class="sxs-lookup"><span data-stu-id="2abe3-117">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Add-AzADGroupMember cmdlet to add the user to that group.</span></span>

### <span data-ttu-id="2abe3-118">예제 3: 주체 이름으로 그룹에 사용자 추가</span><span class="sxs-lookup"><span data-stu-id="2abe3-118">Example 3: Add a user to a group by principal name</span></span>

```powershell
PS C:\> Add-AzADGroupMember -MemberUserPrincipalName "myemail@domain.com" -TargetGroupDisplayName "MyGroupDisplayName" 
PS C:\> Get-AzADGroupMember -GroupDisplayName "MyGroupDisplayName"
```

<span data-ttu-id="2abe3-119">그룹에 사용자를 추가하고 그룹의 구성원을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="2abe3-119">Adds an user to a group and list the members of the group.</span></span>

## <span data-ttu-id="2abe3-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2abe3-120">PARAMETERS</span></span>

### <span data-ttu-id="2abe3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2abe3-121">-DefaultProfile</span></span>
<span data-ttu-id="2abe3-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2abe3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2abe3-123">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="2abe3-123">-MemberObjectId</span></span>
<span data-ttu-id="2abe3-124">멤버의 개체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2abe3-124">The object id of the member.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2abe3-125">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="2abe3-125">-MemberUserPrincipalName</span></span>
<span data-ttu-id="2abe3-126">그룹에 추가할 멤버의 UPN입니다.</span><span class="sxs-lookup"><span data-stu-id="2abe3-126">The UPN of the member(s) to add to the group.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MemberUPNWithGroupDisplayNameParameterSet, MemberUPNWithGroupObjectParameterSet, MemberUPNWithGroupObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2abe3-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2abe3-127">-PassThru</span></span>
<span data-ttu-id="2abe3-128">명령이 성공하면 이를 지정하면 true가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="2abe3-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="2abe3-129">-TargetGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="2abe3-129">-TargetGroupDisplayName</span></span>
<span data-ttu-id="2abe3-130">멤버를 추가할 그룹의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2abe3-130">The display name of the group to add the member(s) to.</span></span>

```yaml
Type: System.String
Parameter Sets: MemberObjectIdWithGroupDisplayName, MemberUPNWithGroupDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2abe3-131">-TargetGroupObject</span><span class="sxs-lookup"><span data-stu-id="2abe3-131">-TargetGroupObject</span></span>
<span data-ttu-id="2abe3-132">멤버를 추가할 그룹의 개체 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="2abe3-132">The object representation of the group to add the member(s) to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADGroup
Parameter Sets: MemberObjectIdWithGroupObject, MemberUPNWithGroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2abe3-133">-TargetGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="2abe3-133">-TargetGroupObjectId</span></span>
<span data-ttu-id="2abe3-134">멤버를 추가할 그룹의 개체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2abe3-134">The object id of the group to add the member(s) to.</span></span>

```yaml
Type: System.String
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberUPNWithGroupObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2abe3-135">-확인</span><span class="sxs-lookup"><span data-stu-id="2abe3-135">-Confirm</span></span>
<span data-ttu-id="2abe3-136">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2abe3-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2abe3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2abe3-137">-WhatIf</span></span>
<span data-ttu-id="2abe3-138">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="2abe3-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2abe3-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2abe3-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2abe3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2abe3-140">CommonParameters</span></span>
<span data-ttu-id="2abe3-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2abe3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2abe3-142">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2abe3-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2abe3-143">입력</span><span class="sxs-lookup"><span data-stu-id="2abe3-143">INPUTS</span></span>

### <span data-ttu-id="2abe3-144">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="2abe3-144">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="2abe3-145">출력</span><span class="sxs-lookup"><span data-stu-id="2abe3-145">OUTPUTS</span></span>

### <span data-ttu-id="2abe3-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2abe3-146">System.Boolean</span></span>

## <span data-ttu-id="2abe3-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2abe3-147">NOTES</span></span>

## <span data-ttu-id="2abe3-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2abe3-148">RELATED LINKS</span></span>
