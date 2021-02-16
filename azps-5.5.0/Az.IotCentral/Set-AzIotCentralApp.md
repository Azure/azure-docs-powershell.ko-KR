---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/set-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
ms.openlocfilehash: 94a6e4d2b140487b279d85db1a8b663e03523ce4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185772"
---
# <span data-ttu-id="5af09-101">Set-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="5af09-101">Set-AzIotCentralApp</span></span>

## <span data-ttu-id="5af09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5af09-102">SYNOPSIS</span></span>
<span data-ttu-id="5af09-103">IoT Central 애플리케이션에 대한 메타데이터를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5af09-103">Updates the metadata for an IoT Central Application.</span></span>

## <span data-ttu-id="5af09-104">구문</span><span class="sxs-lookup"><span data-stu-id="5af09-104">SYNTAX</span></span>

### <span data-ttu-id="5af09-105">ResourceIdParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="5af09-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>]
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5af09-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5af09-106">InputObjectParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>]
 -InputObject <PSIotCentralApp> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5af09-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="5af09-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5af09-108">설명</span><span class="sxs-lookup"><span data-stu-id="5af09-108">DESCRIPTION</span></span>
<span data-ttu-id="5af09-109">IoT Central 애플리케이션에 대한 메타데이터를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5af09-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="5af09-110">예제</span><span class="sxs-lookup"><span data-stu-id="5af09-110">EXAMPLES</span></span>

### <span data-ttu-id="5af09-111">예제 1 표시 이름 업데이트</span><span class="sxs-lookup"><span data-stu-id="5af09-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="5af09-112">기존 IoT Central 애플리케이션에서 표시 이름을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5af09-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="5af09-113">예제 출력:</span><span class="sxs-lookup"><span data-stu-id="5af09-113">Example Output:</span></span>

<span data-ttu-id="5af09-114">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName 이름 : MyAppResourceName 형식 : Microsoft.IoTCentral/IoTApps 위치 : westus 태그 : Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXXX-XXXXX-XXXX-X XXXXX-XXXXXXXXXXX DisplayName : 내 새로운 사용자 지정 표시 이름 하위omain : MyAppSubdomain 템플릿 : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5af09-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="5af09-115">예제 2 하위omain 업데이트</span><span class="sxs-lookup"><span data-stu-id="5af09-115">Example 2 Update Subdomain</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "new-subdomain"
```

<span data-ttu-id="5af09-116">기존 IoT Central 애플리케이션에서 표시 이름을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5af09-116">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="5af09-117">예제 출력:</span><span class="sxs-lookup"><span data-stu-id="5af09-117">Example Output:</span></span>

<span data-ttu-id="5af09-118">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName 이름 : MyAppResourceName 형식 : Microsoft.IoTCentral/IoTApps 위치 : westus 태그 : Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXXX-XXXXX-XXXXX-XXXX-XXXXXXXXXXX DisplayName : 표시 이름 하위omain : new-subdomain 템플릿 : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXX-XXXXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5af09-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : new-subdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="5af09-119">예제 3 앱 SKU 정보 업데이트</span><span class="sxs-lookup"><span data-stu-id="5af09-119">Example 3 Update App Sku Info</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Sku "ST2"
```

<span data-ttu-id="5af09-120">기존 IoT Central 애플리케이션에서 SKU를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5af09-120">Update the sku on an existing IoT Central Application.</span></span>

<span data-ttu-id="5af09-121">예제 출력:</span><span class="sxs-lookup"><span data-stu-id="5af09-121">Example Output:</span></span>

<span data-ttu-id="5af09-122">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName 이름 : MyAppResourceName 형식 : Microsoft.IoTCentral/IoTApps 위치 : westus 태그 : Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXXX-XXXXX-XXXX-XXXX-XXXXXXXXXXX DisplayName : 표시 이름 하위omain : MyAppSubdomain 템플릿 : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5af09-122">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="5af09-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5af09-123">PARAMETERS</span></span>

### <span data-ttu-id="5af09-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5af09-124">-AsJob</span></span>
<span data-ttu-id="5af09-125">백그라운드에서 작업으로 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="5af09-125">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="5af09-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5af09-126">-DefaultProfile</span></span>
<span data-ttu-id="5af09-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5af09-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5af09-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5af09-128">-DisplayName</span></span>
<span data-ttu-id="5af09-129">Iot Central 애플리케이션의 사용자 지정 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5af09-129">Custom Display Name of the Iot Central Application.</span></span>

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

### <span data-ttu-id="5af09-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5af09-130">-InputObject</span></span>
<span data-ttu-id="5af09-131">Iot Central 애플리케이션 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="5af09-131">Iot Central Application Input Object.</span></span>

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

### <span data-ttu-id="5af09-132">-Name</span><span class="sxs-lookup"><span data-stu-id="5af09-132">-Name</span></span>
<span data-ttu-id="5af09-133">Iot Central 애플리케이션 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5af09-133">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="5af09-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5af09-134">-ResourceGroupName</span></span>
<span data-ttu-id="5af09-135">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5af09-135">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="5af09-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5af09-136">-ResourceId</span></span>
<span data-ttu-id="5af09-137">Iot Central 애플리케이션 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5af09-137">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="5af09-138">-Sku</span><span class="sxs-lookup"><span data-stu-id="5af09-138">-Sku</span></span>
<span data-ttu-id="5af09-139">IoT Central 애플리케이션에 대한 가격 책정 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="5af09-139">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="5af09-140">기본값은 ST2입니다.</span><span class="sxs-lookup"><span data-stu-id="5af09-140">Default value is ST2.</span></span>

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

### <span data-ttu-id="5af09-141">-Subdomain</span><span class="sxs-lookup"><span data-stu-id="5af09-141">-Subdomain</span></span>
<span data-ttu-id="5af09-142">IoT Central 애플리케이션의 하위omain입니다.</span><span class="sxs-lookup"><span data-stu-id="5af09-142">Subdomain of the IoT Central Application.</span></span>

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

### <span data-ttu-id="5af09-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="5af09-143">-Tag</span></span>
<span data-ttu-id="5af09-144">Iot Central 애플리케이션 리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="5af09-144">Iot Central Application Resource Tags.</span></span>

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

### <span data-ttu-id="5af09-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5af09-145">-Confirm</span></span>
<span data-ttu-id="5af09-146">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5af09-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5af09-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5af09-147">-WhatIf</span></span>
<span data-ttu-id="5af09-148">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5af09-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5af09-149">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5af09-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5af09-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5af09-150">CommonParameters</span></span>
<span data-ttu-id="5af09-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5af09-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5af09-152">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5af09-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5af09-153">입력</span><span class="sxs-lookup"><span data-stu-id="5af09-153">INPUTS</span></span>

### <span data-ttu-id="5af09-154">System.String</span><span class="sxs-lookup"><span data-stu-id="5af09-154">System.String</span></span>

### <span data-ttu-id="5af09-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="5af09-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="5af09-156">출력</span><span class="sxs-lookup"><span data-stu-id="5af09-156">OUTPUTS</span></span>

### <span data-ttu-id="5af09-157">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="5af09-157">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="5af09-158">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5af09-158">NOTES</span></span>

## <span data-ttu-id="5af09-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5af09-159">RELATED LINKS</span></span>
