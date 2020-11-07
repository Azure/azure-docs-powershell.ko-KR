---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDscExtension.md
ms.openlocfilehash: 69eff38068c379dadc4f3a061cfba4f9cb6539e3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876947"
---
# <span data-ttu-id="50680-101">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="50680-101">Remove-AzVMDscExtension</span></span>

## <span data-ttu-id="50680-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50680-102">SYNOPSIS</span></span>
<span data-ttu-id="50680-103">리소스 그룹의 가상 컴퓨터에서 DSC 확장 처리기를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="50680-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="50680-104">구문과</span><span class="sxs-lookup"><span data-stu-id="50680-104">SYNTAX</span></span>

```
Remove-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50680-105">설명은</span><span class="sxs-lookup"><span data-stu-id="50680-105">DESCRIPTION</span></span>
<span data-ttu-id="50680-106">**AzVMDscExtension** cmdlet은 리소스 그룹의 가상 컴퓨터에서 원하는 상태 구성 (DSC) 확장 처리기를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="50680-106">The **Remove-AzVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="50680-107">예제의</span><span class="sxs-lookup"><span data-stu-id="50680-107">EXAMPLES</span></span>

### <span data-ttu-id="50680-108">예제 1: DSC 확장 제거</span><span class="sxs-lookup"><span data-stu-id="50680-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="50680-109">이 명령은 VM07 이라는 가상 컴퓨터에서 DSC 라는 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="50680-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="50680-110">변수</span><span class="sxs-lookup"><span data-stu-id="50680-110">PARAMETERS</span></span>

### <span data-ttu-id="50680-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50680-111">-DefaultProfile</span></span>
<span data-ttu-id="50680-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="50680-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50680-113">-이름</span><span class="sxs-lookup"><span data-stu-id="50680-113">-Name</span></span>
<span data-ttu-id="50680-114">이 cmdlet이 제거 하는 DSC 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50680-114">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="50680-115">Set-AzVMDscExtension cmdlet은이 이름을 **AzVMDscExtension** 에 사용 되는 기본 값인 Microsoft Powershell로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50680-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzVMDscExtension**.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50680-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50680-116">-ResourceGroupName</span></span>
<span data-ttu-id="50680-117">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50680-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="50680-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="50680-118">-VMName</span></span>
<span data-ttu-id="50680-119">이 cmdlet이 DSC 확장을 제거 하는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50680-119">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50680-120">-확인</span><span class="sxs-lookup"><span data-stu-id="50680-120">-Confirm</span></span>
<span data-ttu-id="50680-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="50680-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50680-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50680-122">-WhatIf</span></span>
<span data-ttu-id="50680-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="50680-123">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="50680-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="50680-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50680-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50680-125">CommonParameters</span></span>
<span data-ttu-id="50680-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="50680-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50680-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50680-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50680-128">입력</span><span class="sxs-lookup"><span data-stu-id="50680-128">INPUTS</span></span>

### <span data-ttu-id="50680-129">않아야</span><span class="sxs-lookup"><span data-stu-id="50680-129">None</span></span>
<span data-ttu-id="50680-130">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="50680-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="50680-131">출력</span><span class="sxs-lookup"><span data-stu-id="50680-131">OUTPUTS</span></span>

### <span data-ttu-id="50680-132">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="50680-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="50680-133">상속자</span><span class="sxs-lookup"><span data-stu-id="50680-133">NOTES</span></span>

## <span data-ttu-id="50680-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="50680-134">RELATED LINKS</span></span>

[<span data-ttu-id="50680-135">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="50680-135">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="50680-136">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="50680-136">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


