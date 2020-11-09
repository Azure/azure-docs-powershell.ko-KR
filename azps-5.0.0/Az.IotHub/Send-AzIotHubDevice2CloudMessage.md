---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/send-aziothubdevice2cloudmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Send-AzIotHubDevice2CloudMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Send-AzIotHubDevice2CloudMessage.md
ms.openlocfilehash: 2445ba6a4436af1dad4b940d18c5576bdf9a5bfc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304697"
---
# <span data-ttu-id="4a92f-101">Send-AzIotHubDevice2CloudMessage</span><span class="sxs-lookup"><span data-stu-id="4a92f-101">Send-AzIotHubDevice2CloudMessage</span></span>

## <span data-ttu-id="4a92f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a92f-102">SYNOPSIS</span></span>
<span data-ttu-id="4a92f-103">장치에서 클라우드로 메시지 보내기</span><span class="sxs-lookup"><span data-stu-id="4a92f-103">Send device-to-cloud message.</span></span>

## <span data-ttu-id="4a92f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4a92f-104">SYNTAX</span></span>

### <span data-ttu-id="4a92f-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="4a92f-105">ResourceSet (Default)</span></span>
```
Send-AzIotHubDevice2CloudMessage [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -Message <String> [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a92f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4a92f-106">InputObjectSet</span></span>
```
Send-AzIotHubDevice2CloudMessage [-InputObject] <PSIotHub> -DeviceId <String> -Message <String>
 [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4a92f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4a92f-107">ResourceIdSet</span></span>
```
Send-AzIotHubDevice2CloudMessage [-ResourceId] <String> -DeviceId <String> -Message <String>
 [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4a92f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4a92f-108">DESCRIPTION</span></span>
<span data-ttu-id="4a92f-109">명령은 응용 프로그램 및 시스템 속성과 함께 메시지 보내기를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a92f-109">The command supports sending messages with application and system properties.</span></span>

## <span data-ttu-id="4a92f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4a92f-110">EXAMPLES</span></span>

### <span data-ttu-id="4a92f-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="4a92f-111">Example 1</span></span>
```powershell
PS C:\> Send-AzIotHubDevice2CloudMessage -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Message "Ping from PS"
```

<span data-ttu-id="4a92f-112">기본 전송 유형을 사용 하 여 장치에서 클라우드로 메시지 보내기</span><span class="sxs-lookup"><span data-stu-id="4a92f-112">Sending device to cloud message using default transport type.</span></span>

### <span data-ttu-id="4a92f-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="4a92f-113">Example 2</span></span>
```powershell
PS C:\> Send-AzIotHubDevice2CloudMessage -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Message "Ping from PS" -TransportType Mqtt
```

<span data-ttu-id="4a92f-114">클라우드 메시지에 mqtt 장치를 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="4a92f-114">Sending an mqtt device to cloud message.</span></span>

## <span data-ttu-id="4a92f-115">변수</span><span class="sxs-lookup"><span data-stu-id="4a92f-115">PARAMETERS</span></span>

### <span data-ttu-id="4a92f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a92f-116">-DefaultProfile</span></span>
<span data-ttu-id="4a92f-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4a92f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a92f-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="4a92f-118">-DeviceId</span></span>
<span data-ttu-id="4a92f-119">대상 장치 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="4a92f-119">Target Device Id.</span></span>

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

### <span data-ttu-id="4a92f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a92f-120">-InputObject</span></span>
<span data-ttu-id="4a92f-121">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="4a92f-121">IotHub object</span></span>

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

### <span data-ttu-id="4a92f-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="4a92f-122">-IotHubName</span></span>
<span data-ttu-id="4a92f-123">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="4a92f-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="4a92f-124">-메시지</span><span class="sxs-lookup"><span data-stu-id="4a92f-124">-Message</span></span>
<span data-ttu-id="4a92f-125">IoT Hub로 보낼 메시지 본문</span><span class="sxs-lookup"><span data-stu-id="4a92f-125">Message body to send to IoT Hub.</span></span>

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

### <span data-ttu-id="4a92f-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4a92f-126">-PassThru</span></span>
<span data-ttu-id="4a92f-127">Boolean 개체를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4a92f-127">Allows to return the boolean object.</span></span> <span data-ttu-id="4a92f-128">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4a92f-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4a92f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a92f-129">-ResourceGroupName</span></span>
<span data-ttu-id="4a92f-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a92f-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4a92f-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a92f-131">-ResourceId</span></span>
<span data-ttu-id="4a92f-132">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="4a92f-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="4a92f-133">-TransportType</span><span class="sxs-lookup"><span data-stu-id="4a92f-133">-TransportType</span></span>
<span data-ttu-id="4a92f-134">사용할 전송 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="4a92f-134">Transport type to use.</span></span>
<span data-ttu-id="4a92f-135">기본값은 Amqp입니다.</span><span class="sxs-lookup"><span data-stu-id="4a92f-135">Default is Amqp.</span></span>

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

### <span data-ttu-id="4a92f-136">-확인</span><span class="sxs-lookup"><span data-stu-id="4a92f-136">-Confirm</span></span>
<span data-ttu-id="4a92f-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a92f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a92f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a92f-138">-WhatIf</span></span>
<span data-ttu-id="4a92f-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4a92f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a92f-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4a92f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a92f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a92f-141">CommonParameters</span></span>
<span data-ttu-id="4a92f-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a92f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a92f-143">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a92f-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a92f-144">입력</span><span class="sxs-lookup"><span data-stu-id="4a92f-144">INPUTS</span></span>

### <span data-ttu-id="4a92f-145">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="4a92f-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="4a92f-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4a92f-146">System.String</span></span>

## <span data-ttu-id="4a92f-147">출력</span><span class="sxs-lookup"><span data-stu-id="4a92f-147">OUTPUTS</span></span>

### <span data-ttu-id="4a92f-148">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="4a92f-148">System.Boolean</span></span>

## <span data-ttu-id="4a92f-149">상속자</span><span class="sxs-lookup"><span data-stu-id="4a92f-149">NOTES</span></span>

## <span data-ttu-id="4a92f-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4a92f-150">RELATED LINKS</span></span>
