---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/set-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHub.md
ms.openlocfilehash: a6e4e9e87f43ee5796c47836c3fa29fcdbdb8f26
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711101"
---
# <span data-ttu-id="80dd7-101">Set-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="80dd7-101">Set-AzureRmIotHub</span></span>

## <span data-ttu-id="80dd7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80dd7-102">SYNOPSIS</span></span>
<span data-ttu-id="80dd7-103">IotHub의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="80dd7-103">Updates the properties of an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80dd7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="80dd7-104">SYNTAX</span></span>

### <span data-ttu-id="80dd7-105">UpdateSku (기본값)</span><span class="sxs-lookup"><span data-stu-id="80dd7-105">UpdateSku (Default)</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> [-Units <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80dd7-106">UpdateEventHubEndpointProperties</span><span class="sxs-lookup"><span data-stu-id="80dd7-106">UpdateEventHubEndpointProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> -EventHubRetentionTimeInDays <Int64>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80dd7-107">UpdateFileUploadProperties</span><span class="sxs-lookup"><span data-stu-id="80dd7-107">UpdateFileUploadProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> [-FileUploadStorageConnectionString <String>]
 [-FileUploadContainerName <String>] [-FileUploadSasUriTtl <TimeSpan>] [-FileUploadNotificationTtl <TimeSpan>]
 [-FileUploadNotificationMaxDeliveryCount <Int32>] -EnableFileUploadNotifications <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80dd7-108">UpdateCloudToDeviceProperties</span><span class="sxs-lookup"><span data-stu-id="80dd7-108">UpdateCloudToDeviceProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> -CloudToDevice <PSCloudToDeviceProperties>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80dd7-109">UpdateOperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="80dd7-109">UpdateOperationsMonitoringProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String>
 -OperationsMonitoringProperties <PSOperationsMonitoringProperties> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80dd7-110">UpdateRoutingProperties</span><span class="sxs-lookup"><span data-stu-id="80dd7-110">UpdateRoutingProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> [-RoutingProperties <PSRoutingProperties>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80dd7-111">UpdateRouteProperties</span><span class="sxs-lookup"><span data-stu-id="80dd7-111">UpdateRouteProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String>
 [-Routes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80dd7-112">UpdateFallbackRouteProperty</span><span class="sxs-lookup"><span data-stu-id="80dd7-112">UpdateFallbackRouteProperty</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> [-FallbackRoute <PSFallbackRouteMetadata>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80dd7-113">설명은</span><span class="sxs-lookup"><span data-stu-id="80dd7-113">DESCRIPTION</span></span>
<span data-ttu-id="80dd7-114">IotHub의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="80dd7-114">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="80dd7-115">예제의</span><span class="sxs-lookup"><span data-stu-id="80dd7-115">EXAMPLES</span></span>

### <span data-ttu-id="80dd7-116">예제 1 sku 업데이트</span><span class="sxs-lookup"><span data-stu-id="80dd7-116">Example 1 Update the sku</span></span>
```
PS C:\> Set-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName S1 -Units 5
```

<span data-ttu-id="80dd7-117">"Myiothub" IotHub에 대 한 sku에서 S1로, 단위를 5로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="80dd7-117">Update the sku to S1 and units to 5 for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="80dd7-118">예제 2 eventhub 속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="80dd7-118">Example 2 Update the eventhub properties</span></span>
```
PS C:\> Set-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubRetentionTimeInDays 4
```

<span data-ttu-id="80dd7-119">"Myiothub" IotHub에 대 한 원격 분석 및 operationsmonitoringevents 이벤트 모두의 보존 시간을 일에서 4로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="80dd7-119">Update the retention time in days to 4 for both the telemetry and operationsmonitoringevents events for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="80dd7-120">변수</span><span class="sxs-lookup"><span data-stu-id="80dd7-120">PARAMETERS</span></span>

### <span data-ttu-id="80dd7-121">-CloudToDevice</span><span class="sxs-lookup"><span data-stu-id="80dd7-121">-CloudToDevice</span></span>
<span data-ttu-id="80dd7-122">클라우드 투 장치용 명령 큐의 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="80dd7-122">The properties for the cloud to device command queue.</span></span> 

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

### <span data-ttu-id="80dd7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80dd7-123">-DefaultProfile</span></span>
<span data-ttu-id="80dd7-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="80dd7-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="80dd7-125">-EnableFileUploadNotifications</span><span class="sxs-lookup"><span data-stu-id="80dd7-125">-EnableFileUploadNotifications</span></span>
<span data-ttu-id="80dd7-126">파일 업로드에 알림을 사용할지 여부를 지정 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="80dd7-126">Flag that specifies whether notifications should be enabled for file upload.</span></span> 

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

### <span data-ttu-id="80dd7-127">-EventHubRetentionTimeInDays</span><span class="sxs-lookup"><span data-stu-id="80dd7-127">-EventHubRetentionTimeInDays</span></span>
<span data-ttu-id="80dd7-128">보존 시간 (일)입니다.</span><span class="sxs-lookup"><span data-stu-id="80dd7-128">Retention time in days.</span></span> 

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

### <span data-ttu-id="80dd7-129">-FallbackRoute</span><span class="sxs-lookup"><span data-stu-id="80dd7-129">-FallbackRoute</span></span>
<span data-ttu-id="80dd7-130">라우팅에 대 한 대체 경로</span><span class="sxs-lookup"><span data-stu-id="80dd7-130">Fallback Route for Routing</span></span>

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

### <span data-ttu-id="80dd7-131">-FileUploadContainerName</span><span class="sxs-lookup"><span data-stu-id="80dd7-131">-FileUploadContainerName</span></span>
<span data-ttu-id="80dd7-132">파일을 업로드할 컨테이너의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80dd7-132">The name of the container to upload the files to.</span></span>

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

### <span data-ttu-id="80dd7-133">-FileUploadNotificationMaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="80dd7-133">-FileUploadNotificationMaxDeliveryCount</span></span>
<span data-ttu-id="80dd7-134">파일 업로드 알림의 최대 배달 횟수입니다.</span><span class="sxs-lookup"><span data-stu-id="80dd7-134">The maximum delivery count for file upload notifications.</span></span>  

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

### <span data-ttu-id="80dd7-135">-FileUploadNotificationTtl</span><span class="sxs-lookup"><span data-stu-id="80dd7-135">-FileUploadNotificationTtl</span></span>
<span data-ttu-id="80dd7-136">파일 업로드 알림 큐에 있는 메시지의 ttl (Time to live) 값입니다.</span><span class="sxs-lookup"><span data-stu-id="80dd7-136">Time to live value for the messages in the file upload notification queue.</span></span> 

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

### <span data-ttu-id="80dd7-137">-FileUploadSasUriTtl</span><span class="sxs-lookup"><span data-stu-id="80dd7-137">-FileUploadSasUriTtl</span></span>
<span data-ttu-id="80dd7-138">파일 업로드에 대해 생성 된 SAS Uri에 대 한 ttl (Time to live)입니다.</span><span class="sxs-lookup"><span data-stu-id="80dd7-138">Time to live for the for the SAS Uri thats generated for file upload.</span></span> 

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

### <span data-ttu-id="80dd7-139">-FileUploadStorageConnectionString</span><span class="sxs-lookup"><span data-stu-id="80dd7-139">-FileUploadStorageConnectionString</span></span>
<span data-ttu-id="80dd7-140">파일을 업로드할 저장소 연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="80dd7-140">The storage connection string to upload the files to.</span></span> 

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

### <span data-ttu-id="80dd7-141">-이름</span><span class="sxs-lookup"><span data-stu-id="80dd7-141">-Name</span></span>
<span data-ttu-id="80dd7-142">IotHub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80dd7-142">Name of the IotHub</span></span>

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

### <span data-ttu-id="80dd7-143">-OperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="80dd7-143">-OperationsMonitoringProperties</span></span>
<span data-ttu-id="80dd7-144">작업 모니터링과 관련 된 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="80dd7-144">The properties related to operations monitoring.</span></span> 

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

### <span data-ttu-id="80dd7-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80dd7-145">-ResourceGroupName</span></span>
<span data-ttu-id="80dd7-146">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="80dd7-146">Resource Group Name</span></span>

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

### <span data-ttu-id="80dd7-147">-경로</span><span class="sxs-lookup"><span data-stu-id="80dd7-147">-Routes</span></span>
<span data-ttu-id="80dd7-148">라우팅에 추가 될 경로</span><span class="sxs-lookup"><span data-stu-id="80dd7-148">Routes to be added for Routing</span></span>

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

### <span data-ttu-id="80dd7-149">-RoutingProperties</span><span class="sxs-lookup"><span data-stu-id="80dd7-149">-RoutingProperties</span></span>
<span data-ttu-id="80dd7-150">외부 끝점으로 메시지를 라우팅하는 라우팅 속성</span><span class="sxs-lookup"><span data-stu-id="80dd7-150">The Routing properties for routing messages to external endpoints</span></span> 

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

### <span data-ttu-id="80dd7-151">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="80dd7-151">-SkuName</span></span>
<span data-ttu-id="80dd7-152">Sku의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80dd7-152">Name of the Sku.</span></span>

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

### <span data-ttu-id="80dd7-153">-단위</span><span class="sxs-lookup"><span data-stu-id="80dd7-153">-Units</span></span>
<span data-ttu-id="80dd7-154">단위 수</span><span class="sxs-lookup"><span data-stu-id="80dd7-154">Number of Units</span></span>

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

### <span data-ttu-id="80dd7-155">-확인</span><span class="sxs-lookup"><span data-stu-id="80dd7-155">-Confirm</span></span>
<span data-ttu-id="80dd7-156">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="80dd7-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80dd7-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80dd7-157">-WhatIf</span></span>
<span data-ttu-id="80dd7-158">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="80dd7-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80dd7-159">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="80dd7-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80dd7-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80dd7-160">CommonParameters</span></span>
<span data-ttu-id="80dd7-161">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="80dd7-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80dd7-162">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80dd7-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80dd7-163">입력</span><span class="sxs-lookup"><span data-stu-id="80dd7-163">INPUTS</span></span>

### <span data-ttu-id="80dd7-164">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="80dd7-164">System.String</span></span>

## <span data-ttu-id="80dd7-165">출력</span><span class="sxs-lookup"><span data-stu-id="80dd7-165">OUTPUTS</span></span>

### <span data-ttu-id="80dd7-166">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="80dd7-166">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="80dd7-167">상속자</span><span class="sxs-lookup"><span data-stu-id="80dd7-167">NOTES</span></span>

## <span data-ttu-id="80dd7-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="80dd7-168">RELATED LINKS</span></span>
