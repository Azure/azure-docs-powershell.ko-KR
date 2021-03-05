---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/powershell/module/az.communication/set-azcommunicationservicenotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Set-AzCommunicationServiceNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Set-AzCommunicationServiceNotificationHub.md
ms.openlocfilehash: 1dbdbc6a616e9903c6a79192d089ea959835a9f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991592"
---
# <span data-ttu-id="cea91-101">Set-AzCommunicationServiceNotificationHub</span><span class="sxs-lookup"><span data-stu-id="cea91-101">Set-AzCommunicationServiceNotificationHub</span></span>

## <span data-ttu-id="cea91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cea91-102">SYNOPSIS</span></span>
<span data-ttu-id="cea91-103">Azure Notification Hub를 이 통신 서비스에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="cea91-103">Links an Azure Notification Hub to this communication service.</span></span>

## <span data-ttu-id="cea91-104">구문</span><span class="sxs-lookup"><span data-stu-id="cea91-104">SYNTAX</span></span>

### <span data-ttu-id="cea91-105">LinkExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="cea91-105">LinkExpanded (Default)</span></span>
```
Set-AzCommunicationServiceNotificationHub -CommunicationServiceName <String> -ResourceGroupName <String>
 -ConnectionString <String> -NotificationHubResourceId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cea91-106">링크</span><span class="sxs-lookup"><span data-stu-id="cea91-106">Link</span></span>
```
Set-AzCommunicationServiceNotificationHub -CommunicationServiceName <String> -ResourceGroupName <String>
 -LinkNotificationHubParameter <ILinkNotificationHubParameters> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cea91-107">설명</span><span class="sxs-lookup"><span data-stu-id="cea91-107">DESCRIPTION</span></span>
<span data-ttu-id="cea91-108">Azure Notification Hub를 이 통신 서비스에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="cea91-108">Links an Azure Notification Hub to this communication service.</span></span>

## <span data-ttu-id="cea91-109">예제</span><span class="sxs-lookup"><span data-stu-id="cea91-109">EXAMPLES</span></span>

### <span data-ttu-id="cea91-110">예제 1: 알림 허브 세부 정보 대화형 제공</span><span class="sxs-lookup"><span data-stu-id="cea91-110">Example 1: Provide Notification Hub details interactively</span></span>
```powershell
PS C:\> Set-AzCommunicationServiceNotificationHub -CommunicationServiceName ContosoAcsResource2 -ResourceGroupName ContosoResourceProvider1 -ConnectionString "<notificationhub-connectionstring>" -NotificationHubResourceId "<notificationhub-resourceid>"
```

<span data-ttu-id="cea91-111">연결된 알림 허브를 사용하면 ACS 리소스가 특정 이벤트에 대한 알림을 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cea91-111">A linked notification hub allows a ACS resource to send notifications for certain events.</span></span>

## <span data-ttu-id="cea91-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="cea91-112">PARAMETERS</span></span>

### <span data-ttu-id="cea91-113">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="cea91-113">-CommunicationServiceName</span></span>
<span data-ttu-id="cea91-114">CommunicationService 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cea91-114">The name of the CommunicationService resource.</span></span>

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

### <span data-ttu-id="cea91-115">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="cea91-115">-ConnectionString</span></span>
<span data-ttu-id="cea91-116">알림 허브에 대한 연결 문자열</span><span class="sxs-lookup"><span data-stu-id="cea91-116">Connection string for the notification hub</span></span>

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

### <span data-ttu-id="cea91-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cea91-117">-DefaultProfile</span></span>
<span data-ttu-id="cea91-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cea91-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cea91-119">-LinkNotificationHubParameter</span><span class="sxs-lookup"><span data-stu-id="cea91-119">-LinkNotificationHubParameter</span></span>
<span data-ttu-id="cea91-120">통신 서비스에 연결하기 위한 Azure Notification Hub에 대한 설명을 구성하려면 LINKNOTIFICATIONHUBPARAMETER 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="cea91-120">Description of an Azure Notification Hub to link to the communication service To construct, see NOTES section for LINKNOTIFICATIONHUBPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="cea91-121">-NotificationHubResourceId</span><span class="sxs-lookup"><span data-stu-id="cea91-121">-NotificationHubResourceId</span></span>
<span data-ttu-id="cea91-122">알림 허브의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="cea91-122">The resource ID of the notification hub</span></span>

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

### <span data-ttu-id="cea91-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cea91-123">-ResourceGroupName</span></span>
<span data-ttu-id="cea91-124">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cea91-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="cea91-125">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cea91-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="cea91-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cea91-126">-SubscriptionId</span></span>
<span data-ttu-id="cea91-127">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cea91-127">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="cea91-128">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="cea91-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cea91-129">-확인</span><span class="sxs-lookup"><span data-stu-id="cea91-129">-Confirm</span></span>
<span data-ttu-id="cea91-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cea91-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cea91-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cea91-131">-WhatIf</span></span>
<span data-ttu-id="cea91-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="cea91-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cea91-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cea91-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cea91-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cea91-134">CommonParameters</span></span>
<span data-ttu-id="cea91-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cea91-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cea91-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cea91-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cea91-137">입력</span><span class="sxs-lookup"><span data-stu-id="cea91-137">INPUTS</span></span>

### <span data-ttu-id="cea91-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ILinkNotificationHubParameters</span><span class="sxs-lookup"><span data-stu-id="cea91-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ILinkNotificationHubParameters</span></span>

## <span data-ttu-id="cea91-139">출력</span><span class="sxs-lookup"><span data-stu-id="cea91-139">OUTPUTS</span></span>

### <span data-ttu-id="cea91-140">System.String</span><span class="sxs-lookup"><span data-stu-id="cea91-140">System.String</span></span>

## <span data-ttu-id="cea91-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cea91-141">NOTES</span></span>

<span data-ttu-id="cea91-142">별칭</span><span class="sxs-lookup"><span data-stu-id="cea91-142">ALIASES</span></span>

<span data-ttu-id="cea91-143">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="cea91-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cea91-144">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="cea91-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cea91-145">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cea91-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cea91-146">LINKNOTIFICATIONHUBPARAMETER : 통신 서비스에 연결하기 위한 Azure Notification Hub에 대한 <ILinkNotificationHubParameters> 설명</span><span class="sxs-lookup"><span data-stu-id="cea91-146">LINKNOTIFICATIONHUBPARAMETER <ILinkNotificationHubParameters>: Description of an Azure Notification Hub to link to the communication service</span></span>
  - <span data-ttu-id="cea91-147">`ConnectionString <String>`: 알림 허브에 대한 연결 문자열</span><span class="sxs-lookup"><span data-stu-id="cea91-147">`ConnectionString <String>`: Connection string for the notification hub</span></span>
  - <span data-ttu-id="cea91-148">`ResourceId <String>`: 알림 허브의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="cea91-148">`ResourceId <String>`: The resource ID of the notification hub</span></span>

## <span data-ttu-id="cea91-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cea91-149">RELATED LINKS</span></span>

