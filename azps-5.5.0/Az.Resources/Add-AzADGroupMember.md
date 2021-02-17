---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/add-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
ms.openlocfilehash: bf64c2fd139a4174496ba48cdb94aab89486a62a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192788"
---
# <span data-ttu-id="eb782-101">Add-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="eb782-101">Add-AzADGroupMember</span></span>

## <span data-ttu-id="eb782-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb782-102">SYNOPSIS</span></span>
<span data-ttu-id="eb782-103">기존 AD 그룹에 사용자를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="eb782-103">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="eb782-104">구문</span><span class="sxs-lookup"><span data-stu-id="eb782-104">SYNTAX</span></span>

### <span data-ttu-id="eb782-105">MemberObjectIdWithGroupObjectId(기본값)</span><span class="sxs-lookup"><span data-stu-id="eb782-105">MemberObjectIdWithGroupObjectId (Default)</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb782-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="eb782-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb782-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="eb782-107">MemberObjectIdWithGroupObject</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb782-108">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb782-108">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb782-109">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb782-109">MemberUPNWithGroupObjectParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb782-110">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb782-110">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb782-111">설명</span><span class="sxs-lookup"><span data-stu-id="eb782-111">DESCRIPTION</span></span>
<span data-ttu-id="eb782-112">기존 AD 그룹에 사용자를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="eb782-112">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="eb782-113">예제</span><span class="sxs-lookup"><span data-stu-id="eb782-113">EXAMPLES</span></span>

### <span data-ttu-id="eb782-114">예제 1: 개체 ID로 그룹에 사용자 추가</span><span class="sxs-lookup"><span data-stu-id="eb782-114">Example 1: Add a user to a group by object id</span></span>

```powershell
PS C:\> Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -TargetGroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="eb782-115">개체 ID가 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405'인 사용자를 개체 ID가 '85F89C90-780E-4AA6-9F4F-6F268D322EEE'인 그룹에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="eb782-115">Adds the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' to the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="eb782-116">예제 2: 파이핑을 통해 그룹에 사용자 추가</span><span class="sxs-lookup"><span data-stu-id="eb782-116">Example 2: Add a user to a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="eb782-117">개체 ID가 '85F89C90-780E-4AA6-9F4F-6F268D322EEE'인 그룹을 해당 그룹에 추가하기 위해 Add-AzADGroupMember cmdlet에 파이프합니다.</span><span class="sxs-lookup"><span data-stu-id="eb782-117">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Add-AzADGroupMember cmdlet to add the user to that group.</span></span>

### <span data-ttu-id="eb782-118">예제 3: 보안 주체 이름으로 그룹에 사용자 추가</span><span class="sxs-lookup"><span data-stu-id="eb782-118">Example 3: Add a user to a group by principal name</span></span>

```powershell
PS C:\> Add-AzADGroupMember -MemberUserPrincipalName "myemail@domain.com" -TargetGroupDisplayName "MyGroupDisplayName" 
PS C:\> Get-AzADGroupMember -GroupDisplayName "MyGroupDisplayName"
```

<span data-ttu-id="eb782-119">그룹에 사용자를 추가하고 그룹의 구성원을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="eb782-119">Adds an user to a group and list the members of the group.</span></span>

## <span data-ttu-id="eb782-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb782-120">PARAMETERS</span></span>

### <span data-ttu-id="eb782-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb782-121">-DefaultProfile</span></span>
<span data-ttu-id="eb782-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eb782-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb782-123">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="eb782-123">-MemberObjectId</span></span>
<span data-ttu-id="eb782-124">멤버의 개체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="eb782-124">The object id of the member.</span></span>

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

### <span data-ttu-id="eb782-125">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="eb782-125">-MemberUserPrincipalName</span></span>
<span data-ttu-id="eb782-126">그룹에 추가할 멤버의 UPN입니다.</span><span class="sxs-lookup"><span data-stu-id="eb782-126">The UPN of the member(s) to add to the group.</span></span>

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

### <span data-ttu-id="eb782-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb782-127">-PassThru</span></span>
<span data-ttu-id="eb782-128">명령이 성공하면 이를 지정하면 true가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="eb782-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="eb782-129">-TargetGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="eb782-129">-TargetGroupDisplayName</span></span>
<span data-ttu-id="eb782-130">멤버를 추가할 그룹의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eb782-130">The display name of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="eb782-131">-TargetGroupObject</span><span class="sxs-lookup"><span data-stu-id="eb782-131">-TargetGroupObject</span></span>
<span data-ttu-id="eb782-132">멤버를 추가할 그룹의 개체 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="eb782-132">The object representation of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="eb782-133">-TargetGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="eb782-133">-TargetGroupObjectId</span></span>
<span data-ttu-id="eb782-134">멤버를 추가할 그룹의 개체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="eb782-134">The object id of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="eb782-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eb782-135">-Confirm</span></span>
<span data-ttu-id="eb782-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="eb782-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb782-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb782-137">-WhatIf</span></span>
<span data-ttu-id="eb782-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="eb782-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb782-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eb782-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb782-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb782-140">CommonParameters</span></span>
<span data-ttu-id="eb782-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="eb782-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb782-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="eb782-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb782-143">입력</span><span class="sxs-lookup"><span data-stu-id="eb782-143">INPUTS</span></span>

### <span data-ttu-id="eb782-144">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="eb782-144">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="eb782-145">출력</span><span class="sxs-lookup"><span data-stu-id="eb782-145">OUTPUTS</span></span>

### <span data-ttu-id="eb782-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="eb782-146">System.Boolean</span></span>

## <span data-ttu-id="eb782-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="eb782-147">NOTES</span></span>

## <span data-ttu-id="eb782-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eb782-148">RELATED LINKS</span></span>
