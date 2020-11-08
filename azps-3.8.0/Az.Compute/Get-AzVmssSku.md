---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsssku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
ms.openlocfilehash: 4b17cbb748a9841e0c22f4b8d8742562876fb9db
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94033946"
---
# <span data-ttu-id="06cee-101">Get-AzVmssSku</span><span class="sxs-lookup"><span data-stu-id="06cee-101">Get-AzVmssSku</span></span>

## <span data-ttu-id="06cee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06cee-102">SYNOPSIS</span></span>
<span data-ttu-id="06cee-103">VMSS에 사용할 수 있는 Sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06cee-103">Gets the available SKUs for the VMSS.</span></span>

## <span data-ttu-id="06cee-104">구문과</span><span class="sxs-lookup"><span data-stu-id="06cee-104">SYNTAX</span></span>

```
Get-AzVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06cee-105">설명은</span><span class="sxs-lookup"><span data-stu-id="06cee-105">DESCRIPTION</span></span>
<span data-ttu-id="06cee-106">**AzVmssSku** CMDLET은 Vmss (가상 머신 확장 집합)에 사용할 수 있는 sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06cee-106">The **Get-AzVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="06cee-107">예제의</span><span class="sxs-lookup"><span data-stu-id="06cee-107">EXAMPLES</span></span>

### <span data-ttu-id="06cee-108">예제 1: VMSS에서 사용 가능한 모든 Sku 가져오기</span><span class="sxs-lookup"><span data-stu-id="06cee-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="06cee-109">이 명령은 ContosoGroup 이라는 리소스 그룹에 속하는 VMSS 인 ContosoVMSS의 모든 사용 가능한 Sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06cee-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="06cee-110">변수</span><span class="sxs-lookup"><span data-stu-id="06cee-110">PARAMETERS</span></span>

### <span data-ttu-id="06cee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06cee-111">-DefaultProfile</span></span>
<span data-ttu-id="06cee-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="06cee-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06cee-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06cee-113">-ResourceGroupName</span></span>
<span data-ttu-id="06cee-114">VMSS의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06cee-114">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="06cee-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="06cee-115">-VMScaleSetName</span></span>
<span data-ttu-id="06cee-116">VMSS의 이름을 종류로 합니다.</span><span class="sxs-lookup"><span data-stu-id="06cee-116">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="06cee-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06cee-117">CommonParameters</span></span>
<span data-ttu-id="06cee-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="06cee-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06cee-119">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="06cee-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06cee-120">입력</span><span class="sxs-lookup"><span data-stu-id="06cee-120">INPUTS</span></span>

### <span data-ttu-id="06cee-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="06cee-121">System.String</span></span>

## <span data-ttu-id="06cee-122">출력</span><span class="sxs-lookup"><span data-stu-id="06cee-122">OUTPUTS</span></span>

### <span data-ttu-id="06cee-123">PSVirtualMachineScaleSetSku의. m a.</span><span class="sxs-lookup"><span data-stu-id="06cee-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetSku</span></span>

## <span data-ttu-id="06cee-124">상속자</span><span class="sxs-lookup"><span data-stu-id="06cee-124">NOTES</span></span>

## <span data-ttu-id="06cee-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="06cee-125">RELATED LINKS</span></span>

[<span data-ttu-id="06cee-126">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="06cee-126">Get-AzVmss</span></span>](./Get-AzVmss.md)


