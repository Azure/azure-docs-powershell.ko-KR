---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/new-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
ms.openlocfilehash: 636c40763c69a4c39ca0bbf8b15fe04fad318d84
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689767"
---
# <span data-ttu-id="9705c-101">New-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="9705c-101">New-AzIotCentralApp</span></span>

## <span data-ttu-id="9705c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9705c-102">SYNOPSIS</span></span>
<span data-ttu-id="9705c-103">새 IoT 중앙 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9705c-103">Creates a new IoT Central Application.</span></span>

## <span data-ttu-id="9705c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9705c-104">SYNTAX</span></span>

```
New-AzIotCentralApp [-Subdomain] <String> [-DisplayName <String>] [-Template <String>] [-Sku <String>]
 [-Location <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9705c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9705c-105">DESCRIPTION</span></span>
<span data-ttu-id="9705c-106">제공 된 속성 및 메타 데이터로 새 IoT 중앙 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9705c-106">Creates a new IoT Central Application with the provided properties and metadata.</span></span> <span data-ttu-id="9705c-107">IoT Central 소개에 대 한 자세한 내용은을 참조 https://docs.microsoft.com/en-us/azure/iot-central/ 하세요.</span><span class="sxs-lookup"><span data-stu-id="9705c-107">For an introduction to IoT Central, see https://docs.microsoft.com/en-us/azure/iot-central/.</span></span>

## <span data-ttu-id="9705c-108">예제의</span><span class="sxs-lookup"><span data-stu-id="9705c-108">EXAMPLES</span></span>

### <span data-ttu-id="9705c-109">예제 1 간단한 IoT 중앙 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9705c-109">Example 1 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain"
```

<span data-ttu-id="9705c-110">출력 예:</span><span class="sxs-lookup"><span data-stu-id="9705c-110">Example Output:</span></span>

<span data-ttu-id="9705c-111">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/Iotcentral/MyAppResourceName Name: MyAppResourceName Type: Microsoft. IoTCentral/Iotcentral 위치: westus Tag: Sku: Microsoft. p r o. r a p. p r a p. r a p: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX 이름 DisplayName: MyAppResourceName 하위 도메인: MyAppSubdomain Template: iotc-default@1.0.0 SubscriptionId: Xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9705c-111">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : MyAppResourceName Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="9705c-112">표준 가격 책정 계층 S1에서 리소스 그룹의 영역에 IoT 중앙 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9705c-112">Create an IoT Central application in the standard pricing tier S1, in the region of the resource group.</span></span>

