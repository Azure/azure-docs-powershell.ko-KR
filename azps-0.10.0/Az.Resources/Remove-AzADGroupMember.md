---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADGroupMember.md
ms.openlocfilehash: 7ec2fb7e30abc5e04854e34aabe27d928d4d0031
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876406"
---
# <span data-ttu-id="e2732-101">Remove-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="e2732-101">Remove-AzADGroupMember</span></span>

## <span data-ttu-id="e2732-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2732-102">SYNOPSIS</span></span>
<span data-ttu-id="e2732-103">광고 그룹에서 사용자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2732-103">Removes a user from an AD group.</span></span>

## <span data-ttu-id="e2732-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e2732-104">SYNTAX</span></span>

### <span data-ttu-id="e2732-105">ExplicitParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e2732-105">ExplicitParameterSet (Default)</span></span>
```
Remove-AzADGroupMember [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2732-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="e2732-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Remove-AzADGroupMember -MemberObjectId <Guid[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2732-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="e2732-107">MemberObjectIdWithGroupObject</span></span>
```
Remove-AzADGroupMember -MemberObjectId <Guid[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2732-108">MemberObjectIdWithGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="e2732-108">MemberObjectIdWithGroupObjectId</span></span>
```
Remove-AzADGroupMember -MemberObjectId <Guid[]> -GroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2732-109">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2732-109">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2732-110">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2732-110">MemberUPNWithGroupObjectParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2732-111">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2732-111">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2732-112">설명은</span><span class="sxs-lookup"><span data-stu-id="e2732-112">DESCRIPTION</span></span>
<span data-ttu-id="e2732-113">광고 그룹에서 사용자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2732-113">Removes a user from an AD group.</span></span>

## <span data-ttu-id="e2732-114">예제의</span><span class="sxs-lookup"><span data-stu-id="e2732-114">EXAMPLES</span></span>

### <span data-ttu-id="e2732-115">예제 1-개체 id를 기준으로 그룹에서 사용자 제거</span><span class="sxs-lookup"><span data-stu-id="e2732-115">Example 1 - Remove a user from a group by object id</span></span>

```
PS C:\> Remove-AzADGroup -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="e2732-116">개체 id가 ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' 인 그룹에서 개체 id가 ' D9076BBC-D62C-4105-9C78-A7F5BC4A3405 ' 인 사용자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2732-116">Removes the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' from the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="e2732-117">예제 2-파이핑을 기준으로 그룹에서 사용자 제거</span><span class="sxs-lookup"><span data-stu-id="e2732-117">Example 2 - Remove a user from a group by piping</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="e2732-118">개체 id가 ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' 인 그룹을 가져오고이를 Remove-AzADGroupMember cmdlet에 파이프 하 여 해당 그룹에 대 한 사용자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2732-118">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Remove-AzADGroupMember cmdlet to remove the user to that group.</span></span>

## <span data-ttu-id="e2732-119">변수</span><span class="sxs-lookup"><span data-stu-id="e2732-119">PARAMETERS</span></span>

### <span data-ttu-id="e2732-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2732-120">-DefaultProfile</span></span>
<span data-ttu-id="e2732-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e2732-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2732-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="e2732-122">-GroupDisplayName</span></span>
<span data-ttu-id="e2732-123">구성원을 제거할 그룹의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2732-123">The display name of the group to remove the member(s) from.</span></span>

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

### <span data-ttu-id="e2732-124">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="e2732-124">-GroupObject</span></span>
<span data-ttu-id="e2732-125">구성원을 제거할 그룹의 개체 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="e2732-125">The object representation of the group to remove the member from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup
Parameter Sets: MemberObjectIdWithGroupObject, MemberUPNWithGroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2732-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="e2732-126">-GroupObjectId</span></span>
<span data-ttu-id="e2732-127">구성원을 제거할 그룹의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="e2732-127">The object id of the group to remove the member from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberUPNWithGroupObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2732-128">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="e2732-128">-MemberObjectId</span></span>
<span data-ttu-id="e2732-129">구성원의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="e2732-129">The object id of the member.</span></span>

```yaml
Type: System.Guid[]
Parameter Sets: MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject, MemberObjectIdWithGroupObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2732-130">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="e2732-130">-MemberUserPrincipalName</span></span>
<span data-ttu-id="e2732-131">제거할 구성원의 UPN입니다.</span><span class="sxs-lookup"><span data-stu-id="e2732-131">The UPN of the member(s) to remove.</span></span>

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

### <span data-ttu-id="e2732-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2732-132">-PassThru</span></span>
<span data-ttu-id="e2732-133">명령이 성공적으로 실행 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2732-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="e2732-134">-확인</span><span class="sxs-lookup"><span data-stu-id="e2732-134">-Confirm</span></span>
<span data-ttu-id="e2732-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2732-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2732-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2732-136">-WhatIf</span></span>
<span data-ttu-id="e2732-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e2732-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2732-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2732-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2732-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2732-139">CommonParameters</span></span>
<span data-ttu-id="e2732-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2732-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2732-141">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2732-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2732-142">입력</span><span class="sxs-lookup"><span data-stu-id="e2732-142">INPUTS</span></span>

### <span data-ttu-id="e2732-143">Microsoft.Azure.Graph.RBAC.Version1_6 PSADGroup ActiveDirectory.</span><span class="sxs-lookup"><span data-stu-id="e2732-143">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="e2732-144">매개 변수: GroupObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e2732-144">Parameters: GroupObject (ByValue)</span></span>

## <span data-ttu-id="e2732-145">출력</span><span class="sxs-lookup"><span data-stu-id="e2732-145">OUTPUTS</span></span>

### <span data-ttu-id="e2732-146">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="e2732-146">System.Boolean</span></span>

## <span data-ttu-id="e2732-147">상속자</span><span class="sxs-lookup"><span data-stu-id="e2732-147">NOTES</span></span>

## <span data-ttu-id="e2732-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2732-148">RELATED LINKS</span></span>
