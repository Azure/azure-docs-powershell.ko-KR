---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 8EDDA991-55B6-4151-8619-E13E14599ECD
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHub.md
ms.openlocfilehash: 3fb98dc1ef4b13b87fc7cfa41e165d9bc24fc17c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336225"
---
# <span data-ttu-id="32cbe-101">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="32cbe-101">New-AzNotificationHub</span></span>

## <span data-ttu-id="32cbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32cbe-102">SYNOPSIS</span></span>
<span data-ttu-id="32cbe-103">알림 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="32cbe-103">Creates a notification hub.</span></span>

## <span data-ttu-id="32cbe-104">구문</span><span class="sxs-lookup"><span data-stu-id="32cbe-104">SYNTAX</span></span>

### <span data-ttu-id="32cbe-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="32cbe-105">InputFileParameterSet</span></span>
```
New-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32cbe-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="32cbe-106">NotificationHubParameterSet</span></span>
```
New-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32cbe-107">설명</span><span class="sxs-lookup"><span data-stu-id="32cbe-107">DESCRIPTION</span></span>
<span data-ttu-id="32cbe-108">**New-AzNotificationHub** cmdlet은 알림 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="32cbe-108">The **New-AzNotificationHub** cmdlet creates a notification hub.</span></span>
<span data-ttu-id="32cbe-109">알림 허브는 해당 클라이언트에서 사용하는 플랫폼에 관계없이 여러 클라이언트에 푸시 알림을 보내는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="32cbe-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="32cbe-110">알림 허브는 개별 앱과 거의 동일합니다. 각 앱에는 일반적으로 자체 알림 허브가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32cbe-110">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="32cbe-111">**New-AzNotificationHub** cmdlet은 새 알림 허브를 만드는 두 가지 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="32cbe-111">The **New-AzNotificationHub** cmdlet provides two ways to create a new notification hub.</span></span>
<span data-ttu-id="32cbe-112">**NotificationHubAttributes** 개체의 인스턴스를 만든 다음 해당 개체를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32cbe-112">You can create an instance of the **NotificationHubAttributes** object and then configure that object.</span></span>
<span data-ttu-id="32cbe-113">그런 다음 *NotificationHubObj* 매개 변수를 통해 새 허브에 해당 속성 값을 복사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32cbe-113">You can then copy those property values to your new hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="32cbe-114">또는 관련 구성 값을 포함하는 JSON(JavaScript Object Notation) 파일을 만든 다음 *InputFile* 매개 변수를 사용하여 해당 값을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32cbe-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and  then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="32cbe-115">**New-AzNotificationHub** cmdlet과 함께 사용하는 경우 이전 JSON 샘플은 미국 서부 데이터 센터에 있는 ContosoNotificationHub라는 알림 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="32cbe-115">When used in conjunction with the **New-AzNotificationHub** cmdlet, the preceding JSON sample creates a notification hub named ContosoNotificationHub located on the West US datacenter.</span></span>

## <span data-ttu-id="32cbe-116">예제</span><span class="sxs-lookup"><span data-stu-id="32cbe-116">EXAMPLES</span></span>

