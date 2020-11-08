---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 84e17ac36e446d784715c2de38944f7b44d1337d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044572"
---
# <span data-ttu-id="49545-101">Remove-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="49545-101">Remove-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="49545-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49545-102">SYNOPSIS</span></span>
<span data-ttu-id="49545-103">장치에 대 한 주문을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="49545-103">Removes the order for a device.</span></span>

## <span data-ttu-id="49545-104">구문과</span><span class="sxs-lookup"><span data-stu-id="49545-104">SYNTAX</span></span>

### <span data-ttu-id="49545-105">DeleteByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="49545-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49545-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="49545-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49545-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49545-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -InputObject <PSDataBoxEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49545-108">설명은</span><span class="sxs-lookup"><span data-stu-id="49545-108">DESCRIPTION</span></span>
<span data-ttu-id="49545-109">**AzDataBoxEdgeOrder** Cmdlet은 데이터 상자 가장자리 장치에 대 한 기존 주문을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="49545-109">The **Remove-AzDataBoxEdgeOrder** cmdlet deletes an existing order for a Data Box Edge device.</span></span>

## <span data-ttu-id="49545-110">예제의</span><span class="sxs-lookup"><span data-stu-id="49545-110">EXAMPLES</span></span>

### <span data-ttu-id="49545-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="49545-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="49545-112">변수</span><span class="sxs-lookup"><span data-stu-id="49545-112">PARAMETERS</span></span>

### <span data-ttu-id="49545-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49545-113">-AsJob</span></span>
<span data-ttu-id="49545-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="49545-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="49545-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49545-115">-DefaultProfile</span></span>
<span data-ttu-id="49545-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="49545-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49545-117">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="49545-117">-DeviceName</span></span>
<span data-ttu-id="49545-118">장치 이름</span><span class="sxs-lookup"><span data-stu-id="49545-118">Device Name</span></span>

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

### <span data-ttu-id="49545-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49545-119">-InputObject</span></span>
<span data-ttu-id="49545-120">입력 개체</span><span class="sxs-lookup"><span data-stu-id="49545-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49545-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49545-121">-PassThru</span></span>
<span data-ttu-id="49545-122">성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="49545-122">returns true if successful</span></span>

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

### <span data-ttu-id="49545-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49545-123">-ResourceGroupName</span></span>
<span data-ttu-id="49545-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="49545-124">Resource Group Name</span></span>

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

### <span data-ttu-id="49545-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49545-125">-ResourceId</span></span>
<span data-ttu-id="49545-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="49545-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="49545-127">-확인</span><span class="sxs-lookup"><span data-stu-id="49545-127">-Confirm</span></span>
<span data-ttu-id="49545-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="49545-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49545-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49545-129">-WhatIf</span></span>
<span data-ttu-id="49545-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="49545-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="49545-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="49545-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49545-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49545-132">CommonParameters</span></span>
<span data-ttu-id="49545-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="49545-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49545-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="49545-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49545-135">입력</span><span class="sxs-lookup"><span data-stu-id="49545-135">INPUTS</span></span>

### <span data-ttu-id="49545-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="49545-136">System.String</span></span>

### <span data-ttu-id="49545-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="49545-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="49545-138">출력</span><span class="sxs-lookup"><span data-stu-id="49545-138">OUTPUTS</span></span>

### <span data-ttu-id="49545-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="49545-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="49545-140">상속자</span><span class="sxs-lookup"><span data-stu-id="49545-140">NOTES</span></span>

## <span data-ttu-id="49545-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="49545-141">RELATED LINKS</span></span>