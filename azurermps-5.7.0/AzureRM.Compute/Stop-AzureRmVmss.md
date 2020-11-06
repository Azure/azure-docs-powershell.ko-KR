---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVmss.md
ms.openlocfilehash: 3798590f3b4df738bc38231018adabf99ba39237
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536059"
---
# <span data-ttu-id="4e59d-101">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="4e59d-101">Stop-AzureRmVmss</span></span>

## <span data-ttu-id="4e59d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e59d-102">SYNOPSIS</span></span>
<span data-ttu-id="4e59d-103">Vmss 또는 VMSS 내의 가상 컴퓨터 집합을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e59d-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e59d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4e59d-104">SYNTAX</span></span>

### <span data-ttu-id="4e59d-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="4e59d-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e59d-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="4e59d-106">FriendMethod</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e59d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4e59d-107">DESCRIPTION</span></span>
<span data-ttu-id="4e59d-108">**AzureRmVmss** CMDLET은 vmss (가상 컴퓨터 크기 집합) 또는 가상 컴퓨터 집합 내의 모든 가상 컴퓨터를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e59d-108">The **Stop-AzureRmVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="4e59d-109">*InstanceId* 매개 변수를 사용 하 여 가상 컴퓨터 집합을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4e59d-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="4e59d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4e59d-110">EXAMPLES</span></span>

### <span data-ttu-id="4e59d-111">예제 1: VMSS 내의 모든 가상 컴퓨터 중지</span><span class="sxs-lookup"><span data-stu-id="4e59d-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="4e59d-112">이 명령은 ContosoVMSS 이라는 VMSS에 속한 모든 가상 컴퓨터를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e59d-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="4e59d-113">예제 2: VMSS 내에서 특정 가상 컴퓨터 집합 중지</span><span class="sxs-lookup"><span data-stu-id="4e59d-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="4e59d-114">이 명령은 ContosoVMSS 이라는 VMSS에 속하는 인스턴스 ID 문자열 배열로 지정 된 특정 가상 컴퓨터 집합을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e59d-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="4e59d-115">변수</span><span class="sxs-lookup"><span data-stu-id="4e59d-115">PARAMETERS</span></span>

### <span data-ttu-id="4e59d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="4e59d-116">-Force</span></span>
<span data-ttu-id="4e59d-117">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e59d-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e59d-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="4e59d-118">-InstanceId</span></span>
<span data-ttu-id="4e59d-119">이 cmdlet이 중지 하는 가상 컴퓨터 인스턴스의 ID 또는 식별자를 문자열 배열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e59d-119">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="4e59d-120">예: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="4e59d-120">For instance: `-InstanceId "0", "3"`.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e59d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e59d-121">-ResourceGroupName</span></span>
<span data-ttu-id="4e59d-122">VMSS의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e59d-122">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e59d-123">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="4e59d-123">-StayProvisioned</span></span>
<span data-ttu-id="4e59d-124">지정 된 경우 가상 컴퓨터는 중지 됨 상태로 전환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4e59d-124">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="4e59d-125">지정 하지 않으면 가상 컴퓨터가 중지 된 할당 취소 상태로 전환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4e59d-125">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="4e59d-126">중지 된 상태의 Vm에 대해서는 사용자가 여전히 청구 되지만 중지 되지 않은 상태의 Vm에 대해서는 할당 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4e59d-126">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e59d-127">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="4e59d-127">-VMScaleSetName</span></span>
<span data-ttu-id="4e59d-128">이 cmdlet이 가상 컴퓨터를 중지 하는 VMSS의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e59d-128">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e59d-129">-확인</span><span class="sxs-lookup"><span data-stu-id="4e59d-129">-Confirm</span></span>
<span data-ttu-id="4e59d-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e59d-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e59d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e59d-131">-WhatIf</span></span>
<span data-ttu-id="4e59d-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4e59d-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4e59d-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4e59d-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e59d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e59d-134">CommonParameters</span></span>
<span data-ttu-id="4e59d-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e59d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e59d-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e59d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e59d-137">입력</span><span class="sxs-lookup"><span data-stu-id="4e59d-137">INPUTS</span></span>

### <span data-ttu-id="4e59d-138">않아야</span><span class="sxs-lookup"><span data-stu-id="4e59d-138">None</span></span>
<span data-ttu-id="4e59d-139">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4e59d-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4e59d-140">출력</span><span class="sxs-lookup"><span data-stu-id="4e59d-140">OUTPUTS</span></span>

## <span data-ttu-id="4e59d-141">상속자</span><span class="sxs-lookup"><span data-stu-id="4e59d-141">NOTES</span></span>

## <span data-ttu-id="4e59d-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4e59d-142">RELATED LINKS</span></span>

[<span data-ttu-id="4e59d-143">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="4e59d-143">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="4e59d-144">새로운 AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="4e59d-144">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="4e59d-145">제거-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="4e59d-145">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="4e59d-146">다시 시작-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="4e59d-146">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="4e59d-147">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="4e59d-147">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="4e59d-148">시작-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="4e59d-148">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="4e59d-149">업데이트-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="4e59d-149">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


