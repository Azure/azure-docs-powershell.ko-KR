---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/get-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
ms.openlocfilehash: cbc7e255f74943ea2aff3518d278035f72394235
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203911"
---
# <span data-ttu-id="32bad-101">Get-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="32bad-101">Get-AzIotCentralApp</span></span>

## <span data-ttu-id="32bad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32bad-102">SYNOPSIS</span></span>
<span data-ttu-id="32bad-103">하나 또는 여러 IoT Central 애플리케이션에 대한 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="32bad-103">Gets properties for either one or several IoT Central Applications.</span></span>

## <span data-ttu-id="32bad-104">구문</span><span class="sxs-lookup"><span data-stu-id="32bad-104">SYNTAX</span></span>

### <span data-ttu-id="32bad-105">ListIotCentralAppsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="32bad-105">ListIotCentralAppsParameterSet (Default)</span></span>
```
Get-AzIotCentralApp [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="32bad-106">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="32bad-106">InteractiveIotCentralParameterSet</span></span>
```
Get-AzIotCentralApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="32bad-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="32bad-107">ResourceIdParameterSet</span></span>
```
Get-AzIotCentralApp -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32bad-108">설명</span><span class="sxs-lookup"><span data-stu-id="32bad-108">DESCRIPTION</span></span>
<span data-ttu-id="32bad-109">매개 변수 집합에 따라 특정 IoT Central 애플리케이션 또는 리소스 그룹 또는 구독의 모든 애플리케이션에 대한 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="32bad-109">Gets the metadata for either a specific IoT Central Application, or all the applications in a Resource Group or Subscription, depending on Parameter Set.</span></span> 

## <span data-ttu-id="32bad-110">예제</span><span class="sxs-lookup"><span data-stu-id="32bad-110">EXAMPLES</span></span>

### <span data-ttu-id="32bad-111">예제 1 특정 IoT Central 애플리케이션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="32bad-111">Example 1 Get Specific IoT Central Application.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="32bad-112">지정된 IoT Central 애플리케이션에 대한 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="32bad-112">Gets the metadata for the specified IoT Central Application.</span></span>

<span data-ttu-id="32bad-113">예제 출력:</span><span class="sxs-lookup"><span data-stu-id="32bad-113">Example Output:</span></span>

<span data-ttu-id="32bad-114">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName 이름 : MyAppResourceName 형식 : Microsoft.IoTCentral/IoTApps 위치 : westus 태그 : {[key, val]} Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXXX DisplayName: 내 사용자 지정 표시 이름 하위omain : MyAppSubdomain 템플릿 : iotc-default@1.0.0 SubscriptionId : XXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32bad-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="32bad-115">예제 2 구독에서 IoT Central 애플리케이션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="32bad-115">Example 2 Get IoT Central Applications in Subscription.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp
```

<span data-ttu-id="32bad-116">현재 구독의 모든 IoT Central 애플리케이션에 대한 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="32bad-116">Gets the metadata for all the IoT Central Applications in the current Subscription.</span></span>

<span data-ttu-id="32bad-117">예제 출력:</span><span class="sxs-lookup"><span data-stu-id="32bad-117">Example Output:</span></span>

<span data-ttu-id="32bad-118">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName 이름 : MyAppResourceName 형식 : Microsoft.IoTCentral/IoTApps 위치 : westus 태그 : {[key, val]} Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXXX DisplayName: 내 사용자 지정 표시 이름 하위omain : MyAppSubdomain 템플릿 : iotc-default@1.0.0 SubscriptionId : XXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32bad-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="32bad-119">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName2 이름 : MyAppResourceName2 형식 : Microsoft.IoTCentral/IoTApps 위치 : westus 태그 : {[key, val]} Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX DisplayName : 내 사용자 지정 표시 이름 2 하위omain : MyAppSubdomain2 템플릿 : iotc-default@1.0.0 SubscriptionId : XXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXXX ResourceGroupName : MyResourceGroupName2</span><span class="sxs-lookup"><span data-stu-id="32bad-119">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName2</span></span>

### <span data-ttu-id="32bad-120">예제 3 리소스 그룹에서 IoT Central 애플리케이션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="32bad-120">Example 3 Get IoT Central Applications in Resource Group.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName"
```

<span data-ttu-id="32bad-121">제공된 리소스 그룹의 모든 IoT Central 애플리케이션에 대한 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="32bad-121">Gets the metadata for all IoT Central Applications in the provided Resource Group.</span></span>

<span data-ttu-id="32bad-122">예제 출력:</span><span class="sxs-lookup"><span data-stu-id="32bad-122">Example Output:</span></span>

<span data-ttu-id="32bad-123">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName 이름 : MyAppResourceName 형식 : Microsoft.IoTCentral/IoTApps 위치 : westus 태그 : {[key, val]} Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXXX DisplayName: 내 사용자 지정 표시 이름 하위omain : MyAppSubdomain 템플릿 : iotc-default@1.0.0 SubscriptionId : XXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32bad-123">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="32bad-124">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName2 이름 : MyAppResourceName2 형식 : Microsoft.IoTCentral/IoTApps 위치 : westus 태그 : {[key, val]} Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX-XXXXXXXX DisplayName : 내 사용자 지정 표시 이름 2 하위omain : MyAppSubdomain2 템플릿 : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32bad-124">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="32bad-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32bad-125">PARAMETERS</span></span>

### <span data-ttu-id="32bad-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32bad-126">-DefaultProfile</span></span>
<span data-ttu-id="32bad-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="32bad-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32bad-128">-Name</span><span class="sxs-lookup"><span data-stu-id="32bad-128">-Name</span></span>
<span data-ttu-id="32bad-129">Iot Central 애플리케이션 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32bad-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="32bad-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32bad-130">-ResourceGroupName</span></span>
<span data-ttu-id="32bad-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32bad-131">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListIotCentralAppsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="32bad-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32bad-132">-ResourceId</span></span>
<span data-ttu-id="32bad-133">Iot Central 애플리케이션 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="32bad-133">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="32bad-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32bad-134">CommonParameters</span></span>
<span data-ttu-id="32bad-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="32bad-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32bad-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="32bad-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32bad-137">입력</span><span class="sxs-lookup"><span data-stu-id="32bad-137">INPUTS</span></span>

### <span data-ttu-id="32bad-138">System.String</span><span class="sxs-lookup"><span data-stu-id="32bad-138">System.String</span></span>

## <span data-ttu-id="32bad-139">출력</span><span class="sxs-lookup"><span data-stu-id="32bad-139">OUTPUTS</span></span>

### <span data-ttu-id="32bad-140">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="32bad-140">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="32bad-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="32bad-141">NOTES</span></span>

## <span data-ttu-id="32bad-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="32bad-142">RELATED LINKS</span></span>
