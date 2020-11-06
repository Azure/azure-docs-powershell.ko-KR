---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
ms.openlocfilehash: 1e0c04bd7283bc2a741b5e2a7130e83b35d00133
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534423"
---
# <span data-ttu-id="8f343-101">Remove-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="8f343-101">Remove-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="8f343-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f343-102">SYNOPSIS</span></span>
<span data-ttu-id="8f343-103">VMSS에서 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f343-103">Removes a data disk from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f343-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8f343-104">SYNTAX</span></span>

### <span data-ttu-id="8f343-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f343-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f343-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f343-106">LunParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f343-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8f343-107">DESCRIPTION</span></span>
<span data-ttu-id="8f343-108">**AzureRmVmssDataDisk** CMDLET은 Vmss (가상 컴퓨터 배율 집합) 인스턴스에서 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f343-108">The **Remove-AzureRmVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="8f343-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8f343-109">EXAMPLES</span></span>

### <span data-ttu-id="8f343-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="8f343-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="8f343-111">이 명령은 VMSS 개체에서 이름이 ' DataDisk1 ' 인 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f343-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="8f343-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="8f343-112">Example 2</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="8f343-113">이 명령은 VMSS 개체에서 LUN 0의 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f343-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="8f343-114">변수</span><span class="sxs-lookup"><span data-stu-id="8f343-114">PARAMETERS</span></span>

### <span data-ttu-id="8f343-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f343-115">-DefaultProfile</span></span>
<span data-ttu-id="8f343-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8f343-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f343-117">-Lun</span><span class="sxs-lookup"><span data-stu-id="8f343-117">-Lun</span></span>
<span data-ttu-id="8f343-118">디스크의 논리 단위 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f343-118">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: LunParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f343-119">-이름</span><span class="sxs-lookup"><span data-stu-id="8f343-119">-Name</span></span>
<span data-ttu-id="8f343-120">디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f343-120">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="8f343-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8f343-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="8f343-122">VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f343-122">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="8f343-123">-확인</span><span class="sxs-lookup"><span data-stu-id="8f343-123">-Confirm</span></span>
<span data-ttu-id="8f343-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f343-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f343-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f343-125">-WhatIf</span></span>
<span data-ttu-id="8f343-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8f343-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f343-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8f343-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f343-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f343-128">CommonParameters</span></span>
<span data-ttu-id="8f343-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f343-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f343-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f343-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f343-131">입력</span><span class="sxs-lookup"><span data-stu-id="8f343-131">INPUTS</span></span>

### <span data-ttu-id="8f343-132">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="8f343-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="8f343-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8f343-133">System.String</span></span>

### <span data-ttu-id="8f343-134">시스템 Null 허용 ' 1 [[b77a5c561934e089, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="8f343-134">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="8f343-135">출력</span><span class="sxs-lookup"><span data-stu-id="8f343-135">OUTPUTS</span></span>

### <span data-ttu-id="8f343-136">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="8f343-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="8f343-137">상속자</span><span class="sxs-lookup"><span data-stu-id="8f343-137">NOTES</span></span>

## <span data-ttu-id="8f343-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8f343-138">RELATED LINKS</span></span>
