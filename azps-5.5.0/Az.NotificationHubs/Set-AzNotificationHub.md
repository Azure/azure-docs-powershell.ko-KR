---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F7BBEF57-0DC2-4EFF-9AA2-119B3BD19AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
ms.openlocfilehash: 7083c6872981cefaa12dc01612f3eb27cc7676ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206397"
---
# <span data-ttu-id="16111-101">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="16111-101">Set-AzNotificationHub</span></span>

## <span data-ttu-id="16111-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16111-102">SYNOPSIS</span></span>
<span data-ttu-id="16111-103">알림 허브에 대한 속성 값을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="16111-103">Sets property values for a notification hub.</span></span>

## <span data-ttu-id="16111-104">구문</span><span class="sxs-lookup"><span data-stu-id="16111-104">SYNTAX</span></span>

### <span data-ttu-id="16111-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="16111-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16111-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="16111-106">NotificationHubParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16111-107">설명</span><span class="sxs-lookup"><span data-stu-id="16111-107">DESCRIPTION</span></span>
<span data-ttu-id="16111-108">**Set-AzNotificationHub** cmdlet은 알림 허브의 속성 값을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="16111-108">The **Set-AzNotificationHub** cmdlet modifies the property values of a notification hub.</span></span>
<span data-ttu-id="16111-109">알림 허브 속성 값은 두 가지 방법으로 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16111-109">You can modify a notification hub property value in two ways.</span></span>
<span data-ttu-id="16111-110">하나에 대해 **NotificationHubAttributes** 개체의 인스턴스를 만든 다음 새 허브에서 소유하려는 속성 값으로 해당 개체를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16111-110">For one, you can create an instance of the **NotificationHubAttributes** object and then configure that object with the property values you want the new hub to possess.</span></span>
<span data-ttu-id="16111-111">.NET Framework를 통해 이 일을 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16111-111">This can be done through the .NET Framework.</span></span>
<span data-ttu-id="16111-112">그런 다음 *NotificationHubObj* 매개 변수를 통해 해당 속성 값을 허브에 복사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16111-112">You can then copy those property values to your hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="16111-113">또는 관련 구성 값을 포함하는 JSON(JavaScript Object Notation) 파일을 만든 다음 *InputFile* 매개 변수를 통해 해당 값을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16111-113">Alternatively, you can create a JSON (JavaScript Object Notation) file that contains the relevant configuration values, then apply those values by through the *InputFile* parameter.</span></span>
<span data-ttu-id="16111-114">JSON 파일은 {과 유사한 구문을 사용하는 텍스트 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="16111-114">A JSON file is a text file that uses syntax similar to the following: {</span></span>  
    <span data-ttu-id="16111-115">"Name": "ContosoNotificationHub",</span><span class="sxs-lookup"><span data-stu-id="16111-115">"Name": "ContosoNotificationHub",</span></span>  
    <span data-ttu-id="16111-116">"Location": "West US",</span><span class="sxs-lookup"><span data-stu-id="16111-116">"Location": "West US",</span></span>  
<span data-ttu-id="16111-117">} **Set-AzNotificationHub** cmdlet과 함께 사용하는 경우 이전 JSON 샘플은 ContosoNotificationHub라는 알림 허브의 위치 값을 미국 서부로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="16111-117">} When used in conjunction with the **Set-AzNotificationHub** cmdlet, the preceding JSON sample sets the Location value of a notification hub named ContosoNotificationHub to West US.</span></span>

## <span data-ttu-id="16111-118">예제</span><span class="sxs-lookup"><span data-stu-id="16111-118">EXAMPLES</span></span>

### <span data-ttu-id="16111-119">예제 1: 알림 허브에 대한 속성 값 수정</span><span class="sxs-lookup"><span data-stu-id="16111-119">Example 1: Modify the property values for a notification hub</span></span>
```powershell
PS C:\>Set-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\Hubs.json"
```

