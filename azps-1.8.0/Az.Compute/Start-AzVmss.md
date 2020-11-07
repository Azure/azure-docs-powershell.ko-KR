---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmss.md
ms.openlocfilehash: 93c70344b2a5ce9f03e4b0c1088fa785989912da
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868857"
---
# <span data-ttu-id="e6cfe-101">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e6cfe-101">Start-AzVmss</span></span>

## <span data-ttu-id="e6cfe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6cfe-102">SYNOPSIS</span></span>
<span data-ttu-id="e6cfe-103">Vmss 또는 VMSS 내의 가상 컴퓨터 집합을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6cfe-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="e6cfe-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e6cfe-104">SYNTAX</span></span>

```
Start-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6cfe-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e6cfe-105">DESCRIPTION</span></span>
<span data-ttu-id="e6cfe-106">**AzVmss** CMDLET은 vmss (가상 컴퓨터 크기 집합) 또는 가상 컴퓨터 집합 내의 모든 가상 컴퓨터를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6cfe-106">The **Start-AzVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="e6cfe-107">*InstanceId* 매개 변수를 사용 하 여 가상 컴퓨터 집합을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6cfe-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="e6cfe-108">예제의</span><span class="sxs-lookup"><span data-stu-id="e6cfe-108">EXAMPLES</span></span>

### <span data-ttu-id="e6cfe-109">예제 1: VMSS 내에서 가상 컴퓨터의 특정 집합 시작</span><span class="sxs-lookup"><span data-stu-id="e6cfe-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="e6cfe-110">이 명령은 ContosoVMSS 이라는 VMSS에 속하는 인스턴스 ID 문자열 배열에 지정 된 가상 컴퓨터의 특정 집합을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6cfe-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="e6cfe-111">예제 2: VMSS 내의 모든 가상 컴퓨터 시작</span><span class="sxs-lookup"><span data-stu-id="e6cfe-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="e6cfe-112">이 명령은 ContosoVMSS 이라는 VMSS에 속하는 모든 가상 컴퓨터를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6cfe-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="e6cfe-113">변수</span><span class="sxs-lookup"><span data-stu-id="e6cfe-113">PARAMETERS</span></span>

### <span data-ttu-id="e6cfe-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6cfe-114">-AsJob</span></span>
<span data-ttu-id="e6cfe-115">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6cfe-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e6cfe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6cfe-116">-DefaultProfile</span></span>
<span data-ttu-id="e6cfe-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e6cfe-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6cfe-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="e6cfe-118">-InstanceId</span></span>
<span data-ttu-id="e6cfe-119">Cmdlet이 시작 되는 인스턴스의 ID 또는 식별자를 문자열 배열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6cfe-119">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="e6cfe-120">예를 들면 다음과 같습니다. `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="e6cfe-120">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="e6cfe-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6cfe-121">-ResourceGroupName</span></span>
<span data-ttu-id="e6cfe-122">VMSS의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6cfe-122">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="e6cfe-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="e6cfe-123">-VMScaleSetName</span></span>
<span data-ttu-id="e6cfe-124">이 cmdlet이 가상 컴퓨터를 시작 하는 VMSS의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6cfe-124">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

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

### <span data-ttu-id="e6cfe-125">-확인</span><span class="sxs-lookup"><span data-stu-id="e6cfe-125">-Confirm</span></span>
<span data-ttu-id="e6cfe-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6cfe-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6cfe-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6cfe-127">-WhatIf</span></span>
<span data-ttu-id="e6cfe-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e6cfe-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6cfe-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e6cfe-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6cfe-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6cfe-130">CommonParameters</span></span>
<span data-ttu-id="e6cfe-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6cfe-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6cfe-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6cfe-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6cfe-133">입력</span><span class="sxs-lookup"><span data-stu-id="e6cfe-133">INPUTS</span></span>

### <span data-ttu-id="e6cfe-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e6cfe-134">System.String</span></span>

### <span data-ttu-id="e6cfe-135">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="e6cfe-135">System.String[]</span></span>

## <span data-ttu-id="e6cfe-136">출력</span><span class="sxs-lookup"><span data-stu-id="e6cfe-136">OUTPUTS</span></span>

### <span data-ttu-id="e6cfe-137">PSOperationStatusResponse의. m a.</span><span class="sxs-lookup"><span data-stu-id="e6cfe-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="e6cfe-138">상속자</span><span class="sxs-lookup"><span data-stu-id="e6cfe-138">NOTES</span></span>

## <span data-ttu-id="e6cfe-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e6cfe-139">RELATED LINKS</span></span>

[<span data-ttu-id="e6cfe-140">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e6cfe-140">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="e6cfe-141">새로운 AzVmss</span><span class="sxs-lookup"><span data-stu-id="e6cfe-141">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="e6cfe-142">제거-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e6cfe-142">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="e6cfe-143">다시 시작-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e6cfe-143">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="e6cfe-144">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e6cfe-144">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="e6cfe-145">중지-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e6cfe-145">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="e6cfe-146">업데이트-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e6cfe-146">Update-AzVmss</span></span>](./Update-AzVmss.md)


