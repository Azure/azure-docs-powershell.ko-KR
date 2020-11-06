---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
ms.openlocfilehash: 89ab4ea57f5f03fbc26d33e1a9087371f215d4ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525303"
---
# <span data-ttu-id="4aa7d-101">Remove-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4aa7d-101">Remove-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="4aa7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4aa7d-102">SYNOPSIS</span></span>
<span data-ttu-id="4aa7d-103">가상 머신에서 네트워크 인터페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aa7d-103">Removes a network interface from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4aa7d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4aa7d-104">SYNTAX</span></span>

```
Remove-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4aa7d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4aa7d-105">DESCRIPTION</span></span>
<span data-ttu-id="4aa7d-106">**AzureRmVMNetworkInterface** cmdlet은 가상 컴퓨터에서 네트워크 인터페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aa7d-106">The **Remove-AzureRmVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="4aa7d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4aa7d-107">EXAMPLES</span></span>

## <span data-ttu-id="4aa7d-108">변수</span><span class="sxs-lookup"><span data-stu-id="4aa7d-108">PARAMETERS</span></span>

### <span data-ttu-id="4aa7d-109">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="4aa7d-109">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="4aa7d-110">이 cmdlet이 제거 하는 네트워크 인터페이스 Id의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aa7d-110">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4aa7d-111">-VM</span><span class="sxs-lookup"><span data-stu-id="4aa7d-111">-VM</span></span>
<span data-ttu-id="4aa7d-112">이 cmdlet에서 네트워크 인터페이스를 제거할 가상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aa7d-112">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="4aa7d-113">가상 컴퓨터 개체를 가져오려면 Get-AzureRmVM cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aa7d-113">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="4aa7d-114">-확인</span><span class="sxs-lookup"><span data-stu-id="4aa7d-114">-Confirm</span></span>
<span data-ttu-id="4aa7d-115">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aa7d-115">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="4aa7d-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4aa7d-116">-WhatIf</span></span>
<span data-ttu-id="4aa7d-117">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4aa7d-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4aa7d-118">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4aa7d-118">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="4aa7d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aa7d-119">CommonParameters</span></span>
<span data-ttu-id="4aa7d-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aa7d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aa7d-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4aa7d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aa7d-122">입력</span><span class="sxs-lookup"><span data-stu-id="4aa7d-122">INPUTS</span></span>

### <span data-ttu-id="4aa7d-123">않아야</span><span class="sxs-lookup"><span data-stu-id="4aa7d-123">None</span></span>
<span data-ttu-id="4aa7d-124">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4aa7d-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4aa7d-125">출력</span><span class="sxs-lookup"><span data-stu-id="4aa7d-125">OUTPUTS</span></span>

## <span data-ttu-id="4aa7d-126">상속자</span><span class="sxs-lookup"><span data-stu-id="4aa7d-126">NOTES</span></span>

## <span data-ttu-id="4aa7d-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4aa7d-127">RELATED LINKS</span></span>

[<span data-ttu-id="4aa7d-128">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4aa7d-128">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


