---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmnetworkinterface
schema: 2.0.0
ms.openlocfilehash: 0c7900d50074e185d26f4fafccd9b63756749fd8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881970"
---
# <span data-ttu-id="33d02-101">Remove-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="33d02-101">Remove-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="33d02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33d02-102">SYNOPSIS</span></span>
<span data-ttu-id="33d02-103">가상 머신에서 네트워크 인터페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="33d02-103">Removes a network interface from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33d02-104">구문과</span><span class="sxs-lookup"><span data-stu-id="33d02-104">SYNTAX</span></span>

```
Remove-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33d02-105">설명은</span><span class="sxs-lookup"><span data-stu-id="33d02-105">DESCRIPTION</span></span>
<span data-ttu-id="33d02-106">**AzureRmVMNetworkInterface** cmdlet은 가상 컴퓨터에서 네트워크 인터페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="33d02-106">The **Remove-AzureRmVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="33d02-107">예제의</span><span class="sxs-lookup"><span data-stu-id="33d02-107">EXAMPLES</span></span>

### <span data-ttu-id="33d02-108">raid-1</span><span class="sxs-lookup"><span data-stu-id="33d02-108">1:</span></span>
```

```

## <span data-ttu-id="33d02-109">변수</span><span class="sxs-lookup"><span data-stu-id="33d02-109">PARAMETERS</span></span>

### <span data-ttu-id="33d02-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33d02-110">-DefaultProfile</span></span>
<span data-ttu-id="33d02-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="33d02-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33d02-112">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="33d02-112">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="33d02-113">이 cmdlet이 제거 하는 네트워크 인터페이스 Id의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33d02-113">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Id, NicIds

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33d02-114">-VM</span><span class="sxs-lookup"><span data-stu-id="33d02-114">-VM</span></span>
<span data-ttu-id="33d02-115">이 cmdlet에서 네트워크 인터페이스를 제거할 가상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33d02-115">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="33d02-116">가상 컴퓨터 개체를 가져오려면 Get-AzureRmVM cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="33d02-116">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33d02-117">-확인</span><span class="sxs-lookup"><span data-stu-id="33d02-117">-Confirm</span></span>
<span data-ttu-id="33d02-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="33d02-118">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="33d02-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33d02-119">-WhatIf</span></span>
<span data-ttu-id="33d02-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="33d02-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="33d02-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="33d02-121">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="33d02-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33d02-122">CommonParameters</span></span>
<span data-ttu-id="33d02-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="33d02-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33d02-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33d02-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33d02-125">입력</span><span class="sxs-lookup"><span data-stu-id="33d02-125">INPUTS</span></span>

### <span data-ttu-id="33d02-126">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="33d02-126">PSVirtualMachine</span></span>
<span data-ttu-id="33d02-127">' VM ' 매개 변수는 파이프라인에서 ' PSVirtualMachine ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="33d02-127">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="33d02-128">출력</span><span class="sxs-lookup"><span data-stu-id="33d02-128">OUTPUTS</span></span>

### <span data-ttu-id="33d02-129">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="33d02-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="33d02-130">상속자</span><span class="sxs-lookup"><span data-stu-id="33d02-130">NOTES</span></span>

## <span data-ttu-id="33d02-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="33d02-131">RELATED LINKS</span></span>

[<span data-ttu-id="33d02-132">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="33d02-132">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


