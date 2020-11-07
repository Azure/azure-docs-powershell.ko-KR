---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
ms.openlocfilehash: ca7fe171e95d87dd054f0dac27e1a5ccd07396a3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868057"
---
# <span data-ttu-id="9f599-101">Set-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="9f599-101">Set-AzIotHub</span></span>

## <span data-ttu-id="9f599-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f599-102">SYNOPSIS</span></span>
<span data-ttu-id="9f599-103">IotHub의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f599-103">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="9f599-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9f599-104">SYNTAX</span></span>

### <span data-ttu-id="9f599-105">UpdateSku (기본값)</span><span class="sxs-lookup"><span data-stu-id="9f599-105">UpdateSku (Default)</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> [-Units <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f599-106">UpdateEventHubEndpointProperties</span><span class="sxs-lookup"><span data-stu-id="9f599-106">UpdateEventHubEndpointProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -EventHubRetentionTimeInDays <Int64>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f599-107">UpdateFileUploadProperties</span><span class="sxs-lookup"><span data-stu-id="9f599-107">UpdateFileUploadProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FileUploadStorageConnectionString <String>]
 [-FileUploadContainerName <String>] [-FileUploadSasUriTtl <TimeSpan>] [-FileUploadNotificationTtl <TimeSpan>]
 [-FileUploadNotificationMaxDeliveryCount <Int32>] -EnableFileUploadNotifications <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f599-108">UpdateCloudToDeviceProperties</span><span class="sxs-lookup"><span data-stu-id="9f599-108">UpdateCloudToDeviceProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -CloudToDevice <PSCloudToDeviceProperties>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f599-109">UpdateOperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="9f599-109">UpdateOperationsMonitoringProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String>
 -OperationsMonitoringProperties <PSOperationsMonitoringProperties> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f599-110">UpdateRoutingProperties</span><span class="sxs-lookup"><span data-stu-id="9f599-110">UpdateRoutingProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-RoutingProperties <PSRoutingProperties>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f599-111">UpdateRouteProperties</span><span class="sxs-lookup"><span data-stu-id="9f599-111">UpdateRouteProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String>
 [-Routes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f599-112">UpdateFallbackRouteProperty</span><span class="sxs-lookup"><span data-stu-id="9f599-112">UpdateFallbackRouteProperty</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FallbackRoute <PSFallbackRouteMetadata>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f599-113">설명은</span><span class="sxs-lookup"><span data-stu-id="9f599-113">DESCRIPTION</span></span>
<span data-ttu-id="9f599-114">IotHub의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f599-114">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="9f599-115">예제의</span><span class="sxs-lookup"><span data-stu-id="9f599-115">EXAMPLES</span></span>

### <span data-ttu-id="9f599-116">예제 1 sku 업데이트</span><span class="sxs-lookup"><span data-stu-id="9f599-116">Example 1 Update the sku</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName S1 -Units 5
```

<span data-ttu-id="9f599-117">"Myiothub" IotHub에 대 한 sku에서 S1로, 단위를 5로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f599-117">Update the sku to S1 and units to 5 for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="9f599-118">예제 2 eventhub 속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="9f599-118">Example 2 Update the eventhub properties</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubRetentionTimeInDays 4
```

<span data-ttu-id="9f599-119">"Myiothub" IotHub에 대 한 원격 분석 및 operationsmonitoringevents 이벤트 모두의 보존 시간을 일에서 4로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f599-119">Update the retention time in days to 4 for both the telemetry and operationsmonitoringevents events for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="9f599-120">변수</span><span class="sxs-lookup"><span data-stu-id="9f599-120">PARAMETERS</span></span>

### <span data-ttu-id="9f599-121">-CloudToDevice</span><span class="sxs-lookup"><span data-stu-id="9f599-121">-CloudToDevice</span></span>
<span data-ttu-id="9f599-122">클라우드 투 장치용 명령 큐의 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="9f599-122">The properties for the cloud to device command queue.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties
Parameter Sets: UpdateCloudToDeviceProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f599-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f599-123">-DefaultProfile</span></span>
<span data-ttu-id="9f599-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9f599-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f599-125">-EnableFileUploadNotifications</span><span class="sxs-lookup"><span data-stu-id="9f599-125">-EnableFileUploadNotifications</span></span>
<span data-ttu-id="9f599-126">파일 업로드에 알림을 사용할지 여부를 지정 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="9f599-126">Flag that specifies whether notifications should be enabled for file upload.</span></span> 

```yaml
Type: System.Boolean
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f599-127">-EventHubRetentionTimeInDays</span><span class="sxs-lookup"><span data-stu-id="9f599-127">-EventHubRetentionTimeInDays</span></span>
<span data-ttu-id="9f599-128">보존 시간 (일)입니다.</span><span class="sxs-lookup"><span data-stu-id="9f599-128">Retention time in days.</span></span> 

```yaml
Type: System.Int64
Parameter Sets: UpdateEventHubEndpointProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f599-129">-FallbackRoute</span><span class="sxs-lookup"><span data-stu-id="9f599-129">-FallbackRoute</span></span>
<span data-ttu-id="9f599-130">라우팅에 대 한 대체 경로</span><span class="sxs-lookup"><span data-stu-id="9f599-130">Fallback Route for Routing</span></span>

```yaml
Type: Microsoft.Azure.Management.IotHub.Models.PSFallbackRouteMetadata
Parameter Sets: UpdateFallbackRouteProperty
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f599-131">-FileUploadContainerName</span><span class="sxs-lookup"><span data-stu-id="9f599-131">-FileUploadContainerName</span></span>
<span data-ttu-id="9f599-132">파일을 업로드할 컨테이너의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9f599-132">The name of the container to upload the files to.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f599-133">-FileUploadNotificationMaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="9f599-133">-FileUploadNotificationMaxDeliveryCount</span></span>
<span data-ttu-id="9f599-134">파일 업로드 알림의 최대 배달 횟수입니다.</span><span class="sxs-lookup"><span data-stu-id="9f599-134">The maximum delivery count for file upload notifications.</span></span>  

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f599-135">-FileUploadNotificationTtl</span><span class="sxs-lookup"><span data-stu-id="9f599-135">-FileUploadNotificationTtl</span></span>
<span data-ttu-id="9f599-136">파일 업로드 알림 큐에 있는 메시지의 ttl (Time to live) 값입니다.</span><span class="sxs-lookup"><span data-stu-id="9f599-136">Time to live value for the messages in the file upload notification queue.</span></span> 

```yaml
Type: System.TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f599-137">-FileUploadSasUriTtl</span><span class="sxs-lookup"><span data-stu-id="9f599-137">-FileUploadSasUriTtl</span></span>
<span data-ttu-id="9f599-138">파일 업로드에 대해 생성 된 SAS Uri에 대 한 ttl (Time to live)입니다.</span><span class="sxs-lookup"><span data-stu-id="9f599-138">Time to live for the for the SAS Uri thats generated for file upload.</span></span> 

```yaml
Type: System.TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f599-139">-FileUploadStorageConnectionString</span><span class="sxs-lookup"><span data-stu-id="9f599-139">-FileUploadStorageConnectionString</span></span>
<span data-ttu-id="9f599-140">파일을 업로드할 저장소 연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="9f599-140">The storage connection string to upload the files to.</span></span> 

```yaml
Type: System.String
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f599-141">-이름</span><span class="sxs-lookup"><span data-stu-id="9f599-141">-Name</span></span>
<span data-ttu-id="9f599-142">IotHub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9f599-142">Name of the IotHub</span></span>

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

### <span data-ttu-id="9f599-143">-OperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="9f599-143">-OperationsMonitoringProperties</span></span>
<span data-ttu-id="9f599-144">작업 모니터링과 관련 된 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="9f599-144">The properties related to operations monitoring.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSOperationsMonitoringProperties
Parameter Sets: UpdateOperationsMonitoringProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f599-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f599-145">-ResourceGroupName</span></span>
<span data-ttu-id="9f599-146">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="9f599-146">Resource Group Name</span></span>

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

### <span data-ttu-id="9f599-147">-경로</span><span class="sxs-lookup"><span data-stu-id="9f599-147">-Routes</span></span>
<span data-ttu-id="9f599-148">라우팅에 추가 될 경로</span><span class="sxs-lookup"><span data-stu-id="9f599-148">Routes to be added for Routing</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]
Parameter Sets: UpdateRouteProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f599-149">-RoutingProperties</span><span class="sxs-lookup"><span data-stu-id="9f599-149">-RoutingProperties</span></span>
<span data-ttu-id="9f599-150">외부 끝점으로 메시지를 라우팅하는 라우팅 속성</span><span class="sxs-lookup"><span data-stu-id="9f599-150">The Routing properties for routing messages to external endpoints</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingProperties
Parameter Sets: UpdateRoutingProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f599-151">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="9f599-151">-SkuName</span></span>
<span data-ttu-id="9f599-152">Sku의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9f599-152">Name of the Sku.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSku
Parameter Sets: UpdateSku
Aliases:
Accepted values: F1, S1, S2, S3, B1, B2, B3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f599-153">-단위</span><span class="sxs-lookup"><span data-stu-id="9f599-153">-Units</span></span>
<span data-ttu-id="9f599-154">단위 수</span><span class="sxs-lookup"><span data-stu-id="9f599-154">Number of Units</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateSku
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f599-155">-확인</span><span class="sxs-lookup"><span data-stu-id="9f599-155">-Confirm</span></span>
<span data-ttu-id="9f599-156">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f599-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f599-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f599-157">-WhatIf</span></span>
<span data-ttu-id="9f599-158">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9f599-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f599-159">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9f599-159">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f599-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f599-160">CommonParameters</span></span>
<span data-ttu-id="9f599-161">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f599-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f599-162">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f599-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f599-163">입력</span><span class="sxs-lookup"><span data-stu-id="9f599-163">INPUTS</span></span>

### <span data-ttu-id="9f599-164">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9f599-164">System.String</span></span>

## <span data-ttu-id="9f599-165">출력</span><span class="sxs-lookup"><span data-stu-id="9f599-165">OUTPUTS</span></span>

### <span data-ttu-id="9f599-166">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="9f599-166">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="9f599-167">상속자</span><span class="sxs-lookup"><span data-stu-id="9f599-167">NOTES</span></span>

## <span data-ttu-id="9f599-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9f599-168">RELATED LINKS</span></span>
