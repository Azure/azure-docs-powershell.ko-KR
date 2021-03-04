---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: A03F32C3-BB01-46A5-86C5-B7A4DDC42351
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/new-aznotificationhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
ms.openlocfilehash: 8c6b24dd2d208ea4465138f1e901b030ee5c30e6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951264"
---
# <span data-ttu-id="04edd-101">New-AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="04edd-101">New-AzNotificationHubKey</span></span>

## <span data-ttu-id="04edd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04edd-102">SYNOPSIS</span></span>
<span data-ttu-id="04edd-103">NotificationHub에 대한 권한 부여 규칙 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="04edd-103">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

## <span data-ttu-id="04edd-104">구문</span><span class="sxs-lookup"><span data-stu-id="04edd-104">SYNTAX</span></span>

```
New-AzNotificationHubKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04edd-105">설명</span><span class="sxs-lookup"><span data-stu-id="04edd-105">DESCRIPTION</span></span>
<span data-ttu-id="04edd-106">New-AzNotificationHubKey cmdlet은 NotificationHub 권한 부여 규칙에 대한 기본 키/보조 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="04edd-106">New-AzNotificationHubKey cmdlet regenerates the Primary Key/Secondary Key for the NotificationHub Authorization Rule.</span></span>

## <span data-ttu-id="04edd-107">예제</span><span class="sxs-lookup"><span data-stu-id="04edd-107">EXAMPLES</span></span>

### <span data-ttu-id="04edd-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="04edd-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="04edd-109">{{ 여기에 예제 설명 추가 }}</span><span class="sxs-lookup"><span data-stu-id="04edd-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="04edd-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="04edd-110">PARAMETERS</span></span>

### <span data-ttu-id="04edd-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="04edd-111">-AuthorizationRule</span></span>
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

### <span data-ttu-id="04edd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04edd-112">-DefaultProfile</span></span>
<span data-ttu-id="04edd-113">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="04edd-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="04edd-114">-Force</span><span class="sxs-lookup"><span data-stu-id="04edd-114">-Force</span></span>
<span data-ttu-id="04edd-115">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04edd-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="04edd-116">-네임스페이스</span><span class="sxs-lookup"><span data-stu-id="04edd-116">-Namespace</span></span>
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

### <span data-ttu-id="04edd-117">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="04edd-117">-NotificationHub</span></span>
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

### <span data-ttu-id="04edd-118">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="04edd-118">-PolicyKey</span></span>
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

### <span data-ttu-id="04edd-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="04edd-119">-ResourceGroup</span></span>
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

### <span data-ttu-id="04edd-120">-확인</span><span class="sxs-lookup"><span data-stu-id="04edd-120">-Confirm</span></span>
<span data-ttu-id="04edd-121">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="04edd-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04edd-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04edd-122">-WhatIf</span></span>
<span data-ttu-id="04edd-123">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="04edd-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04edd-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04edd-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04edd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04edd-125">CommonParameters</span></span>
<span data-ttu-id="04edd-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="04edd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04edd-127">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="04edd-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04edd-128">입력</span><span class="sxs-lookup"><span data-stu-id="04edd-128">INPUTS</span></span>

### <span data-ttu-id="04edd-129">System.String</span><span class="sxs-lookup"><span data-stu-id="04edd-129">System.String</span></span>

## <span data-ttu-id="04edd-130">출력</span><span class="sxs-lookup"><span data-stu-id="04edd-130">OUTPUTS</span></span>

### <span data-ttu-id="04edd-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="04edd-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="04edd-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="04edd-132">NOTES</span></span>

## <span data-ttu-id="04edd-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="04edd-133">RELATED LINKS</span></span>
