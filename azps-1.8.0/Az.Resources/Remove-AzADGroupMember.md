---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroupMember.md
ms.openlocfilehash: 1196480735705186ad3493b6c34a473baf35dc0e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699356"
---
# <span data-ttu-id="0dc90-101">Remove-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="0dc90-101">Remove-AzADGroupMember</span></span>

## <span data-ttu-id="0dc90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0dc90-102">SYNOPSIS</span></span>
<span data-ttu-id="0dc90-103">광고 그룹에서 사용자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0dc90-103">Removes a user from an AD group.</span></span>

## <span data-ttu-id="0dc90-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0dc90-104">SYNTAX</span></span>

### <span data-ttu-id="0dc90-105">ExplicitParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="0dc90-105">ExplicitParameterSet (Default)</span></span>
```
Remove-AzADGroupMember [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0dc90-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="0dc90-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0dc90-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="0dc90-107">MemberObjectIdWithGroupObject</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0dc90-108">MemberObjectIdWithGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="0dc90-108">MemberObjectIdWithGroupObjectId</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0dc90-109">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dc90-109">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0dc90-110">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dc90-110">MemberUPNWithGroupObjectParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0dc90-111">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dc90-111">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0dc90-112">설명은</span><span class="sxs-lookup"><span data-stu-id="0dc90-112">DESCRIPTION</span></span>
<span data-ttu-id="0dc90-113">광고 그룹에서 사용자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0dc90-113">Removes a user from an AD group.</span></span>

## <span data-ttu-id="0dc90-114">예제의</span><span class="sxs-lookup"><span data-stu-id="0dc90-114">EXAMPLES</span></span>

### <span data-ttu-id="0dc90-115">예제 1-개체 id를 기준으로 그룹에서 사용자 제거</span><span class="sxs-lookup"><span data-stu-id="0dc90-115">Example 1 - Remove a user from a group by object id</span></span>

```
PS C:\> Remove-AzADGroup -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="0dc90-116">개체 id가 ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' 인 그룹에서 개체 id가 ' D9076BBC-D62C-4105-9C78-A7F5BC4A3405 ' 인 사용자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0dc90-116">Removes the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' from the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="0dc90-117">예제 2-파이핑을 기준으로 그룹에서 사용자 제거</span><span class="sxs-lookup"><span data-stu-id="0dc90-117">Example 2 - Remove a user from a group by piping</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="0dc90-118">개체 id가 ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' 인 그룹을 가져오고이를 Remove-AzADGroupMember cmdlet에 파이프 하 여 해당 그룹에 대 한 사용자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0dc90-118">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Remove-AzADGroupMember cmdlet to remove the user to that group.</span></span>

## <span data-ttu-id="0dc90-119">변수</span><span class="sxs-lookup"><span data-stu-id="0dc90-119">PARAMETERS</span></span>

### <span data-ttu-id="0dc90-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dc90-120">-DefaultProfile</span></span>
<span data-ttu-id="0dc90-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0dc90-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0dc90-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="0dc90-122">-GroupDisplayName</span></span>
<span data-ttu-id="0dc90-123">구성원을 제거할 그룹의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0dc90-123">The display name of the group to remove the member(s) from.</span></span>

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

### <span data-ttu-id="0dc90-124">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="0dc90-124">-GroupObject</span></span>
<span data-ttu-id="0dc90-125">구성원을 제거할 그룹의 개체 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="0dc90-125">The object representation of the group to remove the member from.</span></span>

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

### <span data-ttu-id="0dc90-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="0dc90-126">-GroupObjectId</span></span>
<span data-ttu-id="0dc90-127">구성원을 제거할 그룹의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="0dc90-127">The object id of the group to remove the member from.</span></span>

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

### <span data-ttu-id="0dc90-128">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="0dc90-128">-MemberObjectId</span></span>
<span data-ttu-id="0dc90-129">구성원의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="0dc90-129">The object id of the member.</span></span>

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

### <span data-ttu-id="0dc90-130">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="0dc90-130">-MemberUserPrincipalName</span></span>
<span data-ttu-id="0dc90-131">제거할 구성원의 UPN입니다.</span><span class="sxs-lookup"><span data-stu-id="0dc90-131">The UPN of the member(s) to remove.</span></span>

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

### <span data-ttu-id="0dc90-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0dc90-132">-PassThru</span></span>
<span data-ttu-id="0dc90-133">명령이 성공적으로 실행 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0dc90-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="0dc90-134">-확인</span><span class="sxs-lookup"><span data-stu-id="0dc90-134">-Confirm</span></span>
<span data-ttu-id="0dc90-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0dc90-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0dc90-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0dc90-136">-WhatIf</span></span>
<span data-ttu-id="0dc90-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0dc90-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0dc90-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0dc90-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0dc90-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dc90-139">CommonParameters</span></span>
<span data-ttu-id="0dc90-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0dc90-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dc90-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dc90-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dc90-142">입력</span><span class="sxs-lookup"><span data-stu-id="0dc90-142">INPUTS</span></span>

### <span data-ttu-id="0dc90-143">ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="0dc90-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="0dc90-144">출력</span><span class="sxs-lookup"><span data-stu-id="0dc90-144">OUTPUTS</span></span>

### <span data-ttu-id="0dc90-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="0dc90-145">System.Boolean</span></span>

## <span data-ttu-id="0dc90-146">상속자</span><span class="sxs-lookup"><span data-stu-id="0dc90-146">NOTES</span></span>

## <span data-ttu-id="0dc90-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0dc90-147">RELATED LINKS</span></span>
