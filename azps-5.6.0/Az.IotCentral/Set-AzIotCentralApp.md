---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/powershell/module/az.iotcentral/set-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
ms.openlocfilehash: f99faf1ce7420212e87c894c8f5aadeb16578334
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997962"
---
# <span data-ttu-id="5820d-101">Set-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="5820d-101">Set-AzIotCentralApp</span></span>

## <span data-ttu-id="5820d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5820d-102">SYNOPSIS</span></span>
<span data-ttu-id="5820d-103">IoT Central Application에 대한 메타데이터를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5820d-103">Updates the metadata for an IoT Central Application.</span></span>

## <span data-ttu-id="5820d-104">구문</span><span class="sxs-lookup"><span data-stu-id="5820d-104">SYNTAX</span></span>

### <span data-ttu-id="5820d-105">ResourceIdParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="5820d-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>]
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5820d-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5820d-106">InputObjectParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>]
 -InputObject <PSIotCentralApp> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5820d-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="5820d-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5820d-108">설명</span><span class="sxs-lookup"><span data-stu-id="5820d-108">DESCRIPTION</span></span>
<span data-ttu-id="5820d-109">IoT Central Application의 메타데이터를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5820d-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="5820d-110">예제</span><span class="sxs-lookup"><span data-stu-id="5820d-110">EXAMPLES</span></span>

### <span data-ttu-id="5820d-111">예제 1 표시 이름 업데이트</span><span class="sxs-lookup"><span data-stu-id="5820d-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="5820d-112">기존 IoT Central 애플리케이션에서 표시 이름을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5820d-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="5820d-113">출력 예제:</span><span class="sxs-lookup"><span data-stu-id="5820d-113">Example Output:</span></span>

<span data-ttu-id="5820d-114">ResourceId : /subscriptions/XXXXXXX-XXXX-XXXXXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName 이름 : MyAppResourceName 유형 : Microsoft.IoTCentral/IoTApps 위치 : Westus Tag : Sku : Microsoft.Azure.Commands.PSIotCentralAppSkuInfo ApplicationId : XXXXXXX-XXXX-XXXX-XXX-XXX-XXXX-XXX-X XXXXXXXXXXXXXXXXXXXXXXX 디스플레이 이름 : MyAppSubdomain 템플릿 : SubscriptionId : XXXXXXXX-XXXX-XXXXXXXXXXXXXXXXXXXXXXXXXXX iotc-default@1.0.0 ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5820d-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="5820d-115">예제 2 하위마인 업데이트</span><span class="sxs-lookup"><span data-stu-id="5820d-115">Example 2 Update Subdomain</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "new-subdomain"
```

<span data-ttu-id="5820d-116">기존 IoT Central 애플리케이션에서 표시 이름을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5820d-116">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="5820d-117">출력 예제:</span><span class="sxs-lookup"><span data-stu-id="5820d-117">Example Output:</span></span>

<span data-ttu-id="5820d-118">ResourceId : /subscriptions/XXXXXXX-XXXX-XXXXXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName 이름 : MyAppResourceName 유형 : Microsoft.IoTCentral/IoTApps 위치 : Westus Tag : Sku : Microsoft.Azure.Commands.PSIotCentralAppSkuInfo ApplicationId : XXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXXXXXXXX 디스플레이 이름 : 표시 이름 하위omain : new-subdomain 템플릿 : SubscriptionId : XXXXXXX-XXXX-XXXXX-XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX iotc-default@1.0.0 ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5820d-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : new-subdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="5820d-119">예제 3 앱 Sku 정보 업데이트</span><span class="sxs-lookup"><span data-stu-id="5820d-119">Example 3 Update App Sku Info</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Sku "ST2"
```

<span data-ttu-id="5820d-120">기존 IoT Central 애플리케이션에서 sku를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5820d-120">Update the sku on an existing IoT Central Application.</span></span>

<span data-ttu-id="5820d-121">출력 예제:</span><span class="sxs-lookup"><span data-stu-id="5820d-121">Example Output:</span></span>

