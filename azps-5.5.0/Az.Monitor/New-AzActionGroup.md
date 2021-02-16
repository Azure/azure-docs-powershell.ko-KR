---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroup.md
ms.openlocfilehash: 99fb63a5dd4ba60b44e96139418a76701334444e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184953"
---
# <span data-ttu-id="acdfd-101">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="acdfd-101">New-AzActionGroup</span></span>

## <span data-ttu-id="acdfd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acdfd-102">SYNOPSIS</span></span>
<span data-ttu-id="acdfd-103">메모리에 ActionGroup 참조 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="acdfd-103">Creates an ActionGroup reference object in memory.</span></span>

## <span data-ttu-id="acdfd-104">구문</span><span class="sxs-lookup"><span data-stu-id="acdfd-104">SYNTAX</span></span>

```
New-AzActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acdfd-105">설명</span><span class="sxs-lookup"><span data-stu-id="acdfd-105">DESCRIPTION</span></span>
<span data-ttu-id="acdfd-106">**New-AzActionGroup** cmdlet은 메모리에 작업 그룹 참조 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="acdfd-106">The **New-AzActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="acdfd-107">예제</span><span class="sxs-lookup"><span data-stu-id="acdfd-107">EXAMPLES</span></span>

### <span data-ttu-id="acdfd-108">예제 1: 메모리에 작업 그룹 참조 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="acdfd-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperty $dict
```

## <span data-ttu-id="acdfd-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="acdfd-109">PARAMETERS</span></span>

### <span data-ttu-id="acdfd-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="acdfd-110">-ActionGroupId</span></span>
<span data-ttu-id="acdfd-111">작업 그룹의 ID/이름입니다.</span><span class="sxs-lookup"><span data-stu-id="acdfd-111">The Id/name of the action group.</span></span>

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

### <span data-ttu-id="acdfd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acdfd-112">-DefaultProfile</span></span>
<span data-ttu-id="acdfd-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="acdfd-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="acdfd-114">-WebhookProperty</span><span class="sxs-lookup"><span data-stu-id="acdfd-114">-WebhookProperty</span></span>
<span data-ttu-id="acdfd-115">작업 그룹의 웹후크 속성</span><span class="sxs-lookup"><span data-stu-id="acdfd-115">The webhook properties of the action group</span></span>

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

### <span data-ttu-id="acdfd-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acdfd-116">CommonParameters</span></span>
<span data-ttu-id="acdfd-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="acdfd-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acdfd-118">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="acdfd-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acdfd-119">입력</span><span class="sxs-lookup"><span data-stu-id="acdfd-119">INPUTS</span></span>

### <span data-ttu-id="acdfd-120">System.String</span><span class="sxs-lookup"><span data-stu-id="acdfd-120">System.String</span></span>

### <span data-ttu-id="acdfd-121">System.Collections.Generic.Dictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="acdfd-121">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="acdfd-122">출력</span><span class="sxs-lookup"><span data-stu-id="acdfd-122">OUTPUTS</span></span>

### <span data-ttu-id="acdfd-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="acdfd-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="acdfd-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="acdfd-124">NOTES</span></span>

## <span data-ttu-id="acdfd-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="acdfd-125">RELATED LINKS</span></span>

[<span data-ttu-id="acdfd-126">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="acdfd-126">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="acdfd-127">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="acdfd-127">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="acdfd-128">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="acdfd-128">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="acdfd-129">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="acdfd-129">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="acdfd-130">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="acdfd-130">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="acdfd-131">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="acdfd-131">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)

