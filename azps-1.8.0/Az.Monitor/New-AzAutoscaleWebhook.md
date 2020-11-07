---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 674A11E4-36B9-4075-9F4E-952BD9FF07A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleWebhook.md
ms.openlocfilehash: de63737d72e1b7d6030448668445e6fdec9d460a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867261"
---
# <span data-ttu-id="622c4-101">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="622c4-101">New-AzAutoscaleWebhook</span></span>

## <span data-ttu-id="622c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="622c4-102">SYNOPSIS</span></span>
<span data-ttu-id="622c4-103">자동 크기 조정 webhook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="622c4-103">Creates an Autoscale webhook.</span></span>

## <span data-ttu-id="622c4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="622c4-104">SYNTAX</span></span>

```
New-AzAutoscaleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="622c4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="622c4-105">DESCRIPTION</span></span>
<span data-ttu-id="622c4-106">**AzAutoscaleWebhook** Cmdlet은 자동 크기 조정 webhook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="622c4-106">The **New-AzAutoscaleWebhook** cmdlet creates an Autoscale webhook.</span></span>

## <span data-ttu-id="622c4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="622c4-107">EXAMPLES</span></span>

## <span data-ttu-id="622c4-108">변수</span><span class="sxs-lookup"><span data-stu-id="622c4-108">PARAMETERS</span></span>

### <span data-ttu-id="622c4-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="622c4-109">-DefaultProfile</span></span>
<span data-ttu-id="622c4-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="622c4-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="622c4-111">-속성</span><span class="sxs-lookup"><span data-stu-id="622c4-111">-Property</span></span>
<span data-ttu-id="622c4-112">@ (Property1 = ' value1 ',.... 형식으로 속성 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="622c4-112">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="622c4-113">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="622c4-113">-ServiceUri</span></span>
<span data-ttu-id="622c4-114">서비스 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="622c4-114">Specifies the service URI.</span></span>

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

### <span data-ttu-id="622c4-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="622c4-115">CommonParameters</span></span>
<span data-ttu-id="622c4-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="622c4-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="622c4-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="622c4-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="622c4-118">입력</span><span class="sxs-lookup"><span data-stu-id="622c4-118">INPUTS</span></span>

### <span data-ttu-id="622c4-119">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="622c4-119">System.String</span></span>

### <span data-ttu-id="622c4-120">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="622c4-120">System.Collections.Hashtable</span></span>

## <span data-ttu-id="622c4-121">출력</span><span class="sxs-lookup"><span data-stu-id="622c4-121">OUTPUTS</span></span>

### <span data-ttu-id="622c4-122">WebhookNotification를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="622c4-122">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification</span></span>

## <span data-ttu-id="622c4-123">상속자</span><span class="sxs-lookup"><span data-stu-id="622c4-123">NOTES</span></span>

## <span data-ttu-id="622c4-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="622c4-124">RELATED LINKS</span></span>

[<span data-ttu-id="622c4-125">새로운 AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="622c4-125">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


