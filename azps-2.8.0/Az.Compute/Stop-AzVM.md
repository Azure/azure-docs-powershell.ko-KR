---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
ms.openlocfilehash: d0895fc436f4f7d59a4d9f5b6cfc18574d7e8d9b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697176"
---
# <span data-ttu-id="dab86-101">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="dab86-101">Stop-AzVM</span></span>

## <span data-ttu-id="dab86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dab86-102">SYNOPSIS</span></span>
<span data-ttu-id="dab86-103">Azure 가상 컴퓨터를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="dab86-103">Stops an Azure virtual machine.</span></span>

## <span data-ttu-id="dab86-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dab86-104">SYNTAX</span></span>

### <span data-ttu-id="dab86-105">ResourceGroupNameParameterSetName (기본값)</span><span class="sxs-lookup"><span data-stu-id="dab86-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-ResourceGroupName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dab86-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="dab86-106">IdParameterSetName</span></span>
```
Stop-AzVM [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dab86-107">설명은</span><span class="sxs-lookup"><span data-stu-id="dab86-107">DESCRIPTION</span></span>
<span data-ttu-id="dab86-108">**AzVM** Cmdlet은 Azure 가상 컴퓨터를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="dab86-108">The **Stop-AzVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="dab86-109">예제의</span><span class="sxs-lookup"><span data-stu-id="dab86-109">EXAMPLES</span></span>

### <span data-ttu-id="dab86-110">예제 1: 가상 컴퓨터 중지</span><span class="sxs-lookup"><span data-stu-id="dab86-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="dab86-111">이 명령은 ResourceGroup11에서 VirtualMachine07 이라는 가상 컴퓨터를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="dab86-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="dab86-112">변수</span><span class="sxs-lookup"><span data-stu-id="dab86-112">PARAMETERS</span></span>

### <span data-ttu-id="dab86-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dab86-113">-AsJob</span></span>
<span data-ttu-id="dab86-114">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="dab86-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="dab86-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dab86-115">-DefaultProfile</span></span>
<span data-ttu-id="dab86-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dab86-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dab86-117">-Force</span><span class="sxs-lookup"><span data-stu-id="dab86-117">-Force</span></span>
<span data-ttu-id="dab86-118">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="dab86-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dab86-119">-Id</span><span class="sxs-lookup"><span data-stu-id="dab86-119">-Id</span></span>
<span data-ttu-id="dab86-120">가상 컴퓨터의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="dab86-120">The ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dab86-121">-이름</span><span class="sxs-lookup"><span data-stu-id="dab86-121">-Name</span></span>
<span data-ttu-id="dab86-122">가상 컴퓨터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dab86-122">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dab86-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="dab86-123">-NoWait</span></span>
<span data-ttu-id="dab86-124">작업이 완료 되기 전에 작업을 시작 하 고 즉시 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="dab86-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="dab86-125">작업이 성공적으로 완료 되었는지 확인 하려면 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dab86-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="dab86-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dab86-126">-ResourceGroupName</span></span>
<span data-ttu-id="dab86-127">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dab86-127">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dab86-128">-SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="dab86-128">-SkipShutdown</span></span>
<span data-ttu-id="dab86-129">VM을 프로 비전 된 상태로 유지할 때 정상 되지 않은 VM 종료를 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="dab86-129">To request non-graceful VM shutdown when keeping the VM provisioned.</span></span>

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

### <span data-ttu-id="dab86-130">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="dab86-130">-StayProvisioned</span></span>
<span data-ttu-id="dab86-131">Cmdlet은 VMSS 내의 모든 가상 컴퓨터를 중지 하지만 할당을 취소 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dab86-131">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="dab86-132">중지 된 가상 컴퓨터에 대해 계정이 청구 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dab86-132">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="dab86-133">-확인</span><span class="sxs-lookup"><span data-stu-id="dab86-133">-Confirm</span></span>
<span data-ttu-id="dab86-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dab86-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dab86-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dab86-135">-WhatIf</span></span>
<span data-ttu-id="dab86-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dab86-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dab86-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dab86-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dab86-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dab86-138">CommonParameters</span></span>
<span data-ttu-id="dab86-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dab86-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dab86-140">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dab86-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dab86-141">입력</span><span class="sxs-lookup"><span data-stu-id="dab86-141">INPUTS</span></span>

### <span data-ttu-id="dab86-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dab86-142">System.String</span></span>

## <span data-ttu-id="dab86-143">출력</span><span class="sxs-lookup"><span data-stu-id="dab86-143">OUTPUTS</span></span>

### <span data-ttu-id="dab86-144">PSComputeLongRunningOperation를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="dab86-144">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="dab86-145">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="dab86-145">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="dab86-146">상속자</span><span class="sxs-lookup"><span data-stu-id="dab86-146">NOTES</span></span>

## <span data-ttu-id="dab86-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dab86-147">RELATED LINKS</span></span>

[<span data-ttu-id="dab86-148">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="dab86-148">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="dab86-149">새로운 AzVM</span><span class="sxs-lookup"><span data-stu-id="dab86-149">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="dab86-150">제거-AzVM</span><span class="sxs-lookup"><span data-stu-id="dab86-150">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="dab86-151">다시 시작-AzVM</span><span class="sxs-lookup"><span data-stu-id="dab86-151">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="dab86-152">시작-AzVM</span><span class="sxs-lookup"><span data-stu-id="dab86-152">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="dab86-153">업데이트-AzVM</span><span class="sxs-lookup"><span data-stu-id="dab86-153">Update-AzVM</span></span>](./Update-AzVM.md)

