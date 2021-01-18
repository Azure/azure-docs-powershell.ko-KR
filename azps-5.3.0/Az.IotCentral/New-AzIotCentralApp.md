---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/new-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
ms.openlocfilehash: 1be2aa8e198ae096f445b9f1972d1e0b903ae729
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495483"
---
# <span data-ttu-id="ceae1-101">New-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="ceae1-101">New-AzIotCentralApp</span></span>

## <span data-ttu-id="ceae1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ceae1-102">SYNOPSIS</span></span>
<span data-ttu-id="ceae1-103">새 IoT Central 애플리케이션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ceae1-103">Creates a new IoT Central Application.</span></span>

## <span data-ttu-id="ceae1-104">구문</span><span class="sxs-lookup"><span data-stu-id="ceae1-104">SYNTAX</span></span>

```
New-AzIotCentralApp [-Subdomain] <String> [-DisplayName <String>] [-Template <String>] [-Sku <String>]
 [-Location <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ceae1-105">설명</span><span class="sxs-lookup"><span data-stu-id="ceae1-105">DESCRIPTION</span></span>
<span data-ttu-id="ceae1-106">제공된 속성 및 메타데이터를 사용하여 새 IoT Central 애플리케이션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ceae1-106">Creates a new IoT Central Application with the provided properties and metadata.</span></span> <span data-ttu-id="ceae1-107">IoT Central에 대한 소개는 https://docs.microsoft.com/en-us/azure/iot-central/ 다음을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="ceae1-107">For an introduction to IoT Central, see https://docs.microsoft.com/en-us/azure/iot-central/.</span></span>

## <span data-ttu-id="ceae1-108">예제</span><span class="sxs-lookup"><span data-stu-id="ceae1-108">EXAMPLES</span></span>

### <span data-ttu-id="ceae1-109">예제 1 간단한 IoT Central 애플리케이션 만들기</span><span class="sxs-lookup"><span data-stu-id="ceae1-109">Example 1 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain"
```

<span data-ttu-id="ceae1-110">예제 출력:</span><span class="sxs-lookup"><span data-stu-id="ceae1-110">Example Output:</span></span>

<span data-ttu-id="ceae1-111">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName 이름 : MyAppResourceName 형식 : Microsoft.IoTCentral/IoTApps 위치 : westus 태그 : Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXXX-XXX XXX-XXXXXXXXXXXXX DisplayName : MyAppResourceName 하위omain : MyAppSubdomain 템플릿 : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXXX-XXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ceae1-111">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : MyAppResourceName Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="ceae1-112">리소스 그룹의 지역에 있는 표준 가격 책정 계층 ST2에서 IoT Central 애플리케이션을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ceae1-112">Create an IoT Central application in the standard pricing tier ST2, in the region of the resource group.</span></span>

