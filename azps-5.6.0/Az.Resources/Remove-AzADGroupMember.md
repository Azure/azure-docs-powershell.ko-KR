---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroupMember.md
ms.openlocfilehash: 7cc64ad6d0f17666ac1e97ae00473907c53a5552
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955664"
---
# <span data-ttu-id="3f691-101">Remove-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="3f691-101">Remove-AzADGroupMember</span></span>

## <span data-ttu-id="3f691-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f691-102">SYNOPSIS</span></span>
<span data-ttu-id="3f691-103">AD 그룹에서 사용자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3f691-103">Removes a user from an AD group.</span></span>

## <span data-ttu-id="3f691-104">구문</span><span class="sxs-lookup"><span data-stu-id="3f691-104">SYNTAX</span></span>

### <span data-ttu-id="3f691-105">ExplicitParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="3f691-105">ExplicitParameterSet (Default)</span></span>
```
Remove-AzADGroupMember [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3f691-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="3f691-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f691-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="3f691-107">MemberObjectIdWithGroupObject</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f691-108">MemberObjectIdWithGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="3f691-108">MemberObjectIdWithGroupObjectId</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f691-109">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f691-109">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f691-110">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f691-110">MemberUPNWithGroupObjectParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f691-111">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f691-111">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f691-112">설명</span><span class="sxs-lookup"><span data-stu-id="3f691-112">DESCRIPTION</span></span>
<span data-ttu-id="3f691-113">AD 그룹에서 사용자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3f691-113">Removes a user from an AD group.</span></span>

## <span data-ttu-id="3f691-114">예제</span><span class="sxs-lookup"><span data-stu-id="3f691-114">EXAMPLES</span></span>

### <span data-ttu-id="3f691-115">예제 1: 개체 ID로 그룹에서 사용자 제거</span><span class="sxs-lookup"><span data-stu-id="3f691-115">Example 1: Remove a user from a group by object id</span></span>

```powershell
PS C:\> Remove-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="3f691-116">개체 ID '85F89C90-780E-4AA6-9F4F-6F268D322EEE'가 있는 그룹에서 개체 ID 'D9076BBC-D62C-4105-9F4F-6F268D322EEE'를 사용하여 사용자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3f691-116">Removes the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' from the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="3f691-117">예제 2: 배관을 사용하여 그룹에서 사용자 제거</span><span class="sxs-lookup"><span data-stu-id="3f691-117">Example 2: Remove a user from a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="3f691-118">개체 ID '85F89C90-780E-4AA6-9F4F-6F268D322EEE'를 사용하여 그룹을 Remove-AzADGroupMember cmdlet에 파이프하여 해당 그룹에 사용자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3f691-118">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Remove-AzADGroupMember cmdlet to remove the user to that group.</span></span>

## <span data-ttu-id="3f691-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3f691-119">PARAMETERS</span></span>

### <span data-ttu-id="3f691-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f691-120">-DefaultProfile</span></span>
<span data-ttu-id="3f691-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3f691-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f691-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="3f691-122">-GroupDisplayName</span></span>
<span data-ttu-id="3f691-123">멤버를 제거할 그룹의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f691-123">The display name of the group to remove the member(s) from.</span></span>

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

### <span data-ttu-id="3f691-124">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="3f691-124">-GroupObject</span></span>
<span data-ttu-id="3f691-125">구성원을 제거할 그룹의 개체 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="3f691-125">The object representation of the group to remove the member from.</span></span>

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

### <span data-ttu-id="3f691-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="3f691-126">-GroupObjectId</span></span>
<span data-ttu-id="3f691-127">구성원을 제거할 그룹의 개체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3f691-127">The object id of the group to remove the member from.</span></span>

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

### <span data-ttu-id="3f691-128">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="3f691-128">-MemberObjectId</span></span>
<span data-ttu-id="3f691-129">멤버의 개체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3f691-129">The object id of the member.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject, MemberObjectIdWithGroupObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f691-130">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="3f691-130">-MemberUserPrincipalName</span></span>
<span data-ttu-id="3f691-131">제거할 멤버의 UPN입니다.</span><span class="sxs-lookup"><span data-stu-id="3f691-131">The UPN of the member(s) to remove.</span></span>

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

### <span data-ttu-id="3f691-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f691-132">-PassThru</span></span>
<span data-ttu-id="3f691-133">명령이 성공하면 이를 지정하면 true가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="3f691-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="3f691-134">-확인</span><span class="sxs-lookup"><span data-stu-id="3f691-134">-Confirm</span></span>
<span data-ttu-id="3f691-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3f691-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f691-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f691-136">-WhatIf</span></span>
<span data-ttu-id="3f691-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="3f691-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f691-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3f691-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f691-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f691-139">CommonParameters</span></span>
<span data-ttu-id="3f691-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3f691-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f691-141">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f691-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f691-142">입력</span><span class="sxs-lookup"><span data-stu-id="3f691-142">INPUTS</span></span>

### <span data-ttu-id="3f691-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="3f691-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="3f691-144">출력</span><span class="sxs-lookup"><span data-stu-id="3f691-144">OUTPUTS</span></span>

### <span data-ttu-id="3f691-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3f691-145">System.Boolean</span></span>

## <span data-ttu-id="3f691-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3f691-146">NOTES</span></span>

## <span data-ttu-id="3f691-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3f691-147">RELATED LINKS</span></span>
