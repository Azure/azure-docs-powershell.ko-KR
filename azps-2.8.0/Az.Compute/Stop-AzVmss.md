---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmss.md
ms.openlocfilehash: eb05601028d43a7260186754f2a3e55b0691793d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697174"
---
# <span data-ttu-id="b8bc4-101">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b8bc4-101">Stop-AzVmss</span></span>

## <span data-ttu-id="b8bc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8bc4-102">SYNOPSIS</span></span>
<span data-ttu-id="b8bc4-103">Vmss 또는 VMSS 내의 가상 컴퓨터 집합을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8bc4-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="b8bc4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b8bc4-104">SYNTAX</span></span>

### <span data-ttu-id="b8bc4-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="b8bc4-105">DefaultParameter (Default)</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8bc4-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="b8bc4-106">FriendMethod</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-SkipShutdown] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b8bc4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b8bc4-107">DESCRIPTION</span></span>
<span data-ttu-id="b8bc4-108">**AzVmss** CMDLET은 vmss (가상 컴퓨터 크기 집합) 또는 가상 컴퓨터 집합 내의 모든 가상 컴퓨터를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8bc4-108">The **Stop-AzVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="b8bc4-109">*InstanceId* 매개 변수를 사용 하 여 가상 컴퓨터 집합을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b8bc4-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="b8bc4-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b8bc4-110">EXAMPLES</span></span>

### <span data-ttu-id="b8bc4-111">예제 1: VMSS 내의 모든 가상 컴퓨터 중지</span><span class="sxs-lookup"><span data-stu-id="b8bc4-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="b8bc4-112">이 명령은 ContosoVMSS 이라는 VMSS에 속한 모든 가상 컴퓨터를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8bc4-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="b8bc4-113">예제 2: VMSS 내에서 특정 가상 컴퓨터 집합 중지</span><span class="sxs-lookup"><span data-stu-id="b8bc4-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="b8bc4-114">이 명령은 ContosoVMSS 이라는 VMSS에 속하는 인스턴스 ID 문자열 배열로 지정 된 특정 가상 컴퓨터 집합을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8bc4-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="b8bc4-115">변수</span><span class="sxs-lookup"><span data-stu-id="b8bc4-115">PARAMETERS</span></span>

### <span data-ttu-id="b8bc4-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8bc4-116">-AsJob</span></span>
<span data-ttu-id="b8bc4-117">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8bc4-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b8bc4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8bc4-118">-DefaultProfile</span></span>
<span data-ttu-id="b8bc4-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b8bc4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8bc4-120">-Force</span><span class="sxs-lookup"><span data-stu-id="b8bc4-120">-Force</span></span>
<span data-ttu-id="b8bc4-121">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8bc4-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b8bc4-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="b8bc4-122">-InstanceId</span></span>
<span data-ttu-id="b8bc4-123">이 cmdlet이 중지 하는 가상 컴퓨터 인스턴스의 ID 또는 식별자를 문자열 배열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8bc4-123">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="b8bc4-124">예: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="b8bc4-124">For instance: `-InstanceId "0", "3"`.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8bc4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8bc4-125">-ResourceGroupName</span></span>
<span data-ttu-id="b8bc4-126">VMSS의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8bc4-126">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="b8bc4-127">-SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="b8bc4-127">-SkipShutdown</span></span>
<span data-ttu-id="b8bc4-128">정상 되지 않은 VM 종료를 요청 하려면</span><span class="sxs-lookup"><span data-stu-id="b8bc4-128">To request non-graceful VM shutdown</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8bc4-129">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="b8bc4-129">-StayProvisioned</span></span>
<span data-ttu-id="b8bc4-130">지정 된 경우 가상 컴퓨터는 중지 됨 상태로 전환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8bc4-130">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="b8bc4-131">지정 하지 않으면 가상 컴퓨터가 중지 된 할당 취소 상태로 전환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8bc4-131">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="b8bc4-132">중지 된 상태의 Vm에 대해서는 사용자가 여전히 청구 되지만 중지 되지 않은 상태의 Vm에 대해서는 할당 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b8bc4-132">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8bc4-133">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b8bc4-133">-VMScaleSetName</span></span>
<span data-ttu-id="b8bc4-134">이 cmdlet이 가상 컴퓨터를 중지 하는 VMSS의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8bc4-134">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

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

### <span data-ttu-id="b8bc4-135">-확인</span><span class="sxs-lookup"><span data-stu-id="b8bc4-135">-Confirm</span></span>
<span data-ttu-id="b8bc4-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8bc4-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8bc4-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8bc4-137">-WhatIf</span></span>
<span data-ttu-id="b8bc4-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b8bc4-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b8bc4-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b8bc4-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8bc4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8bc4-140">CommonParameters</span></span>
<span data-ttu-id="b8bc4-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8bc4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8bc4-142">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b8bc4-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8bc4-143">입력</span><span class="sxs-lookup"><span data-stu-id="b8bc4-143">INPUTS</span></span>

### <span data-ttu-id="b8bc4-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b8bc4-144">System.String</span></span>

### <span data-ttu-id="b8bc4-145">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="b8bc4-145">System.String[]</span></span>

## <span data-ttu-id="b8bc4-146">출력</span><span class="sxs-lookup"><span data-stu-id="b8bc4-146">OUTPUTS</span></span>

### <span data-ttu-id="b8bc4-147">PSOperationStatusResponse의. m a.</span><span class="sxs-lookup"><span data-stu-id="b8bc4-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="b8bc4-148">상속자</span><span class="sxs-lookup"><span data-stu-id="b8bc4-148">NOTES</span></span>

## <span data-ttu-id="b8bc4-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8bc4-149">RELATED LINKS</span></span>

[<span data-ttu-id="b8bc4-150">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b8bc4-150">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="b8bc4-151">새로운 AzVmss</span><span class="sxs-lookup"><span data-stu-id="b8bc4-151">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="b8bc4-152">제거-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b8bc4-152">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="b8bc4-153">다시 시작-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b8bc4-153">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="b8bc4-154">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b8bc4-154">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="b8bc4-155">시작-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b8bc4-155">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="b8bc4-156">업데이트-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b8bc4-156">Update-AzVmss</span></span>](./Update-AzVmss.md)

