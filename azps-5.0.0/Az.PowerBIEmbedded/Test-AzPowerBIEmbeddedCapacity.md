---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/test-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 73960bb3efbc3d1a55d9894943c2f92bcf931faa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94219175"
---
# <span data-ttu-id="16df0-101">Test-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="16df0-101">Test-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="16df0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16df0-102">SYNOPSIS</span></span>
<span data-ttu-id="16df0-103">PowerBI 포함 용량의 인스턴스가 있는지 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="16df0-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="16df0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="16df0-104">SYNTAX</span></span>

```
Test-AzPowerBIEmbeddedCapacity [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16df0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="16df0-105">DESCRIPTION</span></span>
<span data-ttu-id="16df0-106">Test-AzPowerBIEmbeddedCapacity cmdlet은 PowerBI 포함 용량의 인스턴스가 있는지 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="16df0-106">The Test-AzPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="16df0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="16df0-107">EXAMPLES</span></span>

### <span data-ttu-id="16df0-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="16df0-108">Example 1</span></span>
```
PS C:\> Test-AzPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="16df0-109">이 명령은 testcapacity 라는 용량이 있는지 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="16df0-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="16df0-110">변수</span><span class="sxs-lookup"><span data-stu-id="16df0-110">PARAMETERS</span></span>

### <span data-ttu-id="16df0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16df0-111">-DefaultProfile</span></span>
<span data-ttu-id="16df0-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="16df0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16df0-113">-이름</span><span class="sxs-lookup"><span data-stu-id="16df0-113">-Name</span></span>
<span data-ttu-id="16df0-114">PowerBI 포함 용량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16df0-114">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="16df0-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16df0-115">CommonParameters</span></span>
<span data-ttu-id="16df0-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="16df0-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16df0-117">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16df0-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16df0-118">입력</span><span class="sxs-lookup"><span data-stu-id="16df0-118">INPUTS</span></span>

### <span data-ttu-id="16df0-119">않아야</span><span class="sxs-lookup"><span data-stu-id="16df0-119">None</span></span>

## <span data-ttu-id="16df0-120">출력</span><span class="sxs-lookup"><span data-stu-id="16df0-120">OUTPUTS</span></span>

### <span data-ttu-id="16df0-121">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="16df0-121">System.Boolean</span></span>

## <span data-ttu-id="16df0-122">상속자</span><span class="sxs-lookup"><span data-stu-id="16df0-122">NOTES</span></span>

## <span data-ttu-id="16df0-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="16df0-123">RELATED LINKS</span></span>

[<span data-ttu-id="16df0-124">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="16df0-124">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="16df0-125">제거-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="16df0-125">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
