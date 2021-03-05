---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azactiongroupreceiver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
ms.openlocfilehash: 917f6287c40d4c26123217cccbf1dfc11866a488
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979904"
---
# <span data-ttu-id="47884-101">New-AzActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="47884-101">New-AzActionGroupReceiver</span></span>

## <span data-ttu-id="47884-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47884-102">SYNOPSIS</span></span>
<span data-ttu-id="47884-103">새 작업 그룹 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="47884-103">Creates an new action group receiver.</span></span>

## <span data-ttu-id="47884-104">구문</span><span class="sxs-lookup"><span data-stu-id="47884-104">SYNTAX</span></span>

### <span data-ttu-id="47884-105">NewEmailReceiver(기본값)</span><span class="sxs-lookup"><span data-stu-id="47884-105">NewEmailReceiver (Default)</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47884-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="47884-106">NewSmsReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-SmsReceiver] [-CountryCode <String>]
 -PhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47884-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="47884-107">NewWebhookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-WebhookReceiver] -ServiceUri <String>
 [-UseAadAuth] [-ObjectId <String>] [-IdentifierUri <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47884-108">NewItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="47884-108">NewItsmReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ItsmReceiver] -WorkspaceId <String>
 -ConnectionId <String> -TicketConfiguration <String> -Region <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47884-109">NewVoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="47884-109">NewVoiceReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-VoiceReceiver] [-VoiceCountryCode <String>]
 -VoicePhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47884-110">NewArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="47884-110">NewArmRoleReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ArmRoleReceiver] -RoleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47884-111">NewAzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="47884-111">NewAzureFunctionReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureFunctionReceiver]
 -FunctionAppResourceId <String> -HttpTriggerUrl <String> -FunctionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47884-112">NewLogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="47884-112">NewLogicAppReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-LogicAppReceiver] -ResourceId <String>
 -CallbackUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47884-113">NewAutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="47884-113">NewAutomationRunbookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AutomationRunbookReceiver]
 -AutomationAccountId <String> -RunbookName <String> [-IsGlobalRunbook] -AutomationRunbookServiceUri <String>
 -WebhookResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47884-114">NewAzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="47884-114">NewAzureAppPushReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureAppPushReceiver]
 -AzureAppPushEmailAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47884-115">설명</span><span class="sxs-lookup"><span data-stu-id="47884-115">DESCRIPTION</span></span>
<span data-ttu-id="47884-116">**New-AzActionGroupReceiver** cmdlet은 메모리에 새 작업 그룹 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="47884-116">The **New-AzActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="47884-117">예제</span><span class="sxs-lookup"><span data-stu-id="47884-117">EXAMPLES</span></span>

### <span data-ttu-id="47884-118">예제 1: 메모리에 새 전자 메일 수신기를 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="47884-118">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="47884-119">이 명령은 메모리에 새 전자 메일 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="47884-119">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="47884-120">예제 2: 메모리에 새 SMS 수신기를 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="47884-120">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="47884-121">이 명령은 메모리에 새 SMS 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="47884-121">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="47884-122">예제 3: 메모리에 새 웹후크 수신기를 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="47884-122">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzActionGroupReceiver -Name 'webhookReceiver1' -WebhookReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="47884-123">이 명령은 메모리에 새 웹후크 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="47884-123">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="47884-124">매개 변수</span><span class="sxs-lookup"><span data-stu-id="47884-124">PARAMETERS</span></span>

### <span data-ttu-id="47884-125">-ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="47884-125">-ArmRoleReceiver</span></span>
<span data-ttu-id="47884-126">ArmRoleReceiver 만들기</span><span class="sxs-lookup"><span data-stu-id="47884-126">Create a ArmRoleReceiver</span></span>

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

### <span data-ttu-id="47884-127">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="47884-127">-AutomationAccountId</span></span>
<span data-ttu-id="47884-128">AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="47884-128">the AutomationAccountId</span></span>

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

