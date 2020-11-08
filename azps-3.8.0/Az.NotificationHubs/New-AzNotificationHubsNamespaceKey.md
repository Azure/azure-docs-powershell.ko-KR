---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1EC19069-B64C-4F0F-99A3-07C16E46C0A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespacekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceKey.md
ms.openlocfilehash: a575ae0151cd28a9bcc3580a77ad3a0c79a2984b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042781"
---
# <span data-ttu-id="3d1c5-101">New-AzNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="3d1c5-101">New-AzNotificationHubsNamespaceKey</span></span>

## <span data-ttu-id="3d1c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d1c5-102">SYNOPSIS</span></span>
<span data-ttu-id="3d1c5-103">네임 스페이스에 대 한 권한 부여 규칙 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1c5-103">Regenerate the Authorization Rule Key for a Namespace.</span></span>

## <span data-ttu-id="3d1c5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3d1c5-104">SYNTAX</span></span>

```
New-AzNotificationHubsNamespaceKey [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d1c5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3d1c5-105">DESCRIPTION</span></span>
<span data-ttu-id="3d1c5-106">New-AzNotificationHubNamespaceKey cmdlet은 네임 스페이스 권한 부여 규칙에 대 한 기본 키/보조 키를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1c5-106">New-AzNotificationHubNamespaceKey cmdlet regenerates the Primary Key/Secondary Key for the Namespace Authorization Rule.</span></span>

## <span data-ttu-id="3d1c5-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3d1c5-107">EXAMPLES</span></span>

### <span data-ttu-id="3d1c5-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="3d1c5-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="3d1c5-109">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="3d1c5-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="3d1c5-110">변수</span><span class="sxs-lookup"><span data-stu-id="3d1c5-110">PARAMETERS</span></span>

### <span data-ttu-id="3d1c5-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3d1c5-111">-AuthorizationRule</span></span>
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

### <span data-ttu-id="3d1c5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d1c5-112">-DefaultProfile</span></span>
<span data-ttu-id="3d1c5-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3d1c5-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d1c5-114">-Force</span><span class="sxs-lookup"><span data-stu-id="3d1c5-114">-Force</span></span>
<span data-ttu-id="3d1c5-115">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3d1c5-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3d1c5-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3d1c5-116">-Namespace</span></span>
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

### <span data-ttu-id="3d1c5-117">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="3d1c5-117">-PolicyKey</span></span>
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

### <span data-ttu-id="3d1c5-118">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3d1c5-118">-ResourceGroup</span></span>
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

### <span data-ttu-id="3d1c5-119">-확인</span><span class="sxs-lookup"><span data-stu-id="3d1c5-119">-Confirm</span></span>
<span data-ttu-id="3d1c5-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1c5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d1c5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d1c5-121">-WhatIf</span></span>
<span data-ttu-id="3d1c5-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3d1c5-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d1c5-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3d1c5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d1c5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d1c5-124">CommonParameters</span></span>
<span data-ttu-id="3d1c5-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1c5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d1c5-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d1c5-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d1c5-127">입력</span><span class="sxs-lookup"><span data-stu-id="3d1c5-127">INPUTS</span></span>

### <span data-ttu-id="3d1c5-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3d1c5-128">System.String</span></span>

## <span data-ttu-id="3d1c5-129">출력</span><span class="sxs-lookup"><span data-stu-id="3d1c5-129">OUTPUTS</span></span>

### <span data-ttu-id="3d1c5-130">Microsoft. 관리.. i g m. 목록 키</span><span class="sxs-lookup"><span data-stu-id="3d1c5-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="3d1c5-131">상속자</span><span class="sxs-lookup"><span data-stu-id="3d1c5-131">NOTES</span></span>

## <span data-ttu-id="3d1c5-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3d1c5-132">RELATED LINKS</span></span>
