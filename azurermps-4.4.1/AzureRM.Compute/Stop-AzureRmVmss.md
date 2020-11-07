---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVmss.md
ms.openlocfilehash: 11b387e4022bce98e1275bb2af09bc97beff0041
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703125"
---
# <span data-ttu-id="922d2-101">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="922d2-101">Stop-AzureRmVmss</span></span>

## <span data-ttu-id="922d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="922d2-102">SYNOPSIS</span></span>
<span data-ttu-id="922d2-103">Vmss 또는 VMSS 내의 가상 컴퓨터 집합을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="922d2-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="922d2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="922d2-104">SYNTAX</span></span>

### <span data-ttu-id="922d2-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="922d2-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="922d2-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="922d2-106">FriendMethod</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="922d2-107">설명은</span><span class="sxs-lookup"><span data-stu-id="922d2-107">DESCRIPTION</span></span>
<span data-ttu-id="922d2-108">**AzureRmVmss** CMDLET은 vmss (가상 컴퓨터 크기 집합) 또는 가상 컴퓨터 집합 내의 모든 가상 컴퓨터를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="922d2-108">The **Stop-AzureRmVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="922d2-109">*InstanceId* 매개 변수를 사용 하 여 가상 컴퓨터 집합을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="922d2-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="922d2-110">예제의</span><span class="sxs-lookup"><span data-stu-id="922d2-110">EXAMPLES</span></span>

### <span data-ttu-id="922d2-111">예제 1: VMSS 내의 모든 가상 컴퓨터 중지</span><span class="sxs-lookup"><span data-stu-id="922d2-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="922d2-112">이 명령은 ContosoVMSS 이라는 VMSS에 속한 모든 가상 컴퓨터를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="922d2-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="922d2-113">예제 2: VMSS 내에서 특정 가상 컴퓨터 집합 중지</span><span class="sxs-lookup"><span data-stu-id="922d2-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="922d2-114">이 명령은 ContosoVMSS 이라는 VMSS에 속하는 인스턴스 ID 문자열 배열로 지정 된 특정 가상 컴퓨터 집합을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="922d2-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="922d2-115">변수</span><span class="sxs-lookup"><span data-stu-id="922d2-115">PARAMETERS</span></span>

### <span data-ttu-id="922d2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="922d2-116">-DefaultProfile</span></span>
<span data-ttu-id="922d2-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="922d2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="922d2-118">-Force</span><span class="sxs-lookup"><span data-stu-id="922d2-118">-Force</span></span>
<span data-ttu-id="922d2-119">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="922d2-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="922d2-120">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="922d2-120">-InstanceId</span></span>
<span data-ttu-id="922d2-121">이 cmdlet이 중지 하는 가상 컴퓨터 인스턴스의 ID 또는 식별자를 문자열 배열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="922d2-121">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="922d2-122">예: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="922d2-122">For instance: `-InstanceId "0", "3"`.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="922d2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="922d2-123">-ResourceGroupName</span></span>
<span data-ttu-id="922d2-124">VMSS의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="922d2-124">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="922d2-125">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="922d2-125">-StayProvisioned</span></span>
<span data-ttu-id="922d2-126">지정 된 경우 가상 컴퓨터는 중지 됨 상태로 전환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="922d2-126">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="922d2-127">지정 하지 않으면 가상 컴퓨터가 중지 된 할당 취소 상태로 전환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="922d2-127">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="922d2-128">중지 된 상태의 Vm에 대해서는 사용자가 여전히 청구 되지만 중지 되지 않은 상태의 Vm에 대해서는 할당 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="922d2-128">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>


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

### <span data-ttu-id="922d2-129">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="922d2-129">-VMScaleSetName</span></span>
<span data-ttu-id="922d2-130">이 cmdlet이 가상 컴퓨터를 중지 하는 VMSS의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="922d2-130">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="922d2-131">-확인</span><span class="sxs-lookup"><span data-stu-id="922d2-131">-Confirm</span></span>
<span data-ttu-id="922d2-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="922d2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="922d2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="922d2-133">-WhatIf</span></span>
<span data-ttu-id="922d2-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="922d2-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="922d2-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="922d2-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="922d2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="922d2-136">CommonParameters</span></span>
<span data-ttu-id="922d2-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="922d2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="922d2-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="922d2-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="922d2-139">입력</span><span class="sxs-lookup"><span data-stu-id="922d2-139">INPUTS</span></span>

## <span data-ttu-id="922d2-140">출력</span><span class="sxs-lookup"><span data-stu-id="922d2-140">OUTPUTS</span></span>

## <span data-ttu-id="922d2-141">상속자</span><span class="sxs-lookup"><span data-stu-id="922d2-141">NOTES</span></span>

## <span data-ttu-id="922d2-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="922d2-142">RELATED LINKS</span></span>

[<span data-ttu-id="922d2-143">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="922d2-143">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="922d2-144">새로운 AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="922d2-144">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="922d2-145">제거-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="922d2-145">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="922d2-146">다시 시작-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="922d2-146">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="922d2-147">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="922d2-147">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="922d2-148">시작-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="922d2-148">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="922d2-149">업데이트-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="922d2-149">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


