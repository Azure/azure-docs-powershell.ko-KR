---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroup.md
ms.openlocfilehash: d4afe709d70872c1d7fb59e99f2f98d3dfe19d6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703375"
---
# <span data-ttu-id="4765c-101">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="4765c-101">New-AzureRmActionGroup</span></span>

## <span data-ttu-id="4765c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4765c-102">SYNOPSIS</span></span>
<span data-ttu-id="4765c-103">메모리에 ActionGroup reference 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4765c-103">Creates an ActionGroup reference object in memory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4765c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4765c-104">SYNTAX</span></span>

```
New-AzureRmActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4765c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4765c-105">DESCRIPTION</span></span>
<span data-ttu-id="4765c-106">**AzureRmActionGroup** cmdlet은 메모리에 작업 그룹 참조 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4765c-106">The **New-AzureRmActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="4765c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4765c-107">EXAMPLES</span></span>

### <span data-ttu-id="4765c-108">예제 1: 메모리에 작업 그룹 참조 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="4765c-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
```

## <span data-ttu-id="4765c-109">변수</span><span class="sxs-lookup"><span data-stu-id="4765c-109">PARAMETERS</span></span>

### <span data-ttu-id="4765c-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="4765c-110">-ActionGroupId</span></span>
<span data-ttu-id="4765c-111">작업 그룹의 Id/이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4765c-111">The Id/name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4765c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4765c-112">-DefaultProfile</span></span>
<span data-ttu-id="4765c-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4765c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4765c-114">-WebhookProperty</span><span class="sxs-lookup"><span data-stu-id="4765c-114">-WebhookProperty</span></span>
<span data-ttu-id="4765c-115">작업 그룹의 webhook 속성</span><span class="sxs-lookup"><span data-stu-id="4765c-115">The webhook properties of the action group</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4765c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4765c-116">CommonParameters</span></span>
<span data-ttu-id="4765c-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4765c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4765c-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4765c-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4765c-119">입력</span><span class="sxs-lookup"><span data-stu-id="4765c-119">INPUTS</span></span>

## <span data-ttu-id="4765c-120">출력</span><span class="sxs-lookup"><span data-stu-id="4765c-120">OUTPUTS</span></span>

### <span data-ttu-id="4765c-121">Microsoft. 관리. 관리자. ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="4765c-121">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="4765c-122">상속자</span><span class="sxs-lookup"><span data-stu-id="4765c-122">NOTES</span></span>

## <span data-ttu-id="4765c-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4765c-123">RELATED LINKS</span></span>

[<span data-ttu-id="4765c-124">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4765c-124">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="4765c-125">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4765c-125">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="4765c-126">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4765c-126">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="4765c-127">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4765c-127">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="4765c-128">제거-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4765c-128">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="4765c-129">새로운 AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="4765c-129">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

