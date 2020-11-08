---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssorchestrationservicestate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOrchestrationServiceState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOrchestrationServiceState.md
ms.openlocfilehash: c1fbc45a9d82733f73a13b13985bdd6746f4c075
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044717"
---
# <span data-ttu-id="cd250-101">Set-AzVmssOrchestrationServiceState</span><span class="sxs-lookup"><span data-stu-id="cd250-101">Set-AzVmssOrchestrationServiceState</span></span>

## <span data-ttu-id="cd250-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd250-102">SYNOPSIS</span></span>
<span data-ttu-id="cd250-103">VMSS의 오케스트레이션 서비스 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd250-103">Sets the orchestration service state for the VMSS.</span></span>

## <span data-ttu-id="cd250-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cd250-104">SYNTAX</span></span>

### <span data-ttu-id="cd250-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="cd250-105">DefaultParameter (Default)</span></span>
```
Set-AzVmssOrchestrationServiceState [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-ServiceName] <String> [-Action] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd250-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="cd250-106">ResourceIdParameter</span></span>
```
Set-AzVmssOrchestrationServiceState [-ServiceName] <String> [-Action] <String> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd250-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="cd250-107">ObjectParameter</span></span>
```
Set-AzVmssOrchestrationServiceState [-ServiceName] <String> [-Action] <String>
 [-InputObject] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd250-108">설명은</span><span class="sxs-lookup"><span data-stu-id="cd250-108">DESCRIPTION</span></span>
<span data-ttu-id="cd250-109">VMSS의 오케스트레이션 서비스 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd250-109">Sets the orchestration service state for the VMSS.</span></span>

## <span data-ttu-id="cd250-110">예제의</span><span class="sxs-lookup"><span data-stu-id="cd250-110">EXAMPLES</span></span>

### <span data-ttu-id="cd250-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="cd250-111">Example 1</span></span>
```
PS C:\> Set-AzVmssOrchestrationServiceState -ResourceGroupName "rg" -VMScaleSetName "vmss1" -ServiceName "AutomaticRepairs" -Action "Suspend"
```

<span data-ttu-id="cd250-112">이 명령은 리소스 그룹 "rg"의 VMSS "vmss1"의 자동 복구 서비스를 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd250-112">This command suspends Automatic Repairs service on the VMSS "vmss1" in the resource group "rg".</span></span>

### <span data-ttu-id="cd250-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="cd250-113">Example 2</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "rg" -VMScaleSetName "vmss1" | Set-AzVmssOrchestrationServiceState -ServiceName "AutomaticRepairs" -Action "Resume"
```

<span data-ttu-id="cd250-114">이 명령은 리소스 그룹 "rg"에서 VMSS "vmss1"의 자동 복구 서비스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd250-114">This command resumes Automatic Repairs service on the VMSS "vmss1" in the resource group "rg".</span></span>

## <span data-ttu-id="cd250-115">변수</span><span class="sxs-lookup"><span data-stu-id="cd250-115">PARAMETERS</span></span>

### <span data-ttu-id="cd250-116">-작업</span><span class="sxs-lookup"><span data-stu-id="cd250-116">-Action</span></span>
<span data-ttu-id="cd250-117">수행할 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="cd250-117">The action to be performed.</span></span>  <span data-ttu-id="cd250-118">사용할 수 있는 값은: Resume, Suspend입니다.</span><span class="sxs-lookup"><span data-stu-id="cd250-118">Possible values are: Resume, Suspend.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd250-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd250-119">-AsJob</span></span>
<span data-ttu-id="cd250-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="cd250-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd250-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd250-121">-DefaultProfile</span></span>
<span data-ttu-id="cd250-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cd250-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd250-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd250-123">-InputObject</span></span>
<span data-ttu-id="cd250-124">가상 컴퓨터 크기 집합의 로컬 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="cd250-124">The local object of the virtual machine scale set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd250-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd250-125">-ResourceGroupName</span></span>
<span data-ttu-id="cd250-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd250-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd250-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd250-127">-ResourceId</span></span>
<span data-ttu-id="cd250-128">리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="cd250-128">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd250-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="cd250-129">-ServiceName</span></span>
<span data-ttu-id="cd250-130">서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd250-130">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd250-131">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="cd250-131">-VMScaleSetName</span></span>
<span data-ttu-id="cd250-132">가상 컴퓨터 배율 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd250-132">The name of the virtual machine scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd250-133">-확인</span><span class="sxs-lookup"><span data-stu-id="cd250-133">-Confirm</span></span>
<span data-ttu-id="cd250-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd250-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd250-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd250-135">-WhatIf</span></span>
<span data-ttu-id="cd250-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cd250-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd250-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd250-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd250-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd250-138">CommonParameters</span></span>
<span data-ttu-id="cd250-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd250-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd250-140">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cd250-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd250-141">입력</span><span class="sxs-lookup"><span data-stu-id="cd250-141">INPUTS</span></span>

### <span data-ttu-id="cd250-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cd250-142">System.String</span></span>

### <span data-ttu-id="cd250-143">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="cd250-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="cd250-144">출력</span><span class="sxs-lookup"><span data-stu-id="cd250-144">OUTPUTS</span></span>

### <span data-ttu-id="cd250-145">PSOperationStatusResponse의. m a.</span><span class="sxs-lookup"><span data-stu-id="cd250-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="cd250-146">상속자</span><span class="sxs-lookup"><span data-stu-id="cd250-146">NOTES</span></span>

## <span data-ttu-id="cd250-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cd250-147">RELATED LINKS</span></span>
