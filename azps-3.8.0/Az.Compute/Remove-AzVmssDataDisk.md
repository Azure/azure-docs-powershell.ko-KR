---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
ms.openlocfilehash: 908405de847526682d8526ef2e576e6a07893c3a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043660"
---
# <span data-ttu-id="5924c-101">Remove-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="5924c-101">Remove-AzVmssDataDisk</span></span>

## <span data-ttu-id="5924c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5924c-102">SYNOPSIS</span></span>
<span data-ttu-id="5924c-103">VMSS에서 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5924c-103">Removes a data disk from the VMSS.</span></span>

## <span data-ttu-id="5924c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5924c-104">SYNTAX</span></span>

### <span data-ttu-id="5924c-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5924c-105">NameParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5924c-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="5924c-106">LunParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5924c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5924c-107">DESCRIPTION</span></span>
<span data-ttu-id="5924c-108">**AzVmssDataDisk** CMDLET은 Vmss (가상 컴퓨터 배율 집합) 인스턴스에서 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5924c-108">The **Remove-AzVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="5924c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5924c-109">EXAMPLES</span></span>

### <span data-ttu-id="5924c-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="5924c-110">Example 1</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="5924c-111">이 명령은 VMSS 개체에서 이름이 ' DataDisk1 ' 인 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5924c-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="5924c-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="5924c-112">Example 2</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="5924c-113">이 명령은 VMSS 개체에서 LUN 0의 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5924c-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="5924c-114">변수</span><span class="sxs-lookup"><span data-stu-id="5924c-114">PARAMETERS</span></span>

### <span data-ttu-id="5924c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5924c-115">-DefaultProfile</span></span>
<span data-ttu-id="5924c-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5924c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5924c-117">-Lun</span><span class="sxs-lookup"><span data-stu-id="5924c-117">-Lun</span></span>
<span data-ttu-id="5924c-118">디스크의 논리 단위 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5924c-118">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="5924c-119">-이름</span><span class="sxs-lookup"><span data-stu-id="5924c-119">-Name</span></span>
<span data-ttu-id="5924c-120">디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5924c-120">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="5924c-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5924c-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="5924c-122">VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5924c-122">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="5924c-123">-확인</span><span class="sxs-lookup"><span data-stu-id="5924c-123">-Confirm</span></span>
<span data-ttu-id="5924c-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5924c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5924c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5924c-125">-WhatIf</span></span>
<span data-ttu-id="5924c-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5924c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5924c-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5924c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5924c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5924c-128">CommonParameters</span></span>
<span data-ttu-id="5924c-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5924c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5924c-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5924c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5924c-131">입력</span><span class="sxs-lookup"><span data-stu-id="5924c-131">INPUTS</span></span>

### <span data-ttu-id="5924c-132">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="5924c-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="5924c-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5924c-133">System.String</span></span>

### <span data-ttu-id="5924c-134">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])</span><span class="sxs-lookup"><span data-stu-id="5924c-134">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="5924c-135">출력</span><span class="sxs-lookup"><span data-stu-id="5924c-135">OUTPUTS</span></span>

### <span data-ttu-id="5924c-136">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="5924c-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="5924c-137">상속자</span><span class="sxs-lookup"><span data-stu-id="5924c-137">NOTES</span></span>

## <span data-ttu-id="5924c-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5924c-138">RELATED LINKS</span></span>
