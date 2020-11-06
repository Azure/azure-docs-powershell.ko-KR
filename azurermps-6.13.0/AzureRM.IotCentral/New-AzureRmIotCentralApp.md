---
external help file: Microsoft.Azure.Commands.IotCentral.dll-Help.xml
Module Name: AzureRM.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iotcentral/new-azurermiotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/New-AzureRmIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/New-AzureRmIotCentralApp.md
ms.openlocfilehash: d0bb10324c1a97b6228a26a7ab079edb4845d48a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537612"
---
# <span data-ttu-id="50612-101">New-AzureRmIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="50612-101">New-AzureRmIotCentralApp</span></span>

## <span data-ttu-id="50612-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50612-102">SYNOPSIS</span></span>
<span data-ttu-id="50612-103">새 IoT 중앙 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="50612-103">Creates a new IoT Central Application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50612-104">구문과</span><span class="sxs-lookup"><span data-stu-id="50612-104">SYNTAX</span></span>

```
New-AzureRmIotCentralApp [-Subdomain] <String> [-DisplayName <String>] [-Template <String>] [-Sku <String>]
 [-Location <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50612-105">설명은</span><span class="sxs-lookup"><span data-stu-id="50612-105">DESCRIPTION</span></span>
<span data-ttu-id="50612-106">제공 된 속성 및 메타 데이터로 새 IoT 중앙 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="50612-106">Creates a new IoT Central Application with the provided properties and metadata.</span></span> <span data-ttu-id="50612-107">IoT Central 소개에 대 한 자세한 내용은을 참조 https://docs.microsoft.com/en-us/azure/iot-central/ 하세요.</span><span class="sxs-lookup"><span data-stu-id="50612-107">For an introduction to IoT Central, see https://docs.microsoft.com/en-us/azure/iot-central/.</span></span>

## <span data-ttu-id="50612-108">예제의</span><span class="sxs-lookup"><span data-stu-id="50612-108">EXAMPLES</span></span>

### <span data-ttu-id="50612-109">예제 1 간단한 IoT 중앙 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="50612-109">Example 1 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain"
```

<span data-ttu-id="50612-110">출력 예:</span><span class="sxs-lookup"><span data-stu-id="50612-110">Example Output:</span></span>

<span data-ttu-id="50612-111">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/Iotcentral/MyAppResourceName Name: MyAppResourceName Type: Microsoft. IoTCentral/Iotcentral 위치: westus Tag: Sku: Microsoft. p r o. r a p. p r a p. r a p: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX 이름 DisplayName: MyAppResourceName 하위 도메인: MyAppSubdomain Template: iotc-default@1.0.0 SubscriptionId: Xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50612-111">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : MyAppResourceName Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="50612-112">표준 가격 책정 계층 S1에서 리소스 그룹의 영역에 IoT 중앙 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="50612-112">Create an IoT Central application in the standard pricing tier S1, in the region of the resource group.</span></span>

