---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/set-azcommunicationservicenotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Set-AzCommunicationServiceNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Set-AzCommunicationServiceNotificationHub.md
ms.openlocfilehash: aa9084f067131abb780de798dcd1af0ed8f9d235
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493927"
---
# <span data-ttu-id="93e71-101">Set-AzCommunicationServiceNotificationHub</span><span class="sxs-lookup"><span data-stu-id="93e71-101">Set-AzCommunicationServiceNotificationHub</span></span>

## <span data-ttu-id="93e71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93e71-102">SYNOPSIS</span></span>
<span data-ttu-id="93e71-103">Azure Notification Hub를 이 통신 서비스에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="93e71-103">Links an Azure Notification Hub to this communication service.</span></span>

## <span data-ttu-id="93e71-104">구문</span><span class="sxs-lookup"><span data-stu-id="93e71-104">SYNTAX</span></span>

### <span data-ttu-id="93e71-105">LinkExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="93e71-105">LinkExpanded (Default)</span></span>
```
Set-AzCommunicationServiceNotificationHub -CommunicationServiceName <String> -ResourceGroupName <String>
 -ConnectionString <String> -NotificationHubResourceId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="93e71-106">링크</span><span class="sxs-lookup"><span data-stu-id="93e71-106">Link</span></span>
```
Set-AzCommunicationServiceNotificationHub -CommunicationServiceName <String> -ResourceGroupName <String>
 -LinkNotificationHubParameter <ILinkNotificationHubParameters> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="93e71-107">설명</span><span class="sxs-lookup"><span data-stu-id="93e71-107">DESCRIPTION</span></span>
<span data-ttu-id="93e71-108">Azure Notification Hub를 이 통신 서비스에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="93e71-108">Links an Azure Notification Hub to this communication service.</span></span>

## <span data-ttu-id="93e71-109">예제</span><span class="sxs-lookup"><span data-stu-id="93e71-109">EXAMPLES</span></span>

### <span data-ttu-id="93e71-110">예제 1: 대화형으로 알림 허브 세부 정보 제공</span><span class="sxs-lookup"><span data-stu-id="93e71-110">Example 1: Provide Notification Hub details interactively</span></span>
```powershell
PS C:\> Set-AzCommunicationServiceNotificationHub -CommunicationServiceName ContosoAcsResource2 -ResourceGroupName ContosoResourceProvider1 -ConnectionString "<notificationhub-connectionstring>" -NotificationHubResourceId "<notificationhub-resourceid>"
```

<span data-ttu-id="93e71-111">연결된 알림 허브를 사용하면 ACS 리소스가 특정 이벤트에 대한 알림을 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93e71-111">A linked notification hub allows a ACS resource to send notifications for certain events.</span></span>

## <span data-ttu-id="93e71-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93e71-112">PARAMETERS</span></span>

### <span data-ttu-id="93e71-113">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="93e71-113">-CommunicationServiceName</span></span>
<span data-ttu-id="93e71-114">CommunicationService 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="93e71-114">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93e71-115">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="93e71-115">-ConnectionString</span></span>
<span data-ttu-id="93e71-116">알림 허브에 대한 연결 문자열</span><span class="sxs-lookup"><span data-stu-id="93e71-116">Connection string for the notification hub</span></span>

```yaml
Type: System.String
Parameter Sets: LinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93e71-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93e71-117">-DefaultProfile</span></span>
<span data-ttu-id="93e71-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="93e71-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93e71-119">-LinkNotificationHubParameter</span><span class="sxs-lookup"><span data-stu-id="93e71-119">-LinkNotificationHubParameter</span></span>
<span data-ttu-id="93e71-120">통신 서비스에 연결하기 위한 Azure 알림 허브에 대한 설명은 LINKNOTIFICATIONHUBPARAMETER 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="93e71-120">Description of an Azure Notification Hub to link to the communication service To construct, see NOTES section for LINKNOTIFICATIONHUBPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ILinkNotificationHubParameters
Parameter Sets: Link
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93e71-121">-NotificationHubResourceId</span><span class="sxs-lookup"><span data-stu-id="93e71-121">-NotificationHubResourceId</span></span>
<span data-ttu-id="93e71-122">알림 허브의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="93e71-122">The resource ID of the notification hub</span></span>

```yaml
Type: System.String
Parameter Sets: LinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93e71-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93e71-123">-ResourceGroupName</span></span>
<span data-ttu-id="93e71-124">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="93e71-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="93e71-125">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93e71-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93e71-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="93e71-126">-SubscriptionId</span></span>
<span data-ttu-id="93e71-127">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="93e71-127">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="93e71-128">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="93e71-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93e71-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93e71-129">-Confirm</span></span>
<span data-ttu-id="93e71-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="93e71-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93e71-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93e71-131">-WhatIf</span></span>
<span data-ttu-id="93e71-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="93e71-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93e71-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="93e71-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93e71-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93e71-134">CommonParameters</span></span>
<span data-ttu-id="93e71-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="93e71-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93e71-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="93e71-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93e71-137">입력</span><span class="sxs-lookup"><span data-stu-id="93e71-137">INPUTS</span></span>

### <span data-ttu-id="93e71-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ILinkNotificationHubParameters</span><span class="sxs-lookup"><span data-stu-id="93e71-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ILinkNotificationHubParameters</span></span>

## <span data-ttu-id="93e71-139">출력</span><span class="sxs-lookup"><span data-stu-id="93e71-139">OUTPUTS</span></span>

### <span data-ttu-id="93e71-140">System.String</span><span class="sxs-lookup"><span data-stu-id="93e71-140">System.String</span></span>

## <span data-ttu-id="93e71-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="93e71-141">NOTES</span></span>

<span data-ttu-id="93e71-142">별칭</span><span class="sxs-lookup"><span data-stu-id="93e71-142">ALIASES</span></span>

<span data-ttu-id="93e71-143">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="93e71-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="93e71-144">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="93e71-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="93e71-145">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="93e71-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="93e71-146">LINKNOTIFICATIONHUBPARAMETER: 통신 서비스에 연결하기 위한 Azure 알림 허브에 <ILinkNotificationHubParameters> 대한 설명</span><span class="sxs-lookup"><span data-stu-id="93e71-146">LINKNOTIFICATIONHUBPARAMETER <ILinkNotificationHubParameters>: Description of an Azure Notification Hub to link to the communication service</span></span>
  - <span data-ttu-id="93e71-147">`ConnectionString <String>`: 알림 허브에 대한 연결 문자열</span><span class="sxs-lookup"><span data-stu-id="93e71-147">`ConnectionString <String>`: Connection string for the notification hub</span></span>
  - <span data-ttu-id="93e71-148">`ResourceId <String>`: 알림 허브의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="93e71-148">`ResourceId <String>`: The resource ID of the notification hub</span></span>

## <span data-ttu-id="93e71-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="93e71-149">RELATED LINKS</span></span>