### <span data-ttu-id="47884-129">-AutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="47884-129">-AutomationRunbookReceiver</span></span>
<span data-ttu-id="47884-130">AutomationRunbookReceiver 만들기</span><span class="sxs-lookup"><span data-stu-id="47884-130">Create a AutomationRunbookReceiver</span></span>

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

### <span data-ttu-id="47884-131">-AutomationRunbookServiceUri</span><span class="sxs-lookup"><span data-stu-id="47884-131">-AutomationRunbookServiceUri</span></span>
<span data-ttu-id="47884-132">웹후크를 보내야 하는 URI</span><span class="sxs-lookup"><span data-stu-id="47884-132">the URI where webhooks should be sent</span></span>

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

### <span data-ttu-id="47884-133">-AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="47884-133">-AzureAppPushEmailAddress</span></span>
<span data-ttu-id="47884-134">AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="47884-134">the AzureAppPushEmailAddress</span></span>

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

### <span data-ttu-id="47884-135">-AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="47884-135">-AzureAppPushReceiver</span></span>
<span data-ttu-id="47884-136">AzureAppPushReceiver 만들기</span><span class="sxs-lookup"><span data-stu-id="47884-136">Create a AzureAppPushReceiver</span></span>

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

### <span data-ttu-id="47884-137">-AzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="47884-137">-AzureFunctionReceiver</span></span>
<span data-ttu-id="47884-138">ArmRoleReceiver 만들기</span><span class="sxs-lookup"><span data-stu-id="47884-138">Create a ArmRoleReceiver</span></span>

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

### <span data-ttu-id="47884-139">-CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="47884-139">-CallbackUrl</span></span>
<span data-ttu-id="47884-140">CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="47884-140">the CallbackUrl</span></span>

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

### <span data-ttu-id="47884-141">-ConnectionId</span><span class="sxs-lookup"><span data-stu-id="47884-141">-ConnectionId</span></span>
<span data-ttu-id="47884-142">이 수신기의 itsm 연결 ID</span><span class="sxs-lookup"><span data-stu-id="47884-142">the itsm connection id of this receiver</span></span>

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

### <span data-ttu-id="47884-143">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="47884-143">-CountryCode</span></span>
<span data-ttu-id="47884-144">SMS 수신기에 대한 국가 코드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="47884-144">Specifies the country code for the SMS receiver.</span></span>

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

### <span data-ttu-id="47884-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47884-145">-DefaultProfile</span></span>
<span data-ttu-id="47884-146">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="47884-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47884-147">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="47884-147">-EmailAddress</span></span>
<span data-ttu-id="47884-148">전자 메일 수신기에 대한 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="47884-148">Specifies the address for the Email receiver.</span></span>

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

### <span data-ttu-id="47884-149">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="47884-149">-EmailReceiver</span></span>
<span data-ttu-id="47884-150">전자 메일 수신기 만들기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="47884-150">Specifies to create an Email receiver</span></span>

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

### <span data-ttu-id="47884-151">-FunctionAppResourceId</span><span class="sxs-lookup"><span data-stu-id="47884-151">-FunctionAppResourceId</span></span>
<span data-ttu-id="47884-152">함수 앱 resourceId</span><span class="sxs-lookup"><span data-stu-id="47884-152">the function app resourceId</span></span>

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

### <span data-ttu-id="47884-153">-FunctionName</span><span class="sxs-lookup"><span data-stu-id="47884-153">-FunctionName</span></span>
<span data-ttu-id="47884-154">functionName</span><span class="sxs-lookup"><span data-stu-id="47884-154">the functionName</span></span>

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

### <span data-ttu-id="47884-155">-HttpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="47884-155">-HttpTriggerUrl</span></span>
<span data-ttu-id="47884-156">httpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="47884-156">the httpTriggerUrl</span></span>

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

### <span data-ttu-id="47884-157">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="47884-157">-IdentifierUri</span></span>
<span data-ttu-id="47884-158">aad auth에 대한 식별자 uri</span><span class="sxs-lookup"><span data-stu-id="47884-158">the Identifier uri for aad auth</span></span>

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

