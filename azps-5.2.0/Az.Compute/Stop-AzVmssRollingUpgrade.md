---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
ms.openlocfilehash: 331f390890e6349c5a48f9b57c3d0e99fa972532
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347217"
---
# <span data-ttu-id="e83ff-101">Stop-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="e83ff-101">Stop-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="e83ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e83ff-102">SYNOPSIS</span></span>
<span data-ttu-id="e83ff-103">현재 가상 머신 확장 집합 롤링 업그레이드를 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="e83ff-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="e83ff-104">구문</span><span class="sxs-lookup"><span data-stu-id="e83ff-104">SYNTAX</span></span>

```
Stop-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e83ff-105">설명</span><span class="sxs-lookup"><span data-stu-id="e83ff-105">DESCRIPTION</span></span>
<span data-ttu-id="e83ff-106">현재 가상 머신 확장 집합 롤링 업그레이드를 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="e83ff-106">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="e83ff-107">예제</span><span class="sxs-lookup"><span data-stu-id="e83ff-107">EXAMPLES</span></span>

### <span data-ttu-id="e83ff-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e83ff-108">Example 1</span></span>
```
PS C:\> Stop-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="e83ff-109">이 명령은 리소스 그룹 "Group001"에서 VM 확장 집합 "VMSS001"의 진행하는 롤링 업그레이드를 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="e83ff-109">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="e83ff-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e83ff-110">PARAMETERS</span></span>

### <span data-ttu-id="e83ff-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e83ff-111">-AsJob</span></span>
<span data-ttu-id="e83ff-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e83ff-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e83ff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e83ff-113">-DefaultProfile</span></span>
<span data-ttu-id="e83ff-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e83ff-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e83ff-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e83ff-115">-Force</span></span>
<span data-ttu-id="e83ff-116">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e83ff-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e83ff-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e83ff-117">-ResourceGroupName</span></span>
<span data-ttu-id="e83ff-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e83ff-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="e83ff-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="e83ff-119">-VMScaleSetName</span></span>
<span data-ttu-id="e83ff-120">VM 확장 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e83ff-120">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e83ff-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e83ff-121">-Confirm</span></span>
<span data-ttu-id="e83ff-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e83ff-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e83ff-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e83ff-123">-WhatIf</span></span>
<span data-ttu-id="e83ff-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e83ff-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e83ff-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e83ff-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e83ff-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e83ff-126">CommonParameters</span></span>
<span data-ttu-id="e83ff-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e83ff-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e83ff-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e83ff-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e83ff-129">입력</span><span class="sxs-lookup"><span data-stu-id="e83ff-129">INPUTS</span></span>

### <span data-ttu-id="e83ff-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e83ff-130">System.String</span></span>

## <span data-ttu-id="e83ff-131">출력</span><span class="sxs-lookup"><span data-stu-id="e83ff-131">OUTPUTS</span></span>

### <span data-ttu-id="e83ff-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="e83ff-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="e83ff-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e83ff-133">NOTES</span></span>

## <span data-ttu-id="e83ff-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e83ff-134">RELATED LINKS</span></span>
