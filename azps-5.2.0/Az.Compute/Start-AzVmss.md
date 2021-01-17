---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmss.md
ms.openlocfilehash: 1845e7f1e76f4b05624c9c79500389b2839d25dd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362321"
---
# <span data-ttu-id="9d126-101">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9d126-101">Start-AzVmss</span></span>

## <span data-ttu-id="9d126-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d126-102">SYNOPSIS</span></span>
<span data-ttu-id="9d126-103">VMSS 또는 VMSS 내의 가상 머신 집합을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="9d126-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="9d126-104">구문</span><span class="sxs-lookup"><span data-stu-id="9d126-104">SYNTAX</span></span>

```
Start-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d126-105">설명</span><span class="sxs-lookup"><span data-stu-id="9d126-105">DESCRIPTION</span></span>
<span data-ttu-id="9d126-106">**Start-AzVmss** cmdlet은 VMSS(Virtual Machine Scale Set) 또는 가상 머신 집합 내의 모든 가상 머신을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="9d126-106">The **Start-AzVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="9d126-107">*InstanceId* 매개 변수를 사용하여 가상 머신 집합을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9d126-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="9d126-108">예제</span><span class="sxs-lookup"><span data-stu-id="9d126-108">EXAMPLES</span></span>

### <span data-ttu-id="9d126-109">예제 1: VMSS 내에서 특정 가상 머신 집합 시작</span><span class="sxs-lookup"><span data-stu-id="9d126-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="9d126-110">이 명령은 ContosoVMSS라는 VMSS에 속하는 인스턴스 ID 문자열 배열로 지정된 특정 가상 머신 집합을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="9d126-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="9d126-111">예제 2: VMSS 내의 모든 가상 머신 시작</span><span class="sxs-lookup"><span data-stu-id="9d126-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="9d126-112">이 명령은 ContosoVMSS라는 VMSS에 속한 모든 가상 머신을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="9d126-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="9d126-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d126-113">PARAMETERS</span></span>

### <span data-ttu-id="9d126-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9d126-114">-AsJob</span></span>
<span data-ttu-id="9d126-115">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="9d126-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="9d126-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d126-116">-DefaultProfile</span></span>
<span data-ttu-id="9d126-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9d126-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d126-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="9d126-118">-InstanceId</span></span>
<span data-ttu-id="9d126-119">cmdlet이 시작하는 인스턴스의 ID 또는 ID를 문자열 배열로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9d126-119">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="9d126-120">예: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="9d126-120">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="9d126-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d126-121">-ResourceGroupName</span></span>
<span data-ttu-id="9d126-122">VMSS의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9d126-122">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="9d126-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="9d126-123">-VMScaleSetName</span></span>
<span data-ttu-id="9d126-124">이 cmdlet이 가상 머신을 시작하는 VMSS의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9d126-124">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

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

### <span data-ttu-id="9d126-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9d126-125">-Confirm</span></span>
<span data-ttu-id="9d126-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9d126-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d126-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d126-127">-WhatIf</span></span>
<span data-ttu-id="9d126-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9d126-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9d126-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9d126-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d126-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d126-130">CommonParameters</span></span>
<span data-ttu-id="9d126-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9d126-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d126-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9d126-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d126-133">입력</span><span class="sxs-lookup"><span data-stu-id="9d126-133">INPUTS</span></span>

### <span data-ttu-id="9d126-134">System.String</span><span class="sxs-lookup"><span data-stu-id="9d126-134">System.String</span></span>

### <span data-ttu-id="9d126-135">System.String[]</span><span class="sxs-lookup"><span data-stu-id="9d126-135">System.String[]</span></span>

## <span data-ttu-id="9d126-136">출력</span><span class="sxs-lookup"><span data-stu-id="9d126-136">OUTPUTS</span></span>

### <span data-ttu-id="9d126-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="9d126-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="9d126-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9d126-138">NOTES</span></span>

## <span data-ttu-id="9d126-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9d126-139">RELATED LINKS</span></span>

[<span data-ttu-id="9d126-140">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9d126-140">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="9d126-141">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9d126-141">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="9d126-142">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9d126-142">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="9d126-143">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9d126-143">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="9d126-144">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9d126-144">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="9d126-145">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9d126-145">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="9d126-146">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9d126-146">Update-AzVmss</span></span>](./Update-AzVmss.md)


