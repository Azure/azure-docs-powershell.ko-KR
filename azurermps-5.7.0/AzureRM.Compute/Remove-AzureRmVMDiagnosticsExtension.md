---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiagnosticsExtension.md
ms.openlocfilehash: b9c2499c3172fcd34000c8adaa0bde144217bcbf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529891"
---
# <span data-ttu-id="6ec66-101">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="6ec66-101">Remove-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="6ec66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ec66-102">SYNOPSIS</span></span>
<span data-ttu-id="6ec66-103">가상 컴퓨터에서 진단 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ec66-103">Removes the Diagnostics extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ec66-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6ec66-104">SYNTAX</span></span>

```
Remove-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="6ec66-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6ec66-105">DESCRIPTION</span></span>
<span data-ttu-id="6ec66-106">**AzureRmVMDiagnosticsExtension** cmdlet은 가상 머신에서 Azure Diagnostics 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ec66-106">The **Remove-AzureRmVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="6ec66-107">이 cmdlet의 출력을 Update-AzureRmVM cmdlet에 전달 하 여 변경 내용을 구현 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ec66-107">You must pass the output of this cmdlet to the Update-AzureRmVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="6ec66-108">예제의</span><span class="sxs-lookup"><span data-stu-id="6ec66-108">EXAMPLES</span></span>

### <span data-ttu-id="6ec66-109">예제 1: 가상 머신에서 진단 확장 제거</span><span class="sxs-lookup"><span data-stu-id="6ec66-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzureRmVM
```

<span data-ttu-id="6ec66-110">이 명령은 ContosoVM22 이라는 가상 컴퓨터에서 진단 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ec66-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="6ec66-111">이 명령은 파이프라인 연산자를 사용 하 여 결과를 Update-AzureRmVM cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ec66-111">The command passes the result to the Update-AzureRmVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6ec66-112">이 명령은 가상 컴퓨터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ec66-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="6ec66-113">변수</span><span class="sxs-lookup"><span data-stu-id="6ec66-113">PARAMETERS</span></span>

### <span data-ttu-id="6ec66-114">-이름</span><span class="sxs-lookup"><span data-stu-id="6ec66-114">-Name</span></span>
<span data-ttu-id="6ec66-115">이 cmdlet이 제거 하는 진단 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ec66-115">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ec66-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ec66-116">-ResourceGroupName</span></span>
<span data-ttu-id="6ec66-117">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ec66-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="6ec66-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="6ec66-118">-VMName</span></span>
<span data-ttu-id="6ec66-119">이 cmdlet이 진단 확장을 제거 하는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ec66-119">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="6ec66-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ec66-120">CommonParameters</span></span>
<span data-ttu-id="6ec66-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ec66-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ec66-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ec66-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ec66-123">입력</span><span class="sxs-lookup"><span data-stu-id="6ec66-123">INPUTS</span></span>

### <span data-ttu-id="6ec66-124">않아야</span><span class="sxs-lookup"><span data-stu-id="6ec66-124">None</span></span>
<span data-ttu-id="6ec66-125">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6ec66-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6ec66-126">출력</span><span class="sxs-lookup"><span data-stu-id="6ec66-126">OUTPUTS</span></span>

## <span data-ttu-id="6ec66-127">상속자</span><span class="sxs-lookup"><span data-stu-id="6ec66-127">NOTES</span></span>

## <span data-ttu-id="6ec66-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6ec66-128">RELATED LINKS</span></span>

[<span data-ttu-id="6ec66-129">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="6ec66-129">Get-AzureRmVMDiagnosticsExtension</span></span>](./Get-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="6ec66-130">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="6ec66-130">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="6ec66-131">업데이트-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6ec66-131">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


