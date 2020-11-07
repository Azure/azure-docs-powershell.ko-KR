---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/test-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 306bb6e4e12adcb4a4eda65b2517ddf0648a81fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702910"
---
# <span data-ttu-id="1cd03-101">Test-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="1cd03-101">Test-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="1cd03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cd03-102">SYNOPSIS</span></span>
<span data-ttu-id="1cd03-103">PowerBI 포함 용량의 인스턴스가 있는지 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cd03-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1cd03-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1cd03-104">SYNTAX</span></span>

```
Test-AzureRmPowerBIEmbeddedCapacity [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1cd03-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1cd03-105">DESCRIPTION</span></span>
<span data-ttu-id="1cd03-106">Test-AzureRmPowerBIEmbeddedCapacity cmdlet은 PowerBI 포함 용량의 인스턴스가 있는지 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cd03-106">The Test-AzureRmPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="1cd03-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1cd03-107">EXAMPLES</span></span>

### <span data-ttu-id="1cd03-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="1cd03-108">Example 1</span></span>
```
PS C:\> Test-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="1cd03-109">이 명령은 testcapacity 라는 용량이 있는지 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cd03-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="1cd03-110">변수</span><span class="sxs-lookup"><span data-stu-id="1cd03-110">PARAMETERS</span></span>

### <span data-ttu-id="1cd03-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cd03-111">-DefaultProfile</span></span>
<span data-ttu-id="1cd03-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1cd03-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cd03-113">-이름</span><span class="sxs-lookup"><span data-stu-id="1cd03-113">-Name</span></span>
<span data-ttu-id="1cd03-114">PowerBI 포함 용량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1cd03-114">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cd03-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cd03-115">CommonParameters</span></span>
<span data-ttu-id="1cd03-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cd03-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cd03-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cd03-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cd03-118">입력</span><span class="sxs-lookup"><span data-stu-id="1cd03-118">INPUTS</span></span>

### <span data-ttu-id="1cd03-119">않아야</span><span class="sxs-lookup"><span data-stu-id="1cd03-119">None</span></span>

## <span data-ttu-id="1cd03-120">출력</span><span class="sxs-lookup"><span data-stu-id="1cd03-120">OUTPUTS</span></span>

### <span data-ttu-id="1cd03-121">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="1cd03-121">System.Boolean</span></span>

## <span data-ttu-id="1cd03-122">상속자</span><span class="sxs-lookup"><span data-stu-id="1cd03-122">NOTES</span></span>

## <span data-ttu-id="1cd03-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1cd03-123">RELATED LINKS</span></span>

[<span data-ttu-id="1cd03-124">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="1cd03-124">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="1cd03-125">제거-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="1cd03-125">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
