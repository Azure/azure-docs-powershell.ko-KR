---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 5EDFBF19-928F-4F95-BD93-CF8BAEA11C52
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespace.md
ms.openlocfilehash: e03be5a1daae753e1538b171586d9a8e46ad8021
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309101"
---
# <span data-ttu-id="1719f-101">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="1719f-101">Remove-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="1719f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1719f-102">SYNOPSIS</span></span>
<span data-ttu-id="1719f-103">알림 허브 네임 스페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1719f-103">Removes a notification hub namespace.</span></span>

## <span data-ttu-id="1719f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1719f-104">SYNTAX</span></span>

```
Remove-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1719f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1719f-105">DESCRIPTION</span></span>
<span data-ttu-id="1719f-106">**AzNotificationHubsNamespace** cmdlet은 배포에서 알림 허브 네임 스페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1719f-106">The **Remove-AzNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="1719f-107">네임 스페이스는 알림 허브를 구성 하 고 관리 하는 데 도움이 되는 논리적 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="1719f-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="1719f-108">**AzNotificationHubsNamespace** cmdlet은 배포에서 알림 허브 네임 스페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1719f-108">The **Remove-AzNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="1719f-109">이 cmdlet을 실행할 때 지정 된 네임 스페이스는 해당 네임 스페이스와 연결 된 모든 알림 허브와 함께 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1719f-109">When you run this cmdlet, the specified namespace will be deleted along with all the notification hubs associated with that namespace.</span></span>

## <span data-ttu-id="1719f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="1719f-110">EXAMPLES</span></span>

### <span data-ttu-id="1719f-111">예제 1: 알림 허브 네임 스페이스 제거</span><span class="sxs-lookup"><span data-stu-id="1719f-111">Example 1: Remove a notification hub namespace</span></span>
```
PS C:\>Remove-AzNotificationHubsNamespace -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="1719f-112">이 명령은 ContosoNamespace 이라는 네임 스페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1719f-112">This command removes the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="1719f-113">네임 스페이스에 할당 되는 리소스 그룹을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1719f-113">You must specify the resource group the namespace is assigned to.</span></span>

## <span data-ttu-id="1719f-114">변수</span><span class="sxs-lookup"><span data-stu-id="1719f-114">PARAMETERS</span></span>

### <span data-ttu-id="1719f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1719f-115">-DefaultProfile</span></span>
<span data-ttu-id="1719f-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1719f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1719f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1719f-117">-Force</span></span>
<span data-ttu-id="1719f-118">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1719f-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1719f-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1719f-119">-Namespace</span></span>
<span data-ttu-id="1719f-120">이 cmdlet이 제거 하는 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1719f-120">Specifies the namespace that this cmdlet removes.</span></span>
<span data-ttu-id="1719f-121">네임 스페이스는 알림 허브를 그룹화 하 고 분류 하는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="1719f-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="1719f-122">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1719f-122">-ResourceGroup</span></span>
<span data-ttu-id="1719f-123">네임 스페이스를 할당할 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1719f-123">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="1719f-124">리소스 그룹은 관리 및 Azure 관리를 쉽게 할 수 있는 방식으로 네임 스페이스, 알림 허브, 권한 부여 규칙 등의 항목을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1719f-124">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="1719f-125">-확인</span><span class="sxs-lookup"><span data-stu-id="1719f-125">-Confirm</span></span>
<span data-ttu-id="1719f-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1719f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1719f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1719f-127">-WhatIf</span></span>
<span data-ttu-id="1719f-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1719f-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1719f-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1719f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1719f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1719f-130">CommonParameters</span></span>
<span data-ttu-id="1719f-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1719f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1719f-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1719f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1719f-133">입력</span><span class="sxs-lookup"><span data-stu-id="1719f-133">INPUTS</span></span>

### <span data-ttu-id="1719f-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1719f-134">System.String</span></span>

## <span data-ttu-id="1719f-135">출력</span><span class="sxs-lookup"><span data-stu-id="1719f-135">OUTPUTS</span></span>

### <span data-ttu-id="1719f-136">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="1719f-136">System.Void</span></span>

## <span data-ttu-id="1719f-137">상속자</span><span class="sxs-lookup"><span data-stu-id="1719f-137">NOTES</span></span>

## <span data-ttu-id="1719f-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1719f-138">RELATED LINKS</span></span>

[<span data-ttu-id="1719f-139">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="1719f-139">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="1719f-140">새로운 AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="1719f-140">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="1719f-141">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="1719f-141">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


