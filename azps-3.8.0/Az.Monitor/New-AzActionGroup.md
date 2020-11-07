---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroup.md
ms.openlocfilehash: 0f5112929e36edcac0ca45103ed8c02583be1eb3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879726"
---
# <span data-ttu-id="3c0ca-101">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="3c0ca-101">New-AzActionGroup</span></span>

## <span data-ttu-id="3c0ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c0ca-102">SYNOPSIS</span></span>
<span data-ttu-id="3c0ca-103">메모리에 ActionGroup reference 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3c0ca-103">Creates an ActionGroup reference object in memory.</span></span>

## <span data-ttu-id="3c0ca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3c0ca-104">SYNTAX</span></span>

```
New-AzActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c0ca-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3c0ca-105">DESCRIPTION</span></span>
<span data-ttu-id="3c0ca-106">**AzActionGroup** cmdlet은 메모리에 작업 그룹 참조 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3c0ca-106">The **New-AzActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="3c0ca-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3c0ca-107">EXAMPLES</span></span>

### <span data-ttu-id="3c0ca-108">예제 1: 메모리에 작업 그룹 참조 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="3c0ca-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperty $dict
```

## <span data-ttu-id="3c0ca-109">변수</span><span class="sxs-lookup"><span data-stu-id="3c0ca-109">PARAMETERS</span></span>

### <span data-ttu-id="3c0ca-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="3c0ca-110">-ActionGroupId</span></span>
<span data-ttu-id="3c0ca-111">작업 그룹의 Id/이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3c0ca-111">The Id/name of the action group.</span></span>

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

### <span data-ttu-id="3c0ca-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c0ca-112">-DefaultProfile</span></span>
<span data-ttu-id="3c0ca-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3c0ca-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3c0ca-114">-WebhookProperty</span><span class="sxs-lookup"><span data-stu-id="3c0ca-114">-WebhookProperty</span></span>
<span data-ttu-id="3c0ca-115">작업 그룹의 webhook 속성</span><span class="sxs-lookup"><span data-stu-id="3c0ca-115">The webhook properties of the action group</span></span>

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

### <span data-ttu-id="3c0ca-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c0ca-116">CommonParameters</span></span>
<span data-ttu-id="3c0ca-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c0ca-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c0ca-118">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3c0ca-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c0ca-119">입력</span><span class="sxs-lookup"><span data-stu-id="3c0ca-119">INPUTS</span></span>

### <span data-ttu-id="3c0ca-120">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3c0ca-120">System.String</span></span>

### <span data-ttu-id="3c0ca-121">System.webserver. Dictionary ' 2 [[4.0.0.0], CoreLib, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e], [System.webserver,, CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3c0ca-121">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="3c0ca-122">출력</span><span class="sxs-lookup"><span data-stu-id="3c0ca-122">OUTPUTS</span></span>

### <span data-ttu-id="3c0ca-123">Microsoft. 관리. 관리자. ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="3c0ca-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="3c0ca-124">상속자</span><span class="sxs-lookup"><span data-stu-id="3c0ca-124">NOTES</span></span>

## <span data-ttu-id="3c0ca-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3c0ca-125">RELATED LINKS</span></span>

[<span data-ttu-id="3c0ca-126">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3c0ca-126">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="3c0ca-127">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3c0ca-127">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="3c0ca-128">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3c0ca-128">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="3c0ca-129">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3c0ca-129">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="3c0ca-130">제거-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3c0ca-130">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="3c0ca-131">새로운 AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="3c0ca-131">New-AzActivityLogAlertCondition</span></span>](./Get-AzActivityLogAlertCondition.md)