### <span data-ttu-id="ceae1-113">예제 2 간단한 IoT Central 애플리케이션 만들기</span><span class="sxs-lookup"><span data-stu-id="ceae1-113">Example 2 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain" -Sku "ST2" -DisplayName "My Custom Display Name" -Template "iotc-default" -Location "westus"
```

<span data-ttu-id="ceae1-114">예제 출력:</span><span class="sxs-lookup"><span data-stu-id="ceae1-114">Example Output:</span></span>

<span data-ttu-id="ceae1-115">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName 이름 : MyAppResourceName 형식 : Microsoft.IoTCentral/IoTApps 위치 : westus 태그 : Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXXX-XXXXX-XXXX-X XXXXX-XXXXXXXXXXX DisplayName : 내 사용자 지정 표시 이름 하위omain : MyAppSubdomain 템플릿 : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ceae1-115">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="ceae1-116">iotc 기본 템플릿에 따라 사용자 지정 표시 이름을 사용하여 'westus' 지역에 표준 가격 책정 계층 ST2를 사용하여 IoT Central 애플리케이션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ceae1-116">Create an IoT Central application with the standard pricing tier ST2 in the 'westus' region, with a custom display name, based on the iotc-default template.</span></span>

## <span data-ttu-id="ceae1-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ceae1-117">PARAMETERS</span></span>

### <span data-ttu-id="ceae1-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ceae1-118">-AsJob</span></span>
<span data-ttu-id="ceae1-119">백그라운드에서 작업으로 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="ceae1-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="ceae1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceae1-120">-DefaultProfile</span></span>
<span data-ttu-id="ceae1-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ceae1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ceae1-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ceae1-122">-DisplayName</span></span>
<span data-ttu-id="ceae1-123">IoT Central 애플리케이션에 대한 사용자 지정 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ceae1-123">Custom display name for the IoT Central application.</span></span>
<span data-ttu-id="ceae1-124">기본값은 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ceae1-124">Default is resource name.</span></span>

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

### <span data-ttu-id="ceae1-125">-Location</span><span class="sxs-lookup"><span data-stu-id="ceae1-125">-Location</span></span>
<span data-ttu-id="ceae1-126">IoT Central 애플리케이션의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="ceae1-126">Location of your IoT Central application.</span></span>
<span data-ttu-id="ceae1-127">기본값은 대상 리소스 그룹의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="ceae1-127">Default is the location of target resource group.</span></span>

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

### <span data-ttu-id="ceae1-128">-Name</span><span class="sxs-lookup"><span data-stu-id="ceae1-128">-Name</span></span>
<span data-ttu-id="ceae1-129">Iot Central 애플리케이션 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ceae1-129">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceae1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ceae1-130">-ResourceGroupName</span></span>
<span data-ttu-id="ceae1-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ceae1-131">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceae1-132">-Sku</span><span class="sxs-lookup"><span data-stu-id="ceae1-132">-Sku</span></span>
<span data-ttu-id="ceae1-133">IoT Central 애플리케이션에 대한 가격 책정 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="ceae1-133">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="ceae1-134">기본값은 ST2입니다.</span><span class="sxs-lookup"><span data-stu-id="ceae1-134">Default value is ST2.</span></span>

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

### <span data-ttu-id="ceae1-135">-Subdomain</span><span class="sxs-lookup"><span data-stu-id="ceae1-135">-Subdomain</span></span>
<span data-ttu-id="ceae1-136">IoT Central URL에 대한 하위 페이지입니다.</span><span class="sxs-lookup"><span data-stu-id="ceae1-136">Subdomain for the IoT Central URL.</span></span>
<span data-ttu-id="ceae1-137">각 애플리케이션에는 고유한 하위omain이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceae1-137">Each application must have a unique subdomain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceae1-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="ceae1-138">-Tag</span></span>
<span data-ttu-id="ceae1-139">Iot Central 애플리케이션 리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="ceae1-139">Iot Central Application Resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceae1-140">-Template</span><span class="sxs-lookup"><span data-stu-id="ceae1-140">-Template</span></span>
<span data-ttu-id="ceae1-141">IoT Central 애플리케이션 템플릿 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ceae1-141">IoT Central application template name.</span></span>
<span data-ttu-id="ceae1-142">기본값은 사용자 지정 애플리케이션입니다.</span><span class="sxs-lookup"><span data-stu-id="ceae1-142">Default is a custom application.</span></span>

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

### <span data-ttu-id="ceae1-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ceae1-143">-Confirm</span></span>
<span data-ttu-id="ceae1-144">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ceae1-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ceae1-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ceae1-145">-WhatIf</span></span>
<span data-ttu-id="ceae1-146">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ceae1-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ceae1-147">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ceae1-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ceae1-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceae1-148">CommonParameters</span></span>
<span data-ttu-id="ceae1-149">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ceae1-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceae1-150">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ceae1-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceae1-151">입력</span><span class="sxs-lookup"><span data-stu-id="ceae1-151">INPUTS</span></span>

### <span data-ttu-id="ceae1-152">System.String</span><span class="sxs-lookup"><span data-stu-id="ceae1-152">System.String</span></span>

### <span data-ttu-id="ceae1-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ceae1-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ceae1-154">출력</span><span class="sxs-lookup"><span data-stu-id="ceae1-154">OUTPUTS</span></span>

### <span data-ttu-id="ceae1-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="ceae1-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="ceae1-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ceae1-156">NOTES</span></span>

## <span data-ttu-id="ceae1-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ceae1-157">RELATED LINKS</span></span>