<span data-ttu-id="5820d-122">ResourceId : /subscriptions/XXXXXXX-XXXX-XXXXXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName 이름 : MyAppResourceName 유형 : Microsoft.IoTCentral/IoTApps 위치 : Westus Tag : Sku : Microsoft.Azure.Commands.PSIotCentralAppSkuInfo ApplicationId : XXXXXXX-XXXX-XXXX-XXXX-XXXX-XXX-XXXX-XXXX-XXXXXXXXXXXXXXXXXX 디스플레이 이름 : 표시 이름 하위omain : MyAppSubdomain 템플릿 : SubscriptionId : XXXXXXX-XXXX-XXXXX-XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX iotc-default@1.0.0 ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5820d-122">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="5820d-123">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5820d-123">PARAMETERS</span></span>

### <span data-ttu-id="5820d-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5820d-124">-AsJob</span></span>
<span data-ttu-id="5820d-125">백그라운드에서 작업으로 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="5820d-125">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="5820d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5820d-126">-DefaultProfile</span></span>
<span data-ttu-id="5820d-127">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5820d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5820d-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5820d-128">-DisplayName</span></span>
<span data-ttu-id="5820d-129">Iot Central 애플리케이션의 사용자 지정 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5820d-129">Custom Display Name of the Iot Central Application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5820d-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5820d-130">-InputObject</span></span>
<span data-ttu-id="5820d-131">Iot Central 애플리케이션 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="5820d-131">Iot Central Application Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5820d-132">-Name</span><span class="sxs-lookup"><span data-stu-id="5820d-132">-Name</span></span>
<span data-ttu-id="5820d-133">Iot Central Application Resource의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5820d-133">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5820d-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5820d-134">-ResourceGroupName</span></span>
<span data-ttu-id="5820d-135">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5820d-135">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5820d-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5820d-136">-ResourceId</span></span>
<span data-ttu-id="5820d-137">Iot Central 애플리케이션 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5820d-137">Iot Central Application Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5820d-138">-Sku</span><span class="sxs-lookup"><span data-stu-id="5820d-138">-Sku</span></span>
<span data-ttu-id="5820d-139">IoT Central 애플리케이션에 대한 가격 책정 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="5820d-139">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="5820d-140">기본값은 ST2입니다.</span><span class="sxs-lookup"><span data-stu-id="5820d-140">Default value is ST2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5820d-141">-Subdomain</span><span class="sxs-lookup"><span data-stu-id="5820d-141">-Subdomain</span></span>
<span data-ttu-id="5820d-142">IoT Central Application의 하위종입니다.</span><span class="sxs-lookup"><span data-stu-id="5820d-142">Subdomain of the IoT Central Application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5820d-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="5820d-143">-Tag</span></span>
<span data-ttu-id="5820d-144">Iot Central 애플리케이션 리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="5820d-144">Iot Central Application Resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5820d-145">-확인</span><span class="sxs-lookup"><span data-stu-id="5820d-145">-Confirm</span></span>
<span data-ttu-id="5820d-146">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5820d-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5820d-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5820d-147">-WhatIf</span></span>
<span data-ttu-id="5820d-148">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="5820d-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5820d-149">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5820d-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5820d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5820d-150">CommonParameters</span></span>
<span data-ttu-id="5820d-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5820d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5820d-152">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5820d-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5820d-153">입력</span><span class="sxs-lookup"><span data-stu-id="5820d-153">INPUTS</span></span>

### <span data-ttu-id="5820d-154">System.String</span><span class="sxs-lookup"><span data-stu-id="5820d-154">System.String</span></span>

### <span data-ttu-id="5820d-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="5820d-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="5820d-156">출력</span><span class="sxs-lookup"><span data-stu-id="5820d-156">OUTPUTS</span></span>

### <span data-ttu-id="5820d-157">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="5820d-157">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="5820d-158">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5820d-158">NOTES</span></span>

## <span data-ttu-id="5820d-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5820d-159">RELATED LINKS</span></span>
