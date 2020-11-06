---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
ms.openlocfilehash: b77d741c0313e202304be3fd51fb3e1cd5b25b94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525643"
---
# <span data-ttu-id="a5fdf-101">Remove-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a5fdf-101">Remove-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="a5fdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5fdf-102">SYNOPSIS</span></span>
<span data-ttu-id="a5fdf-103">가상 머신에서 네트워크 인터페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fdf-103">Removes a network interface from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5fdf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a5fdf-104">SYNTAX</span></span>

```
Remove-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5fdf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a5fdf-105">DESCRIPTION</span></span>
<span data-ttu-id="a5fdf-106">**AzureRmVMNetworkInterface** cmdlet은 가상 컴퓨터에서 네트워크 인터페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fdf-106">The **Remove-AzureRmVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="a5fdf-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a5fdf-107">EXAMPLES</span></span>

## <span data-ttu-id="a5fdf-108">변수</span><span class="sxs-lookup"><span data-stu-id="a5fdf-108">PARAMETERS</span></span>

### <span data-ttu-id="a5fdf-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5fdf-109">-DefaultProfile</span></span>
<span data-ttu-id="a5fdf-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a5fdf-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5fdf-111">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="a5fdf-111">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="a5fdf-112">이 cmdlet이 제거 하는 네트워크 인터페이스 Id의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fdf-112">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Id, NicIds

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5fdf-113">-VM</span><span class="sxs-lookup"><span data-stu-id="a5fdf-113">-VM</span></span>
<span data-ttu-id="a5fdf-114">이 cmdlet에서 네트워크 인터페이스를 제거할 가상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fdf-114">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="a5fdf-115">가상 컴퓨터 개체를 가져오려면 Get-AzureRmVM cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fdf-115">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5fdf-116">-확인</span><span class="sxs-lookup"><span data-stu-id="a5fdf-116">-Confirm</span></span>
<span data-ttu-id="a5fdf-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fdf-117">Prompts you for confirmation before running the cmdlet.</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5fdf-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5fdf-118">-WhatIf</span></span>
<span data-ttu-id="a5fdf-119">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a5fdf-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5fdf-120">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5fdf-120">The cmdlet is not run.</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5fdf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5fdf-121">CommonParameters</span></span>
<span data-ttu-id="a5fdf-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5fdf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5fdf-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5fdf-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5fdf-124">입력</span><span class="sxs-lookup"><span data-stu-id="a5fdf-124">INPUTS</span></span>

## <span data-ttu-id="a5fdf-125">출력</span><span class="sxs-lookup"><span data-stu-id="a5fdf-125">OUTPUTS</span></span>

## <span data-ttu-id="a5fdf-126">상속자</span><span class="sxs-lookup"><span data-stu-id="a5fdf-126">NOTES</span></span>

## <span data-ttu-id="a5fdf-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5fdf-127">RELATED LINKS</span></span>

[<span data-ttu-id="a5fdf-128">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a5fdf-128">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