### <span data-ttu-id="47884-159">-IsGlobalRunbook</span><span class="sxs-lookup"><span data-stu-id="47884-159">-IsGlobalRunbook</span></span>
<span data-ttu-id="47884-160">이 인스턴스가 전역 Runbook인지 여부를 나타내는</span><span class="sxs-lookup"><span data-stu-id="47884-160">indicating whether this instance is global runbook</span></span>

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

### <span data-ttu-id="47884-161">-ItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="47884-161">-ItsmReceiver</span></span>
<span data-ttu-id="47884-162">ItsmReceiver 만들기</span><span class="sxs-lookup"><span data-stu-id="47884-162">Create a ItsmReceiver</span></span>

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

### <span data-ttu-id="47884-163">-LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="47884-163">-LogicAppReceiver</span></span>
<span data-ttu-id="47884-164">LogicAppReceiver 만들기</span><span class="sxs-lookup"><span data-stu-id="47884-164">Create a LogicAppReceiver</span></span>

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

### <span data-ttu-id="47884-165">-Name</span><span class="sxs-lookup"><span data-stu-id="47884-165">-Name</span></span>
<span data-ttu-id="47884-166">수신기에 대한 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="47884-166">Specifies the name for the receiver.</span></span>

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

### <span data-ttu-id="47884-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="47884-167">-ObjectId</span></span>
<span data-ttu-id="47884-168">aad auth에 대한 webhook 앱 개체 ID</span><span class="sxs-lookup"><span data-stu-id="47884-168">the webhook app object Id for aad auth</span></span>

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

### <span data-ttu-id="47884-169">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="47884-169">-PhoneNumber</span></span>
<span data-ttu-id="47884-170">SMS 수신기에 대한 전화 번호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="47884-170">Specifies the phone number for the SMS receiver.</span></span>

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

### <span data-ttu-id="47884-171">-Region</span><span class="sxs-lookup"><span data-stu-id="47884-171">-Region</span></span>
<span data-ttu-id="47884-172">이 수신기의 itsm 지역</span><span class="sxs-lookup"><span data-stu-id="47884-172">the itsm Region of this receiver</span></span>

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

### <span data-ttu-id="47884-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47884-173">-ResourceId</span></span>
<span data-ttu-id="47884-174">ResourceId</span><span class="sxs-lookup"><span data-stu-id="47884-174">the ResourceId</span></span>

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

### <span data-ttu-id="47884-175">-RoleId</span><span class="sxs-lookup"><span data-stu-id="47884-175">-RoleId</span></span>
<span data-ttu-id="47884-176">수신기의 암 역할 ID</span><span class="sxs-lookup"><span data-stu-id="47884-176">The arm role id of the receiver</span></span>

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

### <span data-ttu-id="47884-177">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="47884-177">-RunbookName</span></span>
<span data-ttu-id="47884-178">RunbookName</span><span class="sxs-lookup"><span data-stu-id="47884-178">the RunbookName</span></span>

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

### <span data-ttu-id="47884-179">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="47884-179">-ServiceUri</span></span>
<span data-ttu-id="47884-180">웹후크 수신기에 대한 URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="47884-180">Specifies the URI for the webhook receiver.</span></span>

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

### <span data-ttu-id="47884-181">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="47884-181">-SmsReceiver</span></span>
<span data-ttu-id="47884-182">SMS 수신기 만들기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="47884-182">Specifies to create a SMS receiver</span></span>

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

### <span data-ttu-id="47884-183">-TenantId</span><span class="sxs-lookup"><span data-stu-id="47884-183">-TenantId</span></span>
<span data-ttu-id="47884-184">aad auth에 대한 테넌트 ID</span><span class="sxs-lookup"><span data-stu-id="47884-184">the tenant id for aad auth</span></span>

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

