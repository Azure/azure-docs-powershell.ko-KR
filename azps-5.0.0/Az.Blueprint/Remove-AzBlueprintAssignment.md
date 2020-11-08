---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/remove-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
ms.openlocfilehash: 40452c250b58edf4d1e45f54c953dee8c433c436
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216097"
---
# <span data-ttu-id="c3f61-101">Remove-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="c3f61-101">Remove-AzBlueprintAssignment</span></span>

## <span data-ttu-id="c3f61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3f61-102">SYNOPSIS</span></span>
<span data-ttu-id="c3f61-103">구독 또는 관리 그룹에서 청사진 과제를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3f61-103">Remove a blueprint assignment from a subscription or a management group.</span></span>

## <span data-ttu-id="c3f61-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c3f61-104">SYNTAX</span></span>

### <span data-ttu-id="c3f61-105">BySubscriptionAndName (기본값)</span><span class="sxs-lookup"><span data-stu-id="c3f61-105">BySubscriptionAndName (Default)</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [[-SubscriptionId] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3f61-106">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="c3f61-106">ByManagementGroupAndName</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [-ManagementGroupId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3f61-107">DeleteBlueprintAssignmentByObject</span><span class="sxs-lookup"><span data-stu-id="c3f61-107">DeleteBlueprintAssignmentByObject</span></span>
```
Remove-AzBlueprintAssignment -InputObject <PSBlueprintAssignment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3f61-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c3f61-108">DESCRIPTION</span></span>
<span data-ttu-id="c3f61-109">구독에 할당 된 청사진을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3f61-109">Remove a blueprint that has been assigned to a subscription.</span></span>

## <span data-ttu-id="c3f61-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c3f61-110">EXAMPLES</span></span>

### <span data-ttu-id="c3f61-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c3f61-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzBlueprintAssignment -Name "myAssignment" -Subscription "00000000-1111-0000-1111-000000000000" -Confirm
```

<span data-ttu-id="c3f61-112">지정 된 구독에서 이름으로 지정 된 청사진 과제를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3f61-112">Remove the blueprint assignment specified by name from the specified subscription.</span></span> <span data-ttu-id="c3f61-113">Cmdlet은 명령을 실행 하기 전에 확인을 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3f61-113">The cmdlet will prompt for confirmation before executing the command.</span></span>

## <span data-ttu-id="c3f61-114">변수</span><span class="sxs-lookup"><span data-stu-id="c3f61-114">PARAMETERS</span></span>

### <span data-ttu-id="c3f61-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3f61-115">-DefaultProfile</span></span>
<span data-ttu-id="c3f61-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c3f61-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3f61-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3f61-117">-InputObject</span></span>
<span data-ttu-id="c3f61-118">청사진 과제 개체</span><span class="sxs-lookup"><span data-stu-id="c3f61-118">Blueprint assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment
Parameter Sets: DeleteBlueprintAssignmentByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3f61-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="c3f61-119">-ManagementGroupId</span></span>
<span data-ttu-id="c3f61-120">청사진 배정이 저장 된 관리 그룹의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c3f61-120">The ID of the management group where the Blueprint assignment is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3f61-121">-이름</span><span class="sxs-lookup"><span data-stu-id="c3f61-121">-Name</span></span>
<span data-ttu-id="c3f61-122">청사진 과제 이름.</span><span class="sxs-lookup"><span data-stu-id="c3f61-122">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName, ByManagementGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3f61-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c3f61-123">-PassThru</span></span>
<span data-ttu-id="c3f61-124">이 설정을 지정 하면 cmdlet은 제거 된 청사진 배정을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3f61-124">When set, the cmdlet will return an object representing the removed Blueprint assignment.</span></span> <span data-ttu-id="c3f61-125">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c3f61-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c3f61-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c3f61-126">-SubscriptionId</span></span>
<span data-ttu-id="c3f61-127">청사진 배정이 배포 되는 구독 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="c3f61-127">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3f61-128">-확인</span><span class="sxs-lookup"><span data-stu-id="c3f61-128">-Confirm</span></span>
<span data-ttu-id="c3f61-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3f61-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3f61-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3f61-130">-WhatIf</span></span>
<span data-ttu-id="c3f61-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c3f61-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3f61-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c3f61-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3f61-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3f61-133">CommonParameters</span></span>
<span data-ttu-id="c3f61-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3f61-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3f61-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c3f61-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3f61-136">입력</span><span class="sxs-lookup"><span data-stu-id="c3f61-136">INPUTS</span></span>

### <span data-ttu-id="c3f61-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c3f61-137">System.String</span></span>

### <span data-ttu-id="c3f61-138">PSBlueprintAssignment []를 통해 명령을</span><span class="sxs-lookup"><span data-stu-id="c3f61-138">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span></span>

## <span data-ttu-id="c3f61-139">출력</span><span class="sxs-lookup"><span data-stu-id="c3f61-139">OUTPUTS</span></span>

### <span data-ttu-id="c3f61-140">System. 개체</span><span class="sxs-lookup"><span data-stu-id="c3f61-140">System.Object</span></span>
## <span data-ttu-id="c3f61-141">상속자</span><span class="sxs-lookup"><span data-stu-id="c3f61-141">NOTES</span></span>

## <span data-ttu-id="c3f61-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c3f61-142">RELATED LINKS</span></span>
