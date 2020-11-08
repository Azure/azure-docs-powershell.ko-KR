---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssExtension.md
ms.openlocfilehash: ceca2477d66cb6ce19564899e67a3b66d6917cfe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043657"
---
# <span data-ttu-id="ab52b-101">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="ab52b-101">Remove-AzVmssExtension</span></span>

## <span data-ttu-id="ab52b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab52b-102">SYNOPSIS</span></span>
<span data-ttu-id="ab52b-103">VMSS에서 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab52b-103">Removes an extension from the VMSS.</span></span>

## <span data-ttu-id="ab52b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ab52b-104">SYNTAX</span></span>

### <span data-ttu-id="ab52b-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab52b-105">NameParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab52b-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab52b-106">IdParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab52b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ab52b-107">DESCRIPTION</span></span>
<span data-ttu-id="ab52b-108">**AzVmssExtension** CMDLET은 Vmss (가상 컴퓨터 크기 조정 집합)에서 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab52b-108">The **Remove-AzVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="ab52b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ab52b-109">EXAMPLES</span></span>

### <span data-ttu-id="ab52b-110">예제 1: VMSS 확장 제거</span><span class="sxs-lookup"><span data-stu-id="ab52b-110">Example 1: Remove a VMSS extension</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName
PS C:\> Update-AzVmss -ResourceGroupName $RGName -Name $vmssName -VirtualMachineScaleSet $vmss
```

<span data-ttu-id="ab52b-111">이 명령은 VMSS의 확장을 제거 하 고 수정 후 VMSS를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab52b-111">This command removes the extension of a VMSS and update the VMSS after the modification.</span></span>

### <span data-ttu-id="ab52b-112">예제 2: VMSS 내에서 인스턴스 제거</span><span class="sxs-lookup"><span data-stu-id="ab52b-112">Example 2: Remove an instance from within a VMSS</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzVmssExtension -ResourceGroupName "Group002" -VirtualMachineScaleSet $vmss -Id $extensionId
```

<span data-ttu-id="ab52b-113">이 명령은 Group002 이라는 리소스 그룹에 속하는 VMSS에서 지정 된 확장명 id를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab52b-113">This command removes specify extension id from the VMSS that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="ab52b-114">변수</span><span class="sxs-lookup"><span data-stu-id="ab52b-114">PARAMETERS</span></span>

### <span data-ttu-id="ab52b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab52b-115">-DefaultProfile</span></span>
<span data-ttu-id="ab52b-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ab52b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab52b-117">-Id</span><span class="sxs-lookup"><span data-stu-id="ab52b-117">-Id</span></span>
<span data-ttu-id="ab52b-118">이 cmdlet이 VMSS에서 제거 하는 확장의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab52b-118">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab52b-119">-이름</span><span class="sxs-lookup"><span data-stu-id="ab52b-119">-Name</span></span>
<span data-ttu-id="ab52b-120">이 cmdlet이 VMSS에서 제거 하는 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab52b-120">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab52b-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ab52b-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="ab52b-122">확장명을 제거할 VMSS를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab52b-122">Specifies the VMSS from which to remove the extension from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab52b-123">-확인</span><span class="sxs-lookup"><span data-stu-id="ab52b-123">-Confirm</span></span>
<span data-ttu-id="ab52b-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab52b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab52b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab52b-125">-WhatIf</span></span>
<span data-ttu-id="ab52b-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ab52b-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ab52b-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ab52b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab52b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab52b-128">CommonParameters</span></span>
<span data-ttu-id="ab52b-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab52b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab52b-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ab52b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab52b-131">입력</span><span class="sxs-lookup"><span data-stu-id="ab52b-131">INPUTS</span></span>

### <span data-ttu-id="ab52b-132">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="ab52b-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="ab52b-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ab52b-133">System.String</span></span>

## <span data-ttu-id="ab52b-134">출력</span><span class="sxs-lookup"><span data-stu-id="ab52b-134">OUTPUTS</span></span>

### <span data-ttu-id="ab52b-135">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="ab52b-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="ab52b-136">상속자</span><span class="sxs-lookup"><span data-stu-id="ab52b-136">NOTES</span></span>

## <span data-ttu-id="ab52b-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ab52b-137">RELATED LINKS</span></span>

[<span data-ttu-id="ab52b-138">추가-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="ab52b-138">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)