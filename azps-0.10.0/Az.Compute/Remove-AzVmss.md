---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: E6F2EE87-97C4-416A-9AE1-9FBD72062F0F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmss.md
ms.openlocfilehash: c8de667ae818749e980d3e917838717ec3c85b07
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876941"
---
# <span data-ttu-id="524d5-101">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="524d5-101">Remove-AzVmss</span></span>

## <span data-ttu-id="524d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="524d5-102">SYNOPSIS</span></span>
<span data-ttu-id="524d5-103">Vmss 또는 VMSS 내에 있는 가상 컴퓨터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="524d5-103">Removes the VMSS or a virtual machine that is within the VMSS.</span></span>

## <span data-ttu-id="524d5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="524d5-104">SYNTAX</span></span>

```
Remove-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="524d5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="524d5-105">DESCRIPTION</span></span>
<span data-ttu-id="524d5-106">**AzVmss** Cmdlet은 AZURE에서 Vmss (가상 컴퓨터 크기 집합)를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="524d5-106">The **Remove-AzVmss** cmdlet removes the Virtual Machine Scale Set (VMSS) from Azure.</span></span>
<span data-ttu-id="524d5-107">이 cmdlet을 사용 하 여 VMSS 내의 특정 가상 컴퓨터를 제거할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="524d5-107">This cmdlet can also be used to remove a specific virtual machine inside the VMSS.</span></span>
<span data-ttu-id="524d5-108">*InstanceId* 매개 변수를 사용 하 여 vmss 내의 특정 가상 컴퓨터를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="524d5-108">You can use the *InstanceId* parameter to remove a specific virtual machine inside the VMSS.</span></span>

## <span data-ttu-id="524d5-109">예제의</span><span class="sxs-lookup"><span data-stu-id="524d5-109">EXAMPLES</span></span>

### <span data-ttu-id="524d5-110">예제 1: VMSS 제거</span><span class="sxs-lookup"><span data-stu-id="524d5-110">Example 1: Remove a VMSS</span></span>
```
PS C:\> Remove-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMScaleSet001"
```

<span data-ttu-id="524d5-111">이 명령은 Group001 이라는 리소스 그룹에 속한 VMSS 인 VMScaleSet001를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="524d5-111">This command removes the VMSS named VMScaleSet001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="524d5-112">예제 2: VMSS 내에서 가상 컴퓨터 제거</span><span class="sxs-lookup"><span data-stu-id="524d5-112">Example 2: Remove a virtual machine from within a VMSS</span></span>
```
PS C:\> Remove-AzVmss -ResourceGroupName "Group002" -VMScaleSetName "VMScaleSet002" -InstanceId "3";
```

<span data-ttu-id="524d5-113">이 명령은 Group002 이라는 리소스 그룹에 속하는 VMSS 인 VMScaleSet002 이라는 인스턴스 ID가 3 인 가상 컴퓨터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="524d5-113">This command removes the virtual machine with instance ID 3 from the VMSS named VMScaleSet002 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="524d5-114">변수</span><span class="sxs-lookup"><span data-stu-id="524d5-114">PARAMETERS</span></span>

### <span data-ttu-id="524d5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="524d5-115">-AsJob</span></span>
<span data-ttu-id="524d5-116">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="524d5-116">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="524d5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="524d5-117">-DefaultProfile</span></span>
<span data-ttu-id="524d5-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="524d5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="524d5-119">-Force</span><span class="sxs-lookup"><span data-stu-id="524d5-119">-Force</span></span>
<span data-ttu-id="524d5-120">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="524d5-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="524d5-121">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="524d5-121">-InstanceId</span></span>
<span data-ttu-id="524d5-122">시작 해야 하는 인스턴스의 ID를 문자열 배열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="524d5-122">Specifies, as a string array, the ID of the instances that need to be started.</span></span>
<span data-ttu-id="524d5-123">예를 들면 다음과 같습니다. `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="524d5-123">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="524d5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="524d5-124">-ResourceGroupName</span></span>
<span data-ttu-id="524d5-125">VMSS가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="524d5-125">Specifies the name of the resource group that the VMSS belongs to.</span></span>

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

### <span data-ttu-id="524d5-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="524d5-126">-VMScaleSetName</span></span>
<span data-ttu-id="524d5-127">이 cmdlet이 제거 하는 VMSS의 이름을 종류로 합니다.</span><span class="sxs-lookup"><span data-stu-id="524d5-127">Species the name of the VMSS that this cmdlet removes.</span></span>
<span data-ttu-id="524d5-128">*InstanceId* 매개 변수를 지정 하면 cmdlet이이 매개 변수로 명명 된 vmss에서 지정 된 가상 컴퓨터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="524d5-128">If you specify the *InstanceId* parameter, the cmdlet will remove the specified virtual machine from the VMSS named by this parameter.</span></span>

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

### <span data-ttu-id="524d5-129">-확인</span><span class="sxs-lookup"><span data-stu-id="524d5-129">-Confirm</span></span>
<span data-ttu-id="524d5-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="524d5-130">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="524d5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="524d5-131">-WhatIf</span></span>
<span data-ttu-id="524d5-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="524d5-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="524d5-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="524d5-133">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="524d5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="524d5-134">CommonParameters</span></span>
<span data-ttu-id="524d5-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="524d5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="524d5-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="524d5-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="524d5-137">입력</span><span class="sxs-lookup"><span data-stu-id="524d5-137">INPUTS</span></span>

### <span data-ttu-id="524d5-138">않아야</span><span class="sxs-lookup"><span data-stu-id="524d5-138">None</span></span>
<span data-ttu-id="524d5-139">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="524d5-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="524d5-140">출력</span><span class="sxs-lookup"><span data-stu-id="524d5-140">OUTPUTS</span></span>

### <span data-ttu-id="524d5-141">PSOperationStatusResponse의. m a.</span><span class="sxs-lookup"><span data-stu-id="524d5-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="524d5-142">상속자</span><span class="sxs-lookup"><span data-stu-id="524d5-142">NOTES</span></span>

## <span data-ttu-id="524d5-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="524d5-143">RELATED LINKS</span></span>

[<span data-ttu-id="524d5-144">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="524d5-144">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="524d5-145">새로운 AzVmss</span><span class="sxs-lookup"><span data-stu-id="524d5-145">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="524d5-146">다시 시작-AzVmss</span><span class="sxs-lookup"><span data-stu-id="524d5-146">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="524d5-147">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="524d5-147">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="524d5-148">시작-AzVmss</span><span class="sxs-lookup"><span data-stu-id="524d5-148">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="524d5-149">중지-AzVmss</span><span class="sxs-lookup"><span data-stu-id="524d5-149">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="524d5-150">업데이트-AzVmss</span><span class="sxs-lookup"><span data-stu-id="524d5-150">Update-AzVmss</span></span>](./Update-AzVmss.md)


