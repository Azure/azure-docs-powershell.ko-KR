---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/test-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 0b7d1f72b25da91e85a578a88eded7a511d6d1fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996086"
---
# <span data-ttu-id="bf366-101">Test-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="bf366-101">Test-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="bf366-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf366-102">SYNOPSIS</span></span>
<span data-ttu-id="bf366-103">PowerBI Embedded Capacity 인스턴스의 존재를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="bf366-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="bf366-104">구문</span><span class="sxs-lookup"><span data-stu-id="bf366-104">SYNTAX</span></span>

```
Test-AzPowerBIEmbeddedCapacity [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf366-105">설명</span><span class="sxs-lookup"><span data-stu-id="bf366-105">DESCRIPTION</span></span>
<span data-ttu-id="bf366-106">Test-AzPowerBIEmbeddedCapacity cmdlet은 PowerBI Embedded Capacity 인스턴스의 존재를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="bf366-106">The Test-AzPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="bf366-107">예제</span><span class="sxs-lookup"><span data-stu-id="bf366-107">EXAMPLES</span></span>

### <span data-ttu-id="bf366-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="bf366-108">Example 1</span></span>
```
PS C:\> Test-AzPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="bf366-109">이 명령은 testcapacity라는 용량이 있는지 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="bf366-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="bf366-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="bf366-110">PARAMETERS</span></span>

### <span data-ttu-id="bf366-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf366-111">-DefaultProfile</span></span>
<span data-ttu-id="bf366-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bf366-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf366-113">-Name</span><span class="sxs-lookup"><span data-stu-id="bf366-113">-Name</span></span>
<span data-ttu-id="bf366-114">PowerBI 임베디드 용량의 이름</span><span class="sxs-lookup"><span data-stu-id="bf366-114">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="bf366-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf366-115">CommonParameters</span></span>
<span data-ttu-id="bf366-116">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bf366-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf366-117">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bf366-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf366-118">입력</span><span class="sxs-lookup"><span data-stu-id="bf366-118">INPUTS</span></span>

### <span data-ttu-id="bf366-119">없음</span><span class="sxs-lookup"><span data-stu-id="bf366-119">None</span></span>

## <span data-ttu-id="bf366-120">출력</span><span class="sxs-lookup"><span data-stu-id="bf366-120">OUTPUTS</span></span>

### <span data-ttu-id="bf366-121">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bf366-121">System.Boolean</span></span>

## <span data-ttu-id="bf366-122">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bf366-122">NOTES</span></span>

## <span data-ttu-id="bf366-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bf366-123">RELATED LINKS</span></span>

[<span data-ttu-id="bf366-124">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="bf366-124">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="bf366-125">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="bf366-125">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
