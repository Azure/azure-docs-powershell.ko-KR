---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F7BBEF57-0DC2-4EFF-9AA2-119B3BD19AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
ms.openlocfilehash: f59ac6a2e1431c3ba04ff0ac9cf9cafbfdfe367e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872509"
---
# <span data-ttu-id="f2681-101">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f2681-101">Set-AzNotificationHub</span></span>

## <span data-ttu-id="f2681-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2681-102">SYNOPSIS</span></span>
<span data-ttu-id="f2681-103">알림 허브에 대 한 속성 값을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2681-103">Sets property values for a notification hub.</span></span>

## <span data-ttu-id="f2681-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f2681-104">SYNTAX</span></span>

### <span data-ttu-id="f2681-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2681-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2681-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2681-106">NotificationHubParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2681-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f2681-107">DESCRIPTION</span></span>
<span data-ttu-id="f2681-108">**Set-AzNotificationHub** cmdlet은 알림 허브의 속성 값을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2681-108">The **Set-AzNotificationHub** cmdlet modifies the property values of a notification hub.</span></span>
<span data-ttu-id="f2681-109">알림 허브 속성 값은 두 가지 방법으로 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2681-109">You can modify a notification hub property value in two ways.</span></span>
<span data-ttu-id="f2681-110">한 가지 방법으로 **NotificationHubAttributes** 개체의 인스턴스를 만든 다음 새 허브가 포함할 속성 값으로 해당 개체를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2681-110">For one, you can create an instance of the **NotificationHubAttributes** object and then configure that object with the property values you want the new hub to possess.</span></span>
<span data-ttu-id="f2681-111">.NET Framework를 통해이 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2681-111">This can be done through the .NET Framework.</span></span>
<span data-ttu-id="f2681-112">그런 다음 *NotificationHubObj* 매개 변수를 통해 해당 속성 값을 허브에 복사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2681-112">You can then copy those property values to your hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="f2681-113">또는 관련 구성 값이 포함 된 JSON (JavaScript 개체 표시법) 파일을 만든 다음 *InputFile* 매개 변수를 통해 해당 값을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2681-113">Alternatively, you can create a JSON (JavaScript Object Notation) file that contains the relevant configuration values, then apply those values by through the *InputFile* parameter.</span></span>
<span data-ttu-id="f2681-114">JSON 파일은 다음과 같은 구문을 사용 하는 텍스트 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="f2681-114">A JSON file is a text file that uses syntax similar to the following: {</span></span>  
    <span data-ttu-id="f2681-115">"Name": "ContosoNotificationHub",</span><span class="sxs-lookup"><span data-stu-id="f2681-115">"Name": "ContosoNotificationHub",</span></span>  
    <span data-ttu-id="f2681-116">"위치": "서쪽 미국",</span><span class="sxs-lookup"><span data-stu-id="f2681-116">"Location": "West US",</span></span>  
<span data-ttu-id="f2681-117">} **AzNotificationHub** cmdlet과 함께 사용 하는 경우 앞의 JSON 샘플에서는 ContosoNotificationHub 이라는 알림 허브의 위치 값을 서쪽 미국으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2681-117">} When used in conjunction with the **Set-AzNotificationHub** cmdlet, the preceding JSON sample sets the Location value of a notification hub named ContosoNotificationHub to West US.</span></span>

## <span data-ttu-id="f2681-118">예제의</span><span class="sxs-lookup"><span data-stu-id="f2681-118">EXAMPLES</span></span>

### <span data-ttu-id="f2681-119">예제 1: 알림 허브의 속성 값 수정</span><span class="sxs-lookup"><span data-stu-id="f2681-119">Example 1: Modify the property values for a notification hub</span></span>
```
PS C:\>Set-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\Hubs.json"
```

<span data-ttu-id="f2681-120">이 명령은 ContosoNamespace 네임 스페이스에 있는 알림 허브의 속성 값을 수정 하 고 리소스 그룹 ContosoNotificationsGroup에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2681-120">This command modifies the property values for a notification hub found in the ContosoNamespace namespace and assigned it to the resource group ContosoNotificationsGroup.</span></span>
<span data-ttu-id="f2681-121">속성 값 및 수정할 허브의 이름을 명령에 지정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f2681-121">The property values, as well as the name of the hub to be modified, are not specified in the command.</span></span>
<span data-ttu-id="f2681-122">대신,이 정보는 입력 파일 C:\Configuration\Hubs.js에 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2681-122">Instead, that information is contained in the input file C:\Configuration\Hubs.json.</span></span>

## <span data-ttu-id="f2681-123">변수</span><span class="sxs-lookup"><span data-stu-id="f2681-123">PARAMETERS</span></span>

### <span data-ttu-id="f2681-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2681-124">-DefaultProfile</span></span>
<span data-ttu-id="f2681-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f2681-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2681-126">-Force</span><span class="sxs-lookup"><span data-stu-id="f2681-126">-Force</span></span>
<span data-ttu-id="f2681-127">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f2681-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f2681-128">-InputFile</span><span class="sxs-lookup"><span data-stu-id="f2681-128">-InputFile</span></span>
<span data-ttu-id="f2681-129">알림 허브에 대 한 구성 정보를 포함 하는 JSON 파일에 대 한 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2681-129">Specifies the path to a JSON file that contains configuration information for the notification hub.</span></span>

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

### <span data-ttu-id="f2681-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f2681-130">-Namespace</span></span>
<span data-ttu-id="f2681-131">알림 허브가 할당 된 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2681-131">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="f2681-132">네임 스페이스는 알림 허브를 그룹화 하 고 분류 하는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2681-132">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="f2681-133">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="f2681-133">-NotificationHubObj</span></span>
<span data-ttu-id="f2681-134">이 cmdlet이 수정 하는 허브에 대 한 구성 정보를 포함 하는 **NotificationHubAttributes** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2681-134">Specifies the **NotificationHubAttributes** object that contains configuration information for the hub that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f2681-135">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f2681-135">-ResourceGroup</span></span>
<span data-ttu-id="f2681-136">알림 허브가 할당 된 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2681-136">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="f2681-137">리소스 그룹은 관리 및 Azure 관리를 쉽게 할 수 있는 방식으로 네임 스페이스, 알림 허브, 권한 부여 규칙 등의 항목을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2681-137">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="f2681-138">-확인</span><span class="sxs-lookup"><span data-stu-id="f2681-138">-Confirm</span></span>
<span data-ttu-id="f2681-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2681-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2681-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2681-140">-WhatIf</span></span>
<span data-ttu-id="f2681-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f2681-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f2681-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f2681-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2681-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2681-143">CommonParameters</span></span>
<span data-ttu-id="f2681-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2681-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2681-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2681-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2681-146">입력</span><span class="sxs-lookup"><span data-stu-id="f2681-146">INPUTS</span></span>

### <span data-ttu-id="f2681-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f2681-147">System.String</span></span>

## <span data-ttu-id="f2681-148">출력</span><span class="sxs-lookup"><span data-stu-id="f2681-148">OUTPUTS</span></span>

### <span data-ttu-id="f2681-149">Microsoft. Azure. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="f2681-149">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="f2681-150">상속자</span><span class="sxs-lookup"><span data-stu-id="f2681-150">NOTES</span></span>

## <span data-ttu-id="f2681-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f2681-151">RELATED LINKS</span></span>

[<span data-ttu-id="f2681-152">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f2681-152">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="f2681-153">새로운 AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f2681-153">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="f2681-154">제거-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f2681-154">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)