<span data-ttu-id="16111-120">이 명령은 ContosoNamespace 네임스페이스에 있는 알림 허브의 속성 값을 수정하고 리소스 그룹 ContosoNotificationsGroup에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="16111-120">This command modifies the property values for a notification hub found in the ContosoNamespace namespace and assigned it to the resource group ContosoNotificationsGroup.</span></span>
<span data-ttu-id="16111-121">속성 값과 수정할 허브의 이름은 명령에 지정되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16111-121">The property values, as well as the name of the hub to be modified, are not specified in the command.</span></span>
<span data-ttu-id="16111-122">대신, 해당 정보는 설정한 입력 파일에 C:\Configuration\Hubs.js.</span><span class="sxs-lookup"><span data-stu-id="16111-122">Instead, that information is contained in the input file C:\Configuration\Hubs.json.</span></span>

### <span data-ttu-id="16111-123">예제 2</span><span class="sxs-lookup"><span data-stu-id="16111-123">Example 2</span></span>

<span data-ttu-id="16111-124">알림 허브에 대한 속성 값을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="16111-124">Sets property values for a notification hub.</span></span> <span data-ttu-id="16111-125">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="16111-125">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzNotificationHub -Namespace 'ContosoNamespace' -NotificationHubObj <NotificationHubAttributes> -ResourceGroup 'ContosoNotificationsGroup'
```

## <span data-ttu-id="16111-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16111-126">PARAMETERS</span></span>

### <span data-ttu-id="16111-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16111-127">-DefaultProfile</span></span>
<span data-ttu-id="16111-128">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="16111-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16111-129">-Force</span><span class="sxs-lookup"><span data-stu-id="16111-129">-Force</span></span>
<span data-ttu-id="16111-130">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16111-130">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="16111-131">-InputFile</span><span class="sxs-lookup"><span data-stu-id="16111-131">-InputFile</span></span>
<span data-ttu-id="16111-132">알림 허브에 대한 구성 정보를 포함하는 JSON 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="16111-132">Specifies the path to a JSON file that contains configuration information for the notification hub.</span></span>

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

### <span data-ttu-id="16111-133">-Namespace</span><span class="sxs-lookup"><span data-stu-id="16111-133">-Namespace</span></span>
<span data-ttu-id="16111-134">알림 허브가 할당된 네임스페이스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="16111-134">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="16111-135">네임스페이스는 알림 허브를 그룹화하고 분류하는 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="16111-135">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="16111-136">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="16111-136">-NotificationHubObj</span></span>
<span data-ttu-id="16111-137">이 cmdlet이 수정하는 허브에 대한 구성 정보를 포함하는 **NotificationHubAttributes** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="16111-137">Specifies the **NotificationHubAttributes** object that contains configuration information for the hub that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="16111-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="16111-138">-ResourceGroup</span></span>
<span data-ttu-id="16111-139">알림 허브가 할당된 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="16111-139">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="16111-140">리소스 그룹은 인벤토리 관리 및 Azure 관리에 도움이 되는 방식으로 네임스페이스, 알림 허브 및 권한 부여 규칙과 같은 항목을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="16111-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="16111-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="16111-141">-Confirm</span></span>
<span data-ttu-id="16111-142">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="16111-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16111-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16111-143">-WhatIf</span></span>
<span data-ttu-id="16111-144">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="16111-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16111-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16111-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16111-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16111-146">CommonParameters</span></span>
<span data-ttu-id="16111-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="16111-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16111-148">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="16111-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16111-149">입력</span><span class="sxs-lookup"><span data-stu-id="16111-149">INPUTS</span></span>

### <span data-ttu-id="16111-150">System.String</span><span class="sxs-lookup"><span data-stu-id="16111-150">System.String</span></span>

## <span data-ttu-id="16111-151">출력</span><span class="sxs-lookup"><span data-stu-id="16111-151">OUTPUTS</span></span>

### <span data-ttu-id="16111-152">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="16111-152">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="16111-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="16111-153">NOTES</span></span>

## <span data-ttu-id="16111-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="16111-154">RELATED LINKS</span></span>

[<span data-ttu-id="16111-155">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="16111-155">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="16111-156">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="16111-156">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="16111-157">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="16111-157">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)


