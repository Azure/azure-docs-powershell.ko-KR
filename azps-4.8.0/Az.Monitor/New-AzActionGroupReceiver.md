---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroupreceiver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
ms.openlocfilehash: f2862c08212f5e41de10cb600edb22c38eac68d4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211810"
---
# <span data-ttu-id="6afc3-101">New-AzActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="6afc3-101">New-AzActionGroupReceiver</span></span>

## <span data-ttu-id="6afc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6afc3-102">SYNOPSIS</span></span>
<span data-ttu-id="6afc3-103">새 작업 그룹 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6afc3-103">Creates an new action group receiver.</span></span>

## <span data-ttu-id="6afc3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6afc3-104">SYNTAX</span></span>

### <span data-ttu-id="6afc3-105">NewEmailReceiver (기본값)</span><span class="sxs-lookup"><span data-stu-id="6afc3-105">NewEmailReceiver (Default)</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6afc3-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="6afc3-106">NewSmsReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-SmsReceiver] [-CountryCode <String>]
 -PhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6afc3-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="6afc3-107">NewWebhookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-WebhookReceiver] -ServiceUri <String>
 [-UseAadAuth] [-ObjectId <String>] [-IdentifierUri <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6afc3-108">NewItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="6afc3-108">NewItsmReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ItsmReceiver] -WorkspaceId <String>
 -ConnectionId <String> -TicketConfiguration <String> -Region <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6afc3-109">NewVoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="6afc3-109">NewVoiceReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-VoiceReceiver] [-VoiceCountryCode <String>]
 -VoicePhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6afc3-110">NewArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="6afc3-110">NewArmRoleReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ArmRoleReceiver] -RoleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6afc3-111">NewAzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="6afc3-111">NewAzureFunctionReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureFunctionReceiver]
 -FunctionAppResourceId <String> -HttpTriggerUrl <String> -FunctionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6afc3-112">NewLogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="6afc3-112">NewLogicAppReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-LogicAppReceiver] -ResourceId <String>
 -CallbackUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6afc3-113">NewAutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="6afc3-113">NewAutomationRunbookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AutomationRunbookReceiver]
 -AutomationAccountId <String> -RunbookName <String> [-IsGlobalRunbook] -AutomationRunbookServiceUri <String>
 -WebhookResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6afc3-114">NewAzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="6afc3-114">NewAzureAppPushReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureAppPushReceiver]
 -AzureAppPushEmailAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6afc3-115">설명은</span><span class="sxs-lookup"><span data-stu-id="6afc3-115">DESCRIPTION</span></span>
<span data-ttu-id="6afc3-116">**새 AzActionGroupReceiver** cmdlet은 메모리에 새 동작 그룹 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6afc3-116">The **New-AzActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="6afc3-117">예제의</span><span class="sxs-lookup"><span data-stu-id="6afc3-117">EXAMPLES</span></span>

### <span data-ttu-id="6afc3-118">예제 1: 메모리에서 새 전자 메일 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6afc3-118">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="6afc3-119">이 명령은 메모리에 새 전자 메일 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6afc3-119">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="6afc3-120">예제 2: 메모리에 새 SMS 받는 사람 만들기</span><span class="sxs-lookup"><span data-stu-id="6afc3-120">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="6afc3-121">이 명령은 메모리에 새 SMS 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6afc3-121">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="6afc3-122">예제 3: 메모리에 새 webhook 수신기 만들기</span><span class="sxs-lookup"><span data-stu-id="6afc3-122">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzActionGroupReceiver -Name 'webhookReceiver1' -WebhookReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="6afc3-123">이 명령은 메모리에 새 webhook 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6afc3-123">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="6afc3-124">변수</span><span class="sxs-lookup"><span data-stu-id="6afc3-124">PARAMETERS</span></span>

### <span data-ttu-id="6afc3-125">-ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="6afc3-125">-ArmRoleReceiver</span></span>
<span data-ttu-id="6afc3-126">ArmRoleReceiver 만들기</span><span class="sxs-lookup"><span data-stu-id="6afc3-126">Create a ArmRoleReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewArmRoleReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afc3-127">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="6afc3-127">-AutomationAccountId</span></span>
<span data-ttu-id="6afc3-128">AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="6afc3-128">the AutomationAccountId</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afc3-129">-AutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="6afc3-129">-AutomationRunbookReceiver</span></span>
<span data-ttu-id="6afc3-130">AutomationRunbookReceiver 만들기</span><span class="sxs-lookup"><span data-stu-id="6afc3-130">Create a AutomationRunbookReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afc3-131">-AutomationRunbookServiceUri</span><span class="sxs-lookup"><span data-stu-id="6afc3-131">-AutomationRunbookServiceUri</span></span>
<span data-ttu-id="6afc3-132">webhooks를 보낼 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="6afc3-132">the URI where webhooks should be sent</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afc3-133">-AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="6afc3-133">-AzureAppPushEmailAddress</span></span>
<span data-ttu-id="6afc3-134">AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="6afc3-134">the AzureAppPushEmailAddress</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureAppPushReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afc3-135">-AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="6afc3-135">-AzureAppPushReceiver</span></span>
<span data-ttu-id="6afc3-136">AzureAppPushReceiver 만들기</span><span class="sxs-lookup"><span data-stu-id="6afc3-136">Create a AzureAppPushReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAzureAppPushReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afc3-137">-AzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="6afc3-137">-AzureFunctionReceiver</span></span>
<span data-ttu-id="6afc3-138">ArmRoleReceiver 만들기</span><span class="sxs-lookup"><span data-stu-id="6afc3-138">Create a ArmRoleReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afc3-139">-CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="6afc3-139">-CallbackUrl</span></span>
<span data-ttu-id="6afc3-140">CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="6afc3-140">the CallbackUrl</span></span>

