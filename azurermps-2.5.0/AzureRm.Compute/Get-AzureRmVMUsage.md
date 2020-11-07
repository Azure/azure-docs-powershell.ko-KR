---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmusage
schema: 2.0.0
ms.openlocfilehash: 210c66f91836b40c719d91907fc78bd907d0fe86
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93883162"
---
# <span data-ttu-id="3ee0a-101">Get-AzureRmVMUsage</span><span class="sxs-lookup"><span data-stu-id="3ee0a-101">Get-AzureRmVMUsage</span></span>

## <span data-ttu-id="3ee0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ee0a-102">SYNOPSIS</span></span>
<span data-ttu-id="3ee0a-103">위치에 대 한 가상 컴퓨터 코어 수 사용량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3ee0a-103">Gets the virtual machine core count usage for a location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ee0a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3ee0a-104">SYNTAX</span></span>

```
Get-AzureRmVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ee0a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3ee0a-105">DESCRIPTION</span></span>
<span data-ttu-id="3ee0a-106">**AzureRmVMUsage** cmdlet은 위치에 대 한 가상 컴퓨터 코어 수 사용량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3ee0a-106">The **Get-AzureRmVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="3ee0a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3ee0a-107">EXAMPLES</span></span>

### <span data-ttu-id="3ee0a-108">예제 1: 위치에 대 한 코어 카운트 사용 가져오기</span><span class="sxs-lookup"><span data-stu-id="3ee0a-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzureRmVMUsage -Location "Central US"
```

<span data-ttu-id="3ee0a-109">이 명령은 위치 중앙 미국에 대 한 가상 컴퓨터 코어 수 사용량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3ee0a-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="3ee0a-110">변수</span><span class="sxs-lookup"><span data-stu-id="3ee0a-110">PARAMETERS</span></span>

### <span data-ttu-id="3ee0a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ee0a-111">-DefaultProfile</span></span>
<span data-ttu-id="3ee0a-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3ee0a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ee0a-113">-위치</span><span class="sxs-lookup"><span data-stu-id="3ee0a-113">-Location</span></span>
<span data-ttu-id="3ee0a-114">이 cmdlet이 가상 컴퓨터 코어 수 사용량을 가져오는 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ee0a-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="3ee0a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ee0a-115">CommonParameters</span></span>
<span data-ttu-id="3ee0a-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ee0a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ee0a-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ee0a-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ee0a-118">입력</span><span class="sxs-lookup"><span data-stu-id="3ee0a-118">INPUTS</span></span>

### <span data-ttu-id="3ee0a-119">않아야</span><span class="sxs-lookup"><span data-stu-id="3ee0a-119">None</span></span>
<span data-ttu-id="3ee0a-120">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3ee0a-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3ee0a-121">출력</span><span class="sxs-lookup"><span data-stu-id="3ee0a-121">OUTPUTS</span></span>

### <span data-ttu-id="3ee0a-122">Microsoft. \*. m a i. PSUsage</span><span class="sxs-lookup"><span data-stu-id="3ee0a-122">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="3ee0a-123">상속자</span><span class="sxs-lookup"><span data-stu-id="3ee0a-123">NOTES</span></span>

## <span data-ttu-id="3ee0a-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3ee0a-124">RELATED LINKS</span></span>

[<span data-ttu-id="3ee0a-125">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3ee0a-125">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


