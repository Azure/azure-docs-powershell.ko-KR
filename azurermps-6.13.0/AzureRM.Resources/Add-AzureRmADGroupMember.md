---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/add-azurermadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Add-AzureRmADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Add-AzureRmADGroupMember.md
ms.openlocfilehash: 333a56a59c28482c2da228e3e9c0f8c2f1c21f06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528426"
---
# <span data-ttu-id="80997-101">Add-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="80997-101">Add-AzureRmADGroupMember</span></span>

## <span data-ttu-id="80997-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80997-102">SYNOPSIS</span></span>
<span data-ttu-id="80997-103">기존 광고 그룹에 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="80997-103">Adds a user to an existing AD group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80997-104">구문과</span><span class="sxs-lookup"><span data-stu-id="80997-104">SYNTAX</span></span>

### <span data-ttu-id="80997-105">MemberObjectIdWithGroupObjectId (기본값)</span><span class="sxs-lookup"><span data-stu-id="80997-105">MemberObjectIdWithGroupObjectId (Default)</span></span>
```
Add-AzureRmADGroupMember -MemberObjectId <Guid[]> -TargetGroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80997-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="80997-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Add-AzureRmADGroupMember -MemberObjectId <Guid[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80997-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="80997-107">MemberObjectIdWithGroupObject</span></span>
```
Add-AzureRmADGroupMember -MemberObjectId <Guid[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80997-108">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="80997-108">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Add-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80997-109">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="80997-109">MemberUPNWithGroupObjectParameterSet</span></span>
```
Add-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80997-110">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="80997-110">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Add-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80997-111">설명은</span><span class="sxs-lookup"><span data-stu-id="80997-111">DESCRIPTION</span></span>
<span data-ttu-id="80997-112">기존 광고 그룹에 사용자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="80997-112">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="80997-113">예제의</span><span class="sxs-lookup"><span data-stu-id="80997-113">EXAMPLES</span></span>

### <span data-ttu-id="80997-114">예제 1-개체 id를 사용 하 여 그룹에 사용자 추가</span><span class="sxs-lookup"><span data-stu-id="80997-114">Example 1 - Add a user to a group by object id</span></span>

```
PS C:\> Add-AzureRmADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -TargetGroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="80997-115">개체 id가 ' D9076BBC-D62C-4105-9C78-A7F5BC4A3405 ' 인 사용자를 개체 id가 ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' 인 그룹에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="80997-115">Adds the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' to the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="80997-116">예제 2-파이핑을 사용 하 여 그룹에 사용자 추가</span><span class="sxs-lookup"><span data-stu-id="80997-116">Example 2 - Add a user to a group by piping</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Add-AzureRmADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="80997-117">개체 id가 ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' 인 그룹을 가져와이 그룹에 사용자를 추가 하도록 Add-AzureRmADGroupMember cmdlet에 파이프 합니다.</span><span class="sxs-lookup"><span data-stu-id="80997-117">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Add-AzureRmADGroupMember cmdlet to add the user to that group.</span></span>

## <span data-ttu-id="80997-118">변수</span><span class="sxs-lookup"><span data-stu-id="80997-118">PARAMETERS</span></span>

### <span data-ttu-id="80997-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80997-119">-DefaultProfile</span></span>
<span data-ttu-id="80997-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="80997-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80997-121">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="80997-121">-MemberObjectId</span></span>
<span data-ttu-id="80997-122">구성원의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="80997-122">The object id of the member.</span></span>

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

### <span data-ttu-id="80997-123">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="80997-123">-MemberUserPrincipalName</span></span>
<span data-ttu-id="80997-124">그룹에 추가할 구성원의 UPN입니다.</span><span class="sxs-lookup"><span data-stu-id="80997-124">The UPN of the member(s) to add to the group.</span></span>

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

### <span data-ttu-id="80997-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80997-125">-PassThru</span></span>
<span data-ttu-id="80997-126">명령이 성공적으로 실행 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="80997-126">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="80997-127">-TargetGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="80997-127">-TargetGroupDisplayName</span></span>
<span data-ttu-id="80997-128">구성원을 추가할 그룹의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80997-128">The display name of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="80997-129">-TargetGroupObject</span><span class="sxs-lookup"><span data-stu-id="80997-129">-TargetGroupObject</span></span>
<span data-ttu-id="80997-130">구성원을 추가할 그룹의 개체 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="80997-130">The object representation of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="80997-131">-TargetGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="80997-131">-TargetGroupObjectId</span></span>
<span data-ttu-id="80997-132">구성원을 추가할 그룹의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="80997-132">The object id of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="80997-133">-확인</span><span class="sxs-lookup"><span data-stu-id="80997-133">-Confirm</span></span>
<span data-ttu-id="80997-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="80997-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80997-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80997-135">-WhatIf</span></span>
<span data-ttu-id="80997-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="80997-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80997-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="80997-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80997-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80997-138">CommonParameters</span></span>
<span data-ttu-id="80997-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="80997-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80997-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80997-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80997-141">입력</span><span class="sxs-lookup"><span data-stu-id="80997-141">INPUTS</span></span>

### <span data-ttu-id="80997-142">Microsoft.Azure.Graph.RBAC.Version1_6 PSADGroup ActiveDirectory.</span><span class="sxs-lookup"><span data-stu-id="80997-142">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="80997-143">매개 변수: TargetGroupObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="80997-143">Parameters: TargetGroupObject (ByValue)</span></span>

## <span data-ttu-id="80997-144">출력</span><span class="sxs-lookup"><span data-stu-id="80997-144">OUTPUTS</span></span>

### <span data-ttu-id="80997-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="80997-145">System.Boolean</span></span>

## <span data-ttu-id="80997-146">상속자</span><span class="sxs-lookup"><span data-stu-id="80997-146">NOTES</span></span>

## <span data-ttu-id="80997-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="80997-147">RELATED LINKS</span></span>
