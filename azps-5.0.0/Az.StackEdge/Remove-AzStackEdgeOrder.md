---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeOrder.md
ms.openlocfilehash: 5effec8ed39f9219bcecba23f6ca3cabaae5cec9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216513"
---
# <span data-ttu-id="bb940-101">Remove-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="bb940-101">Remove-AzStackEdgeOrder</span></span>

## <span data-ttu-id="bb940-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb940-102">SYNOPSIS</span></span>
<span data-ttu-id="bb940-103">장치에 대 한 주문을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb940-103">Removes the order for a device.</span></span>

## <span data-ttu-id="bb940-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bb940-104">SYNTAX</span></span>

### <span data-ttu-id="bb940-105">DeleteByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="bb940-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb940-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb940-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb940-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb940-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeOrder -InputObject <PSStackEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb940-108">설명은</span><span class="sxs-lookup"><span data-stu-id="bb940-108">DESCRIPTION</span></span>
<span data-ttu-id="bb940-109">**AzStackEdgeOrder** Cmdlet은 스택 경계 장치에 대 한 기존 주문을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb940-109">The **Remove-AzStackEdgeOrder** cmdlet deletes an existing order for a Stack Edge device.</span></span>

## <span data-ttu-id="bb940-110">예제의</span><span class="sxs-lookup"><span data-stu-id="bb940-110">EXAMPLES</span></span>

### <span data-ttu-id="bb940-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="bb940-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="bb940-112">변수</span><span class="sxs-lookup"><span data-stu-id="bb940-112">PARAMETERS</span></span>

### <span data-ttu-id="bb940-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bb940-113">-AsJob</span></span>
<span data-ttu-id="bb940-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="bb940-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bb940-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb940-115">-DefaultProfile</span></span>
<span data-ttu-id="bb940-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bb940-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb940-117">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="bb940-117">-DeviceName</span></span>
<span data-ttu-id="bb940-118">장치 이름</span><span class="sxs-lookup"><span data-stu-id="bb940-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb940-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb940-119">-InputObject</span></span>
<span data-ttu-id="bb940-120">입력 개체</span><span class="sxs-lookup"><span data-stu-id="bb940-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb940-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bb940-121">-PassThru</span></span>
<span data-ttu-id="bb940-122">성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb940-122">returns true if successful</span></span>

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

### <span data-ttu-id="bb940-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb940-123">-ResourceGroupName</span></span>
<span data-ttu-id="bb940-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="bb940-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb940-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb940-125">-ResourceId</span></span>
<span data-ttu-id="bb940-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb940-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb940-127">-확인</span><span class="sxs-lookup"><span data-stu-id="bb940-127">-Confirm</span></span>
<span data-ttu-id="bb940-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb940-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb940-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb940-129">-WhatIf</span></span>
<span data-ttu-id="bb940-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bb940-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bb940-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bb940-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb940-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb940-132">CommonParameters</span></span>
<span data-ttu-id="bb940-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb940-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb940-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bb940-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb940-135">입력</span><span class="sxs-lookup"><span data-stu-id="bb940-135">INPUTS</span></span>

### <span data-ttu-id="bb940-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bb940-136">System.String</span></span>

### <span data-ttu-id="bb940-137">StackEdge. PSStackEdgeOrder에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="bb940-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="bb940-138">출력</span><span class="sxs-lookup"><span data-stu-id="bb940-138">OUTPUTS</span></span>

### <span data-ttu-id="bb940-139">StackEdge. PSStackEdgeOrder에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="bb940-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="bb940-140">상속자</span><span class="sxs-lookup"><span data-stu-id="bb940-140">NOTES</span></span>

## <span data-ttu-id="bb940-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bb940-141">RELATED LINKS</span></span>