```yaml
Type: System.String
Parameter Sets: NewLogicAppReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afc3-141">-ConnectionId</span><span class="sxs-lookup"><span data-stu-id="6afc3-141">-ConnectionId</span></span>
<span data-ttu-id="6afc3-142">이 수신기의 itsm 연결 id</span><span class="sxs-lookup"><span data-stu-id="6afc3-142">the itsm connection id of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afc3-143">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="6afc3-143">-CountryCode</span></span>
<span data-ttu-id="6afc3-144">SMS 받는 사람에 대 한 국가 코드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6afc3-144">Specifies the country code for the SMS receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSmsReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afc3-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6afc3-145">-DefaultProfile</span></span>
<span data-ttu-id="6afc3-146">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6afc3-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6afc3-147">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="6afc3-147">-EmailAddress</span></span>
<span data-ttu-id="6afc3-148">전자 메일 받는 사람에 대 한 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6afc3-148">Specifies the address for the Email receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewEmailReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afc3-149">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="6afc3-149">-EmailReceiver</span></span>
<span data-ttu-id="6afc3-150">전자 메일 받는 사람 만들기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6afc3-150">Specifies to create an Email receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewEmailReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afc3-151">-Functionap보도 Ourceid</span><span class="sxs-lookup"><span data-stu-id="6afc3-151">-FunctionAppResourceId</span></span>
<span data-ttu-id="6afc3-152">함수 앱 resourceId</span><span class="sxs-lookup"><span data-stu-id="6afc3-152">the function app resourceId</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afc3-153">-FunctionName</span><span class="sxs-lookup"><span data-stu-id="6afc3-153">-FunctionName</span></span>
<span data-ttu-id="6afc3-154">functionName</span><span class="sxs-lookup"><span data-stu-id="6afc3-154">the functionName</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afc3-155">-HttpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="6afc3-155">-HttpTriggerUrl</span></span>
<span data-ttu-id="6afc3-156">httpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="6afc3-156">the httpTriggerUrl</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afc3-157">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="6afc3-157">-IdentifierUri</span></span>
<span data-ttu-id="6afc3-158">aad 인증의 식별자 uri</span><span class="sxs-lookup"><span data-stu-id="6afc3-158">the Identifier uri for aad auth</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afc3-159">-IsGlobalRunbook</span><span class="sxs-lookup"><span data-stu-id="6afc3-159">-IsGlobalRunbook</span></span>
<span data-ttu-id="6afc3-160">이 인스턴스가 전역 runbook 인지 여부를 나타내는</span><span class="sxs-lookup"><span data-stu-id="6afc3-160">indicating whether this instance is global runbook</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afc3-161">-ItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="6afc3-161">-ItsmReceiver</span></span>
<span data-ttu-id="6afc3-162">ItsmReceiver 만들기</span><span class="sxs-lookup"><span data-stu-id="6afc3-162">Create a ItsmReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewItsmReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afc3-163">-LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="6afc3-163">-LogicAppReceiver</span></span>
<span data-ttu-id="6afc3-164">LogicAppReceiver 만들기</span><span class="sxs-lookup"><span data-stu-id="6afc3-164">Create a LogicAppReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewLogicAppReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afc3-165">-이름</span><span class="sxs-lookup"><span data-stu-id="6afc3-165">-Name</span></span>
<span data-ttu-id="6afc3-166">수신자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6afc3-166">Specifies the name for the receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afc3-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="6afc3-167">-ObjectId</span></span>
<span data-ttu-id="6afc3-168">aad 인증의 webhook 앱 개체 Id</span><span class="sxs-lookup"><span data-stu-id="6afc3-168">the webhook app object Id for aad auth</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afc3-169">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="6afc3-169">-PhoneNumber</span></span>
<span data-ttu-id="6afc3-170">SMS 받는 사람에 대 한 전화 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6afc3-170">Specifies the phone number for the SMS receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSmsReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afc3-171">-지역</span><span class="sxs-lookup"><span data-stu-id="6afc3-171">-Region</span></span>
<span data-ttu-id="6afc3-172">이 수신기의 itsm 지역</span><span class="sxs-lookup"><span data-stu-id="6afc3-172">the itsm Region of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afc3-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6afc3-173">-ResourceId</span></span>
<span data-ttu-id="6afc3-174">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6afc3-174">the ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: NewLogicAppReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afc3-175">-RoleId</span><span class="sxs-lookup"><span data-stu-id="6afc3-175">-RoleId</span></span>
<span data-ttu-id="6afc3-176">수신자의 arm 역할 id</span><span class="sxs-lookup"><span data-stu-id="6afc3-176">The arm role id of the receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewArmRoleReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afc3-177">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="6afc3-177">-RunbookName</span></span>
<span data-ttu-id="6afc3-178">RunbookName</span><span class="sxs-lookup"><span data-stu-id="6afc3-178">the RunbookName</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afc3-179">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="6afc3-179">-ServiceUri</span></span>
<span data-ttu-id="6afc3-180">Webhook 수신기에 대 한 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6afc3-180">Specifies the URI for the webhook receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afc3-181">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="6afc3-181">-SmsReceiver</span></span>
<span data-ttu-id="6afc3-182">SMS 받는 사람 만들기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6afc3-182">Specifies to create a SMS receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewSmsReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afc3-183">-TenantId</span><span class="sxs-lookup"><span data-stu-id="6afc3-183">-TenantId</span></span>
<span data-ttu-id="6afc3-184">aad 인증의 테 넌 트 id</span><span class="sxs-lookup"><span data-stu-id="6afc3-184">the tenant id for aad auth</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afc3-185">-TicketConfiguration</span><span class="sxs-lookup"><span data-stu-id="6afc3-185">-TicketConfiguration</span></span>
<span data-ttu-id="6afc3-186">이 수신기의 itsm TicketConfiguration</span><span class="sxs-lookup"><span data-stu-id="6afc3-186">the itsm TicketConfiguration of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afc3-187">-UseAadAuth</span><span class="sxs-lookup"><span data-stu-id="6afc3-187">-UseAadAuth</span></span>
<span data-ttu-id="6afc3-188">auth 추가를 사용 하는 플래그</span><span class="sxs-lookup"><span data-stu-id="6afc3-188">the flag to use add auth</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afc3-189">-UseCommonAlertSchema</span><span class="sxs-lookup"><span data-stu-id="6afc3-189">-UseCommonAlertSchema</span></span>
<span data-ttu-id="6afc3-190">공용 경고 스키마를 사용할지 여부를 나타내는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="6afc3-190">The flag whether to use common alert schema .</span></span> <span data-ttu-id="6afc3-191">이 값은 neglectedfor SMS, Azure App push, ITSM 및 음성 recievers 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6afc3-191">This value will be neglectedfor SMS, Azure App push , ITSM and Voice recievers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afc3-192">-VoiceCountryCode</span><span class="sxs-lookup"><span data-stu-id="6afc3-192">-VoiceCountryCode</span></span>
<span data-ttu-id="6afc3-193">음성 수신기의 국가 코드</span><span class="sxs-lookup"><span data-stu-id="6afc3-193">The country code of the voice receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewVoiceReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afc3-194">-VoicePhoneNumber</span><span class="sxs-lookup"><span data-stu-id="6afc3-194">-VoicePhoneNumber</span></span>
<span data-ttu-id="6afc3-195">음성 수신기의 전화 번호</span><span class="sxs-lookup"><span data-stu-id="6afc3-195">The phone number of the voice receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewVoiceReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afc3-196">-VoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="6afc3-196">-VoiceReceiver</span></span>
<span data-ttu-id="6afc3-197">음성 수신기 만들기</span><span class="sxs-lookup"><span data-stu-id="6afc3-197">Create a voice receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewVoiceReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afc3-198">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="6afc3-198">-WebhookReceiver</span></span>
<span data-ttu-id="6afc3-199">Webhook 수신기를 만들도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6afc3-199">Specifies to create a webhook receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afc3-200">-WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="6afc3-200">-WebhookResourceId</span></span>
<span data-ttu-id="6afc3-201">WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="6afc3-201">the WebhookResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afc3-202">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="6afc3-202">-WorkspaceId</span></span>
<span data-ttu-id="6afc3-203">이 수신기의 itsm 작업 영역 id</span><span class="sxs-lookup"><span data-stu-id="6afc3-203">the itsm workspace id of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6afc3-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6afc3-204">CommonParameters</span></span>
<span data-ttu-id="6afc3-205">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6afc3-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6afc3-206">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6afc3-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6afc3-207">입력</span><span class="sxs-lookup"><span data-stu-id="6afc3-207">INPUTS</span></span>

### <span data-ttu-id="6afc3-208">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6afc3-208">System.String</span></span>

### <span data-ttu-id="6afc3-209">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6afc3-209">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6afc3-210">출력</span><span class="sxs-lookup"><span data-stu-id="6afc3-210">OUTPUTS</span></span>

### <span data-ttu-id="6afc3-211">PSActionGroupReceiverBase를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="6afc3-211">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="6afc3-212">상속자</span><span class="sxs-lookup"><span data-stu-id="6afc3-212">NOTES</span></span>

## <span data-ttu-id="6afc3-213">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6afc3-213">RELATED LINKS</span></span>

<span data-ttu-id="6afc3-214">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [제거-AzActionGroup](./Remove-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="6afc3-214">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span></span>
