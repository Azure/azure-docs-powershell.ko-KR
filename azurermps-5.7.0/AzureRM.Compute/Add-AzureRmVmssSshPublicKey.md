---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 9C216103-EB77-468E-8684-F5E5400B73A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssSshPublicKey.md
ms.openlocfilehash: 6ca619ba75fcf639e36650dc66d45d2f86ec8375
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711205"
---
# <span data-ttu-id="c8af0-101">Add-AzureRmVmssSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="c8af0-101">Add-AzureRmVmssSshPublicKey</span></span>

## <span data-ttu-id="c8af0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8af0-102">SYNOPSIS</span></span>
<span data-ttu-id="c8af0-103">VMSS에 SSH 공개 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8af0-103">Adds SSH public keys to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8af0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c8af0-104">SYNTAX</span></span>

```
Add-AzureRmVmssSshPublicKey [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Path] <String>]
 [[-KeyData] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8af0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c8af0-105">DESCRIPTION</span></span>
<span data-ttu-id="c8af0-106">**AzureRmVmssSshPublicKey** Cmdlet은 보안 셸 (SSH)을 통한 Vmss (가상 컴퓨터 크기 집합) 가상 컴퓨터에 연결 하는 데 사용할 수 있는 공개 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8af0-106">The **Add-AzureRmVmssSshPublicKey** cmdlet adds the public keys that you can use to connect to the Virtual Machine Scale Set (VMSS) virtual machines over Secure Shell (SSH).</span></span>

## <span data-ttu-id="c8af0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c8af0-107">EXAMPLES</span></span>

### <span data-ttu-id="c8af0-108">예제 1: VMSS에 SSH 공개 키 추가</span><span class="sxs-lookup"><span data-stu-id="c8af0-108">Example 1: Add an SSH public key to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssSshPublicKey -VirtualMachineScaleSet $VMSS -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="c8af0-109">이 예제에서는 VMSS에 SSH 공개 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8af0-109">This example adds an SSH public key to the VMSS.</span></span>

<span data-ttu-id="c8af0-110">첫 번째 명령은 **AzureRmVmssConfig** cmdlet을 사용 하 여 vmss 구성 개체를 만들고 결과를 $VMSS 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8af0-110">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="c8af0-111">두 번째 명령은 지정 된 키 데이터를 사용 하 여 SSH 키를 추가 하 고 가상 컴퓨터의 지정 된 경로에 키를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8af0-111">The second command adds an SSH key with the specified key data and stores the key at the specified path on the virtual machine.</span></span>

## <span data-ttu-id="c8af0-112">변수</span><span class="sxs-lookup"><span data-stu-id="c8af0-112">PARAMETERS</span></span>

### <span data-ttu-id="c8af0-113">-KeyData</span><span class="sxs-lookup"><span data-stu-id="c8af0-113">-KeyData</span></span>
<span data-ttu-id="c8af0-114">SSH RSA 공개 키 데이터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8af0-114">Specifies a SSH RSA public key data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8af0-115">-Path</span><span class="sxs-lookup"><span data-stu-id="c8af0-115">-Path</span></span>
<span data-ttu-id="c8af0-116">가상 머신에서이 cmdlet이 SSH 공개 키를 저장 하는 파일의 전체 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8af0-116">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="c8af0-117">파일이 이미 있는 경우이 cmdlet은 파일에 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8af0-117">If the file already exists, this cmdlet appends the key to the file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8af0-118">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c8af0-118">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="c8af0-119">VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8af0-119">Specifies the VMSS object.</span></span>
<span data-ttu-id="c8af0-120">[새 AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet을 사용 하 여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c8af0-120">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8af0-121">-확인</span><span class="sxs-lookup"><span data-stu-id="c8af0-121">-Confirm</span></span>
<span data-ttu-id="c8af0-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8af0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8af0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8af0-123">-WhatIf</span></span>
<span data-ttu-id="c8af0-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c8af0-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c8af0-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c8af0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8af0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8af0-126">CommonParameters</span></span>
<span data-ttu-id="c8af0-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8af0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8af0-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8af0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8af0-129">입력</span><span class="sxs-lookup"><span data-stu-id="c8af0-129">INPUTS</span></span>

### <span data-ttu-id="c8af0-130">않아야</span><span class="sxs-lookup"><span data-stu-id="c8af0-130">None</span></span>
<span data-ttu-id="c8af0-131">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c8af0-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c8af0-132">출력</span><span class="sxs-lookup"><span data-stu-id="c8af0-132">OUTPUTS</span></span>

###  
<span data-ttu-id="c8af0-133">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c8af0-133">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="c8af0-134">상속자</span><span class="sxs-lookup"><span data-stu-id="c8af0-134">NOTES</span></span>

## <span data-ttu-id="c8af0-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c8af0-135">RELATED LINKS</span></span>

[<span data-ttu-id="c8af0-136">새로운 AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="c8af0-136">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
