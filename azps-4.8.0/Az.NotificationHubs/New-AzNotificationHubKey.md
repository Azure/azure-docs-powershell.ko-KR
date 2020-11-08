---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: A03F32C3-BB01-46A5-86C5-B7A4DDC42351
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
ms.openlocfilehash: 071f5a7b28b6b6b49e965cc118a4a863cbd0142b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214753"
---
# <span data-ttu-id="d885c-101">New-AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="d885c-101">New-AzNotificationHubKey</span></span>

## <span data-ttu-id="d885c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d885c-102">SYNOPSIS</span></span>
<span data-ttu-id="d885c-103">NotificationHub에 대 한 권한 부여 규칙 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d885c-103">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

## <span data-ttu-id="d885c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d885c-104">SYNTAX</span></span>

```
New-AzNotificationHubKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d885c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d885c-105">DESCRIPTION</span></span>
<span data-ttu-id="d885c-106">New-AzNotificationHubKey cmdlet은 NotificationHub 권한 부여 규칙에 대 한 기본 키/보조 키를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d885c-106">New-AzNotificationHubKey cmdlet regenerates the Primary Key/Secondary Key for the NotificationHub Authorization Rule.</span></span>

## <span data-ttu-id="d885c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d885c-107">EXAMPLES</span></span>

### <span data-ttu-id="d885c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d885c-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="d885c-109">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="d885c-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="d885c-110">변수</span><span class="sxs-lookup"><span data-stu-id="d885c-110">PARAMETERS</span></span>

### <span data-ttu-id="d885c-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d885c-111">-AuthorizationRule</span></span>
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

### <span data-ttu-id="d885c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d885c-112">-DefaultProfile</span></span>
<span data-ttu-id="d885c-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d885c-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d885c-114">-Force</span><span class="sxs-lookup"><span data-stu-id="d885c-114">-Force</span></span>
<span data-ttu-id="d885c-115">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d885c-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d885c-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d885c-116">-Namespace</span></span>
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

### <span data-ttu-id="d885c-117">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="d885c-117">-NotificationHub</span></span>
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

### <span data-ttu-id="d885c-118">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="d885c-118">-PolicyKey</span></span>
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

### <span data-ttu-id="d885c-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d885c-119">-ResourceGroup</span></span>
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

### <span data-ttu-id="d885c-120">-확인</span><span class="sxs-lookup"><span data-stu-id="d885c-120">-Confirm</span></span>
<span data-ttu-id="d885c-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d885c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d885c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d885c-122">-WhatIf</span></span>
<span data-ttu-id="d885c-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d885c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d885c-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d885c-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d885c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d885c-125">CommonParameters</span></span>
<span data-ttu-id="d885c-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d885c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d885c-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d885c-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d885c-128">입력</span><span class="sxs-lookup"><span data-stu-id="d885c-128">INPUTS</span></span>

### <span data-ttu-id="d885c-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d885c-129">System.String</span></span>

## <span data-ttu-id="d885c-130">출력</span><span class="sxs-lookup"><span data-stu-id="d885c-130">OUTPUTS</span></span>

### <span data-ttu-id="d885c-131">Microsoft. 관리.. i g m. 목록 키</span><span class="sxs-lookup"><span data-stu-id="d885c-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="d885c-132">상속자</span><span class="sxs-lookup"><span data-stu-id="d885c-132">NOTES</span></span>

## <span data-ttu-id="d885c-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d885c-133">RELATED LINKS</span></span>
