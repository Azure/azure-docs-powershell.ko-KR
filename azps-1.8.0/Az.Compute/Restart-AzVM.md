---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
ms.openlocfilehash: 5f2c7d4c3a047a4893158e7f1a12b375106d640b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701264"
---
# <span data-ttu-id="b862c-101">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="b862c-101">Restart-AzVM</span></span>

## <span data-ttu-id="b862c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b862c-102">SYNOPSIS</span></span>
<span data-ttu-id="b862c-103">Azure 가상 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="b862c-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="b862c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b862c-104">SYNTAX</span></span>

### <span data-ttu-id="b862c-105">RestartResourceGroupNameParameterSetName (기본값)</span><span class="sxs-lookup"><span data-stu-id="b862c-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b862c-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="b862c-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b862c-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="b862c-107">RestartIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [[-Name] <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b862c-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="b862c-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [[-Name] <String>] [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b862c-109">설명은</span><span class="sxs-lookup"><span data-stu-id="b862c-109">DESCRIPTION</span></span>
<span data-ttu-id="b862c-110">**AzVM** Cmdlet은 Azure 가상 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="b862c-110">The **Restart-AzVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="b862c-111">예제의</span><span class="sxs-lookup"><span data-stu-id="b862c-111">EXAMPLES</span></span>

### <span data-ttu-id="b862c-112">예제 1: 가상 컴퓨터 다시 시작</span><span class="sxs-lookup"><span data-stu-id="b862c-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="b862c-113">이 명령은 ResourceGroup11에서 VirtualMachine07 이라는 가상 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="b862c-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="b862c-114">변수</span><span class="sxs-lookup"><span data-stu-id="b862c-114">PARAMETERS</span></span>

### <span data-ttu-id="b862c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b862c-115">-AsJob</span></span>
<span data-ttu-id="b862c-116">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="b862c-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b862c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b862c-117">-DefaultProfile</span></span>
<span data-ttu-id="b862c-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b862c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b862c-119">-Id</span><span class="sxs-lookup"><span data-stu-id="b862c-119">-Id</span></span>
<span data-ttu-id="b862c-120">가상 컴퓨터의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b862c-120">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="b862c-121">-이름</span><span class="sxs-lookup"><span data-stu-id="b862c-121">-Name</span></span>
<span data-ttu-id="b862c-122">가상 컴퓨터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b862c-122">The virtual machine name.</span></span>

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

```yaml
Type: System.String
Parameter Sets: RestartIdParameterSetName, PerformMaintenanceIdParameterSetName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b862c-123">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="b862c-123">-PerformMaintenance</span></span>
<span data-ttu-id="b862c-124">가상 컴퓨터의 유지 관리를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b862c-124">To perform the maintenance of virtual machine.</span></span>

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

### <span data-ttu-id="b862c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b862c-125">-ResourceGroupName</span></span>
<span data-ttu-id="b862c-126">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b862c-126">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="b862c-127">-확인</span><span class="sxs-lookup"><span data-stu-id="b862c-127">-Confirm</span></span>
<span data-ttu-id="b862c-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b862c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b862c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b862c-129">-WhatIf</span></span>
<span data-ttu-id="b862c-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b862c-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b862c-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b862c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b862c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b862c-132">CommonParameters</span></span>
<span data-ttu-id="b862c-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b862c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b862c-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b862c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b862c-135">입력</span><span class="sxs-lookup"><span data-stu-id="b862c-135">INPUTS</span></span>

### <span data-ttu-id="b862c-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b862c-136">System.String</span></span>

### <span data-ttu-id="b862c-137">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b862c-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b862c-138">출력</span><span class="sxs-lookup"><span data-stu-id="b862c-138">OUTPUTS</span></span>

### <span data-ttu-id="b862c-139">PSComputeLongRunningOperation를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="b862c-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="b862c-140">상속자</span><span class="sxs-lookup"><span data-stu-id="b862c-140">NOTES</span></span>

## <span data-ttu-id="b862c-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b862c-141">RELATED LINKS</span></span>

[<span data-ttu-id="b862c-142">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="b862c-142">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="b862c-143">새로운 AzVM</span><span class="sxs-lookup"><span data-stu-id="b862c-143">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="b862c-144">제거-AzVM</span><span class="sxs-lookup"><span data-stu-id="b862c-144">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="b862c-145">시작-AzVM</span><span class="sxs-lookup"><span data-stu-id="b862c-145">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="b862c-146">중지-AzVM</span><span class="sxs-lookup"><span data-stu-id="b862c-146">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="b862c-147">업데이트-AzVM</span><span class="sxs-lookup"><span data-stu-id="b862c-147">Update-AzVM</span></span>](./Update-AzVM.md)


