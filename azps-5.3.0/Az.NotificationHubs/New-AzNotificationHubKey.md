---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: A03F32C3-BB01-46A5-86C5-B7A4DDC42351
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
ms.openlocfilehash: 071f5a7b28b6b6b49e965cc118a4a863cbd0142b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491748"
---
# <span data-ttu-id="cdc68-101">New-AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="cdc68-101">New-AzNotificationHubKey</span></span>

## <span data-ttu-id="cdc68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdc68-102">SYNOPSIS</span></span>
<span data-ttu-id="cdc68-103">NotificationHub에 대한 권한 부여 규칙 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="cdc68-103">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

## <span data-ttu-id="cdc68-104">구문</span><span class="sxs-lookup"><span data-stu-id="cdc68-104">SYNTAX</span></span>

```
New-AzNotificationHubKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdc68-105">설명</span><span class="sxs-lookup"><span data-stu-id="cdc68-105">DESCRIPTION</span></span>
<span data-ttu-id="cdc68-106">New-AzNotificationHubKey cmdlet은 NotificationHub 권한 부여 규칙에 대한 기본 키/보조 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="cdc68-106">New-AzNotificationHubKey cmdlet regenerates the Primary Key/Secondary Key for the NotificationHub Authorization Rule.</span></span>

## <span data-ttu-id="cdc68-107">예제</span><span class="sxs-lookup"><span data-stu-id="cdc68-107">EXAMPLES</span></span>

### <span data-ttu-id="cdc68-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="cdc68-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="cdc68-109">{{ 여기에 예제 설명 추가 }}</span><span class="sxs-lookup"><span data-stu-id="cdc68-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="cdc68-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cdc68-110">PARAMETERS</span></span>

### <span data-ttu-id="cdc68-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cdc68-111">-AuthorizationRule</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdc68-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdc68-112">-DefaultProfile</span></span>
<span data-ttu-id="cdc68-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="cdc68-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cdc68-114">-Force</span><span class="sxs-lookup"><span data-stu-id="cdc68-114">-Force</span></span>
<span data-ttu-id="cdc68-115">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cdc68-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="cdc68-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="cdc68-116">-Namespace</span></span>
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

### <span data-ttu-id="cdc68-117">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="cdc68-117">-NotificationHub</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdc68-118">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="cdc68-118">-PolicyKey</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdc68-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cdc68-119">-ResourceGroup</span></span>
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

### <span data-ttu-id="cdc68-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cdc68-120">-Confirm</span></span>
<span data-ttu-id="cdc68-121">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cdc68-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdc68-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdc68-122">-WhatIf</span></span>
<span data-ttu-id="cdc68-123">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="cdc68-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdc68-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cdc68-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdc68-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdc68-125">CommonParameters</span></span>
<span data-ttu-id="cdc68-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cdc68-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdc68-127">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cdc68-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdc68-128">입력</span><span class="sxs-lookup"><span data-stu-id="cdc68-128">INPUTS</span></span>

### <span data-ttu-id="cdc68-129">System.String</span><span class="sxs-lookup"><span data-stu-id="cdc68-129">System.String</span></span>

## <span data-ttu-id="cdc68-130">출력</span><span class="sxs-lookup"><span data-stu-id="cdc68-130">OUTPUTS</span></span>

### <span data-ttu-id="cdc68-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="cdc68-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="cdc68-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cdc68-132">NOTES</span></span>

## <span data-ttu-id="cdc68-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cdc68-133">RELATED LINKS</span></span>
