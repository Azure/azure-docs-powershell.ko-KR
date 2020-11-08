---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9C216103-EB77-468E-8684-F5E5400B73A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsssshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSshPublicKey.md
ms.openlocfilehash: 0ba5f9cd618c86eec15eb8b0a02956e5997fc627
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215631"
---
# <span data-ttu-id="a1652-101">Add-AzVmssSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="a1652-101">Add-AzVmssSshPublicKey</span></span>

## <span data-ttu-id="a1652-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1652-102">SYNOPSIS</span></span>
<span data-ttu-id="a1652-103">VMSS에 SSH 공개 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1652-103">Adds SSH public keys to the VMSS.</span></span>

## <span data-ttu-id="a1652-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a1652-104">SYNTAX</span></span>

```
Add-AzVmssSshPublicKey [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Path] <String>]
 [[-KeyData] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1652-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a1652-105">DESCRIPTION</span></span>
<span data-ttu-id="a1652-106">**AzVmssSshPublicKey** Cmdlet은 보안 셸 (SSH)을 통한 Vmss (가상 컴퓨터 크기 집합) 가상 컴퓨터에 연결 하는 데 사용할 수 있는 공개 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1652-106">The **Add-AzVmssSshPublicKey** cmdlet adds the public keys that you can use to connect to the Virtual Machine Scale Set (VMSS) virtual machines over Secure Shell (SSH).</span></span>

## <span data-ttu-id="a1652-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a1652-107">EXAMPLES</span></span>

### <span data-ttu-id="a1652-108">예제 1: VMSS에 SSH 공개 키 추가</span><span class="sxs-lookup"><span data-stu-id="a1652-108">Example 1: Add an SSH public key to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssSshPublicKey -VirtualMachineScaleSet $VMSS -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="a1652-109">이 예제에서는 VMSS에 SSH 공개 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1652-109">This example adds an SSH public key to the VMSS.</span></span>
<span data-ttu-id="a1652-110">첫 번째 명령은 **AzVmssConfig** cmdlet을 사용 하 여 vmss 구성 개체를 만들고 결과를 $VMSS 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1652-110">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="a1652-111">두 번째 명령은 지정 된 키 데이터를 사용 하 여 SSH 키를 추가 하 고 가상 컴퓨터의 지정 된 경로에 키를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1652-111">The second command adds an SSH key with the specified key data and stores the key at the specified path on the virtual machine.</span></span>

## <span data-ttu-id="a1652-112">변수</span><span class="sxs-lookup"><span data-stu-id="a1652-112">PARAMETERS</span></span>

### <span data-ttu-id="a1652-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1652-113">-DefaultProfile</span></span>
<span data-ttu-id="a1652-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a1652-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1652-115">-KeyData</span><span class="sxs-lookup"><span data-stu-id="a1652-115">-KeyData</span></span>
<span data-ttu-id="a1652-116">SSH RSA 공개 키 데이터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1652-116">Specifies a SSH RSA public key data.</span></span>

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

### <span data-ttu-id="a1652-117">-Path</span><span class="sxs-lookup"><span data-stu-id="a1652-117">-Path</span></span>
<span data-ttu-id="a1652-118">가상 머신에서이 cmdlet이 SSH 공개 키를 저장 하는 파일의 전체 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1652-118">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="a1652-119">파일이 이미 있는 경우이 cmdlet은 파일에 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1652-119">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="a1652-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a1652-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="a1652-121">VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1652-121">Specifies the VMSS object.</span></span>
<span data-ttu-id="a1652-122">[새 AzVmssConfig](./New-AzVmssConfig.md) cmdlet을 사용 하 여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a1652-122">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="a1652-123">-확인</span><span class="sxs-lookup"><span data-stu-id="a1652-123">-Confirm</span></span>
<span data-ttu-id="a1652-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1652-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1652-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1652-125">-WhatIf</span></span>
<span data-ttu-id="a1652-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a1652-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1652-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a1652-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1652-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1652-128">CommonParameters</span></span>
<span data-ttu-id="a1652-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1652-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1652-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a1652-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1652-131">입력</span><span class="sxs-lookup"><span data-stu-id="a1652-131">INPUTS</span></span>

### <span data-ttu-id="a1652-132">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="a1652-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="a1652-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a1652-133">System.String</span></span>

## <span data-ttu-id="a1652-134">출력</span><span class="sxs-lookup"><span data-stu-id="a1652-134">OUTPUTS</span></span>

### <span data-ttu-id="a1652-135">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="a1652-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="a1652-136">상속자</span><span class="sxs-lookup"><span data-stu-id="a1652-136">NOTES</span></span>

## <span data-ttu-id="a1652-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a1652-137">RELATED LINKS</span></span>

[<span data-ttu-id="a1652-138">새로운 AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="a1652-138">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
