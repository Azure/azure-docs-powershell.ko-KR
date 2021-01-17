---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/set-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
ms.openlocfilehash: 94a6e4d2b140487b279d85db1a8b663e03523ce4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348134"
---
# <span data-ttu-id="13ba8-101">Set-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="13ba8-101">Set-AzIotCentralApp</span></span>

## <span data-ttu-id="13ba8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13ba8-102">SYNOPSIS</span></span>
<span data-ttu-id="13ba8-103">IoT Central 애플리케이션에 대한 메타데이터를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="13ba8-103">Updates the metadata for an IoT Central Application.</span></span>

## <span data-ttu-id="13ba8-104">구문</span><span class="sxs-lookup"><span data-stu-id="13ba8-104">SYNTAX</span></span>

### <span data-ttu-id="13ba8-105">ResourceIdParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="13ba8-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>]
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13ba8-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="13ba8-106">InputObjectParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>]
 -InputObject <PSIotCentralApp> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13ba8-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="13ba8-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="13ba8-108">설명</span><span class="sxs-lookup"><span data-stu-id="13ba8-108">DESCRIPTION</span></span>
<span data-ttu-id="13ba8-109">IoT Central 애플리케이션에 대한 메타데이터를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="13ba8-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="13ba8-110">예제</span><span class="sxs-lookup"><span data-stu-id="13ba8-110">EXAMPLES</span></span>

### <span data-ttu-id="13ba8-111">예제 1 표시 이름 업데이트</span><span class="sxs-lookup"><span data-stu-id="13ba8-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="13ba8-112">기존 IoT Central 애플리케이션에서 표시 이름을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="13ba8-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="13ba8-113">예제 출력:</span><span class="sxs-lookup"><span data-stu-id="13ba8-113">Example Output:</span></span>

<span data-ttu-id="13ba8-114">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName 이름 : MyAppResourceName 형식 : Microsoft.IoTCentral/IoTApps 위치 : westus 태그 : Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXXX-XXXXX-XXXX-X XXXXX-XXXXXXXXXXX DisplayName : 내 새로운 사용자 지정 표시 이름 하위omain : MyAppSubdomain 템플릿 : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13ba8-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="13ba8-115">예제 2 하위omain 업데이트</span><span class="sxs-lookup"><span data-stu-id="13ba8-115">Example 2 Update Subdomain</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "new-subdomain"
```

<span data-ttu-id="13ba8-116">기존 IoT Central 애플리케이션에서 표시 이름을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="13ba8-116">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="13ba8-117">예제 출력:</span><span class="sxs-lookup"><span data-stu-id="13ba8-117">Example Output:</span></span>

<span data-ttu-id="13ba8-118">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName 이름 : MyAppResourceName 형식 : Microsoft.IoTCentral/IoTApps 위치 : westus 태그 : Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXXX-XXXX-XXXXXXXXXXX DisplayName : 표시 이름 하위omain : new-subdomain 템플릿 : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXX-XXXXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13ba8-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : new-subdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="13ba8-119">예제 3 앱 SKU 정보 업데이트</span><span class="sxs-lookup"><span data-stu-id="13ba8-119">Example 3 Update App Sku Info</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Sku "ST2"
```

<span data-ttu-id="13ba8-120">기존 IoT Central 애플리케이션에서 SKU를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="13ba8-120">Update the sku on an existing IoT Central Application.</span></span>

<span data-ttu-id="13ba8-121">예제 출력:</span><span class="sxs-lookup"><span data-stu-id="13ba8-121">Example Output:</span></span>

<span data-ttu-id="13ba8-122">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName 이름 : MyAppResourceName 형식 : Microsoft.IoTCentral/IoTApps 위치 : westus 태그 : Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXXX-XXXXX-XXXXXXXXXXX DisplayName : 표시 이름 하위omain : MyAppSubdomain 템플릿 : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13ba8-122">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="13ba8-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13ba8-123">PARAMETERS</span></span>

### <span data-ttu-id="13ba8-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13ba8-124">-AsJob</span></span>
<span data-ttu-id="13ba8-125">백그라운드에서 작업으로 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="13ba8-125">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="13ba8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13ba8-126">-DefaultProfile</span></span>
<span data-ttu-id="13ba8-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="13ba8-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13ba8-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="13ba8-128">-DisplayName</span></span>
<span data-ttu-id="13ba8-129">Iot Central 애플리케이션의 사용자 지정 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13ba8-129">Custom Display Name of the Iot Central Application.</span></span>

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

### <span data-ttu-id="13ba8-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13ba8-130">-InputObject</span></span>
<span data-ttu-id="13ba8-131">Iot Central 애플리케이션 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="13ba8-131">Iot Central Application Input Object.</span></span>

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

### <span data-ttu-id="13ba8-132">-Name</span><span class="sxs-lookup"><span data-stu-id="13ba8-132">-Name</span></span>
<span data-ttu-id="13ba8-133">Iot Central 애플리케이션 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13ba8-133">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="13ba8-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13ba8-134">-ResourceGroupName</span></span>
<span data-ttu-id="13ba8-135">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13ba8-135">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="13ba8-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13ba8-136">-ResourceId</span></span>
<span data-ttu-id="13ba8-137">Iot Central 애플리케이션 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="13ba8-137">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="13ba8-138">-Sku</span><span class="sxs-lookup"><span data-stu-id="13ba8-138">-Sku</span></span>
<span data-ttu-id="13ba8-139">IoT Central 애플리케이션에 대한 가격 책정 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="13ba8-139">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="13ba8-140">기본값은 ST2입니다.</span><span class="sxs-lookup"><span data-stu-id="13ba8-140">Default value is ST2.</span></span>

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

### <span data-ttu-id="13ba8-141">-Subdomain</span><span class="sxs-lookup"><span data-stu-id="13ba8-141">-Subdomain</span></span>
<span data-ttu-id="13ba8-142">IoT Central 애플리케이션의 하위omain입니다.</span><span class="sxs-lookup"><span data-stu-id="13ba8-142">Subdomain of the IoT Central Application.</span></span>

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

### <span data-ttu-id="13ba8-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="13ba8-143">-Tag</span></span>
<span data-ttu-id="13ba8-144">Iot Central 애플리케이션 리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="13ba8-144">Iot Central Application Resource Tags.</span></span>

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

### <span data-ttu-id="13ba8-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13ba8-145">-Confirm</span></span>
<span data-ttu-id="13ba8-146">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="13ba8-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13ba8-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13ba8-147">-WhatIf</span></span>
<span data-ttu-id="13ba8-148">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="13ba8-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13ba8-149">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="13ba8-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13ba8-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13ba8-150">CommonParameters</span></span>
<span data-ttu-id="13ba8-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="13ba8-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13ba8-152">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="13ba8-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13ba8-153">입력</span><span class="sxs-lookup"><span data-stu-id="13ba8-153">INPUTS</span></span>

### <span data-ttu-id="13ba8-154">System.String</span><span class="sxs-lookup"><span data-stu-id="13ba8-154">System.String</span></span>

### <span data-ttu-id="13ba8-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="13ba8-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="13ba8-156">출력</span><span class="sxs-lookup"><span data-stu-id="13ba8-156">OUTPUTS</span></span>

### <span data-ttu-id="13ba8-157">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="13ba8-157">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="13ba8-158">참고 사항</span><span class="sxs-lookup"><span data-stu-id="13ba8-158">NOTES</span></span>

## <span data-ttu-id="13ba8-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13ba8-159">RELATED LINKS</span></span>
