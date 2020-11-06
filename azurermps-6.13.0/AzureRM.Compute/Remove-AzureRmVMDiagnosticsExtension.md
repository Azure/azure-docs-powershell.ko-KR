---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMDiagnosticsExtension.md
ms.openlocfilehash: 4a14c5138a0dac983067e6deb4b1e05b88d85259
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534436"
---
# <span data-ttu-id="4c3f7-101">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="4c3f7-101">Remove-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="4c3f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c3f7-102">SYNOPSIS</span></span>
<span data-ttu-id="4c3f7-103">가상 컴퓨터에서 진단 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-103">Removes the Diagnostics extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c3f7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4c3f7-104">SYNTAX</span></span>

```
Remove-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c3f7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4c3f7-105">DESCRIPTION</span></span>
<span data-ttu-id="4c3f7-106">**AzureRmVMDiagnosticsExtension** cmdlet은 가상 머신에서 Azure Diagnostics 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-106">The **Remove-AzureRmVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="4c3f7-107">이 cmdlet의 출력을 Update-AzureRmVM cmdlet에 전달 하 여 변경 내용을 구현 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-107">You must pass the output of this cmdlet to the Update-AzureRmVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="4c3f7-108">예제의</span><span class="sxs-lookup"><span data-stu-id="4c3f7-108">EXAMPLES</span></span>

### <span data-ttu-id="4c3f7-109">예제 1: 가상 머신에서 진단 확장 제거</span><span class="sxs-lookup"><span data-stu-id="4c3f7-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzureRmVM
```

<span data-ttu-id="4c3f7-110">이 명령은 ContosoVM22 이라는 가상 컴퓨터에서 진단 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="4c3f7-111">이 명령은 파이프라인 연산자를 사용 하 여 결과를 Update-AzureRmVM cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-111">The command passes the result to the Update-AzureRmVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4c3f7-112">이 명령은 가상 컴퓨터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="4c3f7-113">변수</span><span class="sxs-lookup"><span data-stu-id="4c3f7-113">PARAMETERS</span></span>

### <span data-ttu-id="4c3f7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c3f7-114">-DefaultProfile</span></span>
<span data-ttu-id="4c3f7-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c3f7-116">-이름</span><span class="sxs-lookup"><span data-stu-id="4c3f7-116">-Name</span></span>
<span data-ttu-id="4c3f7-117">이 cmdlet이 제거 하는 진단 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4c3f7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c3f7-118">-ResourceGroupName</span></span>
<span data-ttu-id="4c3f7-119">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="4c3f7-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="4c3f7-120">-VMName</span></span>
<span data-ttu-id="4c3f7-121">이 cmdlet이 진단 확장을 제거 하는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-121">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="4c3f7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c3f7-122">CommonParameters</span></span>
<span data-ttu-id="4c3f7-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c3f7-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c3f7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c3f7-125">입력</span><span class="sxs-lookup"><span data-stu-id="4c3f7-125">INPUTS</span></span>

### <span data-ttu-id="4c3f7-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4c3f7-126">System.String</span></span>

## <span data-ttu-id="4c3f7-127">출력</span><span class="sxs-lookup"><span data-stu-id="4c3f7-127">OUTPUTS</span></span>

### <span data-ttu-id="4c3f7-128">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="4c3f7-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="4c3f7-129">상속자</span><span class="sxs-lookup"><span data-stu-id="4c3f7-129">NOTES</span></span>

## <span data-ttu-id="4c3f7-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4c3f7-130">RELATED LINKS</span></span>

[<span data-ttu-id="4c3f7-131">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="4c3f7-131">Get-AzureRmVMDiagnosticsExtension</span></span>](./Get-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="4c3f7-132">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="4c3f7-132">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="4c3f7-133">업데이트-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4c3f7-133">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