### <span data-ttu-id="47884-185">-TicketConfiguration</span><span class="sxs-lookup"><span data-stu-id="47884-185">-TicketConfiguration</span></span>
<span data-ttu-id="47884-186">이 수신기의 itsm TicketConfiguration</span><span class="sxs-lookup"><span data-stu-id="47884-186">the itsm TicketConfiguration of this receiver</span></span>

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

### <span data-ttu-id="47884-187">-UseAadAuth</span><span class="sxs-lookup"><span data-stu-id="47884-187">-UseAadAuth</span></span>
<span data-ttu-id="47884-188">추가 auth를 사용할 플래그</span><span class="sxs-lookup"><span data-stu-id="47884-188">the flag to use add auth</span></span>

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

### <span data-ttu-id="47884-189">-UseCommonAlertSchema</span><span class="sxs-lookup"><span data-stu-id="47884-189">-UseCommonAlertSchema</span></span>
<span data-ttu-id="47884-190">일반적인 경고를 사용할지 여부를 플래그로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="47884-190">The flag whether to use common alert schema .</span></span> <span data-ttu-id="47884-191">이 값은 SMS, Azure App push, ITSM 및 Voice recievers에서 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="47884-191">This value will be neglectedfor SMS, Azure App push , ITSM and Voice recievers.</span></span>

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

### <span data-ttu-id="47884-192">-VoiceCountryCode</span><span class="sxs-lookup"><span data-stu-id="47884-192">-VoiceCountryCode</span></span>
<span data-ttu-id="47884-193">음성 수신기의 국가 코드</span><span class="sxs-lookup"><span data-stu-id="47884-193">The country code of the voice receiver</span></span>

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

### <span data-ttu-id="47884-194">-VoicePhoneNumber</span><span class="sxs-lookup"><span data-stu-id="47884-194">-VoicePhoneNumber</span></span>
<span data-ttu-id="47884-195">음성 수신기의 전화 번호</span><span class="sxs-lookup"><span data-stu-id="47884-195">The phone number of the voice receiver</span></span>

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

### <span data-ttu-id="47884-196">-VoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="47884-196">-VoiceReceiver</span></span>
<span data-ttu-id="47884-197">음성 수신기 만들기</span><span class="sxs-lookup"><span data-stu-id="47884-197">Create a voice receiver</span></span>

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

### <span data-ttu-id="47884-198">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="47884-198">-WebhookReceiver</span></span>
<span data-ttu-id="47884-199">웹후크 수신기 만들기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="47884-199">Specifies to create a webhook receiver</span></span>

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

### <span data-ttu-id="47884-200">-WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="47884-200">-WebhookResourceId</span></span>
<span data-ttu-id="47884-201">WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="47884-201">the WebhookResourceId</span></span>

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

### <span data-ttu-id="47884-202">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="47884-202">-WorkspaceId</span></span>
<span data-ttu-id="47884-203">이 수신기의 itsm 작업 영역 ID</span><span class="sxs-lookup"><span data-stu-id="47884-203">the itsm workspace id of this receiver</span></span>

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

### <span data-ttu-id="47884-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47884-204">CommonParameters</span></span>
<span data-ttu-id="47884-205">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="47884-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47884-206">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47884-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47884-207">입력</span><span class="sxs-lookup"><span data-stu-id="47884-207">INPUTS</span></span>

### <span data-ttu-id="47884-208">System.String</span><span class="sxs-lookup"><span data-stu-id="47884-208">System.String</span></span>

### <span data-ttu-id="47884-209">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="47884-209">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="47884-210">출력</span><span class="sxs-lookup"><span data-stu-id="47884-210">OUTPUTS</span></span>

### <span data-ttu-id="47884-211">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="47884-211">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="47884-212">참고 사항</span><span class="sxs-lookup"><span data-stu-id="47884-212">NOTES</span></span>

## <span data-ttu-id="47884-213">관련 링크</span><span class="sxs-lookup"><span data-stu-id="47884-213">RELATED LINKS</span></span>

<span data-ttu-id="47884-214">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="47884-214">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span></span>
