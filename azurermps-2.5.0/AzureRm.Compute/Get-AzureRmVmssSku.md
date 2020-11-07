---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmsssku
schema: 2.0.0
ms.openlocfilehash: 307b9852f506368e1e13c02fac4532dab4d2ddd2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882005"
---
# <span data-ttu-id="f0783-101">Get-AzureRmVmssSku</span><span class="sxs-lookup"><span data-stu-id="f0783-101">Get-AzureRmVmssSku</span></span>

## <span data-ttu-id="f0783-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0783-102">SYNOPSIS</span></span>
<span data-ttu-id="f0783-103">VMSS에 사용할 수 있는 Sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f0783-103">Gets the available SKUs for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0783-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f0783-104">SYNTAX</span></span>

```
Get-AzureRmVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0783-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f0783-105">DESCRIPTION</span></span>
<span data-ttu-id="f0783-106">**AzureRmVmssSku** CMDLET은 Vmss (가상 머신 확장 집합)에 사용할 수 있는 sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f0783-106">The **Get-AzureRmVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="f0783-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f0783-107">EXAMPLES</span></span>

### <span data-ttu-id="f0783-108">예제 1: VMSS에서 사용 가능한 모든 Sku 가져오기</span><span class="sxs-lookup"><span data-stu-id="f0783-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzureRmVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="f0783-109">이 명령은 ContosoGroup 이라는 리소스 그룹에 속하는 VMSS 인 ContosoVMSS의 모든 사용 가능한 Sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f0783-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="f0783-110">변수</span><span class="sxs-lookup"><span data-stu-id="f0783-110">PARAMETERS</span></span>

### <span data-ttu-id="f0783-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0783-111">-DefaultProfile</span></span>
<span data-ttu-id="f0783-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f0783-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0783-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0783-113">-ResourceGroupName</span></span>
<span data-ttu-id="f0783-114">VMSS의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0783-114">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="f0783-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f0783-115">-VMScaleSetName</span></span>
<span data-ttu-id="f0783-116">VMSS의 이름을 종류로 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0783-116">Species the name of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0783-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0783-117">CommonParameters</span></span>
<span data-ttu-id="f0783-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0783-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0783-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0783-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0783-120">입력</span><span class="sxs-lookup"><span data-stu-id="f0783-120">INPUTS</span></span>

### <span data-ttu-id="f0783-121">않아야</span><span class="sxs-lookup"><span data-stu-id="f0783-121">None</span></span>
<span data-ttu-id="f0783-122">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0783-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f0783-123">출력</span><span class="sxs-lookup"><span data-stu-id="f0783-123">OUTPUTS</span></span>

### <span data-ttu-id="f0783-124">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0783-124">This cmdlet does not produce any output.</span></span>

## <span data-ttu-id="f0783-125">상속자</span><span class="sxs-lookup"><span data-stu-id="f0783-125">NOTES</span></span>

## <span data-ttu-id="f0783-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f0783-126">RELATED LINKS</span></span>

[<span data-ttu-id="f0783-127">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f0783-127">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