### <span data-ttu-id="50612-113">예제 2 간단한 IoT 중앙 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="50612-113">Example 2 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain" -Sku "S1" -DisplayName "My Custom Display Name" -Template "iotc-default" -Location "westus"
```

<span data-ttu-id="50612-114">출력 예:</span><span class="sxs-lookup"><span data-stu-id="50612-114">Example Output:</span></span>

<span data-ttu-id="50612-115">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/Iotcentral/MyAppResourceName Name: MyAppResourceName 유형: Microsoft. IoTCentral/Iotcentral 위치: westus Tag: Sku: Microsoft Azure. p s p. p r o: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My 사용자 지정 표시 이름 하위 도메인: MyAppSubdomain Template: iotc-default@1.0.0 SubscriptionId: Xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50612-115">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="50612-116">Iotc-기본 템플릿을 기반으로 하는 사용자 지정 표시 이름을 사용 하 여 ' westus ' 영역에 표준 가격 책정 계층 S1을 사용 하 여 IoT 중앙 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="50612-116">Create an IoT Central application with the standard pricing tier S1 in the 'westus' region, with a custom display name, based on the iotc-default template.</span></span>

## <span data-ttu-id="50612-117">변수</span><span class="sxs-lookup"><span data-stu-id="50612-117">PARAMETERS</span></span>

### <span data-ttu-id="50612-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50612-118">-AsJob</span></span>
<span data-ttu-id="50612-119">백그라운드에서 cmdlet을 작업으로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="50612-119">Run cmdlet as a job in the background.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50612-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50612-120">-DefaultProfile</span></span>
<span data-ttu-id="50612-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="50612-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50612-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="50612-122">-DisplayName</span></span>
<span data-ttu-id="50612-123">IoT 중앙 응용 프로그램의 사용자 지정 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="50612-123">Custom display name for the IoT Central application.</span></span>
<span data-ttu-id="50612-124">기본값은 자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="50612-124">Default is resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50612-125">-위치</span><span class="sxs-lookup"><span data-stu-id="50612-125">-Location</span></span>
<span data-ttu-id="50612-126">IoT 중앙 응용 프로그램의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="50612-126">Location of your IoT Central application.</span></span>
<span data-ttu-id="50612-127">기본값은 대상 리소스 그룹의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="50612-127">Default is the location of target resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50612-128">-이름</span><span class="sxs-lookup"><span data-stu-id="50612-128">-Name</span></span>
<span data-ttu-id="50612-129">Iot 중앙 응용 프로그램 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="50612-129">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50612-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50612-130">-ResourceGroupName</span></span>
<span data-ttu-id="50612-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="50612-131">Name of the Resource Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50612-132">-Sku</span><span class="sxs-lookup"><span data-stu-id="50612-132">-Sku</span></span>
<span data-ttu-id="50612-133">IoT 중앙 응용 프로그램에 대 한 가격 책정 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="50612-133">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="50612-134">기본값은 S1입니다.</span><span class="sxs-lookup"><span data-stu-id="50612-134">Default value is S1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: S1

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50612-135">-하위 도메인</span><span class="sxs-lookup"><span data-stu-id="50612-135">-Subdomain</span></span>
<span data-ttu-id="50612-136">IoT 중앙 URL의 하위 도메인입니다.</span><span class="sxs-lookup"><span data-stu-id="50612-136">Subdomain for the IoT Central URL.</span></span>
<span data-ttu-id="50612-137">각 응용 프로그램에는 고유한 하위 도메인이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="50612-137">Each application must have a unique subdomain.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50612-138">태그</span><span class="sxs-lookup"><span data-stu-id="50612-138">-Tag</span></span>
<span data-ttu-id="50612-139">Iot 중앙 응용 프로그램 리소스 태그</span><span class="sxs-lookup"><span data-stu-id="50612-139">Iot Central Application Resource Tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50612-140">-Template</span><span class="sxs-lookup"><span data-stu-id="50612-140">-Template</span></span>
<span data-ttu-id="50612-141">IoT 중앙 응용 프로그램 서식 파일 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="50612-141">IoT Central application template name.</span></span>
<span data-ttu-id="50612-142">기본값은 사용자 지정 응용 프로그램입니다.</span><span class="sxs-lookup"><span data-stu-id="50612-142">Default is a custom application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50612-143">-확인</span><span class="sxs-lookup"><span data-stu-id="50612-143">-Confirm</span></span>
<span data-ttu-id="50612-144">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="50612-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50612-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50612-145">-WhatIf</span></span>
<span data-ttu-id="50612-146">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="50612-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50612-147">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="50612-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50612-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50612-148">CommonParameters</span></span>
<span data-ttu-id="50612-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="50612-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50612-150">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50612-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50612-151">입력</span><span class="sxs-lookup"><span data-stu-id="50612-151">INPUTS</span></span>

### <span data-ttu-id="50612-152">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="50612-152">System.String</span></span>
### <span data-ttu-id="50612-153">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="50612-153">System.Collections.Hashtable</span></span>
## <span data-ttu-id="50612-154">출력</span><span class="sxs-lookup"><span data-stu-id="50612-154">OUTPUTS</span></span>

### <span data-ttu-id="50612-155">PSIotCentralApp를 통해 서 .exe.</span><span class="sxs-lookup"><span data-stu-id="50612-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>
## <span data-ttu-id="50612-156">상속자</span><span class="sxs-lookup"><span data-stu-id="50612-156">NOTES</span></span>

## <span data-ttu-id="50612-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="50612-157">RELATED LINKS</span></span>
