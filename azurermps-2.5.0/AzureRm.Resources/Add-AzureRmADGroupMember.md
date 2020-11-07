---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/add-azurermadgroupmember
schema: 2.0.0
ms.openlocfilehash: 4f1949a80d16ddbbd22584c314a01785ed9a393d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880886"
---
# <span data-ttu-id="7e620-101">Add-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="7e620-101">Add-AzureRmADGroupMember</span></span>

## <span data-ttu-id="7e620-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e620-102">SYNOPSIS</span></span>
<span data-ttu-id="7e620-103">기존 광고 그룹에 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e620-103">Adds a user to an existing AD group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e620-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7e620-104">SYNTAX</span></span>

### <span data-ttu-id="7e620-105">MemberObjectIdWithGroupObjectId (기본값)</span><span class="sxs-lookup"><span data-stu-id="7e620-105">MemberObjectIdWithGroupObjectId (Default)</span></span>
```
Add-AzureRmADGroupMember -MemberObjectId <Guid[]> -TargetGroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e620-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="7e620-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Add-AzureRmADGroupMember -MemberObjectId <Guid[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e620-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="7e620-107">MemberObjectIdWithGroupObject</span></span>
```
Add-AzureRmADGroupMember -MemberObjectId <Guid[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e620-108">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e620-108">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Add-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e620-109">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e620-109">MemberUPNWithGroupObjectParameterSet</span></span>
```
Add-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e620-110">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e620-110">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Add-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e620-111">설명은</span><span class="sxs-lookup"><span data-stu-id="7e620-111">DESCRIPTION</span></span>
<span data-ttu-id="7e620-112">기존 광고 그룹에 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e620-112">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="7e620-113">예제의</span><span class="sxs-lookup"><span data-stu-id="7e620-113">EXAMPLES</span></span>

### <span data-ttu-id="7e620-114">예제 1-개체 id를 사용 하 여 그룹에 사용자 추가</span><span class="sxs-lookup"><span data-stu-id="7e620-114">Example 1 - Add a user to a group by object id</span></span>

```
PS C:\> Add-AzureRmADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -TargetGroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="7e620-115">개체 id가 ' D9076BBC-D62C-4105-9C78-A7F5BC4A3405 ' 인 사용자를 개체 id가 ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' 인 그룹에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e620-115">Adds the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' to the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="7e620-116">예제 2-파이핑을 사용 하 여 그룹에 사용자 추가</span><span class="sxs-lookup"><span data-stu-id="7e620-116">Example 2 - Add a user to a group by piping</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Add-AzureRmADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="7e620-117">개체 id가 ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' 인 그룹을 가져와이 그룹에 사용자를 추가 하도록 Add-AzureRmADGroupMember cmdlet에 파이프 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e620-117">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Add-AzureRmADGroupMember cmdlet to add the user to that group.</span></span>

## <span data-ttu-id="7e620-118">변수</span><span class="sxs-lookup"><span data-stu-id="7e620-118">PARAMETERS</span></span>

### <span data-ttu-id="7e620-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e620-119">-DefaultProfile</span></span>
<span data-ttu-id="7e620-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7e620-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e620-121">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="7e620-121">-MemberObjectId</span></span>
<span data-ttu-id="7e620-122">구성원의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="7e620-122">The object id of the member.</span></span>

```yaml
Type: System.Guid[]
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e620-123">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="7e620-123">-MemberUserPrincipalName</span></span>
<span data-ttu-id="7e620-124">그룹에 추가할 구성원의 UPN입니다.</span><span class="sxs-lookup"><span data-stu-id="7e620-124">The UPN of the member(s) to add to the group.</span></span>

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

### <span data-ttu-id="7e620-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7e620-125">-PassThru</span></span>
<span data-ttu-id="7e620-126">명령이 성공적으로 실행 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e620-126">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="7e620-127">-TargetGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="7e620-127">-TargetGroupDisplayName</span></span>
<span data-ttu-id="7e620-128">구성원을 추가할 그룹의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e620-128">The display name of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="7e620-129">-TargetGroupObject</span><span class="sxs-lookup"><span data-stu-id="7e620-129">-TargetGroupObject</span></span>
<span data-ttu-id="7e620-130">구성원을 추가할 그룹의 개체 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="7e620-130">The object representation of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="7e620-131">-TargetGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="7e620-131">-TargetGroupObjectId</span></span>
<span data-ttu-id="7e620-132">구성원을 추가할 그룹의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="7e620-132">The object id of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="7e620-133">-확인</span><span class="sxs-lookup"><span data-stu-id="7e620-133">-Confirm</span></span>
<span data-ttu-id="7e620-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e620-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e620-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e620-135">-WhatIf</span></span>
<span data-ttu-id="7e620-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7e620-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e620-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e620-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e620-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e620-138">CommonParameters</span></span>
<span data-ttu-id="7e620-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e620-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e620-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e620-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e620-141">입력</span><span class="sxs-lookup"><span data-stu-id="7e620-141">INPUTS</span></span>

### <span data-ttu-id="7e620-142">Microsoft.Azure.Graph.RBAC.Version1_6 PSADGroup ActiveDirectory.</span><span class="sxs-lookup"><span data-stu-id="7e620-142">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="7e620-143">매개 변수: TargetGroupObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7e620-143">Parameters: TargetGroupObject (ByValue)</span></span>

## <span data-ttu-id="7e620-144">출력</span><span class="sxs-lookup"><span data-stu-id="7e620-144">OUTPUTS</span></span>

### <span data-ttu-id="7e620-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="7e620-145">System.Boolean</span></span>

## <span data-ttu-id="7e620-146">상속자</span><span class="sxs-lookup"><span data-stu-id="7e620-146">NOTES</span></span>

## <span data-ttu-id="7e620-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7e620-147">RELATED LINKS</span></span>
