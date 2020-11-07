---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
ms.openlocfilehash: 548d576ff959dd96a6978675ca5a35c18c97e0a5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876944"
---
# <span data-ttu-id="9fb19-101">Remove-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="9fb19-101">Remove-AzVMNetworkInterface</span></span>

## <span data-ttu-id="9fb19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fb19-102">SYNOPSIS</span></span>
<span data-ttu-id="9fb19-103">가상 머신에서 네트워크 인터페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fb19-103">Removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="9fb19-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9fb19-104">SYNTAX</span></span>

```
Remove-AzVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fb19-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9fb19-105">DESCRIPTION</span></span>
<span data-ttu-id="9fb19-106">**AzVMNetworkInterface** cmdlet은 가상 컴퓨터에서 네트워크 인터페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fb19-106">The **Remove-AzVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="9fb19-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9fb19-107">EXAMPLES</span></span>

### <span data-ttu-id="9fb19-108">raid-1</span><span class="sxs-lookup"><span data-stu-id="9fb19-108">1:</span></span>
```

```

## <span data-ttu-id="9fb19-109">변수</span><span class="sxs-lookup"><span data-stu-id="9fb19-109">PARAMETERS</span></span>

### <span data-ttu-id="9fb19-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fb19-110">-DefaultProfile</span></span>
<span data-ttu-id="9fb19-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9fb19-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fb19-112">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="9fb19-112">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="9fb19-113">이 cmdlet이 제거 하는 네트워크 인터페이스 Id의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fb19-113">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9fb19-114">-VM</span><span class="sxs-lookup"><span data-stu-id="9fb19-114">-VM</span></span>
<span data-ttu-id="9fb19-115">이 cmdlet에서 네트워크 인터페이스를 제거할 가상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fb19-115">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="9fb19-116">가상 컴퓨터 개체를 가져오려면 Get-AzVM cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fb19-116">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="9fb19-117">-확인</span><span class="sxs-lookup"><span data-stu-id="9fb19-117">-Confirm</span></span>
<span data-ttu-id="9fb19-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fb19-118">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="9fb19-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fb19-119">-WhatIf</span></span>
<span data-ttu-id="9fb19-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9fb19-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9fb19-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9fb19-121">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="9fb19-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fb19-122">CommonParameters</span></span>
<span data-ttu-id="9fb19-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fb19-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fb19-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fb19-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fb19-125">입력</span><span class="sxs-lookup"><span data-stu-id="9fb19-125">INPUTS</span></span>

### <span data-ttu-id="9fb19-126">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9fb19-126">PSVirtualMachine</span></span>
<span data-ttu-id="9fb19-127">' VM ' 매개 변수는 파이프라인에서 ' PSVirtualMachine ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fb19-127">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="9fb19-128">출력</span><span class="sxs-lookup"><span data-stu-id="9fb19-128">OUTPUTS</span></span>

### <span data-ttu-id="9fb19-129">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fb19-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="9fb19-130">상속자</span><span class="sxs-lookup"><span data-stu-id="9fb19-130">NOTES</span></span>

## <span data-ttu-id="9fb19-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9fb19-131">RELATED LINKS</span></span>

[<span data-ttu-id="9fb19-132">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="9fb19-132">Get-AzVM</span></span>](./Get-AzVM.md)


