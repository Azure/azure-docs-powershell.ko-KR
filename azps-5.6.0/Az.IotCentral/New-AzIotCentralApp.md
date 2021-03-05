---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/powershell/module/az.iotcentral/new-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
ms.openlocfilehash: ffae73880f66e378c7270ba5ce3645eae63064ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997985"
---
# <span data-ttu-id="01c4f-101">New-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="01c4f-101">New-AzIotCentralApp</span></span>

## <span data-ttu-id="01c4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01c4f-102">SYNOPSIS</span></span>
<span data-ttu-id="01c4f-103">새 IoT Central Application을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="01c4f-103">Creates a new IoT Central Application.</span></span>

## <span data-ttu-id="01c4f-104">구문</span><span class="sxs-lookup"><span data-stu-id="01c4f-104">SYNTAX</span></span>

```
New-AzIotCentralApp [-Subdomain] <String> [-DisplayName <String>] [-Template <String>] [-Sku <String>]
 [-Location <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01c4f-105">설명</span><span class="sxs-lookup"><span data-stu-id="01c4f-105">DESCRIPTION</span></span>
<span data-ttu-id="01c4f-106">제공된 속성 및 메타데이터를 사용하여 새 IoT Central Application을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="01c4f-106">Creates a new IoT Central Application with the provided properties and metadata.</span></span> <span data-ttu-id="01c4f-107">IoT Central에 대한 소개는 https://docs.microsoft.com/azure/iot-central/ 를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="01c4f-107">For an introduction to IoT Central, see https://docs.microsoft.com/azure/iot-central/.</span></span>

## <span data-ttu-id="01c4f-108">예제</span><span class="sxs-lookup"><span data-stu-id="01c4f-108">EXAMPLES</span></span>

### <span data-ttu-id="01c4f-109">예제 1 간단한 IoT Central Application 만들기.</span><span class="sxs-lookup"><span data-stu-id="01c4f-109">Example 1 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain"
```

<span data-ttu-id="01c4f-110">출력 예제:</span><span class="sxs-lookup"><span data-stu-id="01c4f-110">Example Output:</span></span>

<span data-ttu-id="01c4f-111">ResourceId : /subscriptions/XXXXXXX-XXXX-XXXXXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName 이름 : MyAppResourceName 유형 : Microsoft.IoTCentral/IoTApps 위치 : Westus Tag : Sku : Microsoft.Azure.Commands.PSIotCentralAppSkuInfo ApplicationId : XXXXXXX-XXXX-XXXX-XXX-XXX-XXX-XXus XXXXXXXXXXXXXXXXXXXXXXXXXXXX 리소스GroupName : MyAppResourceName Subdomain : MyAppSubdomain 템플릿 : SubscriptionId : XXXXXXXX-XXXX-XXXXXXXXXXXXXX iotc-default@1.0.0 ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01c4f-111">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : MyAppResourceName Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="01c4f-112">리소스 그룹의 지역에 있는 표준 가격 책정 계층 ST2에서 IoT Central 애플리케이션을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="01c4f-112">Create an IoT Central application in the standard pricing tier ST2, in the region of the resource group.</span></span>