### <span data-ttu-id="32cbe-117">예제 1: 알림 허브 만들기</span><span class="sxs-lookup"><span data-stu-id="32cbe-117">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configurations\InternalHub.json"
```

<span data-ttu-id="32cbe-118">이 명령은 ContosoNamespace 네임스페이스에 알림 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="32cbe-118">This command creates a notification hub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="32cbe-119">새 허브가 ContosoNotificationsGroup에 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="32cbe-119">The new hub will be assigned to the ContosoNotificationsGroup.</span></span>
<span data-ttu-id="32cbe-120">허브에 대한 이름 또는 기타 구성 정보를 지정할 필요가 없습니다. 해당 정보는 입력 파일에서 C:\Configurations\InternalHub.js.</span><span class="sxs-lookup"><span data-stu-id="32cbe-120">You do not need to specify a name or any other configuration information for the hub; that information will be taken from the input file C:\Configurations\InternalHub.json.</span></span>

## <span data-ttu-id="32cbe-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32cbe-121">PARAMETERS</span></span>

### <span data-ttu-id="32cbe-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32cbe-122">-DefaultProfile</span></span>
<span data-ttu-id="32cbe-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="32cbe-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32cbe-124">-InputFile</span><span class="sxs-lookup"><span data-stu-id="32cbe-124">-InputFile</span></span>
<span data-ttu-id="32cbe-125">새 알림 허브에 대한 구성 값을 포함하는 JSON 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="32cbe-125">Specifies the path to a JSON file containing configuration values for the new notification hub.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32cbe-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="32cbe-126">-Namespace</span></span>
<span data-ttu-id="32cbe-127">알림 허브가 할당될 네임스페이스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="32cbe-127">Specifies the namespace to which the notification hub will be assigned.</span></span>
<span data-ttu-id="32cbe-128">네임스페이스는 알림 허브를 그룹화하고 분류하는 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="32cbe-128">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="32cbe-129">알림 허브는 기존 네임스페이스에 할당되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="32cbe-129">Notification hubs must be assigned to an existing namespace.</span></span>
<span data-ttu-id="32cbe-130">**New-AzNotificationHub** cmdlet은 새 네임스페이스를 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="32cbe-130">The **New-AzNotificationHub** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="32cbe-131">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="32cbe-131">-NotificationHubObj</span></span>
<span data-ttu-id="32cbe-132">새 허브에 대한 구성 정보를 포함하는 **NotificationHubAttributes** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="32cbe-132">Specifies the **NotificationHubAttributes** object that contains configuration information for the new hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes
Parameter Sets: NotificationHubParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32cbe-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="32cbe-133">-ResourceGroup</span></span>
<span data-ttu-id="32cbe-134">알림 허브를 할당할 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="32cbe-134">Specifies the resource group to which the notification hub will be assigned.</span></span>
<span data-ttu-id="32cbe-135">리소스 그룹은 인벤토리 관리 및 Azure 관리에 도움이 되는 방식으로 네임스페이스, 알림 허브 및 권한 부여 규칙과 같은 항목을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="32cbe-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>
<span data-ttu-id="32cbe-136">기존 리소스 그룹을 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="32cbe-136">You must use an existing resource group.</span></span>
<span data-ttu-id="32cbe-137">**New-AzNotificationHub** cmdlet은 새 리소스 그룹을 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="32cbe-137">The **New-AzNotificationHub** cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="32cbe-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32cbe-138">-Confirm</span></span>
<span data-ttu-id="32cbe-139">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="32cbe-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32cbe-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32cbe-140">-WhatIf</span></span>
<span data-ttu-id="32cbe-141">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="32cbe-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="32cbe-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="32cbe-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32cbe-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32cbe-143">CommonParameters</span></span>
<span data-ttu-id="32cbe-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="32cbe-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32cbe-145">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="32cbe-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32cbe-146">입력</span><span class="sxs-lookup"><span data-stu-id="32cbe-146">INPUTS</span></span>

### <span data-ttu-id="32cbe-147">System.String</span><span class="sxs-lookup"><span data-stu-id="32cbe-147">System.String</span></span>

## <span data-ttu-id="32cbe-148">출력</span><span class="sxs-lookup"><span data-stu-id="32cbe-148">OUTPUTS</span></span>

### <span data-ttu-id="32cbe-149">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="32cbe-149">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="32cbe-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="32cbe-150">NOTES</span></span>

## <span data-ttu-id="32cbe-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="32cbe-151">RELATED LINKS</span></span>

[<span data-ttu-id="32cbe-152">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="32cbe-152">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="32cbe-153">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="32cbe-153">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="32cbe-154">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="32cbe-154">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


