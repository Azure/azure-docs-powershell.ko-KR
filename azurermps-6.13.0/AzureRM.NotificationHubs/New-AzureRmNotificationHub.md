---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 8EDDA991-55B6-4151-8619-E13E14599ECD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHub.md
ms.openlocfilehash: c0a3e2231ef0f27689a08b9199876d04c4e68b2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702784"
---
# <span data-ttu-id="fd450-101">New-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="fd450-101">New-AzureRmNotificationHub</span></span>

## <span data-ttu-id="fd450-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd450-102">SYNOPSIS</span></span>
<span data-ttu-id="fd450-103">알림 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fd450-103">Creates a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd450-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fd450-104">SYNTAX</span></span>

### <span data-ttu-id="fd450-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd450-105">InputFileParameterSet</span></span>
```
New-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd450-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd450-106">NotificationHubParameterSet</span></span>
```
New-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd450-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fd450-107">DESCRIPTION</span></span>
<span data-ttu-id="fd450-108">**새 AzureRmNotificationHub** cmdlet은 알림 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fd450-108">The **New-AzureRmNotificationHub** cmdlet creates a notification hub.</span></span>
<span data-ttu-id="fd450-109">알림 허브는 해당 클라이언트에서 사용 하는 플랫폼에 관계 없이 여러 클라이언트로 푸시 알림을 보내는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd450-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="fd450-110">알림 허브는 개별 앱과 거의 동일 합니다. 각 앱에는 일반적으로 자체 알림 허브가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd450-110">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="fd450-111">새 알림 허브를 만드는 두 가지 방법으로 **AzureRmNotificationHub** cmdlet을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd450-111">The **New-AzureRmNotificationHub** cmdlet provides two ways to create a new notification hub.</span></span>
<span data-ttu-id="fd450-112">**NotificationHubAttributes** 개체의 인스턴스를 만든 다음 해당 개체를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd450-112">You can create an instance of the **NotificationHubAttributes** object and then configure that object.</span></span>
<span data-ttu-id="fd450-113">그런 다음 *NotificationHubObj* 매개 변수를 통해 새 허브에 해당 속성 값을 복사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd450-113">You can then copy those property values to your new hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="fd450-114">또는 관련 구성 값이 포함 된 JSON (JavaScript 개체 표시법) 파일을 만든 다음 *InputFile* 매개 변수를 사용 하 여 해당 값을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd450-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and  then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="fd450-115">**AzureRmNotificationHub** cmdlet과 함께 사용 하는 경우 앞의 JSON 샘플은 경기도 데이터 센터에 있는 ContosoNotificationHub 라는 알림 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fd450-115">When used in conjunction with the **New-AzureRmNotificationHub** cmdlet, the preceding JSON sample creates a notification hub named ContosoNotificationHub located on the West US datacenter.</span></span>

## <span data-ttu-id="fd450-116">예제의</span><span class="sxs-lookup"><span data-stu-id="fd450-116">EXAMPLES</span></span>

