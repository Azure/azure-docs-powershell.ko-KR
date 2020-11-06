---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 556A9F12-DF72-468F-9C3F-A747CC70BD2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermdnsavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmDnsAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmDnsAvailability.md
ms.openlocfilehash: 348fd7e97566520b27163de91d4d52162d4c3978
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531374"
---
# <span data-ttu-id="3f4fa-101">Test-AzureRmDnsAvailability</span><span class="sxs-lookup"><span data-stu-id="3f4fa-101">Test-AzureRmDnsAvailability</span></span>

## <span data-ttu-id="3f4fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f4fa-102">SYNOPSIS</span></span>
<span data-ttu-id="3f4fa-103">Cloudapp.azure.com zone의 도메인 이름을 사용할 수 있는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f4fa-103">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f4fa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3f4fa-104">SYNTAX</span></span>

```
Test-AzureRmDnsAvailability -DomainNameLabel <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f4fa-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3f4fa-105">DESCRIPTION</span></span>
<span data-ttu-id="3f4fa-106">Cloudapp.azure.com zone의 도메인 이름을 사용할 수 있는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f4fa-106">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="3f4fa-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3f4fa-107">EXAMPLES</span></span>

### <span data-ttu-id="3f4fa-108">예제 1: contoso.cloudapp.azure.com을 사용할 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f4fa-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzureRmDnsAvailability -DomainNameLabel contoso -Location westus
```

## <span data-ttu-id="3f4fa-109">변수</span><span class="sxs-lookup"><span data-stu-id="3f4fa-109">PARAMETERS</span></span>

### <span data-ttu-id="3f4fa-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f4fa-110">-DefaultProfile</span></span>
<span data-ttu-id="3f4fa-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3f4fa-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f4fa-112">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="3f4fa-112">-DomainNameLabel</span></span>
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

### <span data-ttu-id="3f4fa-113">-위치</span><span class="sxs-lookup"><span data-stu-id="3f4fa-113">-Location</span></span>
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

### <span data-ttu-id="3f4fa-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f4fa-114">CommonParameters</span></span>
<span data-ttu-id="3f4fa-115">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f4fa-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f4fa-116">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f4fa-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f4fa-117">입력</span><span class="sxs-lookup"><span data-stu-id="3f4fa-117">INPUTS</span></span>

### <span data-ttu-id="3f4fa-118">않아야</span><span class="sxs-lookup"><span data-stu-id="3f4fa-118">None</span></span>

## <span data-ttu-id="3f4fa-119">출력</span><span class="sxs-lookup"><span data-stu-id="3f4fa-119">OUTPUTS</span></span>

### <span data-ttu-id="3f4fa-120">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="3f4fa-120">System.Boolean</span></span>

## <span data-ttu-id="3f4fa-121">상속자</span><span class="sxs-lookup"><span data-stu-id="3f4fa-121">NOTES</span></span>

## <span data-ttu-id="3f4fa-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3f4fa-122">RELATED LINKS</span></span>
