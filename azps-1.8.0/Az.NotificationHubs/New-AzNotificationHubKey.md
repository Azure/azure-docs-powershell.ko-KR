---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: A03F32C3-BB01-46A5-86C5-B7A4DDC42351
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
ms.openlocfilehash: f426dc06d08e10d0811382b00e2072f65ebf1b0b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699902"
---
# <span data-ttu-id="c79f1-101">New-AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="c79f1-101">New-AzNotificationHubKey</span></span>

## <span data-ttu-id="c79f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c79f1-102">SYNOPSIS</span></span>
<span data-ttu-id="c79f1-103">NotificationHub에 대 한 권한 부여 규칙 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c79f1-103">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

## <span data-ttu-id="c79f1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c79f1-104">SYNTAX</span></span>

```
New-AzNotificationHubKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c79f1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c79f1-105">DESCRIPTION</span></span>
<span data-ttu-id="c79f1-106">New-AzNotificationHubKey cmdlet은 NotificationHub 권한 부여 규칙에 대 한 기본 키/보조 키를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c79f1-106">New-AzNotificationHubKey cmdlet regenerates the Primary Key/Secondary Key for the NotificationHub Authorization Rule.</span></span>

## <span data-ttu-id="c79f1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c79f1-107">EXAMPLES</span></span>

### <span data-ttu-id="c79f1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c79f1-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="c79f1-109">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="c79f1-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="c79f1-110">변수</span><span class="sxs-lookup"><span data-stu-id="c79f1-110">PARAMETERS</span></span>

### <span data-ttu-id="c79f1-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c79f1-111">-AuthorizationRule</span></span>
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

### <span data-ttu-id="c79f1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c79f1-112">-DefaultProfile</span></span>
<span data-ttu-id="c79f1-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c79f1-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c79f1-114">-Force</span><span class="sxs-lookup"><span data-stu-id="c79f1-114">-Force</span></span>
<span data-ttu-id="c79f1-115">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c79f1-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c79f1-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c79f1-116">-Namespace</span></span>
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

### <span data-ttu-id="c79f1-117">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="c79f1-117">-NotificationHub</span></span>
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

### <span data-ttu-id="c79f1-118">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="c79f1-118">-PolicyKey</span></span>
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

### <span data-ttu-id="c79f1-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c79f1-119">-ResourceGroup</span></span>
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

### <span data-ttu-id="c79f1-120">-확인</span><span class="sxs-lookup"><span data-stu-id="c79f1-120">-Confirm</span></span>
<span data-ttu-id="c79f1-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c79f1-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c79f1-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c79f1-122">-WhatIf</span></span>
<span data-ttu-id="c79f1-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c79f1-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c79f1-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c79f1-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c79f1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c79f1-125">CommonParameters</span></span>
<span data-ttu-id="c79f1-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c79f1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c79f1-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c79f1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c79f1-128">입력</span><span class="sxs-lookup"><span data-stu-id="c79f1-128">INPUTS</span></span>

### <span data-ttu-id="c79f1-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c79f1-129">System.String</span></span>

## <span data-ttu-id="c79f1-130">출력</span><span class="sxs-lookup"><span data-stu-id="c79f1-130">OUTPUTS</span></span>

### <span data-ttu-id="c79f1-131">Microsoft. 관리.. i g m. 목록 키</span><span class="sxs-lookup"><span data-stu-id="c79f1-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="c79f1-132">상속자</span><span class="sxs-lookup"><span data-stu-id="c79f1-132">NOTES</span></span>

## <span data-ttu-id="c79f1-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c79f1-133">RELATED LINKS</span></span>
