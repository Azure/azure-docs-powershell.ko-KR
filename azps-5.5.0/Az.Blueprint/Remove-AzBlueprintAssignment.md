---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/remove-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
ms.openlocfilehash: 40452c250b58edf4d1e45f54c953dee8c433c436
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181937"
---
# <span data-ttu-id="8fd4e-101">Remove-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="8fd4e-101">Remove-AzBlueprintAssignment</span></span>

## <span data-ttu-id="8fd4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fd4e-102">SYNOPSIS</span></span>
<span data-ttu-id="8fd4e-103">구독 또는 관리 그룹에서 청사진 할당을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="8fd4e-103">Remove a blueprint assignment from a subscription or a management group.</span></span>

## <span data-ttu-id="8fd4e-104">구문</span><span class="sxs-lookup"><span data-stu-id="8fd4e-104">SYNTAX</span></span>

### <span data-ttu-id="8fd4e-105">BySubscriptionAndName(기본값)</span><span class="sxs-lookup"><span data-stu-id="8fd4e-105">BySubscriptionAndName (Default)</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [[-SubscriptionId] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fd4e-106">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="8fd4e-106">ByManagementGroupAndName</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [-ManagementGroupId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fd4e-107">DeleteBlueprintAssignmentByObject</span><span class="sxs-lookup"><span data-stu-id="8fd4e-107">DeleteBlueprintAssignmentByObject</span></span>
```
Remove-AzBlueprintAssignment -InputObject <PSBlueprintAssignment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fd4e-108">설명</span><span class="sxs-lookup"><span data-stu-id="8fd4e-108">DESCRIPTION</span></span>
<span data-ttu-id="8fd4e-109">구독에 할당된 청사진을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="8fd4e-109">Remove a blueprint that has been assigned to a subscription.</span></span>

## <span data-ttu-id="8fd4e-110">예제</span><span class="sxs-lookup"><span data-stu-id="8fd4e-110">EXAMPLES</span></span>

### <span data-ttu-id="8fd4e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="8fd4e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzBlueprintAssignment -Name "myAssignment" -Subscription "00000000-1111-0000-1111-000000000000" -Confirm
```

<span data-ttu-id="8fd4e-112">지정된 구독에서 이름으로 지정된 청사진 할당을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="8fd4e-112">Remove the blueprint assignment specified by name from the specified subscription.</span></span> <span data-ttu-id="8fd4e-113">cmdlet은 명령을 실행하기 전에 확인을 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="8fd4e-113">The cmdlet will prompt for confirmation before executing the command.</span></span>

## <span data-ttu-id="8fd4e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8fd4e-114">PARAMETERS</span></span>

### <span data-ttu-id="8fd4e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fd4e-115">-DefaultProfile</span></span>
<span data-ttu-id="8fd4e-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8fd4e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fd4e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8fd4e-117">-InputObject</span></span>
<span data-ttu-id="8fd4e-118">청사진 할당 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8fd4e-118">Blueprint assignment object.</span></span>

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

### <span data-ttu-id="8fd4e-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="8fd4e-119">-ManagementGroupId</span></span>
<span data-ttu-id="8fd4e-120">청사진 할당이 저장되는 관리 그룹의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8fd4e-120">The ID of the management group where the Blueprint assignment is saved.</span></span>

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

### <span data-ttu-id="8fd4e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8fd4e-121">-Name</span></span>
<span data-ttu-id="8fd4e-122">청사진 할당 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8fd4e-122">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="8fd4e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8fd4e-123">-PassThru</span></span>
<span data-ttu-id="8fd4e-124">설정하면 cmdlet은 제거된 청사진 할당을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="8fd4e-124">When set, the cmdlet will return an object representing the removed Blueprint assignment.</span></span> <span data-ttu-id="8fd4e-125">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8fd4e-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8fd4e-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8fd4e-126">-SubscriptionId</span></span>
<span data-ttu-id="8fd4e-127">청사진 할당이 배포된 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8fd4e-127">Subscription Id the blueprint assignment is deployed to.</span></span>

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

### <span data-ttu-id="8fd4e-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8fd4e-128">-Confirm</span></span>
<span data-ttu-id="8fd4e-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8fd4e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fd4e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fd4e-130">-WhatIf</span></span>
<span data-ttu-id="8fd4e-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="8fd4e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fd4e-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8fd4e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fd4e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fd4e-133">CommonParameters</span></span>
<span data-ttu-id="8fd4e-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8fd4e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fd4e-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8fd4e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fd4e-136">입력</span><span class="sxs-lookup"><span data-stu-id="8fd4e-136">INPUTS</span></span>

### <span data-ttu-id="8fd4e-137">System.String</span><span class="sxs-lookup"><span data-stu-id="8fd4e-137">System.String</span></span>

### <span data-ttu-id="8fd4e-138">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span><span class="sxs-lookup"><span data-stu-id="8fd4e-138">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span></span>

## <span data-ttu-id="8fd4e-139">출력</span><span class="sxs-lookup"><span data-stu-id="8fd4e-139">OUTPUTS</span></span>

### <span data-ttu-id="8fd4e-140">System.Object</span><span class="sxs-lookup"><span data-stu-id="8fd4e-140">System.Object</span></span>
## <span data-ttu-id="8fd4e-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8fd4e-141">NOTES</span></span>

## <span data-ttu-id="8fd4e-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8fd4e-142">RELATED LINKS</span></span>
