---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F7BBEF57-0DC2-4EFF-9AA2-119B3BD19AE6
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/set-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
ms.openlocfilehash: 7f0732225389f5174c2097cea57ed38d9ea2be0b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951120"
---
# <span data-ttu-id="faf20-101">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="faf20-101">Set-AzNotificationHub</span></span>

## <span data-ttu-id="faf20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="faf20-102">SYNOPSIS</span></span>
<span data-ttu-id="faf20-103">알림 허브에 대한 속성 값을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="faf20-103">Sets property values for a notification hub.</span></span>

## <span data-ttu-id="faf20-104">구문</span><span class="sxs-lookup"><span data-stu-id="faf20-104">SYNTAX</span></span>

### <span data-ttu-id="faf20-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="faf20-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="faf20-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="faf20-106">NotificationHubParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="faf20-107">설명</span><span class="sxs-lookup"><span data-stu-id="faf20-107">DESCRIPTION</span></span>
<span data-ttu-id="faf20-108">**Set-AzNotificationHub** cmdlet은 알림 허브의 속성 값을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="faf20-108">The **Set-AzNotificationHub** cmdlet modifies the property values of a notification hub.</span></span>
<span data-ttu-id="faf20-109">두 가지 방법으로 알림 허브 속성 값을 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="faf20-109">You can modify a notification hub property value in two ways.</span></span>
<span data-ttu-id="faf20-110">하나에 대해 **NotificationHubAttributes** 개체의 인스턴스를 만든 다음 새 허브가 소유할 속성 값으로 해당 개체를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="faf20-110">For one, you can create an instance of the **NotificationHubAttributes** object and then configure that object with the property values you want the new hub to possess.</span></span>
<span data-ttu-id="faf20-111">이 경우 다음을 통해 .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="faf20-111">This can be done through the .NET Framework.</span></span>
<span data-ttu-id="faf20-112">그런 다음 *NotificationHubObj* 매개 변수를 통해 해당 속성 값을 허브에 복사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="faf20-112">You can then copy those property values to your hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="faf20-113">또는 관련 구성 값이 포함된 JSON(JavaScript 개체표시) 파일을 만든 다음 *InputFile* 매개 변수를 통해 해당 값을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="faf20-113">Alternatively, you can create a JSON (JavaScript Object Notation) file that contains the relevant configuration values, then apply those values by through the *InputFile* parameter.</span></span>
<span data-ttu-id="faf20-114">JSON 파일은 다음과 유사한 구문을 사용하는 텍스트 파일입니다. {</span><span class="sxs-lookup"><span data-stu-id="faf20-114">A JSON file is a text file that uses syntax similar to the following: {</span></span>  
    <span data-ttu-id="faf20-115">"Name": "ContosoNotificationHub",</span><span class="sxs-lookup"><span data-stu-id="faf20-115">"Name": "ContosoNotificationHub",</span></span>  
    <span data-ttu-id="faf20-116">"Location": "West US",</span><span class="sxs-lookup"><span data-stu-id="faf20-116">"Location": "West US",</span></span>  
<span data-ttu-id="faf20-117">} **Set-AzNotificationHub** cmdlet과 함께 사용하는 경우 위의 JSON 샘플은 ContosoNotificationHub라는 알림 허브의 위치 값을 미국 서부로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="faf20-117">} When used in conjunction with the **Set-AzNotificationHub** cmdlet, the preceding JSON sample sets the Location value of a notification hub named ContosoNotificationHub to West US.</span></span>

## <span data-ttu-id="faf20-118">예제</span><span class="sxs-lookup"><span data-stu-id="faf20-118">EXAMPLES</span></span>

### <span data-ttu-id="faf20-119">예제 1: 알림 허브에 대한 속성 값 수정</span><span class="sxs-lookup"><span data-stu-id="faf20-119">Example 1: Modify the property values for a notification hub</span></span>
```powershell
PS C:\>Set-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\Hubs.json"
```

