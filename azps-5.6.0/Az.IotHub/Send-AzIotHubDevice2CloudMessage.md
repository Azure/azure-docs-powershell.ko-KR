---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/send-aziothubdevice2cloudmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Send-AzIotHubDevice2CloudMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Send-AzIotHubDevice2CloudMessage.md
ms.openlocfilehash: 41c4f5f4852f499f45b5c765263bdf356dbf90ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992679"
---
# <span data-ttu-id="997c5-101">Send-AzIotHubDevice2CloudMessage</span><span class="sxs-lookup"><span data-stu-id="997c5-101">Send-AzIotHubDevice2CloudMessage</span></span>

## <span data-ttu-id="997c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="997c5-102">SYNOPSIS</span></span>
<span data-ttu-id="997c5-103">디바이스-클라우드 메시지를 전송합니다.</span><span class="sxs-lookup"><span data-stu-id="997c5-103">Send device-to-cloud message.</span></span>

## <span data-ttu-id="997c5-104">구문</span><span class="sxs-lookup"><span data-stu-id="997c5-104">SYNTAX</span></span>

### <span data-ttu-id="997c5-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="997c5-105">ResourceSet (Default)</span></span>
```
Send-AzIotHubDevice2CloudMessage [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -Message <String> [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="997c5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="997c5-106">InputObjectSet</span></span>
```
Send-AzIotHubDevice2CloudMessage [-InputObject] <PSIotHub> -DeviceId <String> -Message <String>
 [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="997c5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="997c5-107">ResourceIdSet</span></span>
```
Send-AzIotHubDevice2CloudMessage [-ResourceId] <String> -DeviceId <String> -Message <String>
 [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="997c5-108">설명</span><span class="sxs-lookup"><span data-stu-id="997c5-108">DESCRIPTION</span></span>
<span data-ttu-id="997c5-109">이 명령은 애플리케이션 및 시스템 속성을 사용하여 메시지 보내기를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="997c5-109">The command supports sending messages with application and system properties.</span></span>

## <span data-ttu-id="997c5-110">예제</span><span class="sxs-lookup"><span data-stu-id="997c5-110">EXAMPLES</span></span>

### <span data-ttu-id="997c5-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="997c5-111">Example 1</span></span>
```powershell
PS C:\> Send-AzIotHubDevice2CloudMessage -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Message "Ping from PS"
```

<span data-ttu-id="997c5-112">기본 전송 유형을 사용하여 디바이스를 클라우드 메시지로 전송합니다.</span><span class="sxs-lookup"><span data-stu-id="997c5-112">Sending device to cloud message using default transport type.</span></span>

### <span data-ttu-id="997c5-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="997c5-113">Example 2</span></span>
```powershell
PS C:\> Send-AzIotHubDevice2CloudMessage -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Message "Ping from PS" -TransportType Mqtt
```

<span data-ttu-id="997c5-114">mqtt 디바이스를 클라우드 메시지로 전송합니다.</span><span class="sxs-lookup"><span data-stu-id="997c5-114">Sending an mqtt device to cloud message.</span></span>

## <span data-ttu-id="997c5-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="997c5-115">PARAMETERS</span></span>

### <span data-ttu-id="997c5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="997c5-116">-DefaultProfile</span></span>
<span data-ttu-id="997c5-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="997c5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="997c5-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="997c5-118">-DeviceId</span></span>
<span data-ttu-id="997c5-119">대상 디바이스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="997c5-119">Target Device Id.</span></span>

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

### <span data-ttu-id="997c5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="997c5-120">-InputObject</span></span>
<span data-ttu-id="997c5-121">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="997c5-121">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="997c5-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="997c5-122">-IotHubName</span></span>
<span data-ttu-id="997c5-123">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="997c5-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="997c5-124">-Message</span><span class="sxs-lookup"><span data-stu-id="997c5-124">-Message</span></span>
<span data-ttu-id="997c5-125">IoT Hub로 보낼 메시지 본문입니다.</span><span class="sxs-lookup"><span data-stu-id="997c5-125">Message body to send to IoT Hub.</span></span>

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

### <span data-ttu-id="997c5-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="997c5-126">-PassThru</span></span>
<span data-ttu-id="997c5-127">부울 개체를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="997c5-127">Allows to return the boolean object.</span></span> <span data-ttu-id="997c5-128">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="997c5-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="997c5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="997c5-129">-ResourceGroupName</span></span>
<span data-ttu-id="997c5-130">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="997c5-130">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="997c5-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="997c5-131">-ResourceId</span></span>
<span data-ttu-id="997c5-132">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="997c5-132">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="997c5-133">-TransportType</span><span class="sxs-lookup"><span data-stu-id="997c5-133">-TransportType</span></span>
<span data-ttu-id="997c5-134">사용할 전송 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="997c5-134">Transport type to use.</span></span>
<span data-ttu-id="997c5-135">기본값은 Amqp입니다.</span><span class="sxs-lookup"><span data-stu-id="997c5-135">Default is Amqp.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSTransportType
Parameter Sets: (All)
Aliases:
Accepted values: Amqp, Http1, Amqp_WebSocket_Only, Amqp_Tcp_Only, Mqtt, Mqtt_WebSocket_Only, Mqtt_Tcp_Only

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="997c5-136">-확인</span><span class="sxs-lookup"><span data-stu-id="997c5-136">-Confirm</span></span>
<span data-ttu-id="997c5-137">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="997c5-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="997c5-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="997c5-138">-WhatIf</span></span>
<span data-ttu-id="997c5-139">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="997c5-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="997c5-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="997c5-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="997c5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="997c5-141">CommonParameters</span></span>
<span data-ttu-id="997c5-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="997c5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="997c5-143">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="997c5-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="997c5-144">입력</span><span class="sxs-lookup"><span data-stu-id="997c5-144">INPUTS</span></span>

### <span data-ttu-id="997c5-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="997c5-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="997c5-146">System.String</span><span class="sxs-lookup"><span data-stu-id="997c5-146">System.String</span></span>

## <span data-ttu-id="997c5-147">출력</span><span class="sxs-lookup"><span data-stu-id="997c5-147">OUTPUTS</span></span>

### <span data-ttu-id="997c5-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="997c5-148">System.Boolean</span></span>

## <span data-ttu-id="997c5-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="997c5-149">NOTES</span></span>

## <span data-ttu-id="997c5-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="997c5-150">RELATED LINKS</span></span>
