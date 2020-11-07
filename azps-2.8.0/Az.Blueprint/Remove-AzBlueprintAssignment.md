---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/remove-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
ms.openlocfilehash: ccf76449bf2f7e904cbfe6e2507e067df7661dae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697633"
---
# <span data-ttu-id="02579-101">Remove-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="02579-101">Remove-AzBlueprintAssignment</span></span>

## <span data-ttu-id="02579-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02579-102">SYNOPSIS</span></span>
<span data-ttu-id="02579-103">구독에서 청사진 과제를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="02579-103">Remove a blueprint assignment from a subscription.</span></span>

## <span data-ttu-id="02579-104">구문과</span><span class="sxs-lookup"><span data-stu-id="02579-104">SYNTAX</span></span>

### <span data-ttu-id="02579-105">DeleteBlueprintAssignmentByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="02579-105">DeleteBlueprintAssignmentByName (Default)</span></span>
```
Remove-AzBlueprintAssignment [[-SubscriptionId] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02579-106">DeleteBlueprintAssignmentByObject</span><span class="sxs-lookup"><span data-stu-id="02579-106">DeleteBlueprintAssignmentByObject</span></span>
```
Remove-AzBlueprintAssignment [[-SubscriptionId] <String>] [-InputObject] <PSBlueprintAssignment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02579-107">설명은</span><span class="sxs-lookup"><span data-stu-id="02579-107">DESCRIPTION</span></span>
<span data-ttu-id="02579-108">구독에 할당 된 청사진을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="02579-108">Remove a blueprint that has been assigned to a subscription.</span></span>

## <span data-ttu-id="02579-109">예제의</span><span class="sxs-lookup"><span data-stu-id="02579-109">EXAMPLES</span></span>

### <span data-ttu-id="02579-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="02579-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzBlueprintAssignment -Name "myAssignment" -Subscription "00000000-1111-0000-1111-000000000000" -Confirm
```

<span data-ttu-id="02579-111">지정 된 구독에서 이름으로 지정 된 청사진 과제를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="02579-111">Remove the blueprint assignment specified by name from the specified subscription.</span></span> <span data-ttu-id="02579-112">Cmdlet은 명령을 실행 하기 전에 확인을 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="02579-112">The cmdlet will prompt for confirmation before executing the command.</span></span>

## <span data-ttu-id="02579-113">변수</span><span class="sxs-lookup"><span data-stu-id="02579-113">PARAMETERS</span></span>

### <span data-ttu-id="02579-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02579-114">-DefaultProfile</span></span>
<span data-ttu-id="02579-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="02579-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02579-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02579-116">-InputObject</span></span>
<span data-ttu-id="02579-117">청사진 과제 개체</span><span class="sxs-lookup"><span data-stu-id="02579-117">Blueprint assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment
Parameter Sets: DeleteBlueprintAssignmentByObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02579-118">-이름</span><span class="sxs-lookup"><span data-stu-id="02579-118">-Name</span></span>
<span data-ttu-id="02579-119">청사진 과제 이름.</span><span class="sxs-lookup"><span data-stu-id="02579-119">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteBlueprintAssignmentByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02579-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02579-120">-PassThru</span></span>
<span data-ttu-id="02579-121">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="02579-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="02579-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="02579-122">-SubscriptionId</span></span>
<span data-ttu-id="02579-123">청사진 배정이 배포 되는 구독 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="02579-123">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteBlueprintAssignmentByName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DeleteBlueprintAssignmentByObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02579-124">-확인</span><span class="sxs-lookup"><span data-stu-id="02579-124">-Confirm</span></span>
<span data-ttu-id="02579-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="02579-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02579-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02579-126">-WhatIf</span></span>
<span data-ttu-id="02579-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="02579-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02579-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="02579-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02579-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02579-129">CommonParameters</span></span>
<span data-ttu-id="02579-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="02579-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02579-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02579-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02579-132">입력</span><span class="sxs-lookup"><span data-stu-id="02579-132">INPUTS</span></span>

### <span data-ttu-id="02579-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="02579-133">System.String</span></span>

### <span data-ttu-id="02579-134">PSBlueprintAssignment []를 통해 명령을</span><span class="sxs-lookup"><span data-stu-id="02579-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span></span>

## <span data-ttu-id="02579-135">출력</span><span class="sxs-lookup"><span data-stu-id="02579-135">OUTPUTS</span></span>

### <span data-ttu-id="02579-136">System. 개체</span><span class="sxs-lookup"><span data-stu-id="02579-136">System.Object</span></span>
## <span data-ttu-id="02579-137">상속자</span><span class="sxs-lookup"><span data-stu-id="02579-137">NOTES</span></span>

## <span data-ttu-id="02579-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="02579-138">RELATED LINKS</span></span>