<span data-ttu-id="faf20-120">이 명령은 ContosoNamespace 네임스페이스 네임스페이스에 있는 알림 허브에 대한 속성 값을 수정하고 리소스 그룹 ContosoNotificationsGroup에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="faf20-120">This command modifies the property values for a notification hub found in the ContosoNamespace namespace and assigned it to the resource group ContosoNotificationsGroup.</span></span>
<span data-ttu-id="faf20-121">수정할 허브의 이름뿐만 아니라 속성 값도 명령에 지정되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="faf20-121">The property values, as well as the name of the hub to be modified, are not specified in the command.</span></span>
<span data-ttu-id="faf20-122">대신 해당 정보는 입력 파일에 포함되어 C:\Configuration\Hubs.js있습니다.</span><span class="sxs-lookup"><span data-stu-id="faf20-122">Instead, that information is contained in the input file C:\Configuration\Hubs.json.</span></span>

### <span data-ttu-id="faf20-123">예제 2</span><span class="sxs-lookup"><span data-stu-id="faf20-123">Example 2</span></span>

<span data-ttu-id="faf20-124">알림 허브에 대한 속성 값을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="faf20-124">Sets property values for a notification hub.</span></span> <span data-ttu-id="faf20-125">(자동 재생)</span><span class="sxs-lookup"><span data-stu-id="faf20-125">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzNotificationHub -Namespace 'ContosoNamespace' -NotificationHubObj <NotificationHubAttributes> -ResourceGroup 'ContosoNotificationsGroup'
```

## <span data-ttu-id="faf20-126">매개 변수</span><span class="sxs-lookup"><span data-stu-id="faf20-126">PARAMETERS</span></span>

### <span data-ttu-id="faf20-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faf20-127">-DefaultProfile</span></span>
<span data-ttu-id="faf20-128">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="faf20-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="faf20-129">-Force</span><span class="sxs-lookup"><span data-stu-id="faf20-129">-Force</span></span>
<span data-ttu-id="faf20-130">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="faf20-130">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="faf20-131">-InputFile</span><span class="sxs-lookup"><span data-stu-id="faf20-131">-InputFile</span></span>
<span data-ttu-id="faf20-132">알림 허브에 대한 구성 정보가 포함된 JSON 파일에 대한 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="faf20-132">Specifies the path to a JSON file that contains configuration information for the notification hub.</span></span>

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

### <span data-ttu-id="faf20-133">-네임스페이스</span><span class="sxs-lookup"><span data-stu-id="faf20-133">-Namespace</span></span>
<span data-ttu-id="faf20-134">알림 허브가 할당된 네임스페이스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="faf20-134">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="faf20-135">네임스페이스는 알림 허브를 그룹화하고 분류하는 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="faf20-135">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="faf20-136">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="faf20-136">-NotificationHubObj</span></span>
<span data-ttu-id="faf20-137">이 cmdlet이 수정하는 허브에 대한 구성 정보가 포함된 **NotificationHubAttributes** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="faf20-137">Specifies the **NotificationHubAttributes** object that contains configuration information for the hub that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="faf20-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="faf20-138">-ResourceGroup</span></span>
<span data-ttu-id="faf20-139">알림 허브가 할당된 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="faf20-139">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="faf20-140">리소스 그룹은 인벤토리 관리 및 Azure 관리에 도움이 되는 방식으로 네임스페이스, 알림 허브 및 권한 부여 규칙과 같은 항목을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="faf20-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="faf20-141">-확인</span><span class="sxs-lookup"><span data-stu-id="faf20-141">-Confirm</span></span>
<span data-ttu-id="faf20-142">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="faf20-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="faf20-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="faf20-143">-WhatIf</span></span>
<span data-ttu-id="faf20-144">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="faf20-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="faf20-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="faf20-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="faf20-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faf20-146">CommonParameters</span></span>
<span data-ttu-id="faf20-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="faf20-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faf20-148">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="faf20-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faf20-149">입력</span><span class="sxs-lookup"><span data-stu-id="faf20-149">INPUTS</span></span>

### <span data-ttu-id="faf20-150">System.String</span><span class="sxs-lookup"><span data-stu-id="faf20-150">System.String</span></span>

## <span data-ttu-id="faf20-151">출력</span><span class="sxs-lookup"><span data-stu-id="faf20-151">OUTPUTS</span></span>

### <span data-ttu-id="faf20-152">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="faf20-152">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="faf20-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="faf20-153">NOTES</span></span>

## <span data-ttu-id="faf20-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="faf20-154">RELATED LINKS</span></span>

[<span data-ttu-id="faf20-155">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="faf20-155">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="faf20-156">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="faf20-156">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="faf20-157">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="faf20-157">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)


