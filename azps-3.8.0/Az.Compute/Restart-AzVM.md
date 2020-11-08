---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
ms.openlocfilehash: 358b24c403c4b08b221f97ad99271112ee0852be
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042100"
---
# <span data-ttu-id="05a73-101">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="05a73-101">Restart-AzVM</span></span>

## <span data-ttu-id="05a73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05a73-102">SYNOPSIS</span></span>
<span data-ttu-id="05a73-103">Azure 가상 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="05a73-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="05a73-104">구문과</span><span class="sxs-lookup"><span data-stu-id="05a73-104">SYNTAX</span></span>

### <span data-ttu-id="05a73-105">RestartResourceGroupNameParameterSetName (기본값)</span><span class="sxs-lookup"><span data-stu-id="05a73-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05a73-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="05a73-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05a73-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="05a73-107">RestartIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="05a73-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="05a73-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-PerformMaintenance] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05a73-109">설명은</span><span class="sxs-lookup"><span data-stu-id="05a73-109">DESCRIPTION</span></span>
<span data-ttu-id="05a73-110">**AzVM** Cmdlet은 Azure 가상 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="05a73-110">The **Restart-AzVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="05a73-111">예제의</span><span class="sxs-lookup"><span data-stu-id="05a73-111">EXAMPLES</span></span>

### <span data-ttu-id="05a73-112">예제 1: 가상 컴퓨터 다시 시작</span><span class="sxs-lookup"><span data-stu-id="05a73-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="05a73-113">이 명령은 ResourceGroup11에서 VirtualMachine07 이라는 가상 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="05a73-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="05a73-114">변수</span><span class="sxs-lookup"><span data-stu-id="05a73-114">PARAMETERS</span></span>

### <span data-ttu-id="05a73-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05a73-115">-AsJob</span></span>
<span data-ttu-id="05a73-116">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="05a73-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="05a73-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05a73-117">-DefaultProfile</span></span>
<span data-ttu-id="05a73-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="05a73-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05a73-119">-Id</span><span class="sxs-lookup"><span data-stu-id="05a73-119">-Id</span></span>
<span data-ttu-id="05a73-120">가상 컴퓨터의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="05a73-120">The ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartIdParameterSetName, PerformMaintenanceIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05a73-121">-이름</span><span class="sxs-lookup"><span data-stu-id="05a73-121">-Name</span></span>
<span data-ttu-id="05a73-122">가상 컴퓨터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05a73-122">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05a73-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="05a73-123">-NoWait</span></span>
<span data-ttu-id="05a73-124">작업이 완료 되기 전에 작업을 시작 하 고 즉시 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="05a73-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="05a73-125">작업이 성공적으로 완료 되었는지 확인 하려면 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="05a73-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="05a73-126">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="05a73-126">-PerformMaintenance</span></span>
<span data-ttu-id="05a73-127">가상 컴퓨터의 유지 관리를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="05a73-127">To perform the maintenance of virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceResourceGroupNameParameterSetName, PerformMaintenanceIdParameterSetName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05a73-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05a73-128">-ResourceGroupName</span></span>
<span data-ttu-id="05a73-129">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05a73-129">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05a73-130">-확인</span><span class="sxs-lookup"><span data-stu-id="05a73-130">-Confirm</span></span>
<span data-ttu-id="05a73-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="05a73-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05a73-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05a73-132">-WhatIf</span></span>
<span data-ttu-id="05a73-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="05a73-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="05a73-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="05a73-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05a73-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05a73-135">CommonParameters</span></span>
<span data-ttu-id="05a73-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="05a73-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05a73-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="05a73-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05a73-138">입력</span><span class="sxs-lookup"><span data-stu-id="05a73-138">INPUTS</span></span>

### <span data-ttu-id="05a73-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="05a73-139">System.String</span></span>

### <span data-ttu-id="05a73-140">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="05a73-140">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="05a73-141">출력</span><span class="sxs-lookup"><span data-stu-id="05a73-141">OUTPUTS</span></span>

### <span data-ttu-id="05a73-142">PSComputeLongRunningOperation를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="05a73-142">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="05a73-143">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="05a73-143">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="05a73-144">상속자</span><span class="sxs-lookup"><span data-stu-id="05a73-144">NOTES</span></span>

## <span data-ttu-id="05a73-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="05a73-145">RELATED LINKS</span></span>

[<span data-ttu-id="05a73-146">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="05a73-146">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="05a73-147">새로운 AzVM</span><span class="sxs-lookup"><span data-stu-id="05a73-147">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="05a73-148">제거-AzVM</span><span class="sxs-lookup"><span data-stu-id="05a73-148">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="05a73-149">시작-AzVM</span><span class="sxs-lookup"><span data-stu-id="05a73-149">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="05a73-150">중지-AzVM</span><span class="sxs-lookup"><span data-stu-id="05a73-150">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="05a73-151">업데이트-AzVM</span><span class="sxs-lookup"><span data-stu-id="05a73-151">Update-AzVM</span></span>](./Update-AzVM.md)


