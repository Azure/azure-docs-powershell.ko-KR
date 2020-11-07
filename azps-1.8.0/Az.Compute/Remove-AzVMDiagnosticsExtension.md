---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
ms.openlocfilehash: bcfc7f3d80c5601d5797d9af2958d2bed6395fbe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868953"
---
# <span data-ttu-id="75098-101">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="75098-101">Remove-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="75098-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75098-102">SYNOPSIS</span></span>
<span data-ttu-id="75098-103">가상 컴퓨터에서 진단 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="75098-103">Removes the Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="75098-104">구문과</span><span class="sxs-lookup"><span data-stu-id="75098-104">SYNTAX</span></span>

```
Remove-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75098-105">설명은</span><span class="sxs-lookup"><span data-stu-id="75098-105">DESCRIPTION</span></span>
<span data-ttu-id="75098-106">**AzVMDiagnosticsExtension** cmdlet은 가상 머신에서 Azure Diagnostics 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="75098-106">The **Remove-AzVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="75098-107">이 cmdlet의 출력을 Update-AzVM cmdlet에 전달 하 여 변경 내용을 구현 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="75098-107">You must pass the output of this cmdlet to the Update-AzVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="75098-108">예제의</span><span class="sxs-lookup"><span data-stu-id="75098-108">EXAMPLES</span></span>

### <span data-ttu-id="75098-109">예제 1: 가상 머신에서 진단 확장 제거</span><span class="sxs-lookup"><span data-stu-id="75098-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzVM
```

<span data-ttu-id="75098-110">이 명령은 ContosoVM22 이라는 가상 컴퓨터에서 진단 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="75098-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="75098-111">이 명령은 파이프라인 연산자를 사용 하 여 결과를 Update-AzVM cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="75098-111">The command passes the result to the Update-AzVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="75098-112">이 명령은 가상 컴퓨터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="75098-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="75098-113">변수</span><span class="sxs-lookup"><span data-stu-id="75098-113">PARAMETERS</span></span>

### <span data-ttu-id="75098-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75098-114">-DefaultProfile</span></span>
<span data-ttu-id="75098-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="75098-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75098-116">-이름</span><span class="sxs-lookup"><span data-stu-id="75098-116">-Name</span></span>
<span data-ttu-id="75098-117">이 cmdlet이 제거 하는 진단 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75098-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75098-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75098-118">-ResourceGroupName</span></span>
<span data-ttu-id="75098-119">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75098-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="75098-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="75098-120">-VMName</span></span>
<span data-ttu-id="75098-121">이 cmdlet이 진단 확장을 제거 하는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75098-121">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="75098-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75098-122">CommonParameters</span></span>
<span data-ttu-id="75098-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="75098-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75098-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75098-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75098-125">입력</span><span class="sxs-lookup"><span data-stu-id="75098-125">INPUTS</span></span>

### <span data-ttu-id="75098-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="75098-126">System.String</span></span>

## <span data-ttu-id="75098-127">출력</span><span class="sxs-lookup"><span data-stu-id="75098-127">OUTPUTS</span></span>

### <span data-ttu-id="75098-128">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="75098-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="75098-129">상속자</span><span class="sxs-lookup"><span data-stu-id="75098-129">NOTES</span></span>

## <span data-ttu-id="75098-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="75098-130">RELATED LINKS</span></span>

[<span data-ttu-id="75098-131">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="75098-131">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="75098-132">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="75098-132">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="75098-133">업데이트-AzVM</span><span class="sxs-lookup"><span data-stu-id="75098-133">Update-AzVM</span></span>](./Update-AzVM.md)


