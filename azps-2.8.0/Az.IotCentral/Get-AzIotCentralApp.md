---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/get-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
ms.openlocfilehash: a58be60e10be53c1251d8efac5d5fc1551182043
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689768"
---
# <span data-ttu-id="aa538-101">Get-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="aa538-101">Get-AzIotCentralApp</span></span>

## <span data-ttu-id="aa538-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa538-102">SYNOPSIS</span></span>
<span data-ttu-id="aa538-103">하나 또는 여러 IoT 중앙 응용 프로그램에 대 한 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="aa538-103">Gets properties for either one or several IoT Central Applications.</span></span>

## <span data-ttu-id="aa538-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aa538-104">SYNTAX</span></span>

### <span data-ttu-id="aa538-105">ListIotCentralAppsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="aa538-105">ListIotCentralAppsParameterSet (Default)</span></span>
```
Get-AzIotCentralApp [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aa538-106">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa538-106">InteractiveIotCentralParameterSet</span></span>
```
Get-AzIotCentralApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aa538-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa538-107">ResourceIdParameterSet</span></span>
```
Get-AzIotCentralApp -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa538-108">설명은</span><span class="sxs-lookup"><span data-stu-id="aa538-108">DESCRIPTION</span></span>
<span data-ttu-id="aa538-109">매개 변수 집합에 따라 특정 IoT 중앙 응용 프로그램 또는 리소스 그룹 또는 구독의 모든 응용 프로그램에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="aa538-109">Gets the metadata for either a specific IoT Central Application, or all the applications in a Resource Group or Subscription, depending on Parameter Set.</span></span> 

## <span data-ttu-id="aa538-110">예제의</span><span class="sxs-lookup"><span data-stu-id="aa538-110">EXAMPLES</span></span>

### <span data-ttu-id="aa538-111">예제 1 특정 IoT 중앙 응용 프로그램을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa538-111">Example 1 Get Specific IoT Central Application.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="aa538-112">지정 된 IoT 중앙 응용 프로그램에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="aa538-112">Gets the metadata for the specified IoT Central Application.</span></span>

<span data-ttu-id="aa538-113">출력 예:</span><span class="sxs-lookup"><span data-stu-id="aa538-113">Example Output:</span></span>

<span data-ttu-id="aa538-114">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/Iotcentral/MyAppResourceName Name: MyAppResourceName 유형: Microsoft. IoTCentral/Iotcentral 위치: westus Tag: {[key, val]} Sku: Microsoft Azure. p s p. p r o: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My 사용자 지정 표시 이름 하위 도메인: MyAppSubdomain Template: iotc-default@1.0.0 SubscriptionId: Xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa538-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="aa538-115">예제 2 구독에 IoT 중앙 응용 프로그램을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa538-115">Example 2 Get IoT Central Applications in Subscription.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp
```

<span data-ttu-id="aa538-116">현재 구독에 있는 모든 IoT 중앙 응용 프로그램에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="aa538-116">Gets the metadata for all the IoT Central Applications in the current Subscription.</span></span>

<span data-ttu-id="aa538-117">출력 예:</span><span class="sxs-lookup"><span data-stu-id="aa538-117">Example Output:</span></span>

<span data-ttu-id="aa538-118">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/Iotcentral/MyAppResourceName Name: MyAppResourceName 유형: Microsoft. IoTCentral/Iotcentral 위치: westus Tag: {[key, val]} Sku: Microsoft Azure. p s p. p r o: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My 사용자 지정 표시 이름 하위 도메인: MyAppSubdomain Template: iotc-default@1.0.0 SubscriptionId: Xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa538-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="aa538-119">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft. IoTCentral/Iotcentral/MyAppResourceName2 Name: MyAppResourceName2 유형: Microsoft. IoTCentral/Iotcentral 위치: westus Tag: {[key, val]} Sku: Microsoft Azure. p s p. p r o: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My 사용자 지정 표시 이름 2 하위 도메인: MyAppSubdomain2 Template: iotc-default@1.0.0 SubscriptionId: Xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName2</span><span class="sxs-lookup"><span data-stu-id="aa538-119">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName2</span></span>

### <span data-ttu-id="aa538-120">예제 3 리소스 그룹에 IoT 중앙 응용 프로그램을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="aa538-120">Example 3 Get IoT Central Applications in Resource Group.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName"
```

<span data-ttu-id="aa538-121">제공 된 리소스 그룹의 모든 IoT 중앙 응용 프로그램에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="aa538-121">Gets the metadata for all IoT Central Applications in the provided Resource Group.</span></span>

<span data-ttu-id="aa538-122">출력 예:</span><span class="sxs-lookup"><span data-stu-id="aa538-122">Example Output:</span></span>

<span data-ttu-id="aa538-123">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/Iotcentral/MyAppResourceName Name: MyAppResourceName 유형: Microsoft. IoTCentral/Iotcentral 위치: westus Tag: {[key, val]} Sku: Microsoft Azure. p s p. p r o: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My 사용자 지정 표시 이름 하위 도메인: MyAppSubdomain Template: iotc-default@1.0.0 SubscriptionId: Xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa538-123">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="aa538-124">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/Iotcentral/MyAppResourceName2 Name: MyAppResourceName2 유형: Microsoft. IoTCentral/Iotcentral 위치: westus Tag: {[key, val]} Sku: Microsoft Azure. p s p. p r o: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My 사용자 지정 표시 이름 2 하위 도메인: MyAppSubdomain2 Template: iotc-default@1.0.0 SubscriptionId: Xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa538-124">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="aa538-125">변수</span><span class="sxs-lookup"><span data-stu-id="aa538-125">PARAMETERS</span></span>

### <span data-ttu-id="aa538-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa538-126">-DefaultProfile</span></span>
<span data-ttu-id="aa538-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aa538-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa538-128">-이름</span><span class="sxs-lookup"><span data-stu-id="aa538-128">-Name</span></span>
<span data-ttu-id="aa538-129">Iot 중앙 응용 프로그램 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aa538-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="aa538-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa538-130">-ResourceGroupName</span></span>
<span data-ttu-id="aa538-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aa538-131">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="aa538-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa538-132">-ResourceId</span></span>
<span data-ttu-id="aa538-133">Iot 중앙 응용 프로그램 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="aa538-133">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="aa538-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa538-134">CommonParameters</span></span>
<span data-ttu-id="aa538-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa538-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa538-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa538-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa538-137">입력</span><span class="sxs-lookup"><span data-stu-id="aa538-137">INPUTS</span></span>

### <span data-ttu-id="aa538-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="aa538-138">System.String</span></span>

## <span data-ttu-id="aa538-139">출력</span><span class="sxs-lookup"><span data-stu-id="aa538-139">OUTPUTS</span></span>

### <span data-ttu-id="aa538-140">PSIotCentralApp를 통해 서 .exe.</span><span class="sxs-lookup"><span data-stu-id="aa538-140">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="aa538-141">상속자</span><span class="sxs-lookup"><span data-stu-id="aa538-141">NOTES</span></span>

## <span data-ttu-id="aa538-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aa538-142">RELATED LINKS</span></span>
