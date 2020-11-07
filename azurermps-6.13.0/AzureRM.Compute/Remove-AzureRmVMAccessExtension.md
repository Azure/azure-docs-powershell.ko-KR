---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
ms.openlocfilehash: 0360bcdb766de681ab6f54682007076e18266051
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702119"
---
# <span data-ttu-id="6429d-101">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="6429d-101">Remove-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="6429d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6429d-102">SYNOPSIS</span></span>
<span data-ttu-id="6429d-103">가상 머신에서 VMAccess 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6429d-103">Removes the VMAccess extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6429d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6429d-104">SYNTAX</span></span>

```
Remove-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6429d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6429d-105">DESCRIPTION</span></span>
<span data-ttu-id="6429d-106">**AzureRmVMAccessExtension** cmdlet은 가상 컴퓨터에서 vmaccess (Virtual machine Access) 가상 컴퓨터 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6429d-106">The **Remove-AzureRmVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="6429d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6429d-107">EXAMPLES</span></span>

## <span data-ttu-id="6429d-108">변수</span><span class="sxs-lookup"><span data-stu-id="6429d-108">PARAMETERS</span></span>

### <span data-ttu-id="6429d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6429d-109">-DefaultProfile</span></span>
<span data-ttu-id="6429d-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6429d-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6429d-111">-Force</span><span class="sxs-lookup"><span data-stu-id="6429d-111">-Force</span></span>
<span data-ttu-id="6429d-112">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6429d-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6429d-113">-이름</span><span class="sxs-lookup"><span data-stu-id="6429d-113">-Name</span></span>
<span data-ttu-id="6429d-114">이 cmdlet이 제거 하는 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6429d-114">Specifies the name of the extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6429d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6429d-115">-ResourceGroupName</span></span>
<span data-ttu-id="6429d-116">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6429d-116">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6429d-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="6429d-117">-VMName</span></span>
<span data-ttu-id="6429d-118">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6429d-118">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="6429d-119">이 cmdlet은이 매개 변수에서 지정 하는 가상 컴퓨터에 대 한 VMAccess를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6429d-119">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6429d-120">-확인</span><span class="sxs-lookup"><span data-stu-id="6429d-120">-Confirm</span></span>
<span data-ttu-id="6429d-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6429d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6429d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6429d-122">-WhatIf</span></span>
<span data-ttu-id="6429d-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6429d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6429d-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6429d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6429d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6429d-125">CommonParameters</span></span>
<span data-ttu-id="6429d-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6429d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6429d-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6429d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6429d-128">입력</span><span class="sxs-lookup"><span data-stu-id="6429d-128">INPUTS</span></span>

### <span data-ttu-id="6429d-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6429d-129">System.String</span></span>

## <span data-ttu-id="6429d-130">출력</span><span class="sxs-lookup"><span data-stu-id="6429d-130">OUTPUTS</span></span>

### <span data-ttu-id="6429d-131">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="6429d-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="6429d-132">상속자</span><span class="sxs-lookup"><span data-stu-id="6429d-132">NOTES</span></span>

## <span data-ttu-id="6429d-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6429d-133">RELATED LINKS</span></span>

[<span data-ttu-id="6429d-134">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="6429d-134">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="6429d-135">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="6429d-135">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="6429d-136">제거-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="6429d-136">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)
