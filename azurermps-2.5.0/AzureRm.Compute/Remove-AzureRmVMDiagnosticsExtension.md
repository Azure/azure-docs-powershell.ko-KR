---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmdiagnosticsextension
schema: 2.0.0
ms.openlocfilehash: 57e3aef7ff5b6acece0ccba1505d33f2add05ae2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881985"
---
# <span data-ttu-id="73dfc-101">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="73dfc-101">Remove-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="73dfc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73dfc-102">SYNOPSIS</span></span>
<span data-ttu-id="73dfc-103">가상 컴퓨터에서 진단 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="73dfc-103">Removes the Diagnostics extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73dfc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="73dfc-104">SYNTAX</span></span>

```
Remove-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73dfc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="73dfc-105">DESCRIPTION</span></span>
<span data-ttu-id="73dfc-106">**AzureRmVMDiagnosticsExtension** cmdlet은 가상 머신에서 Azure Diagnostics 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="73dfc-106">The **Remove-AzureRmVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="73dfc-107">이 cmdlet의 출력을 Update-AzureRmVM cmdlet에 전달 하 여 변경 내용을 구현 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="73dfc-107">You must pass the output of this cmdlet to the Update-AzureRmVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="73dfc-108">예제의</span><span class="sxs-lookup"><span data-stu-id="73dfc-108">EXAMPLES</span></span>

### <span data-ttu-id="73dfc-109">예제 1: 가상 머신에서 진단 확장 제거</span><span class="sxs-lookup"><span data-stu-id="73dfc-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzureRmVM
```

<span data-ttu-id="73dfc-110">이 명령은 ContosoVM22 이라는 가상 컴퓨터에서 진단 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="73dfc-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="73dfc-111">이 명령은 파이프라인 연산자를 사용 하 여 결과를 Update-AzureRmVM cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="73dfc-111">The command passes the result to the Update-AzureRmVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="73dfc-112">이 명령은 가상 컴퓨터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="73dfc-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="73dfc-113">변수</span><span class="sxs-lookup"><span data-stu-id="73dfc-113">PARAMETERS</span></span>

### <span data-ttu-id="73dfc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73dfc-114">-DefaultProfile</span></span>
<span data-ttu-id="73dfc-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="73dfc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73dfc-116">-이름</span><span class="sxs-lookup"><span data-stu-id="73dfc-116">-Name</span></span>
<span data-ttu-id="73dfc-117">이 cmdlet이 제거 하는 진단 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73dfc-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="73dfc-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73dfc-118">-ResourceGroupName</span></span>
<span data-ttu-id="73dfc-119">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73dfc-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="73dfc-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="73dfc-120">-VMName</span></span>
<span data-ttu-id="73dfc-121">이 cmdlet이 진단 확장을 제거 하는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73dfc-121">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="73dfc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73dfc-122">CommonParameters</span></span>
<span data-ttu-id="73dfc-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="73dfc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73dfc-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73dfc-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73dfc-125">입력</span><span class="sxs-lookup"><span data-stu-id="73dfc-125">INPUTS</span></span>

### <span data-ttu-id="73dfc-126">않아야</span><span class="sxs-lookup"><span data-stu-id="73dfc-126">None</span></span>
<span data-ttu-id="73dfc-127">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73dfc-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="73dfc-128">출력</span><span class="sxs-lookup"><span data-stu-id="73dfc-128">OUTPUTS</span></span>

### <span data-ttu-id="73dfc-129">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="73dfc-129">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="73dfc-130">상속자</span><span class="sxs-lookup"><span data-stu-id="73dfc-130">NOTES</span></span>

## <span data-ttu-id="73dfc-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="73dfc-131">RELATED LINKS</span></span>

[<span data-ttu-id="73dfc-132">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="73dfc-132">Get-AzureRmVMDiagnosticsExtension</span></span>](./Get-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="73dfc-133">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="73dfc-133">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="73dfc-134">업데이트-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="73dfc-134">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


