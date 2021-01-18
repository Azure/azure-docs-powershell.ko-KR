---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsssku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
ms.openlocfilehash: 4b17cbb748a9841e0c22f4b8d8742562876fb9db
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493861"
---
# <span data-ttu-id="5812c-101">Get-AzVmssSku</span><span class="sxs-lookup"><span data-stu-id="5812c-101">Get-AzVmssSku</span></span>

## <span data-ttu-id="5812c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5812c-102">SYNOPSIS</span></span>
<span data-ttu-id="5812c-103">VMSS에 사용 가능한 SKUS를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5812c-103">Gets the available SKUs for the VMSS.</span></span>

## <span data-ttu-id="5812c-104">구문</span><span class="sxs-lookup"><span data-stu-id="5812c-104">SYNTAX</span></span>

```
Get-AzVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5812c-105">설명</span><span class="sxs-lookup"><span data-stu-id="5812c-105">DESCRIPTION</span></span>
<span data-ttu-id="5812c-106">**Get-AzVmssSku** cmdlet은 VMSS(Virtual Machine Scale Set)에 사용 가능한 SKU를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5812c-106">The **Get-AzVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="5812c-107">예제</span><span class="sxs-lookup"><span data-stu-id="5812c-107">EXAMPLES</span></span>

### <span data-ttu-id="5812c-108">예제 1: VMSS에서 사용 가능한 모든 SKUS를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5812c-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="5812c-109">이 명령은 ContosoGroup이라는 리소스 그룹에 속하는 ContosoVMSS라는 VMSS에서 사용 가능한 모든 SKUS를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5812c-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="5812c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5812c-110">PARAMETERS</span></span>

### <span data-ttu-id="5812c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5812c-111">-DefaultProfile</span></span>
<span data-ttu-id="5812c-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5812c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5812c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5812c-113">-ResourceGroupName</span></span>
<span data-ttu-id="5812c-114">VMSS의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5812c-114">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="5812c-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="5812c-115">-VMScaleSetName</span></span>
<span data-ttu-id="5812c-116">VMSS의 이름 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="5812c-116">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5812c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5812c-117">CommonParameters</span></span>
<span data-ttu-id="5812c-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5812c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5812c-119">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5812c-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5812c-120">입력</span><span class="sxs-lookup"><span data-stu-id="5812c-120">INPUTS</span></span>

### <span data-ttu-id="5812c-121">System.String</span><span class="sxs-lookup"><span data-stu-id="5812c-121">System.String</span></span>

## <span data-ttu-id="5812c-122">출력</span><span class="sxs-lookup"><span data-stu-id="5812c-122">OUTPUTS</span></span>

### <span data-ttu-id="5812c-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetSku</span><span class="sxs-lookup"><span data-stu-id="5812c-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetSku</span></span>

## <span data-ttu-id="5812c-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5812c-124">NOTES</span></span>

## <span data-ttu-id="5812c-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5812c-125">RELATED LINKS</span></span>

[<span data-ttu-id="5812c-126">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5812c-126">Get-AzVmss</span></span>](./Get-AzVmss.md)


