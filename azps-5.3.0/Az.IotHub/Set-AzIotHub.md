---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
ms.openlocfilehash: 9011adbbfc7d23c2b9737e315fbec6001428d53c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386604"
---
# <span data-ttu-id="f4fb8-101">Set-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="f4fb8-101">Set-AzIotHub</span></span>

## <span data-ttu-id="f4fb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4fb8-102">SYNOPSIS</span></span>
<span data-ttu-id="f4fb8-103">IotHub의 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f4fb8-103">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="f4fb8-104">구문</span><span class="sxs-lookup"><span data-stu-id="f4fb8-104">SYNTAX</span></span>

### <span data-ttu-id="f4fb8-105">UpdateSku(기본값)</span><span class="sxs-lookup"><span data-stu-id="f4fb8-105">UpdateSku (Default)</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> [-Units <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4fb8-106">UpdateEventHubEndpointProperties</span><span class="sxs-lookup"><span data-stu-id="f4fb8-106">UpdateEventHubEndpointProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -EventHubRetentionTimeInDays <Int64>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4fb8-107">UpdateFileUploadProperties</span><span class="sxs-lookup"><span data-stu-id="f4fb8-107">UpdateFileUploadProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FileUploadStorageConnectionString <String>]
 [-FileUploadContainerName <String>] [-FileUploadSasUriTtl <TimeSpan>] [-FileUploadNotificationTtl <TimeSpan>]
 [-FileUploadNotificationMaxDeliveryCount <Int32>] -EnableFileUploadNotifications <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4fb8-108">UpdateCloudToDeviceProperties</span><span class="sxs-lookup"><span data-stu-id="f4fb8-108">UpdateCloudToDeviceProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -CloudToDevice <PSCloudToDeviceProperties>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4fb8-109">UpdateRoutingProperties</span><span class="sxs-lookup"><span data-stu-id="f4fb8-109">UpdateRoutingProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-RoutingProperties <PSRoutingProperties>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4fb8-110">UpdateRouteProperties</span><span class="sxs-lookup"><span data-stu-id="f4fb8-110">UpdateRouteProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String>
 [-Routes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4fb8-111">UpdateFallbackRouteProperty</span><span class="sxs-lookup"><span data-stu-id="f4fb8-111">UpdateFallbackRouteProperty</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FallbackRoute <PSFallbackRouteMetadata>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4fb8-112">설명</span><span class="sxs-lookup"><span data-stu-id="f4fb8-112">DESCRIPTION</span></span>
<span data-ttu-id="f4fb8-113">IotHub의 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f4fb8-113">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="f4fb8-114">예제</span><span class="sxs-lookup"><span data-stu-id="f4fb8-114">EXAMPLES</span></span>

### <span data-ttu-id="f4fb8-115">예제 1 SKU 업데이트</span><span class="sxs-lookup"><span data-stu-id="f4fb8-115">Example 1 Update the sku</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName S1 -Units 5
```

<span data-ttu-id="f4fb8-116">"myiothub"라는 IotHub에 대해 S1 및 단위를 5로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f4fb8-116">Update the sku to S1 and units to 5 for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="f4fb8-117">예제 2 eventhub 속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="f4fb8-117">Example 2 Update the eventhub properties</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubRetentionTimeInDays 4
```

<span data-ttu-id="f4fb8-118">"myiothub"라는 IotHub에 대한 원격 분석의 보존 기간을 4일로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f4fb8-118">Update the retention time of telemetry in days to 4 for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="f4fb8-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4fb8-119">PARAMETERS</span></span>

### <span data-ttu-id="f4fb8-120">-CloudToDevice</span><span class="sxs-lookup"><span data-stu-id="f4fb8-120">-CloudToDevice</span></span>
<span data-ttu-id="f4fb8-121">클라우드-디바이스 명령 큐에 대한 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="f4fb8-121">The properties for the cloud to device command queue.</span></span> 

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

### <span data-ttu-id="f4fb8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4fb8-122">-DefaultProfile</span></span>
<span data-ttu-id="f4fb8-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f4fb8-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4fb8-124">-EnableFileUploadNotifications</span><span class="sxs-lookup"><span data-stu-id="f4fb8-124">-EnableFileUploadNotifications</span></span>
<span data-ttu-id="f4fb8-125">파일 업로드에 알림을 사용하도록 설정해야 하는지 여부를 지정하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="f4fb8-125">Flag that specifies whether notifications should be enabled for file upload.</span></span> 

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

### <span data-ttu-id="f4fb8-126">-EventHubRetentionTimeInDays</span><span class="sxs-lookup"><span data-stu-id="f4fb8-126">-EventHubRetentionTimeInDays</span></span>
<span data-ttu-id="f4fb8-127">보존 기간(일)입니다.</span><span class="sxs-lookup"><span data-stu-id="f4fb8-127">Retention time in days.</span></span> 

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

### <span data-ttu-id="f4fb8-128">-FallbackRoute</span><span class="sxs-lookup"><span data-stu-id="f4fb8-128">-FallbackRoute</span></span>
<span data-ttu-id="f4fb8-129">라우팅에 대한 Fallback 경로</span><span class="sxs-lookup"><span data-stu-id="f4fb8-129">Fallback Route for Routing</span></span>

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

### <span data-ttu-id="f4fb8-130">-FileUploadContainerName</span><span class="sxs-lookup"><span data-stu-id="f4fb8-130">-FileUploadContainerName</span></span>
<span data-ttu-id="f4fb8-131">파일을 업로드할 컨테이너의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f4fb8-131">The name of the container to upload the files to.</span></span>

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

### <span data-ttu-id="f4fb8-132">-FileUploadNotificationMaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="f4fb8-132">-FileUploadNotificationMaxDeliveryCount</span></span>
<span data-ttu-id="f4fb8-133">파일 업로드 알림의 최대 배달 수입니다.</span><span class="sxs-lookup"><span data-stu-id="f4fb8-133">The maximum delivery count for file upload notifications.</span></span>  

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

### <span data-ttu-id="f4fb8-134">-FileUploadNotificationTtl</span><span class="sxs-lookup"><span data-stu-id="f4fb8-134">-FileUploadNotificationTtl</span></span>
<span data-ttu-id="f4fb8-135">파일 업로드 알림 큐에 있는 메시지에 대한 Time to Live 값입니다.</span><span class="sxs-lookup"><span data-stu-id="f4fb8-135">Time to live value for the messages in the file upload notification queue.</span></span> 

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

### <span data-ttu-id="f4fb8-136">-FileUploadSasUriTtl</span><span class="sxs-lookup"><span data-stu-id="f4fb8-136">-FileUploadSasUriTtl</span></span>
<span data-ttu-id="f4fb8-137">파일 업로드에 대해 생성된 SAS Uri에 대한 Time to Live입니다.</span><span class="sxs-lookup"><span data-stu-id="f4fb8-137">Time to live for the for the SAS Uri thats generated for file upload.</span></span> 

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

### <span data-ttu-id="f4fb8-138">-FileUploadStorageConnectionString</span><span class="sxs-lookup"><span data-stu-id="f4fb8-138">-FileUploadStorageConnectionString</span></span>
<span data-ttu-id="f4fb8-139">파일을 업로드할 저장소 연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="f4fb8-139">The storage connection string to upload the files to.</span></span> 

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

### <span data-ttu-id="f4fb8-140">-Name</span><span class="sxs-lookup"><span data-stu-id="f4fb8-140">-Name</span></span>
<span data-ttu-id="f4fb8-141">IotHub의 이름</span><span class="sxs-lookup"><span data-stu-id="f4fb8-141">Name of the IotHub</span></span>

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

### <span data-ttu-id="f4fb8-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4fb8-142">-ResourceGroupName</span></span>
<span data-ttu-id="f4fb8-143">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="f4fb8-143">Resource Group Name</span></span>

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

### <span data-ttu-id="f4fb8-144">-Routes</span><span class="sxs-lookup"><span data-stu-id="f4fb8-144">-Routes</span></span>
<span data-ttu-id="f4fb8-145">라우팅에 추가할 경로</span><span class="sxs-lookup"><span data-stu-id="f4fb8-145">Routes to be added for Routing</span></span>

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

### <span data-ttu-id="f4fb8-146">-RoutingProperties</span><span class="sxs-lookup"><span data-stu-id="f4fb8-146">-RoutingProperties</span></span>
<span data-ttu-id="f4fb8-147">외부 엔드포인트로 메시지를 라우팅하기 위한 라우팅 속성</span><span class="sxs-lookup"><span data-stu-id="f4fb8-147">The Routing properties for routing messages to external endpoints</span></span> 

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

### <span data-ttu-id="f4fb8-148">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f4fb8-148">-SkuName</span></span>
<span data-ttu-id="f4fb8-149">SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f4fb8-149">Name of the Sku.</span></span>

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

### <span data-ttu-id="f4fb8-150">-Units</span><span class="sxs-lookup"><span data-stu-id="f4fb8-150">-Units</span></span>
<span data-ttu-id="f4fb8-151">단위 수</span><span class="sxs-lookup"><span data-stu-id="f4fb8-151">Number of Units</span></span>

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

### <span data-ttu-id="f4fb8-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4fb8-152">-Confirm</span></span>
<span data-ttu-id="f4fb8-153">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f4fb8-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4fb8-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4fb8-154">-WhatIf</span></span>
<span data-ttu-id="f4fb8-155">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f4fb8-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4fb8-156">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f4fb8-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4fb8-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4fb8-157">CommonParameters</span></span>
<span data-ttu-id="f4fb8-158">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f4fb8-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4fb8-159">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f4fb8-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4fb8-160">입력</span><span class="sxs-lookup"><span data-stu-id="f4fb8-160">INPUTS</span></span>

### <span data-ttu-id="f4fb8-161">System.String</span><span class="sxs-lookup"><span data-stu-id="f4fb8-161">System.String</span></span>

## <span data-ttu-id="f4fb8-162">출력</span><span class="sxs-lookup"><span data-stu-id="f4fb8-162">OUTPUTS</span></span>

### <span data-ttu-id="f4fb8-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="f4fb8-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="f4fb8-164">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f4fb8-164">NOTES</span></span>

## <span data-ttu-id="f4fb8-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f4fb8-165">RELATED LINKS</span></span>
