---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/test-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 8f6e161ad9ae2078da15dda659f1aea13929eec9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525044"
---
# <span data-ttu-id="00bde-101">Test-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="00bde-101">Test-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="00bde-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00bde-102">SYNOPSIS</span></span>
<span data-ttu-id="00bde-103">PowerBI 포함 용량의 인스턴스가 있는지 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="00bde-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00bde-104">구문과</span><span class="sxs-lookup"><span data-stu-id="00bde-104">SYNTAX</span></span>

```
Test-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [<CommonParameters>]
```

## <span data-ttu-id="00bde-105">설명은</span><span class="sxs-lookup"><span data-stu-id="00bde-105">DESCRIPTION</span></span>
<span data-ttu-id="00bde-106">Test-AzureRmPowerBIEmbeddedCapacity cmdlet은 PowerBI 포함 용량의 인스턴스가 있는지 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="00bde-106">The Test-AzureRmPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="00bde-107">예제의</span><span class="sxs-lookup"><span data-stu-id="00bde-107">EXAMPLES</span></span>

### <span data-ttu-id="00bde-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="00bde-108">Example 1</span></span>
```
PS C:\> Test-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="00bde-109">이 명령은 testcapacity 라는 용량이 있는지 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="00bde-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="00bde-110">변수</span><span class="sxs-lookup"><span data-stu-id="00bde-110">PARAMETERS</span></span>

### <span data-ttu-id="00bde-111">-이름</span><span class="sxs-lookup"><span data-stu-id="00bde-111">-Name</span></span>
<span data-ttu-id="00bde-112">PowerBI 포함 용량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00bde-112">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="00bde-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00bde-113">CommonParameters</span></span>
<span data-ttu-id="00bde-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="00bde-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00bde-115">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00bde-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00bde-116">입력</span><span class="sxs-lookup"><span data-stu-id="00bde-116">INPUTS</span></span>

### <span data-ttu-id="00bde-117">않아야</span><span class="sxs-lookup"><span data-stu-id="00bde-117">None</span></span>
<span data-ttu-id="00bde-118">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="00bde-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="00bde-119">출력</span><span class="sxs-lookup"><span data-stu-id="00bde-119">OUTPUTS</span></span>

### <span data-ttu-id="00bde-120">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="00bde-120">System.Boolean</span></span>

## <span data-ttu-id="00bde-121">상속자</span><span class="sxs-lookup"><span data-stu-id="00bde-121">NOTES</span></span>

## <span data-ttu-id="00bde-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="00bde-122">RELATED LINKS</span></span>

[<span data-ttu-id="00bde-123">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="00bde-123">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="00bde-124">제거-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="00bde-124">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
