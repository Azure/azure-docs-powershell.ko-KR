---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 556A9F12-DF72-468F-9C3F-A747CC70BD2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azdnsavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
ms.openlocfilehash: 6d6626164000957ffaa987a71131987f35a977c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699936"
---
# <span data-ttu-id="e8ba8-101">Test-AzDnsAvailability</span><span class="sxs-lookup"><span data-stu-id="e8ba8-101">Test-AzDnsAvailability</span></span>

## <span data-ttu-id="e8ba8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8ba8-102">SYNOPSIS</span></span>
<span data-ttu-id="e8ba8-103">Cloudapp.azure.com zone의 도메인 이름을 사용할 수 있는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8ba8-103">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="e8ba8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e8ba8-104">SYNTAX</span></span>

```
Test-AzDnsAvailability -DomainNameLabel <String> -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e8ba8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e8ba8-105">DESCRIPTION</span></span>
<span data-ttu-id="e8ba8-106">Cloudapp.azure.com zone의 도메인 이름을 사용할 수 있는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8ba8-106">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="e8ba8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e8ba8-107">EXAMPLES</span></span>

### <span data-ttu-id="e8ba8-108">예제 1: contoso.cloudapp.azure.com을 사용할 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8ba8-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzDnsAvailability -DomainNameLabel contoso -Location westus
```

## <span data-ttu-id="e8ba8-109">변수</span><span class="sxs-lookup"><span data-stu-id="e8ba8-109">PARAMETERS</span></span>

### <span data-ttu-id="e8ba8-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8ba8-110">-DefaultProfile</span></span>
<span data-ttu-id="e8ba8-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e8ba8-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8ba8-112">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="e8ba8-112">-DomainNameLabel</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainQualifiedName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ba8-113">-위치</span><span class="sxs-lookup"><span data-stu-id="e8ba8-113">-Location</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ba8-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8ba8-114">CommonParameters</span></span>
<span data-ttu-id="e8ba8-115">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8ba8-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8ba8-116">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8ba8-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8ba8-117">입력</span><span class="sxs-lookup"><span data-stu-id="e8ba8-117">INPUTS</span></span>

### <span data-ttu-id="e8ba8-118">않아야</span><span class="sxs-lookup"><span data-stu-id="e8ba8-118">None</span></span>

## <span data-ttu-id="e8ba8-119">출력</span><span class="sxs-lookup"><span data-stu-id="e8ba8-119">OUTPUTS</span></span>

### <span data-ttu-id="e8ba8-120">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="e8ba8-120">System.Boolean</span></span>

## <span data-ttu-id="e8ba8-121">상속자</span><span class="sxs-lookup"><span data-stu-id="e8ba8-121">NOTES</span></span>

## <span data-ttu-id="e8ba8-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e8ba8-122">RELATED LINKS</span></span>