### <span data-ttu-id="9705c-113">예제 2 간단한 IoT 중앙 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9705c-113">Example 2 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain" -Sku "S1" -DisplayName "My Custom Display Name" -Template "iotc-default" -Location "westus"
```

<span data-ttu-id="9705c-114">출력 예:</span><span class="sxs-lookup"><span data-stu-id="9705c-114">Example Output:</span></span>

<span data-ttu-id="9705c-115">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/Iotcentral/MyAppResourceName Name: MyAppResourceName 유형: Microsoft. IoTCentral/Iotcentral 위치: westus Tag: Sku: Microsoft Azure. p s p. p r o: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My 사용자 지정 표시 이름 하위 도메인: MyAppSubdomain Template: iotc-default@1.0.0 SubscriptionId: Xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9705c-115">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="9705c-116">Iotc-기본 템플릿을 기반으로 하는 사용자 지정 표시 이름을 사용 하 여 ' westus ' 영역에 표준 가격 책정 계층 S1을 사용 하 여 IoT 중앙 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9705c-116">Create an IoT Central application with the standard pricing tier S1 in the 'westus' region, with a custom display name, based on the iotc-default template.</span></span>

## <span data-ttu-id="9705c-117">변수</span><span class="sxs-lookup"><span data-stu-id="9705c-117">PARAMETERS</span></span>

### <span data-ttu-id="9705c-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9705c-118">-AsJob</span></span>
<span data-ttu-id="9705c-119">백그라운드에서 cmdlet을 작업으로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9705c-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="9705c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9705c-120">-DefaultProfile</span></span>
<span data-ttu-id="9705c-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9705c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9705c-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9705c-122">-DisplayName</span></span>
<span data-ttu-id="9705c-123">IoT 중앙 응용 프로그램의 사용자 지정 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9705c-123">Custom display name for the IoT Central application.</span></span>
<span data-ttu-id="9705c-124">기본값은 자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9705c-124">Default is resource name.</span></span>

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

### <span data-ttu-id="9705c-125">-위치</span><span class="sxs-lookup"><span data-stu-id="9705c-125">-Location</span></span>
<span data-ttu-id="9705c-126">IoT 중앙 응용 프로그램의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="9705c-126">Location of your IoT Central application.</span></span>
<span data-ttu-id="9705c-127">기본값은 대상 리소스 그룹의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="9705c-127">Default is the location of target resource group.</span></span>

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

### <span data-ttu-id="9705c-128">-이름</span><span class="sxs-lookup"><span data-stu-id="9705c-128">-Name</span></span>
<span data-ttu-id="9705c-129">Iot 중앙 응용 프로그램 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9705c-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="9705c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9705c-130">-ResourceGroupName</span></span>
<span data-ttu-id="9705c-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9705c-131">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="9705c-132">-Sku</span><span class="sxs-lookup"><span data-stu-id="9705c-132">-Sku</span></span>
<span data-ttu-id="9705c-133">IoT 중앙 응용 프로그램에 대 한 가격 책정 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="9705c-133">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="9705c-134">기본값은 S1입니다.</span><span class="sxs-lookup"><span data-stu-id="9705c-134">Default value is S1.</span></span>

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

### <span data-ttu-id="9705c-135">-하위 도메인</span><span class="sxs-lookup"><span data-stu-id="9705c-135">-Subdomain</span></span>
<span data-ttu-id="9705c-136">IoT 중앙 URL의 하위 도메인입니다.</span><span class="sxs-lookup"><span data-stu-id="9705c-136">Subdomain for the IoT Central URL.</span></span>
<span data-ttu-id="9705c-137">각 응용 프로그램에는 고유한 하위 도메인이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9705c-137">Each application must have a unique subdomain.</span></span>

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

### <span data-ttu-id="9705c-138">태그</span><span class="sxs-lookup"><span data-stu-id="9705c-138">-Tag</span></span>
<span data-ttu-id="9705c-139">Iot 중앙 응용 프로그램 리소스 태그</span><span class="sxs-lookup"><span data-stu-id="9705c-139">Iot Central Application Resource Tags.</span></span>

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

### <span data-ttu-id="9705c-140">-Template</span><span class="sxs-lookup"><span data-stu-id="9705c-140">-Template</span></span>
<span data-ttu-id="9705c-141">IoT 중앙 응용 프로그램 서식 파일 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9705c-141">IoT Central application template name.</span></span>
<span data-ttu-id="9705c-142">기본값은 사용자 지정 응용 프로그램입니다.</span><span class="sxs-lookup"><span data-stu-id="9705c-142">Default is a custom application.</span></span>

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

### <span data-ttu-id="9705c-143">-확인</span><span class="sxs-lookup"><span data-stu-id="9705c-143">-Confirm</span></span>
<span data-ttu-id="9705c-144">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9705c-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9705c-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9705c-145">-WhatIf</span></span>
<span data-ttu-id="9705c-146">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9705c-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9705c-147">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9705c-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9705c-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9705c-148">CommonParameters</span></span>
<span data-ttu-id="9705c-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9705c-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9705c-150">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9705c-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9705c-151">입력</span><span class="sxs-lookup"><span data-stu-id="9705c-151">INPUTS</span></span>

### <span data-ttu-id="9705c-152">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9705c-152">System.String</span></span>

### <span data-ttu-id="9705c-153">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="9705c-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9705c-154">출력</span><span class="sxs-lookup"><span data-stu-id="9705c-154">OUTPUTS</span></span>

### <span data-ttu-id="9705c-155">PSIotCentralApp를 통해 서 .exe.</span><span class="sxs-lookup"><span data-stu-id="9705c-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="9705c-156">상속자</span><span class="sxs-lookup"><span data-stu-id="9705c-156">NOTES</span></span>

## <span data-ttu-id="9705c-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9705c-157">RELATED LINKS</span></span>
