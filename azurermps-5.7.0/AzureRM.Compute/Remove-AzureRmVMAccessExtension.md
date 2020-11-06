---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
ms.openlocfilehash: 16095113dcc0604bfb7b739b1227db337a0cf6f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529900"
---
# <span data-ttu-id="b8a18-101">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="b8a18-101">Remove-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="b8a18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8a18-102">SYNOPSIS</span></span>
<span data-ttu-id="b8a18-103">가상 머신에서 VMAccess 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8a18-103">Removes the VMAccess extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8a18-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b8a18-104">SYNTAX</span></span>

```
Remove-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8a18-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b8a18-105">DESCRIPTION</span></span>
<span data-ttu-id="b8a18-106">**AzureRmVMAccessExtension** cmdlet은 가상 컴퓨터에서 vmaccess (Virtual machine Access) 가상 컴퓨터 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8a18-106">The **Remove-AzureRmVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="b8a18-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b8a18-107">EXAMPLES</span></span>

## <span data-ttu-id="b8a18-108">변수</span><span class="sxs-lookup"><span data-stu-id="b8a18-108">PARAMETERS</span></span>

### <span data-ttu-id="b8a18-109">-Force</span><span class="sxs-lookup"><span data-stu-id="b8a18-109">-Force</span></span>
<span data-ttu-id="b8a18-110">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8a18-110">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8a18-111">-이름</span><span class="sxs-lookup"><span data-stu-id="b8a18-111">-Name</span></span>
<span data-ttu-id="b8a18-112">이 cmdlet이 제거 하는 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8a18-112">Specifies the name of the extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8a18-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8a18-113">-ResourceGroupName</span></span>
<span data-ttu-id="b8a18-114">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8a18-114">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8a18-115">-VMName</span><span class="sxs-lookup"><span data-stu-id="b8a18-115">-VMName</span></span>
<span data-ttu-id="b8a18-116">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8a18-116">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="b8a18-117">이 cmdlet은이 매개 변수에서 지정 하는 가상 컴퓨터에 대 한 VMAccess를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8a18-117">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8a18-118">-확인</span><span class="sxs-lookup"><span data-stu-id="b8a18-118">-Confirm</span></span>
<span data-ttu-id="b8a18-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8a18-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8a18-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8a18-120">-WhatIf</span></span>
<span data-ttu-id="b8a18-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b8a18-121">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="b8a18-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b8a18-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8a18-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8a18-123">CommonParameters</span></span>
<span data-ttu-id="b8a18-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8a18-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8a18-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8a18-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8a18-126">입력</span><span class="sxs-lookup"><span data-stu-id="b8a18-126">INPUTS</span></span>

### <span data-ttu-id="b8a18-127">않아야</span><span class="sxs-lookup"><span data-stu-id="b8a18-127">None</span></span>
<span data-ttu-id="b8a18-128">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b8a18-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b8a18-129">출력</span><span class="sxs-lookup"><span data-stu-id="b8a18-129">OUTPUTS</span></span>

## <span data-ttu-id="b8a18-130">상속자</span><span class="sxs-lookup"><span data-stu-id="b8a18-130">NOTES</span></span>

## <span data-ttu-id="b8a18-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8a18-131">RELATED LINKS</span></span>

[<span data-ttu-id="b8a18-132">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="b8a18-132">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="b8a18-133">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="b8a18-133">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="b8a18-134">제거-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="b8a18-134">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)
