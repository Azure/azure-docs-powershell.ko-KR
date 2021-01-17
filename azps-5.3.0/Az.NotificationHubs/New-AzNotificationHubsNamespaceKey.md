---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1EC19069-B64C-4F0F-99A3-07C16E46C0A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespacekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceKey.md
ms.openlocfilehash: a575ae0151cd28a9bcc3580a77ad3a0c79a2984b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491740"
---
# <span data-ttu-id="6e37d-101">New-AzNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="6e37d-101">New-AzNotificationHubsNamespaceKey</span></span>

## <span data-ttu-id="6e37d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e37d-102">SYNOPSIS</span></span>
<span data-ttu-id="6e37d-103">네임스페이스에 대한 권한 부여 규칙 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="6e37d-103">Regenerate the Authorization Rule Key for a Namespace.</span></span>

## <span data-ttu-id="6e37d-104">구문</span><span class="sxs-lookup"><span data-stu-id="6e37d-104">SYNTAX</span></span>

```
New-AzNotificationHubsNamespaceKey [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e37d-105">설명</span><span class="sxs-lookup"><span data-stu-id="6e37d-105">DESCRIPTION</span></span>
<span data-ttu-id="6e37d-106">New-AzNotificationHubNamespaceKey cmdlet은 네임스페이스 권한 부여 규칙에 대한 기본 키/보조 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="6e37d-106">New-AzNotificationHubNamespaceKey cmdlet regenerates the Primary Key/Secondary Key for the Namespace Authorization Rule.</span></span>

## <span data-ttu-id="6e37d-107">예제</span><span class="sxs-lookup"><span data-stu-id="6e37d-107">EXAMPLES</span></span>

### <span data-ttu-id="6e37d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="6e37d-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="6e37d-109">{{ 여기에 예제 설명 추가 }}</span><span class="sxs-lookup"><span data-stu-id="6e37d-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="6e37d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e37d-110">PARAMETERS</span></span>

### <span data-ttu-id="6e37d-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6e37d-111">-AuthorizationRule</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e37d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e37d-112">-DefaultProfile</span></span>
<span data-ttu-id="6e37d-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6e37d-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e37d-114">-Force</span><span class="sxs-lookup"><span data-stu-id="6e37d-114">-Force</span></span>
<span data-ttu-id="6e37d-115">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e37d-115">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e37d-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6e37d-116">-Namespace</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e37d-117">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="6e37d-117">-PolicyKey</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e37d-118">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6e37d-118">-ResourceGroup</span></span>
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

### <span data-ttu-id="6e37d-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e37d-119">-Confirm</span></span>
<span data-ttu-id="6e37d-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e37d-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e37d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e37d-121">-WhatIf</span></span>
<span data-ttu-id="6e37d-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6e37d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e37d-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e37d-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e37d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e37d-124">CommonParameters</span></span>
<span data-ttu-id="6e37d-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6e37d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e37d-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6e37d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e37d-127">입력</span><span class="sxs-lookup"><span data-stu-id="6e37d-127">INPUTS</span></span>

### <span data-ttu-id="6e37d-128">System.String</span><span class="sxs-lookup"><span data-stu-id="6e37d-128">System.String</span></span>

## <span data-ttu-id="6e37d-129">출력</span><span class="sxs-lookup"><span data-stu-id="6e37d-129">OUTPUTS</span></span>

### <span data-ttu-id="6e37d-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="6e37d-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="6e37d-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6e37d-131">NOTES</span></span>

## <span data-ttu-id="6e37d-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6e37d-132">RELATED LINKS</span></span>