### <span data-ttu-id="01c4f-113">예제 2 간단한 IoT Central Application 만들기</span><span class="sxs-lookup"><span data-stu-id="01c4f-113">Example 2 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain" -Sku "ST2" -DisplayName "My Custom Display Name" -Template "iotc-default" -Location "westus"
```

<span data-ttu-id="01c4f-114">출력 예제:</span><span class="sxs-lookup"><span data-stu-id="01c4f-114">Example Output:</span></span>

<span data-ttu-id="01c4f-115">ResourceId : /subscriptions/XXXXXXX-XXXX-XXXXXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName 이름 : MyAppResourceName 유형 : Microsoft.IoTCentral/IoTApps 위치 : Westus Tag : Sku : Microsoft.Azure.Commands.PSIotCentralAppSkuInfo ApplicationId : XXXXXXX-XXXX-XXXX-XXX-XXX-XXXX-XXX-X XXXX-XXXXXXXXXXXXXXXXX 디스플레이 이름 : 내 사용자 지정 표시 이름 하위omain : MyAppSubdomain 템플릿 : SubscriptionId : XXXXXXX-XXXXX-XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX iotc-default@1.0.0 ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01c4f-115">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="01c4f-116">iotc-default 템플릿을 기반으로 사용자 지정 표시 이름으로 'westus' 지역에서 표준 가격 책정 계층 ST2를 사용하여 IoT Central 애플리케이션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="01c4f-116">Create an IoT Central application with the standard pricing tier ST2 in the 'westus' region, with a custom display name, based on the iotc-default template.</span></span>

## <span data-ttu-id="01c4f-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="01c4f-117">PARAMETERS</span></span>

### <span data-ttu-id="01c4f-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="01c4f-118">-AsJob</span></span>
<span data-ttu-id="01c4f-119">백그라운드에서 작업으로 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="01c4f-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="01c4f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01c4f-120">-DefaultProfile</span></span>
<span data-ttu-id="01c4f-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="01c4f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01c4f-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="01c4f-122">-DisplayName</span></span>
<span data-ttu-id="01c4f-123">IoT Central 애플리케이션에 대한 사용자 지정 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="01c4f-123">Custom display name for the IoT Central application.</span></span>
<span data-ttu-id="01c4f-124">기본값은 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="01c4f-124">Default is resource name.</span></span>

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

### <span data-ttu-id="01c4f-125">-Location</span><span class="sxs-lookup"><span data-stu-id="01c4f-125">-Location</span></span>
<span data-ttu-id="01c4f-126">IoT Central 애플리케이션의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="01c4f-126">Location of your IoT Central application.</span></span>
<span data-ttu-id="01c4f-127">기본값은 대상 리소스 그룹의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="01c4f-127">Default is the location of target resource group.</span></span>

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

### <span data-ttu-id="01c4f-128">-Name</span><span class="sxs-lookup"><span data-stu-id="01c4f-128">-Name</span></span>
<span data-ttu-id="01c4f-129">Iot Central Application Resource의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="01c4f-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="01c4f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01c4f-130">-ResourceGroupName</span></span>
<span data-ttu-id="01c4f-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="01c4f-131">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="01c4f-132">-Sku</span><span class="sxs-lookup"><span data-stu-id="01c4f-132">-Sku</span></span>
<span data-ttu-id="01c4f-133">IoT Central 애플리케이션에 대한 가격 책정 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="01c4f-133">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="01c4f-134">기본값은 ST2입니다.</span><span class="sxs-lookup"><span data-stu-id="01c4f-134">Default value is ST2.</span></span>

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

### <span data-ttu-id="01c4f-135">-Subdomain</span><span class="sxs-lookup"><span data-stu-id="01c4f-135">-Subdomain</span></span>
<span data-ttu-id="01c4f-136">IoT Central URL에 대한 하위omain입니다.</span><span class="sxs-lookup"><span data-stu-id="01c4f-136">Subdomain for the IoT Central URL.</span></span>
<span data-ttu-id="01c4f-137">각 애플리케이션에는 고유한 하위omain이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="01c4f-137">Each application must have a unique subdomain.</span></span>

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

### <span data-ttu-id="01c4f-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="01c4f-138">-Tag</span></span>
<span data-ttu-id="01c4f-139">Iot Central 애플리케이션 리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="01c4f-139">Iot Central Application Resource Tags.</span></span>

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

### <span data-ttu-id="01c4f-140">-Template</span><span class="sxs-lookup"><span data-stu-id="01c4f-140">-Template</span></span>
<span data-ttu-id="01c4f-141">IoT Central 애플리케이션 템플릿 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="01c4f-141">IoT Central application template name.</span></span>
<span data-ttu-id="01c4f-142">기본값은 사용자 지정 애플리케이션입니다.</span><span class="sxs-lookup"><span data-stu-id="01c4f-142">Default is a custom application.</span></span>

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

### <span data-ttu-id="01c4f-143">-확인</span><span class="sxs-lookup"><span data-stu-id="01c4f-143">-Confirm</span></span>
<span data-ttu-id="01c4f-144">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="01c4f-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01c4f-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01c4f-145">-WhatIf</span></span>
<span data-ttu-id="01c4f-146">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="01c4f-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01c4f-147">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="01c4f-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01c4f-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01c4f-148">CommonParameters</span></span>
<span data-ttu-id="01c4f-149">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="01c4f-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01c4f-150">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01c4f-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01c4f-151">입력</span><span class="sxs-lookup"><span data-stu-id="01c4f-151">INPUTS</span></span>

### <span data-ttu-id="01c4f-152">System.String</span><span class="sxs-lookup"><span data-stu-id="01c4f-152">System.String</span></span>

### <span data-ttu-id="01c4f-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="01c4f-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="01c4f-154">출력</span><span class="sxs-lookup"><span data-stu-id="01c4f-154">OUTPUTS</span></span>

### <span data-ttu-id="01c4f-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="01c4f-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="01c4f-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="01c4f-156">NOTES</span></span>

## <span data-ttu-id="01c4f-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="01c4f-157">RELATED LINKS</span></span>
