---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleaznsactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
ms.openlocfilehash: 44f9eae56c822e5fe068679331bcdd3a0ad17d81
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184924"
---
# <span data-ttu-id="f80b8-101">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="f80b8-101">New-AzScheduledQueryRuleAznsActionGroup</span></span>

## <span data-ttu-id="f80b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f80b8-102">SYNOPSIS</span></span>
<span data-ttu-id="f80b8-103">Azns 작업 그룹 형식의 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f80b8-103">Creates an object of type Azns Action Group</span></span>

## <span data-ttu-id="f80b8-104">구문</span><span class="sxs-lookup"><span data-stu-id="f80b8-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAznsActionGroup [-ActionGroup <String[]>] [-EmailSubject <String>]
 [-CustomWebhookPayload <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f80b8-105">설명</span><span class="sxs-lookup"><span data-stu-id="f80b8-105">DESCRIPTION</span></span>
<span data-ttu-id="f80b8-106">Azns 작업 그룹의 형식 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f80b8-106">Creates an object of type Azns Action Group.</span></span>
<span data-ttu-id="f80b8-107">이 개체는 로그 경고 규칙을 만드는 명령에 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="f80b8-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="f80b8-108">예제</span><span class="sxs-lookup"><span data-stu-id="f80b8-108">EXAMPLES</span></span>

### <span data-ttu-id="f80b8-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="f80b8-109">Example 1</span></span>
```powershell
PS C:\> $aznsActionGroup = New-AzScheduledQueryRuleAznsActionGroup -ActionGroup @("/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourcegroups/MyResourceGroup/providers/microsoft.insights/actiongroups/MyActionGroup") -EmailSubject "Email subject" -CustomWebhookPayload "{}"
```

## <span data-ttu-id="f80b8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f80b8-110">PARAMETERS</span></span>

### <span data-ttu-id="f80b8-111">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="f80b8-111">-ActionGroup</span></span>
<span data-ttu-id="f80b8-112">알림을 보낼 작업 그룹 목록</span><span class="sxs-lookup"><span data-stu-id="f80b8-112">The list of action groups to send notification to</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f80b8-113">-CustomWebhookPayload</span><span class="sxs-lookup"><span data-stu-id="f80b8-113">-CustomWebhookPayload</span></span>
<span data-ttu-id="f80b8-114">사용자 지정된 웹후크 페이로드</span><span class="sxs-lookup"><span data-stu-id="f80b8-114">The customized webhook payload</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f80b8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f80b8-115">-DefaultProfile</span></span>
<span data-ttu-id="f80b8-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f80b8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f80b8-117">-EmailSubject</span><span class="sxs-lookup"><span data-stu-id="f80b8-117">-EmailSubject</span></span>
<span data-ttu-id="f80b8-118">경고 알림의 이메일 제목</span><span class="sxs-lookup"><span data-stu-id="f80b8-118">The email subject of alert notification</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f80b8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f80b8-119">CommonParameters</span></span>
<span data-ttu-id="f80b8-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f80b8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f80b8-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f80b8-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f80b8-122">입력</span><span class="sxs-lookup"><span data-stu-id="f80b8-122">INPUTS</span></span>

### <span data-ttu-id="f80b8-123">없음</span><span class="sxs-lookup"><span data-stu-id="f80b8-123">None</span></span>

## <span data-ttu-id="f80b8-124">출력</span><span class="sxs-lookup"><span data-stu-id="f80b8-124">OUTPUTS</span></span>

### <span data-ttu-id="f80b8-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction</span><span class="sxs-lookup"><span data-stu-id="f80b8-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction</span></span>

## <span data-ttu-id="f80b8-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f80b8-126">NOTES</span></span>

## <span data-ttu-id="f80b8-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f80b8-127">RELATED LINKS</span></span>