### <span data-ttu-id="fd450-117">예제 1: 알림 허브 만들기</span><span class="sxs-lookup"><span data-stu-id="fd450-117">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configurations\InternalHub.json"
```

<span data-ttu-id="fd450-118">이 명령은 네임 스페이스 ContosoNamespace에 알림 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fd450-118">This command creates a notification hub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="fd450-119">새 허브가 ContosoNotificationsGroup에 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd450-119">The new hub will be assigned to the ContosoNotificationsGroup.</span></span>
<span data-ttu-id="fd450-120">허브에 대 한 이름 또는 기타 구성 정보를 지정할 필요는 없습니다. C:\Configurations\InternalHub.js입력 파일에서 해당 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fd450-120">You do not need to specify a name or any other configuration information for the hub; that information will be taken from the input file C:\Configurations\InternalHub.json.</span></span>

## <span data-ttu-id="fd450-121">변수</span><span class="sxs-lookup"><span data-stu-id="fd450-121">PARAMETERS</span></span>

### <span data-ttu-id="fd450-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd450-122">-DefaultProfile</span></span>
<span data-ttu-id="fd450-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fd450-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd450-124">-InputFile</span><span class="sxs-lookup"><span data-stu-id="fd450-124">-InputFile</span></span>
<span data-ttu-id="fd450-125">새 알림 허브에 대 한 구성 값이 포함 된 JSON 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd450-125">Specifies the path to a JSON file containing configuration values for the new notification hub.</span></span>

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

### <span data-ttu-id="fd450-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fd450-126">-Namespace</span></span>
<span data-ttu-id="fd450-127">알림 허브가 할당 되는 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd450-127">Specifies the namespace to which the notification hub will be assigned.</span></span>
<span data-ttu-id="fd450-128">네임 스페이스는 알림 허브를 그룹화 하 고 분류 하는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd450-128">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="fd450-129">알림 허브는 기존 네임 스페이스에 할당 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd450-129">Notification hubs must be assigned to an existing namespace.</span></span>
<span data-ttu-id="fd450-130">**AzureRmNotificationHub** cmdlet이 새 네임 스페이스를 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fd450-130">The **New-AzureRmNotificationHub** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="fd450-131">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="fd450-131">-NotificationHubObj</span></span>
<span data-ttu-id="fd450-132">새 허브에 대 한 구성 정보를 포함 하는 **NotificationHubAttributes** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd450-132">Specifies the **NotificationHubAttributes** object that contains configuration information for the new hub.</span></span>

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

### <span data-ttu-id="fd450-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fd450-133">-ResourceGroup</span></span>
<span data-ttu-id="fd450-134">알림 허브가 할당 되는 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd450-134">Specifies the resource group to which the notification hub will be assigned.</span></span>
<span data-ttu-id="fd450-135">리소스 그룹은 관리 및 Azure 관리를 쉽게 할 수 있는 방식으로 네임 스페이스, 알림 허브, 권한 부여 규칙 등의 항목을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd450-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>
<span data-ttu-id="fd450-136">기존 리소스 그룹을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd450-136">You must use an existing resource group.</span></span>
<span data-ttu-id="fd450-137">**새 AzureRmNotificationHub** cmdlet은 새 리소스 그룹을 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fd450-137">The **New-AzureRmNotificationHub** cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="fd450-138">-확인</span><span class="sxs-lookup"><span data-stu-id="fd450-138">-Confirm</span></span>
<span data-ttu-id="fd450-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd450-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd450-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd450-140">-WhatIf</span></span>
<span data-ttu-id="fd450-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fd450-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd450-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd450-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd450-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd450-143">CommonParameters</span></span>
<span data-ttu-id="fd450-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd450-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd450-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd450-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd450-146">입력</span><span class="sxs-lookup"><span data-stu-id="fd450-146">INPUTS</span></span>

### <span data-ttu-id="fd450-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fd450-147">System.String</span></span>

## <span data-ttu-id="fd450-148">출력</span><span class="sxs-lookup"><span data-stu-id="fd450-148">OUTPUTS</span></span>

### <span data-ttu-id="fd450-149">Microsoft. Azure. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="fd450-149">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="fd450-150">상속자</span><span class="sxs-lookup"><span data-stu-id="fd450-150">NOTES</span></span>

## <span data-ttu-id="fd450-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fd450-151">RELATED LINKS</span></span>

[<span data-ttu-id="fd450-152">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="fd450-152">Get-AzureRmNotificationHub</span></span>](./Get-AzureRmNotificationHub.md)

[<span data-ttu-id="fd450-153">제거-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="fd450-153">Remove-AzureRmNotificationHub</span></span>](./Remove-AzureRmNotificationHub.md)

[<span data-ttu-id="fd450-154">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="fd450-154">Set-AzureRmNotificationHub</span></span>](./Set-AzureRmNotificationHub.md)


