---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 556A9F12-DF72-468F-9C3F-A747CC70BD2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azdnsavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
ms.openlocfilehash: 2ee468c47f22e90ce47b003dcae1becfb905134e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495079"
---
# <span data-ttu-id="43a04-101">Test-AzDnsAvailability</span><span class="sxs-lookup"><span data-stu-id="43a04-101">Test-AzDnsAvailability</span></span>

## <span data-ttu-id="43a04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43a04-102">SYNOPSIS</span></span>
<span data-ttu-id="43a04-103">cloudapp.azure.com 영역의 도메인 이름을 사용할 수 있는지 여부를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="43a04-103">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="43a04-104">구문</span><span class="sxs-lookup"><span data-stu-id="43a04-104">SYNTAX</span></span>

```
Test-AzDnsAvailability -DomainNameLabel <String> -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="43a04-105">설명</span><span class="sxs-lookup"><span data-stu-id="43a04-105">DESCRIPTION</span></span>
<span data-ttu-id="43a04-106">cloudapp.azure.com 영역의 도메인 이름을 사용할 수 있는지 여부를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="43a04-106">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="43a04-107">예제</span><span class="sxs-lookup"><span data-stu-id="43a04-107">EXAMPLES</span></span>

### <span data-ttu-id="43a04-108">예제 1: contoso.westus.cloudapp.azure.com 사용할 수 있는지 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="43a04-108">Example 1: Check if contoso.westus.cloudapp.azure.com is available for use.</span></span>
```
Test-AzDnsAvailability -DomainNameLabel contoso -Location westus
```

## <span data-ttu-id="43a04-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43a04-109">PARAMETERS</span></span>

### <span data-ttu-id="43a04-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43a04-110">-DefaultProfile</span></span>
<span data-ttu-id="43a04-111">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="43a04-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43a04-112">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="43a04-112">-DomainNameLabel</span></span>
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

### <span data-ttu-id="43a04-113">-Location</span><span class="sxs-lookup"><span data-stu-id="43a04-113">-Location</span></span>
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

### <span data-ttu-id="43a04-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43a04-114">CommonParameters</span></span>
<span data-ttu-id="43a04-115">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="43a04-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43a04-116">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="43a04-116">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43a04-117">입력</span><span class="sxs-lookup"><span data-stu-id="43a04-117">INPUTS</span></span>

### <span data-ttu-id="43a04-118">없음</span><span class="sxs-lookup"><span data-stu-id="43a04-118">None</span></span>

## <span data-ttu-id="43a04-119">출력</span><span class="sxs-lookup"><span data-stu-id="43a04-119">OUTPUTS</span></span>

### <span data-ttu-id="43a04-120">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="43a04-120">System.Boolean</span></span>

## <span data-ttu-id="43a04-121">참고 사항</span><span class="sxs-lookup"><span data-stu-id="43a04-121">NOTES</span></span>

## <span data-ttu-id="43a04-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="43a04-122">RELATED LINKS</span></span>
