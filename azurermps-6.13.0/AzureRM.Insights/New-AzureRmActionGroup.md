---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroup.md
ms.openlocfilehash: b6782eccb7a27204cffe91d8cb858b23f8e94f5c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536648"
---
# <span data-ttu-id="44c7b-101">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="44c7b-101">New-AzureRmActionGroup</span></span>

## <span data-ttu-id="44c7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44c7b-102">SYNOPSIS</span></span>
<span data-ttu-id="44c7b-103">메모리에 ActionGroup reference 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="44c7b-103">Creates an ActionGroup reference object in memory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44c7b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="44c7b-104">SYNTAX</span></span>

```
New-AzureRmActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44c7b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="44c7b-105">DESCRIPTION</span></span>
<span data-ttu-id="44c7b-106">**AzureRmActionGroup** cmdlet은 메모리에 작업 그룹 참조 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="44c7b-106">The **New-AzureRmActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="44c7b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="44c7b-107">EXAMPLES</span></span>

### <span data-ttu-id="44c7b-108">예제 1: 메모리에 작업 그룹 참조 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="44c7b-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
```

## <span data-ttu-id="44c7b-109">변수</span><span class="sxs-lookup"><span data-stu-id="44c7b-109">PARAMETERS</span></span>

### <span data-ttu-id="44c7b-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="44c7b-110">-ActionGroupId</span></span>
<span data-ttu-id="44c7b-111">작업 그룹의 Id/이름입니다.</span><span class="sxs-lookup"><span data-stu-id="44c7b-111">The Id/name of the action group.</span></span>

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

### <span data-ttu-id="44c7b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44c7b-112">-DefaultProfile</span></span>
<span data-ttu-id="44c7b-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="44c7b-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="44c7b-114">-WebhookProperty</span><span class="sxs-lookup"><span data-stu-id="44c7b-114">-WebhookProperty</span></span>
<span data-ttu-id="44c7b-115">작업 그룹의 webhook 속성</span><span class="sxs-lookup"><span data-stu-id="44c7b-115">The webhook properties of the action group</span></span>

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

### <span data-ttu-id="44c7b-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44c7b-116">CommonParameters</span></span>
<span data-ttu-id="44c7b-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="44c7b-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44c7b-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44c7b-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44c7b-119">입력</span><span class="sxs-lookup"><span data-stu-id="44c7b-119">INPUTS</span></span>

### <span data-ttu-id="44c7b-120">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="44c7b-120">System.String</span></span>

### <span data-ttu-id="44c7b-121">System.webserver ' 2 [[b77a5c561934e089], [시스템 문자열, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =], [System.webserver, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="44c7b-121">System.Collections.Generic.Dictionary\`2[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089],[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="44c7b-122">출력</span><span class="sxs-lookup"><span data-stu-id="44c7b-122">OUTPUTS</span></span>

### <span data-ttu-id="44c7b-123">Microsoft. 관리. 관리자. ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="44c7b-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="44c7b-124">상속자</span><span class="sxs-lookup"><span data-stu-id="44c7b-124">NOTES</span></span>

## <span data-ttu-id="44c7b-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="44c7b-125">RELATED LINKS</span></span>

[<span data-ttu-id="44c7b-126">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="44c7b-126">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="44c7b-127">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="44c7b-127">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="44c7b-128">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="44c7b-128">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="44c7b-129">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="44c7b-129">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="44c7b-130">제거-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="44c7b-130">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="44c7b-131">새로운 AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="44c7b-131">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)
