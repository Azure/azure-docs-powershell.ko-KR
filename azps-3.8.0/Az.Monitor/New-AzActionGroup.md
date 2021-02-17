---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroup.md
ms.openlocfilehash: 5b4b71f3d108d78a15a5993556ab4e78f480170e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100409157"
---
# <span data-ttu-id="eaefa-101">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="eaefa-101">New-AzActionGroup</span></span>

## <span data-ttu-id="eaefa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eaefa-102">SYNOPSIS</span></span>
<span data-ttu-id="eaefa-103">메모리에 ActionGroup 참조 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eaefa-103">Creates an ActionGroup reference object in memory.</span></span>

## <span data-ttu-id="eaefa-104">구문</span><span class="sxs-lookup"><span data-stu-id="eaefa-104">SYNTAX</span></span>

```
New-AzActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eaefa-105">설명</span><span class="sxs-lookup"><span data-stu-id="eaefa-105">DESCRIPTION</span></span>
<span data-ttu-id="eaefa-106">**New-AzActionGroup** cmdlet은 메모리에 작업 그룹 참조 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eaefa-106">The **New-AzActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="eaefa-107">예제</span><span class="sxs-lookup"><span data-stu-id="eaefa-107">EXAMPLES</span></span>

### <span data-ttu-id="eaefa-108">예제 1: 메모리에 작업 그룹 참조 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="eaefa-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperty $dict
```

## <span data-ttu-id="eaefa-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eaefa-109">PARAMETERS</span></span>

### <span data-ttu-id="eaefa-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="eaefa-110">-ActionGroupId</span></span>
<span data-ttu-id="eaefa-111">작업 그룹의 ID/이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eaefa-111">The Id/name of the action group.</span></span>

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

### <span data-ttu-id="eaefa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaefa-112">-DefaultProfile</span></span>
<span data-ttu-id="eaefa-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="eaefa-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eaefa-114">-WebhookProperty</span><span class="sxs-lookup"><span data-stu-id="eaefa-114">-WebhookProperty</span></span>
<span data-ttu-id="eaefa-115">작업 그룹의 웹후크 속성</span><span class="sxs-lookup"><span data-stu-id="eaefa-115">The webhook properties of the action group</span></span>

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

### <span data-ttu-id="eaefa-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaefa-116">CommonParameters</span></span>
<span data-ttu-id="eaefa-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="eaefa-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaefa-118">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="eaefa-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaefa-119">입력</span><span class="sxs-lookup"><span data-stu-id="eaefa-119">INPUTS</span></span>

### <span data-ttu-id="eaefa-120">System.String</span><span class="sxs-lookup"><span data-stu-id="eaefa-120">System.String</span></span>

### <span data-ttu-id="eaefa-121">System.Collections.Generic.Dictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="eaefa-121">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="eaefa-122">출력</span><span class="sxs-lookup"><span data-stu-id="eaefa-122">OUTPUTS</span></span>

### <span data-ttu-id="eaefa-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="eaefa-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="eaefa-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="eaefa-124">NOTES</span></span>

## <span data-ttu-id="eaefa-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eaefa-125">RELATED LINKS</span></span>

[<span data-ttu-id="eaefa-126">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="eaefa-126">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="eaefa-127">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="eaefa-127">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="eaefa-128">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="eaefa-128">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="eaefa-129">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="eaefa-129">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="eaefa-130">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="eaefa-130">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)



