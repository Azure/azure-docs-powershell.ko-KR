---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssExtension.md
ms.openlocfilehash: 8044be4e6d9c353dd50420fe73066a8f47d53855
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876926"
---
# <span data-ttu-id="0c873-101">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="0c873-101">Remove-AzVmssExtension</span></span>

## <span data-ttu-id="0c873-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c873-102">SYNOPSIS</span></span>
<span data-ttu-id="0c873-103">VMSS에서 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c873-103">Removes an extension from the VMSS.</span></span>

## <span data-ttu-id="0c873-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0c873-104">SYNTAX</span></span>

### <span data-ttu-id="0c873-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c873-105">NameParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c873-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c873-106">IdParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c873-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0c873-107">DESCRIPTION</span></span>
<span data-ttu-id="0c873-108">**AzVmssExtension** CMDLET은 Vmss (가상 컴퓨터 크기 조정 집합)에서 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c873-108">The **Remove-AzVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="0c873-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0c873-109">EXAMPLES</span></span>

### <span data-ttu-id="0c873-110">예제 1: VMSS에서 확장 제거</span><span class="sxs-lookup"><span data-stu-id="0c873-110">Example 1: Remove extension from the VMSS</span></span>
```
PS C:\> Remove-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

## <span data-ttu-id="0c873-111">변수</span><span class="sxs-lookup"><span data-stu-id="0c873-111">PARAMETERS</span></span>

### <span data-ttu-id="0c873-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c873-112">-DefaultProfile</span></span>
<span data-ttu-id="0c873-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0c873-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c873-114">-Id</span><span class="sxs-lookup"><span data-stu-id="0c873-114">-Id</span></span>
<span data-ttu-id="0c873-115">이 cmdlet이 VMSS에서 제거 하는 확장의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c873-115">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c873-116">-이름</span><span class="sxs-lookup"><span data-stu-id="0c873-116">-Name</span></span>
<span data-ttu-id="0c873-117">이 cmdlet이 VMSS에서 제거 하는 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c873-117">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c873-118">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0c873-118">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="0c873-119">확장명을 제거할 VMSS를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c873-119">Specifies the VMSS from which to remove the extension from.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c873-120">-확인</span><span class="sxs-lookup"><span data-stu-id="0c873-120">-Confirm</span></span>
<span data-ttu-id="0c873-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c873-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c873-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c873-122">-WhatIf</span></span>
<span data-ttu-id="0c873-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0c873-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c873-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0c873-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c873-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c873-125">CommonParameters</span></span>
<span data-ttu-id="0c873-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c873-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c873-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c873-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c873-128">입력</span><span class="sxs-lookup"><span data-stu-id="0c873-128">INPUTS</span></span>

### <span data-ttu-id="0c873-129">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0c873-129">VirtualMachineScaleSet</span></span>
<span data-ttu-id="0c873-130">' VirtualMachineScaleSet ' 매개 변수는 파이프라인에서 ' VirtualMachineScaleSet ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c873-130">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="0c873-131">출력</span><span class="sxs-lookup"><span data-stu-id="0c873-131">OUTPUTS</span></span>

### <span data-ttu-id="0c873-132">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0c873-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="0c873-133">상속자</span><span class="sxs-lookup"><span data-stu-id="0c873-133">NOTES</span></span>

## <span data-ttu-id="0c873-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0c873-134">RELATED LINKS</span></span>

[<span data-ttu-id="0c873-135">추가-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="0c873-135">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)
