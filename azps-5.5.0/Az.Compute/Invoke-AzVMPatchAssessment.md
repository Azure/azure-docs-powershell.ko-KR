---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMPatchAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMPatchAssessment.md
ms.openlocfilehash: 52e7a7372372bfcb0dfc93a9a89715e91c484b73
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195033"
---
# <span data-ttu-id="6ca61-101">Invoke-AzVMPatchAssessment</span><span class="sxs-lookup"><span data-stu-id="6ca61-101">Invoke-AzVMPatchAssessment</span></span>

## <span data-ttu-id="6ca61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ca61-102">SYNOPSIS</span></span>
<span data-ttu-id="6ca61-103">가상 머신의 패치 상태를 평가합니다.</span><span class="sxs-lookup"><span data-stu-id="6ca61-103">Assess patch state of a virtual machine.</span></span>

## <span data-ttu-id="6ca61-104">구문</span><span class="sxs-lookup"><span data-stu-id="6ca61-104">SYNTAX</span></span>

### <span data-ttu-id="6ca61-105">DefaultParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6ca61-105">DefaultParameterSet (Default)</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ca61-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ca61-106">ResourceIDParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ca61-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ca61-107">InputObjectParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ca61-108">설명</span><span class="sxs-lookup"><span data-stu-id="6ca61-108">DESCRIPTION</span></span>
<span data-ttu-id="6ca61-109">VM의 패치 상태를 평가하고 설치에 사용할 수 있는 검색된 모든 패치를 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="6ca61-109">Assesses the patch status of a VM and reports all detected patches that are available for installation.</span></span>

## <span data-ttu-id="6ca61-110">예제</span><span class="sxs-lookup"><span data-stu-id="6ca61-110">EXAMPLES</span></span>

### <span data-ttu-id="6ca61-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6ca61-111">Example 1</span></span>
```
PS C:\> Invoke-AzVmPatchAssessment -ResourceGroupName "myRG" -VMName "myVM"
```

## <span data-ttu-id="6ca61-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ca61-112">PARAMETERS</span></span>

### <span data-ttu-id="6ca61-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ca61-113">-AsJob</span></span>
<span data-ttu-id="6ca61-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6ca61-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6ca61-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ca61-115">-DefaultProfile</span></span>
<span data-ttu-id="6ca61-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6ca61-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ca61-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ca61-117">-ResourceGroupName</span></span>
<span data-ttu-id="6ca61-118">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6ca61-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ca61-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ca61-119">-ResourceId</span></span>
<span data-ttu-id="6ca61-120">가상 머신에 대한 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6ca61-120">Resource ID for your virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIDParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ca61-121">-VM</span><span class="sxs-lookup"><span data-stu-id="6ca61-121">-VM</span></span>
<span data-ttu-id="6ca61-122">PowerShell Virtual Machine 개체</span><span class="sxs-lookup"><span data-stu-id="6ca61-122">PowerShell Virtual Machine Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: InputObjectParameterSet
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ca61-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="6ca61-123">-VMName</span></span>
<span data-ttu-id="6ca61-124">Virtual Machine 이름</span><span class="sxs-lookup"><span data-stu-id="6ca61-124">Virtual Machine name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ca61-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6ca61-125">-Confirm</span></span>
<span data-ttu-id="6ca61-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6ca61-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ca61-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ca61-127">-WhatIf</span></span>
<span data-ttu-id="6ca61-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6ca61-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6ca61-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6ca61-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ca61-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ca61-130">CommonParameters</span></span>
<span data-ttu-id="6ca61-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6ca61-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ca61-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6ca61-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ca61-133">입력</span><span class="sxs-lookup"><span data-stu-id="6ca61-133">INPUTS</span></span>

### <span data-ttu-id="6ca61-134">System.String</span><span class="sxs-lookup"><span data-stu-id="6ca61-134">System.String</span></span>

## <span data-ttu-id="6ca61-135">출력</span><span class="sxs-lookup"><span data-stu-id="6ca61-135">OUTPUTS</span></span>

### <span data-ttu-id="6ca61-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachinePatchAssessmentResult</span><span class="sxs-lookup"><span data-stu-id="6ca61-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachinePatchAssessmentResult</span></span>

## <span data-ttu-id="6ca61-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6ca61-137">NOTES</span></span>

## <span data-ttu-id="6ca61-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6ca61-138">RELATED LINKS</span></span>
