---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeDevice.md
ms.openlocfilehash: d26482607dafb10de5b9990b003493ca81fc9ccf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335409"
---
# <span data-ttu-id="9a9bb-101">New-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="9a9bb-101">New-AzStackEdgeDevice</span></span>

## <span data-ttu-id="9a9bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a9bb-102">SYNOPSIS</span></span>
<span data-ttu-id="9a9bb-103">새 Stack Edge 디바이스 구성</span><span class="sxs-lookup"><span data-stu-id="9a9bb-103">Configures a new Stack Edge device</span></span>

## <span data-ttu-id="9a9bb-104">구문</span><span class="sxs-lookup"><span data-stu-id="9a9bb-104">SYNTAX</span></span>

```
New-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a9bb-105">설명</span><span class="sxs-lookup"><span data-stu-id="9a9bb-105">DESCRIPTION</span></span>
<span data-ttu-id="9a9bb-106">**New-AzStackEdgeDevice** cmdlet은 새 Stack Edge 디바이스를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="9a9bb-106">The **New-AzStackEdgeDevice** cmdlet configures a new Stack Edge device</span></span>

## <span data-ttu-id="9a9bb-107">예제</span><span class="sxs-lookup"><span data-stu-id="9a9bb-107">EXAMPLES</span></span>

### <span data-ttu-id="9a9bb-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="9a9bb-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -Location eastus -Sku Edge
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="9a9bb-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a9bb-109">PARAMETERS</span></span>

### <span data-ttu-id="9a9bb-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a9bb-110">-AsJob</span></span>
<span data-ttu-id="9a9bb-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9a9bb-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9a9bb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a9bb-112">-DefaultProfile</span></span>
<span data-ttu-id="9a9bb-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9a9bb-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a9bb-114">-Location</span><span class="sxs-lookup"><span data-stu-id="9a9bb-114">-Location</span></span>
<span data-ttu-id="9a9bb-115">디바이스의 위치</span><span class="sxs-lookup"><span data-stu-id="9a9bb-115">Location of the device</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a9bb-116">-Name</span><span class="sxs-lookup"><span data-stu-id="9a9bb-116">-Name</span></span>
<span data-ttu-id="9a9bb-117">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="9a9bb-117">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeviceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a9bb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a9bb-118">-ResourceGroupName</span></span>
<span data-ttu-id="9a9bb-119">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="9a9bb-119">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a9bb-120">-Sku</span><span class="sxs-lookup"><span data-stu-id="9a9bb-120">-Sku</span></span>
<span data-ttu-id="9a9bb-121">사용 가능한 SKU는 Edge, 게이트웨이입니다.</span><span class="sxs-lookup"><span data-stu-id="9a9bb-121">Available Skus are Edge, Gateway</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a9bb-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a9bb-122">-Confirm</span></span>
<span data-ttu-id="9a9bb-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a9bb-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a9bb-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a9bb-124">-WhatIf</span></span>
<span data-ttu-id="9a9bb-125">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9a9bb-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9a9bb-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9a9bb-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a9bb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a9bb-127">CommonParameters</span></span>
<span data-ttu-id="9a9bb-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9a9bb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a9bb-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9a9bb-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a9bb-130">입력</span><span class="sxs-lookup"><span data-stu-id="9a9bb-130">INPUTS</span></span>

### <span data-ttu-id="9a9bb-131">없음</span><span class="sxs-lookup"><span data-stu-id="9a9bb-131">None</span></span>

## <span data-ttu-id="9a9bb-132">출력</span><span class="sxs-lookup"><span data-stu-id="9a9bb-132">OUTPUTS</span></span>

### <span data-ttu-id="9a9bb-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="9a9bb-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="9a9bb-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9a9bb-134">NOTES</span></span>

## <span data-ttu-id="9a9bb-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9a9bb-135">RELATED LINKS</span></span>
