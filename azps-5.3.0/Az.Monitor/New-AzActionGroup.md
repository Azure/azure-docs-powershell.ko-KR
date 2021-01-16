---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroup.md
ms.openlocfilehash: 99fb63a5dd4ba60b44e96139418a76701334444e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382586"
---
# <span data-ttu-id="25d05-101">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="25d05-101">New-AzActionGroup</span></span>

## <span data-ttu-id="25d05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25d05-102">SYNOPSIS</span></span>
<span data-ttu-id="25d05-103">메모리에 ActionGroup 참조 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="25d05-103">Creates an ActionGroup reference object in memory.</span></span>

## <span data-ttu-id="25d05-104">구문</span><span class="sxs-lookup"><span data-stu-id="25d05-104">SYNTAX</span></span>

```
New-AzActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25d05-105">설명</span><span class="sxs-lookup"><span data-stu-id="25d05-105">DESCRIPTION</span></span>
<span data-ttu-id="25d05-106">**New-AzActionGroup** cmdlet은 메모리에 작업 그룹 참조 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="25d05-106">The **New-AzActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="25d05-107">예제</span><span class="sxs-lookup"><span data-stu-id="25d05-107">EXAMPLES</span></span>

### <span data-ttu-id="25d05-108">예제 1: 메모리에 작업 그룹 참조 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="25d05-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperty $dict
```

## <span data-ttu-id="25d05-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25d05-109">PARAMETERS</span></span>

### <span data-ttu-id="25d05-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="25d05-110">-ActionGroupId</span></span>
<span data-ttu-id="25d05-111">작업 그룹의 ID/이름입니다.</span><span class="sxs-lookup"><span data-stu-id="25d05-111">The Id/name of the action group.</span></span>

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

### <span data-ttu-id="25d05-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25d05-112">-DefaultProfile</span></span>
<span data-ttu-id="25d05-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="25d05-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25d05-114">-WebhookProperty</span><span class="sxs-lookup"><span data-stu-id="25d05-114">-WebhookProperty</span></span>
<span data-ttu-id="25d05-115">작업 그룹의 웹후크 속성</span><span class="sxs-lookup"><span data-stu-id="25d05-115">The webhook properties of the action group</span></span>

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

### <span data-ttu-id="25d05-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25d05-116">CommonParameters</span></span>
<span data-ttu-id="25d05-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="25d05-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25d05-118">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="25d05-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25d05-119">입력</span><span class="sxs-lookup"><span data-stu-id="25d05-119">INPUTS</span></span>

### <span data-ttu-id="25d05-120">System.String</span><span class="sxs-lookup"><span data-stu-id="25d05-120">System.String</span></span>

### <span data-ttu-id="25d05-121">System.Collections.Generic.Dictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="25d05-121">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="25d05-122">출력</span><span class="sxs-lookup"><span data-stu-id="25d05-122">OUTPUTS</span></span>

### <span data-ttu-id="25d05-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="25d05-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="25d05-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="25d05-124">NOTES</span></span>

## <span data-ttu-id="25d05-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="25d05-125">RELATED LINKS</span></span>

[<span data-ttu-id="25d05-126">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="25d05-126">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="25d05-127">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="25d05-127">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="25d05-128">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="25d05-128">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="25d05-129">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="25d05-129">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="25d05-130">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="25d05-130">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="25d05-131">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="25d05-131">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)

