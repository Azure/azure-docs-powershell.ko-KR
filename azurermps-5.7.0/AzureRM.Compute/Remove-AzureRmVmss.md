---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: E6F2EE87-97C4-416A-9AE1-9FBD72062F0F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmss.md
ms.openlocfilehash: 9837098586212cfa777c01fcb76a0db05f39eaf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531092"
---
# <span data-ttu-id="1df85-101">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1df85-101">Remove-AzureRmVmss</span></span>

## <span data-ttu-id="1df85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1df85-102">SYNOPSIS</span></span>
<span data-ttu-id="1df85-103">Vmss 또는 VMSS 내에 있는 가상 컴퓨터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1df85-103">Removes the VMSS or a virtual machine that is within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1df85-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1df85-104">SYNTAX</span></span>

```
Remove-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1df85-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1df85-105">DESCRIPTION</span></span>
<span data-ttu-id="1df85-106">**AzureRmVmss** Cmdlet은 AZURE에서 Vmss (가상 컴퓨터 크기 집합)를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1df85-106">The **Remove-AzureRmVmss** cmdlet removes the Virtual Machine Scale Set (VMSS) from Azure.</span></span>
<span data-ttu-id="1df85-107">이 cmdlet을 사용 하 여 VMSS 내의 특정 가상 컴퓨터를 제거할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1df85-107">This cmdlet can also be used to remove a specific virtual machine inside the VMSS.</span></span>
<span data-ttu-id="1df85-108">*InstanceId* 매개 변수를 사용 하 여 vmss 내의 특정 가상 컴퓨터를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1df85-108">You can use the *InstanceId* parameter to remove a specific virtual machine inside the VMSS.</span></span>

## <span data-ttu-id="1df85-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1df85-109">EXAMPLES</span></span>

### <span data-ttu-id="1df85-110">예제 1: VMSS 제거</span><span class="sxs-lookup"><span data-stu-id="1df85-110">Example 1: Remove a VMSS</span></span>
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMScaleSet001"
```

<span data-ttu-id="1df85-111">이 명령은 Group001 이라는 리소스 그룹에 속한 VMSS 인 VMScaleSet001를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1df85-111">This command removes the VMSS named VMScaleSet001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="1df85-112">예제 2: VMSS 내에서 가상 컴퓨터 제거</span><span class="sxs-lookup"><span data-stu-id="1df85-112">Example 2: Remove a virtual machine from within a VMSS</span></span>
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group002" -VMScaleSetName "VMScaleSet002" -InstanceId "3";
```

<span data-ttu-id="1df85-113">이 명령은 Group002 이라는 리소스 그룹에 속하는 VMSS 인 VMScaleSet002 이라는 인스턴스 ID가 3 인 가상 컴퓨터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1df85-113">This command removes the virtual machine with instance ID 3 from the VMSS named VMScaleSet002 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="1df85-114">변수</span><span class="sxs-lookup"><span data-stu-id="1df85-114">PARAMETERS</span></span>

### <span data-ttu-id="1df85-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1df85-115">-Force</span></span>
<span data-ttu-id="1df85-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1df85-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1df85-117">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="1df85-117">-InstanceId</span></span>
<span data-ttu-id="1df85-118">시작 해야 하는 인스턴스의 ID를 문자열 배열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1df85-118">Specifies, as a string array, the ID of the instances that need to be started.</span></span>
<span data-ttu-id="1df85-119">예를 들면 다음과 같습니다. `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="1df85-119">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="1df85-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1df85-120">-ResourceGroupName</span></span>
<span data-ttu-id="1df85-121">VMSS가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1df85-121">Specifies the name of the resource group that the VMSS belongs to.</span></span>

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

### <span data-ttu-id="1df85-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="1df85-122">-VMScaleSetName</span></span>
<span data-ttu-id="1df85-123">이 cmdlet이 제거 하는 VMSS의 이름을 종류로 합니다.</span><span class="sxs-lookup"><span data-stu-id="1df85-123">Species the name of the VMSS that this cmdlet removes.</span></span>
<span data-ttu-id="1df85-124">*InstanceId* 매개 변수를 지정 하면 cmdlet이이 매개 변수로 명명 된 vmss에서 지정 된 가상 컴퓨터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1df85-124">If you specify the *InstanceId* parameter, the cmdlet will remove the specified virtual machine from the VMSS named by this parameter.</span></span>

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

### <span data-ttu-id="1df85-125">-확인</span><span class="sxs-lookup"><span data-stu-id="1df85-125">-Confirm</span></span>
<span data-ttu-id="1df85-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1df85-126">Prompts you for confirmation before running the cmdlet.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1df85-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1df85-127">-WhatIf</span></span>
<span data-ttu-id="1df85-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1df85-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1df85-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1df85-129">The cmdlet is not run.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1df85-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1df85-130">CommonParameters</span></span>
<span data-ttu-id="1df85-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1df85-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1df85-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1df85-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1df85-133">입력</span><span class="sxs-lookup"><span data-stu-id="1df85-133">INPUTS</span></span>

### <span data-ttu-id="1df85-134">않아야</span><span class="sxs-lookup"><span data-stu-id="1df85-134">None</span></span>
<span data-ttu-id="1df85-135">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1df85-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1df85-136">출력</span><span class="sxs-lookup"><span data-stu-id="1df85-136">OUTPUTS</span></span>

## <span data-ttu-id="1df85-137">상속자</span><span class="sxs-lookup"><span data-stu-id="1df85-137">NOTES</span></span>

## <span data-ttu-id="1df85-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1df85-138">RELATED LINKS</span></span>

[<span data-ttu-id="1df85-139">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1df85-139">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="1df85-140">새로운 AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1df85-140">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="1df85-141">다시 시작-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1df85-141">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="1df85-142">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1df85-142">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="1df85-143">시작-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1df85-143">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="1df85-144">중지-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1df85-144">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="1df85-145">업데이트-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="1df85-145">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


