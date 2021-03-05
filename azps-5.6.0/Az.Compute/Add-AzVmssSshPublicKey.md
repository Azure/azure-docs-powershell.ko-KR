---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9C216103-EB77-468E-8684-F5E5400B73A7
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmsssshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSshPublicKey.md
ms.openlocfilehash: 17235c8790928b81b6d796d1d5d7b661c560be7c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991536"
---
# <span data-ttu-id="42321-101">Add-AzVmssSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="42321-101">Add-AzVmssSshPublicKey</span></span>

## <span data-ttu-id="42321-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42321-102">SYNOPSIS</span></span>
<span data-ttu-id="42321-103">VMSS에 SSH 공용 키를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="42321-103">Adds SSH public keys to the VMSS.</span></span>

## <span data-ttu-id="42321-104">구문</span><span class="sxs-lookup"><span data-stu-id="42321-104">SYNTAX</span></span>

```
Add-AzVmssSshPublicKey [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Path] <String>]
 [[-KeyData] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42321-105">설명</span><span class="sxs-lookup"><span data-stu-id="42321-105">DESCRIPTION</span></span>
<span data-ttu-id="42321-106">**Add-AzVmssSshPublicKey** cmdlet은 보안 셸(SSH)을 통해 VMSS(Virtual Machine Scale Set) 가상 머신에 연결하는 데 사용할 수 있는 공개 키를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="42321-106">The **Add-AzVmssSshPublicKey** cmdlet adds the public keys that you can use to connect to the Virtual Machine Scale Set (VMSS) virtual machines over Secure Shell (SSH).</span></span>

## <span data-ttu-id="42321-107">예제</span><span class="sxs-lookup"><span data-stu-id="42321-107">EXAMPLES</span></span>

### <span data-ttu-id="42321-108">예제 1: VMSS에 SSH 공개 키 추가</span><span class="sxs-lookup"><span data-stu-id="42321-108">Example 1: Add an SSH public key to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssSshPublicKey -VirtualMachineScaleSet $VMSS -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="42321-109">이 예제에서는 VMSS에 SSH 공개 키를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="42321-109">This example adds an SSH public key to the VMSS.</span></span>
<span data-ttu-id="42321-110">첫 번째 명령은 **New-AzVmssConfig** cmdlet을 사용하여 VMSS 구성 개체를 만들고 결과를 새 이름의 변수에 $VMSS.</span><span class="sxs-lookup"><span data-stu-id="42321-110">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="42321-111">두 번째 명령은 지정된 키 데이터가 있는 SSH 키를 추가하고 가상 머신의 지정된 경로에 키를 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="42321-111">The second command adds an SSH key with the specified key data and stores the key at the specified path on the virtual machine.</span></span>

## <span data-ttu-id="42321-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="42321-112">PARAMETERS</span></span>

### <span data-ttu-id="42321-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42321-113">-DefaultProfile</span></span>
<span data-ttu-id="42321-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="42321-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42321-115">-KeyData</span><span class="sxs-lookup"><span data-stu-id="42321-115">-KeyData</span></span>
<span data-ttu-id="42321-116">SSH RSA 공개 키 데이터를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="42321-116">Specifies a SSH RSA public key data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42321-117">-Path</span><span class="sxs-lookup"><span data-stu-id="42321-117">-Path</span></span>
<span data-ttu-id="42321-118">이 cmdlet은 SSH 공개 키를 저장하는 가상 머신에 파일의 전체 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="42321-118">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="42321-119">파일이 이미 있는 경우 이 cmdlet은 파일에 키를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="42321-119">If the file already exists, this cmdlet appends the key to the file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42321-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="42321-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="42321-121">VMSS 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="42321-121">Specifies the VMSS object.</span></span>
<span data-ttu-id="42321-122">[New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet을 사용하여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42321-122">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="42321-123">-확인</span><span class="sxs-lookup"><span data-stu-id="42321-123">-Confirm</span></span>
<span data-ttu-id="42321-124">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="42321-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42321-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42321-125">-WhatIf</span></span>
<span data-ttu-id="42321-126">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="42321-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="42321-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="42321-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42321-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42321-128">CommonParameters</span></span>
<span data-ttu-id="42321-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="42321-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42321-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="42321-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42321-131">입력</span><span class="sxs-lookup"><span data-stu-id="42321-131">INPUTS</span></span>

### <span data-ttu-id="42321-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="42321-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="42321-133">System.String</span><span class="sxs-lookup"><span data-stu-id="42321-133">System.String</span></span>

## <span data-ttu-id="42321-134">출력</span><span class="sxs-lookup"><span data-stu-id="42321-134">OUTPUTS</span></span>

### <span data-ttu-id="42321-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="42321-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="42321-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="42321-136">NOTES</span></span>

## <span data-ttu-id="42321-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="42321-137">RELATED LINKS</span></span>

[<span data-ttu-id="42321-138">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="42321-138">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
