---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmssrollingosupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
ms.openlocfilehash: ad5d387a0935150a66924cbfdd19ac40ed57079c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327361"
---
# <span data-ttu-id="13fb3-101">Start-AzVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="13fb3-101">Start-AzVmssRollingOSUpgrade</span></span>

## <span data-ttu-id="13fb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13fb3-102">SYNOPSIS</span></span>
<span data-ttu-id="13fb3-103">모든 가상 머신 확장 집합 인스턴스를 사용 가능한 최신 플랫폼 이미지 OS 버전으로 이동하는 롤링 업그레이드를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="13fb3-103">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>

## <span data-ttu-id="13fb3-104">구문</span><span class="sxs-lookup"><span data-stu-id="13fb3-104">SYNTAX</span></span>

```
Start-AzVmssRollingOSUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13fb3-105">설명</span><span class="sxs-lookup"><span data-stu-id="13fb3-105">DESCRIPTION</span></span>
<span data-ttu-id="13fb3-106">모든 가상 머신 확장 집합 인스턴스를 사용 가능한 최신 플랫폼 이미지 OS 버전으로 이동하는 롤링 업그레이드를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="13fb3-106">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>
<span data-ttu-id="13fb3-107">사용 가능한 최신 OS 버전을 이미 실행 중인 인스턴스는 영향을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="13fb3-107">Instances which are already running the latest available OS version are not affected.</span></span>

## <span data-ttu-id="13fb3-108">예제</span><span class="sxs-lookup"><span data-stu-id="13fb3-108">EXAMPLES</span></span>

### <span data-ttu-id="13fb3-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="13fb3-109">Example 1</span></span>
```
PS C:\> Start-AzVmssRollingOSUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="13fb3-110">이 명령은 리소스 그룹 "Group001"에서 VM 확장 집합 "VMSS001"의 모든 VM 인스턴스의 롤링 업그레이드를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="13fb3-110">This command starts a rolling upgrade of all vm instances of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="13fb3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13fb3-111">PARAMETERS</span></span>

### <span data-ttu-id="13fb3-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13fb3-112">-AsJob</span></span>
<span data-ttu-id="13fb3-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="13fb3-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="13fb3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13fb3-114">-DefaultProfile</span></span>
<span data-ttu-id="13fb3-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="13fb3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13fb3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13fb3-116">-ResourceGroupName</span></span>
<span data-ttu-id="13fb3-117">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13fb3-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="13fb3-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="13fb3-118">-VMScaleSetName</span></span>
<span data-ttu-id="13fb3-119">VM 확장 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13fb3-119">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="13fb3-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13fb3-120">-Confirm</span></span>
<span data-ttu-id="13fb3-121">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="13fb3-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13fb3-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13fb3-122">-WhatIf</span></span>
<span data-ttu-id="13fb3-123">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="13fb3-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13fb3-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="13fb3-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13fb3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13fb3-125">CommonParameters</span></span>
<span data-ttu-id="13fb3-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="13fb3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13fb3-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="13fb3-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13fb3-128">입력</span><span class="sxs-lookup"><span data-stu-id="13fb3-128">INPUTS</span></span>

### <span data-ttu-id="13fb3-129">System.String</span><span class="sxs-lookup"><span data-stu-id="13fb3-129">System.String</span></span>

## <span data-ttu-id="13fb3-130">출력</span><span class="sxs-lookup"><span data-stu-id="13fb3-130">OUTPUTS</span></span>

### <span data-ttu-id="13fb3-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="13fb3-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="13fb3-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="13fb3-132">NOTES</span></span>

## <span data-ttu-id="13fb3-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13fb3-133">RELATED LINKS</span></span>
