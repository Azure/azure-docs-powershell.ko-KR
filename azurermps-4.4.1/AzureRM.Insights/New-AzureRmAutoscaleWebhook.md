---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 674A11E4-36B9-4075-9F4E-952BD9FF07A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleWebhook.md
ms.openlocfilehash: 2fc67e4f50d3c0a045ed6f0e6d82d5bf46d10c25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533076"
---
# <span data-ttu-id="6cf09-101">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="6cf09-101">New-AzureRmAutoscaleWebhook</span></span>

## <span data-ttu-id="6cf09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cf09-102">SYNOPSIS</span></span>
<span data-ttu-id="6cf09-103">자동 크기 조정 webhook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6cf09-103">Creates an Autoscale webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6cf09-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6cf09-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleWebhook [-ServiceUri] <String> [[-Properties] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cf09-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6cf09-105">DESCRIPTION</span></span>
<span data-ttu-id="6cf09-106">**AzureRmAutoscaleWebhook** Cmdlet은 자동 크기 조정 webhook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6cf09-106">The **New-AzureRmAutoscaleWebhook** cmdlet creates an Autoscale webhook.</span></span>

## <span data-ttu-id="6cf09-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6cf09-107">EXAMPLES</span></span>

## <span data-ttu-id="6cf09-108">변수</span><span class="sxs-lookup"><span data-stu-id="6cf09-108">PARAMETERS</span></span>

### <span data-ttu-id="6cf09-109">-속성</span><span class="sxs-lookup"><span data-stu-id="6cf09-109">-Properties</span></span>
<span data-ttu-id="6cf09-110">@ (Property1 = ' value1 ',.... 형식으로 속성 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cf09-110">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cf09-111">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="6cf09-111">-ServiceUri</span></span>
<span data-ttu-id="6cf09-112">서비스 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cf09-112">Specifies the service URI.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cf09-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cf09-113">-DefaultProfile</span></span>
<span data-ttu-id="6cf09-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6cf09-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cf09-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cf09-115">CommonParameters</span></span>
<span data-ttu-id="6cf09-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cf09-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cf09-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cf09-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cf09-118">입력</span><span class="sxs-lookup"><span data-stu-id="6cf09-118">INPUTS</span></span>

## <span data-ttu-id="6cf09-119">출력</span><span class="sxs-lookup"><span data-stu-id="6cf09-119">OUTPUTS</span></span>

### <span data-ttu-id="6cf09-120">WebhookNotification를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cf09-120">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification</span></span>

## <span data-ttu-id="6cf09-121">상속자</span><span class="sxs-lookup"><span data-stu-id="6cf09-121">NOTES</span></span>

## <span data-ttu-id="6cf09-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6cf09-122">RELATED LINKS</span></span>

[<span data-ttu-id="6cf09-123">새로운 AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="6cf09-123">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


