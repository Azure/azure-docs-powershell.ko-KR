---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/set-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
ms.openlocfilehash: cea582481515f519e14df9f430dc1326e72a0877
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94033949"
---
# <span data-ttu-id="52a05-101">Set-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="52a05-101">Set-AzIotCentralApp</span></span>

## <span data-ttu-id="52a05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52a05-102">SYNOPSIS</span></span>
<span data-ttu-id="52a05-103">IoT 중앙 응용 프로그램에 대 한 메타 데이터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="52a05-103">Updates the metadata for an IoT Central Application.</span></span>

## <span data-ttu-id="52a05-104">구문과</span><span class="sxs-lookup"><span data-stu-id="52a05-104">SYNTAX</span></span>

### <span data-ttu-id="52a05-105">ResourceIdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="52a05-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52a05-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="52a05-106">InputObjectParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>]
 -InputObject <PSIotCentralApp> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="52a05-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="52a05-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="52a05-108">설명은</span><span class="sxs-lookup"><span data-stu-id="52a05-108">DESCRIPTION</span></span>
<span data-ttu-id="52a05-109">IoT 중앙 응용 프로그램에 대 한 메타 데이터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="52a05-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="52a05-110">예제의</span><span class="sxs-lookup"><span data-stu-id="52a05-110">EXAMPLES</span></span>

### <span data-ttu-id="52a05-111">예제 1 업데이트 표시 이름</span><span class="sxs-lookup"><span data-stu-id="52a05-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="52a05-112">기존 IoT 중앙 응용 프로그램에서 표시 이름을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="52a05-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="52a05-113">출력 예:</span><span class="sxs-lookup"><span data-stu-id="52a05-113">Example Output:</span></span>

<span data-ttu-id="52a05-114">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/Iotcentral/MyAppResourceName Name: MyAppResourceName 유형: Microsoft. IoTCentral/Iotcentral 위치: westus Tag: Sku: Microsoft Azure. p r o: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My를 통해 새 사용자 지정 표시 이름 하위 도메인: MyAppSubdomain 서식 파일: iotc-default@1.0.0 SubscriptionId: Xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52a05-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="52a05-115">예제 2 하위 도메인 업데이트</span><span class="sxs-lookup"><span data-stu-id="52a05-115">Example 2 Update Subdomain</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "new-subdomain"
```

<span data-ttu-id="52a05-116">기존 IoT 중앙 응용 프로그램에서 표시 이름을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="52a05-116">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="52a05-117">출력 예:</span><span class="sxs-lookup"><span data-stu-id="52a05-117">Example Output:</span></span>

<span data-ttu-id="52a05-118">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/Iotcentral/MyAppResourceName Name: MyAppResourceName 유형: Microsoft. IoTCentral/Iotcentral 위치: westus Tag: Sku: Microsoft Azure. p s p. p r o: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: 표시 이름 하위 도메인: 새 하위 도메인 템플릿: SubscriptionId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX에 대 한 자세한 iotc-default@1.0.0 ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52a05-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : new-subdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="52a05-119">변수</span><span class="sxs-lookup"><span data-stu-id="52a05-119">PARAMETERS</span></span>

### <span data-ttu-id="52a05-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52a05-120">-AsJob</span></span>
<span data-ttu-id="52a05-121">백그라운드에서 cmdlet을 작업으로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="52a05-121">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="52a05-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52a05-122">-DefaultProfile</span></span>
<span data-ttu-id="52a05-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="52a05-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52a05-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="52a05-124">-DisplayName</span></span>
<span data-ttu-id="52a05-125">Iot 중앙 응용 프로그램의 사용자 지정 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="52a05-125">Custom Display Name of the Iot Central Application.</span></span>

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

### <span data-ttu-id="52a05-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52a05-126">-InputObject</span></span>
<span data-ttu-id="52a05-127">Iot 중앙 응용 프로그램 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="52a05-127">Iot Central Application Input Object.</span></span>

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

### <span data-ttu-id="52a05-128">-이름</span><span class="sxs-lookup"><span data-stu-id="52a05-128">-Name</span></span>
<span data-ttu-id="52a05-129">Iot 중앙 응용 프로그램 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="52a05-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="52a05-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52a05-130">-ResourceGroupName</span></span>
<span data-ttu-id="52a05-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="52a05-131">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="52a05-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52a05-132">-ResourceId</span></span>
<span data-ttu-id="52a05-133">Iot 중앙 응용 프로그램 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="52a05-133">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="52a05-134">-하위 도메인</span><span class="sxs-lookup"><span data-stu-id="52a05-134">-Subdomain</span></span>
<span data-ttu-id="52a05-135">IoT 중앙 응용 프로그램의 하위 도메인입니다.</span><span class="sxs-lookup"><span data-stu-id="52a05-135">Subdomain of the IoT Central Application.</span></span>

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

### <span data-ttu-id="52a05-136">태그</span><span class="sxs-lookup"><span data-stu-id="52a05-136">-Tag</span></span>
<span data-ttu-id="52a05-137">Iot 중앙 응용 프로그램 리소스 태그</span><span class="sxs-lookup"><span data-stu-id="52a05-137">Iot Central Application Resource Tags.</span></span>

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

### <span data-ttu-id="52a05-138">-확인</span><span class="sxs-lookup"><span data-stu-id="52a05-138">-Confirm</span></span>
<span data-ttu-id="52a05-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="52a05-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52a05-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52a05-140">-WhatIf</span></span>
<span data-ttu-id="52a05-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="52a05-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52a05-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="52a05-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52a05-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52a05-143">CommonParameters</span></span>
<span data-ttu-id="52a05-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="52a05-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52a05-145">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52a05-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52a05-146">입력</span><span class="sxs-lookup"><span data-stu-id="52a05-146">INPUTS</span></span>

### <span data-ttu-id="52a05-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="52a05-147">System.String</span></span>

### <span data-ttu-id="52a05-148">PSIotCentralApp를 통해 서 .exe.</span><span class="sxs-lookup"><span data-stu-id="52a05-148">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="52a05-149">출력</span><span class="sxs-lookup"><span data-stu-id="52a05-149">OUTPUTS</span></span>

### <span data-ttu-id="52a05-150">PSIotCentralApp를 통해 서 .exe.</span><span class="sxs-lookup"><span data-stu-id="52a05-150">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="52a05-151">상속자</span><span class="sxs-lookup"><span data-stu-id="52a05-151">NOTES</span></span>

## <span data-ttu-id="52a05-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="52a05-152">RELATED LINKS</span></span>
