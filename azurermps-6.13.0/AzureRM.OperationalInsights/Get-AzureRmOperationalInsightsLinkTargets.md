---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 35C6E85B-E5E1-44E8-86E8-F18E197F69DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightslinktargets
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsLinkTargets.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsLinkTargets.md
ms.openlocfilehash: a1040e5fe810a5dfbbb2e41daf7e8933102e3799
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528473"
---
# <span data-ttu-id="5c275-101">Get-AzureRmOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="5c275-101">Get-AzureRmOperationalInsightsLinkTargets</span></span>

## <span data-ttu-id="5c275-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c275-102">SYNOPSIS</span></span>
<span data-ttu-id="5c275-103">구독과 연결 되지 않은 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5c275-103">Gets accounts that are not associated with a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c275-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5c275-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsLinkTargets [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c275-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5c275-105">DESCRIPTION</span></span>
<span data-ttu-id="5c275-106">**AzureRmOperationalInsightsLinkTargets** cmdlet에는 Azure 구독과 연결 되지 않은 기존 계정이 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5c275-106">The **Get-AzureRmOperationalInsightsLinkTargets** cmdlet lists existing accounts that are not associated with an Azure subscription.</span></span>
<span data-ttu-id="5c275-107">새 작업 영역을 기존 계정에 연결 하려면 새 작업 영역의 고객 ID 속성에서이 작업으로 반환 되는 고객 ID를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c275-107">To link a new workspace to an existing account, use a customer ID returned by this operation in the customer ID property of a new workspace.</span></span>

## <span data-ttu-id="5c275-108">예제의</span><span class="sxs-lookup"><span data-stu-id="5c275-108">EXAMPLES</span></span>

### <span data-ttu-id="5c275-109">예제 1: 연결 되지 않은 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="5c275-109">Example 1: Get unlinked accounts</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsLinkTargets
```

<span data-ttu-id="5c275-110">이 명령은 호출자의 ID가 소유 하는 연결 되지 않은 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5c275-110">This command gets unlinked accounts that are owned by the caller's ID.</span></span>

## <span data-ttu-id="5c275-111">변수</span><span class="sxs-lookup"><span data-stu-id="5c275-111">PARAMETERS</span></span>

### <span data-ttu-id="5c275-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c275-112">-DefaultProfile</span></span>
<span data-ttu-id="5c275-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5c275-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c275-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c275-114">CommonParameters</span></span>
<span data-ttu-id="5c275-115">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c275-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c275-116">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c275-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c275-117">입력</span><span class="sxs-lookup"><span data-stu-id="5c275-117">INPUTS</span></span>

### <span data-ttu-id="5c275-118">않아야</span><span class="sxs-lookup"><span data-stu-id="5c275-118">None</span></span>

## <span data-ttu-id="5c275-119">출력</span><span class="sxs-lookup"><span data-stu-id="5c275-119">OUTPUTS</span></span>

### <span data-ttu-id="5c275-120">OperationalInsights 계정이 있는 경우.</span><span class="sxs-lookup"><span data-stu-id="5c275-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSAccount</span></span>

## <span data-ttu-id="5c275-121">상속자</span><span class="sxs-lookup"><span data-stu-id="5c275-121">NOTES</span></span>

## <span data-ttu-id="5c275-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5c275-122">RELATED LINKS</span></span>

[<span data-ttu-id="5c275-123">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5c275-123">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


