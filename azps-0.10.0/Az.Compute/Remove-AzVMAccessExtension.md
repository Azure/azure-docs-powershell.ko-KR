---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
ms.openlocfilehash: 888ba66f1949a687228f5b9f2563c3d810c7cd5f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876963"
---
# <span data-ttu-id="766dc-101">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="766dc-101">Remove-AzVMAccessExtension</span></span>

## <span data-ttu-id="766dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="766dc-102">SYNOPSIS</span></span>
<span data-ttu-id="766dc-103">가상 머신에서 VMAccess 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="766dc-103">Removes the VMAccess extension from a virtual machine.</span></span>

## <span data-ttu-id="766dc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="766dc-104">SYNTAX</span></span>

```
Remove-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="766dc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="766dc-105">DESCRIPTION</span></span>
<span data-ttu-id="766dc-106">**AzVMAccessExtension** cmdlet은 가상 컴퓨터에서 vmaccess (Virtual machine Access) 가상 컴퓨터 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="766dc-106">The **Remove-AzVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="766dc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="766dc-107">EXAMPLES</span></span>

## <span data-ttu-id="766dc-108">변수</span><span class="sxs-lookup"><span data-stu-id="766dc-108">PARAMETERS</span></span>

### <span data-ttu-id="766dc-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="766dc-109">-DefaultProfile</span></span>
<span data-ttu-id="766dc-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="766dc-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="766dc-111">-Force</span><span class="sxs-lookup"><span data-stu-id="766dc-111">-Force</span></span>
<span data-ttu-id="766dc-112">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="766dc-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="766dc-113">-이름</span><span class="sxs-lookup"><span data-stu-id="766dc-113">-Name</span></span>
<span data-ttu-id="766dc-114">이 cmdlet이 제거 하는 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="766dc-114">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="766dc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="766dc-115">-ResourceGroupName</span></span>
<span data-ttu-id="766dc-116">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="766dc-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="766dc-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="766dc-117">-VMName</span></span>
<span data-ttu-id="766dc-118">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="766dc-118">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="766dc-119">이 cmdlet은이 매개 변수에서 지정 하는 가상 컴퓨터에 대 한 VMAccess를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="766dc-119">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="766dc-120">-확인</span><span class="sxs-lookup"><span data-stu-id="766dc-120">-Confirm</span></span>
<span data-ttu-id="766dc-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="766dc-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="766dc-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="766dc-122">-WhatIf</span></span>
<span data-ttu-id="766dc-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="766dc-123">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="766dc-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="766dc-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="766dc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="766dc-125">CommonParameters</span></span>
<span data-ttu-id="766dc-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="766dc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="766dc-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="766dc-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="766dc-128">입력</span><span class="sxs-lookup"><span data-stu-id="766dc-128">INPUTS</span></span>

### <span data-ttu-id="766dc-129">않아야</span><span class="sxs-lookup"><span data-stu-id="766dc-129">None</span></span>
<span data-ttu-id="766dc-130">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="766dc-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="766dc-131">출력</span><span class="sxs-lookup"><span data-stu-id="766dc-131">OUTPUTS</span></span>

### <span data-ttu-id="766dc-132">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="766dc-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="766dc-133">상속자</span><span class="sxs-lookup"><span data-stu-id="766dc-133">NOTES</span></span>

## <span data-ttu-id="766dc-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="766dc-134">RELATED LINKS</span></span>

[<span data-ttu-id="766dc-135">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="766dc-135">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="766dc-136">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="766dc-136">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="766dc-137">제거-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="766dc-137">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)
