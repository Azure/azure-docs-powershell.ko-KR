---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 674A11E4-36B9-4075-9F4E-952BD9FF07A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleWebhook.md
ms.openlocfilehash: 8b94ad5728e7852bb3cd834e7479a29cc11c1698
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532824"
---
# <span data-ttu-id="e9406-101">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="e9406-101">New-AzureRmAutoscaleWebhook</span></span>

## <span data-ttu-id="e9406-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9406-102">SYNOPSIS</span></span>
<span data-ttu-id="e9406-103">자동 크기 조정 webhook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e9406-103">Creates an Autoscale webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9406-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e9406-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9406-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e9406-105">DESCRIPTION</span></span>
<span data-ttu-id="e9406-106">**AzureRmAutoscaleWebhook** Cmdlet은 자동 크기 조정 webhook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e9406-106">The **New-AzureRmAutoscaleWebhook** cmdlet creates an Autoscale webhook.</span></span>

## <span data-ttu-id="e9406-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e9406-107">EXAMPLES</span></span>

## <span data-ttu-id="e9406-108">변수</span><span class="sxs-lookup"><span data-stu-id="e9406-108">PARAMETERS</span></span>

### <span data-ttu-id="e9406-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9406-109">-DefaultProfile</span></span>
<span data-ttu-id="e9406-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e9406-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9406-111">-속성</span><span class="sxs-lookup"><span data-stu-id="e9406-111">-Property</span></span>
<span data-ttu-id="e9406-112">@ (Property1 = ' value1 ',.... 형식으로 속성 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9406-112">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Properties

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9406-113">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="e9406-113">-ServiceUri</span></span>
<span data-ttu-id="e9406-114">서비스 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9406-114">Specifies the service URI.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9406-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9406-115">CommonParameters</span></span>
<span data-ttu-id="e9406-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9406-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9406-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9406-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9406-118">입력</span><span class="sxs-lookup"><span data-stu-id="e9406-118">INPUTS</span></span>

### <span data-ttu-id="e9406-119">않아야</span><span class="sxs-lookup"><span data-stu-id="e9406-119">None</span></span>
<span data-ttu-id="e9406-120">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e9406-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e9406-121">출력</span><span class="sxs-lookup"><span data-stu-id="e9406-121">OUTPUTS</span></span>

### <span data-ttu-id="e9406-122">WebhookNotification를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9406-122">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification</span></span>

## <span data-ttu-id="e9406-123">상속자</span><span class="sxs-lookup"><span data-stu-id="e9406-123">NOTES</span></span>

## <span data-ttu-id="e9406-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e9406-124">RELATED LINKS</span></span>

[<span data-ttu-id="e9406-125">새로운 AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="e9406-125">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


