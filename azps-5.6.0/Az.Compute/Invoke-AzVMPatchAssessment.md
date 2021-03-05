---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMPatchAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMPatchAssessment.md
ms.openlocfilehash: 52e7a7372372bfcb0dfc93a9a89715e91c484b73
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985301"
---
# <span data-ttu-id="12b18-101">Invoke-AzVMPatchAssessment</span><span class="sxs-lookup"><span data-stu-id="12b18-101">Invoke-AzVMPatchAssessment</span></span>

## <span data-ttu-id="12b18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12b18-102">SYNOPSIS</span></span>
<span data-ttu-id="12b18-103">가상 머신의 패치 상태를 평가합니다.</span><span class="sxs-lookup"><span data-stu-id="12b18-103">Assess patch state of a virtual machine.</span></span>

## <span data-ttu-id="12b18-104">구문</span><span class="sxs-lookup"><span data-stu-id="12b18-104">SYNTAX</span></span>

### <span data-ttu-id="12b18-105">DefaultParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="12b18-105">DefaultParameterSet (Default)</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12b18-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="12b18-106">ResourceIDParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12b18-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="12b18-107">InputObjectParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12b18-108">설명</span><span class="sxs-lookup"><span data-stu-id="12b18-108">DESCRIPTION</span></span>
<span data-ttu-id="12b18-109">VM의 패치 상태를 평가하고 설치에 사용할 수 있는 검색된 모든 패치를 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="12b18-109">Assesses the patch status of a VM and reports all detected patches that are available for installation.</span></span>

## <span data-ttu-id="12b18-110">예제</span><span class="sxs-lookup"><span data-stu-id="12b18-110">EXAMPLES</span></span>

### <span data-ttu-id="12b18-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="12b18-111">Example 1</span></span>
```
PS C:\> Invoke-AzVmPatchAssessment -ResourceGroupName "myRG" -VMName "myVM"
```

## <span data-ttu-id="12b18-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="12b18-112">PARAMETERS</span></span>

### <span data-ttu-id="12b18-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12b18-113">-AsJob</span></span>
<span data-ttu-id="12b18-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="12b18-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="12b18-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12b18-115">-DefaultProfile</span></span>
<span data-ttu-id="12b18-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="12b18-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12b18-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12b18-117">-ResourceGroupName</span></span>
<span data-ttu-id="12b18-118">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="12b18-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="12b18-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12b18-119">-ResourceId</span></span>
<span data-ttu-id="12b18-120">가상 머신의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="12b18-120">Resource ID for your virtual machine.</span></span>

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

### <span data-ttu-id="12b18-121">-VM</span><span class="sxs-lookup"><span data-stu-id="12b18-121">-VM</span></span>
<span data-ttu-id="12b18-122">PowerShell Virtual Machine 개체</span><span class="sxs-lookup"><span data-stu-id="12b18-122">PowerShell Virtual Machine Object</span></span>

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

### <span data-ttu-id="12b18-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="12b18-123">-VMName</span></span>
<span data-ttu-id="12b18-124">Virtual Machine 이름</span><span class="sxs-lookup"><span data-stu-id="12b18-124">Virtual Machine name</span></span>

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

### <span data-ttu-id="12b18-125">-확인</span><span class="sxs-lookup"><span data-stu-id="12b18-125">-Confirm</span></span>
<span data-ttu-id="12b18-126">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="12b18-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12b18-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12b18-127">-WhatIf</span></span>
<span data-ttu-id="12b18-128">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="12b18-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="12b18-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="12b18-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12b18-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12b18-130">CommonParameters</span></span>
<span data-ttu-id="12b18-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="12b18-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12b18-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="12b18-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12b18-133">입력</span><span class="sxs-lookup"><span data-stu-id="12b18-133">INPUTS</span></span>

### <span data-ttu-id="12b18-134">System.String</span><span class="sxs-lookup"><span data-stu-id="12b18-134">System.String</span></span>

## <span data-ttu-id="12b18-135">출력</span><span class="sxs-lookup"><span data-stu-id="12b18-135">OUTPUTS</span></span>

### <span data-ttu-id="12b18-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachinePatchAssessmentResult</span><span class="sxs-lookup"><span data-stu-id="12b18-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachinePatchAssessmentResult</span></span>

## <span data-ttu-id="12b18-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="12b18-137">NOTES</span></span>

## <span data-ttu-id="12b18-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="12b18-138">RELATED LINKS</span></span>
