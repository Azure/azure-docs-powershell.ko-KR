---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/test-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 73960bb3efbc3d1a55d9894943c2f92bcf931faa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94033795"
---
# <span data-ttu-id="80542-101">Test-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="80542-101">Test-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="80542-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80542-102">SYNOPSIS</span></span>
<span data-ttu-id="80542-103">PowerBI 포함 용량의 인스턴스가 있는지 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="80542-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="80542-104">구문과</span><span class="sxs-lookup"><span data-stu-id="80542-104">SYNTAX</span></span>

```
Test-AzPowerBIEmbeddedCapacity [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80542-105">설명은</span><span class="sxs-lookup"><span data-stu-id="80542-105">DESCRIPTION</span></span>
<span data-ttu-id="80542-106">Test-AzPowerBIEmbeddedCapacity cmdlet은 PowerBI 포함 용량의 인스턴스가 있는지 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="80542-106">The Test-AzPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="80542-107">예제의</span><span class="sxs-lookup"><span data-stu-id="80542-107">EXAMPLES</span></span>

### <span data-ttu-id="80542-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="80542-108">Example 1</span></span>
```
PS C:\> Test-AzPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="80542-109">이 명령은 testcapacity 라는 용량이 있는지 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="80542-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="80542-110">변수</span><span class="sxs-lookup"><span data-stu-id="80542-110">PARAMETERS</span></span>

### <span data-ttu-id="80542-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80542-111">-DefaultProfile</span></span>
<span data-ttu-id="80542-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="80542-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80542-113">-이름</span><span class="sxs-lookup"><span data-stu-id="80542-113">-Name</span></span>
<span data-ttu-id="80542-114">PowerBI 포함 용량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80542-114">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="80542-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80542-115">CommonParameters</span></span>
<span data-ttu-id="80542-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="80542-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80542-117">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80542-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80542-118">입력</span><span class="sxs-lookup"><span data-stu-id="80542-118">INPUTS</span></span>

### <span data-ttu-id="80542-119">않아야</span><span class="sxs-lookup"><span data-stu-id="80542-119">None</span></span>

## <span data-ttu-id="80542-120">출력</span><span class="sxs-lookup"><span data-stu-id="80542-120">OUTPUTS</span></span>

### <span data-ttu-id="80542-121">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="80542-121">System.Boolean</span></span>

## <span data-ttu-id="80542-122">상속자</span><span class="sxs-lookup"><span data-stu-id="80542-122">NOTES</span></span>

## <span data-ttu-id="80542-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="80542-123">RELATED LINKS</span></span>

[<span data-ttu-id="80542-124">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="80542-124">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="80542-125">제거-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="80542-125">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
